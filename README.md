# Cybersecurity Testing Methodology for Internet of Things Devices

1. [Pre-engagement interactions](#pre-engagement-interactions)
1. [Intelligence gathering](#intelligence-gathering)
1. [Threat modeling](#threat-modeling)
1. [Vulnerability analysis](#vulnerability-analysis)
1. [Exploitation](#exploitation)
1. [Post exploitation](#post-exploitation)
1. [Reporting](#reporting)

## Pre-engagement interactions

This section aims to describe the necessary steps to prepare for the penetration test. Even if the testing is not done for a client but rather for your own needs, it is still important to go through the following steps.

### Scope

The most important part of this step is determining the scope of tests. There are 3 main areas to be addressed when defining the scope:

- hardware,
- firmware,
- and communication protocol.

When describing scope of hardware testing, determine wether it is needed in the first place and if so, which specific components need to be tested. For all tested components, try to acquire the corresponding documentation and schematics.

Determine wether to test the device’s firmware and try to obtain it as well as any documentation or source code associated with it. You may also choose to specify parts of the firmware to be omitted.

If the device’s communication protocol is in-scope determine what layers of the protocol needs testing and acquire the documentation.

If multiple devices are to be tested together, you need to repeat the steps for each device.

### Denial of service

Denial of service (DoS) testing is among the areas to be discussed prior to testing. While it is a valid thing to test, the findings are oftentimes not fixable anyway so you may be able to shorten the time required for testing. Not to mention that there may occur irreversible damage to the device itself.

### Third parties

Oftentimes IoT devices rely on cloud services to be able to control them. Ensure that you do not interfere with these services or have a written permission stating what testing you are able to perform toward the cloud.

### Compliance

When testing a device, you may also check for compliance. Keep in mind that this should not be the primary goal of your testing, as compliance does not imply security.

### Contact

> This section is only relevant if you are testing a device for a client.

Establish proper, safe lines of communication with the client. You will generally need two contact types: normal and emergency.

Emergency contacts are for emergencies—that is, they are to be used only when a critical flaw is found and it is necessary to report it immediately.

For all contacts, you need to establish a reliable and secure line of communication. Use only encrypted channels to transfer any sensitive data.

You should also set up regular status reports with the client where you will go through the curent status of testing. These do not need to be as often as with non-IoT testing as you generally do not need client’s cooperation.

### Time

Before the testing begins, it is important to specify when the testing starts and when it ends. This step is imprtant mainly when dealing with a client and a budget but can be helpful when testing for own use as well.

It can also be helpful to prepare a more detailed timeline showing when each part of testing will take place.

When dealing with a client explicitly stating start and end dates helps with managing expectations. When it comes to budget, it ensures that you do not work more than the budget allows for. If there is a need for more work to be done make sure that it is paid for.

If you are only testing for your own use, setting time boundaries can help not getting stuck on testing.

### Payment

> This section is only relevant if you are testing a device for a client.

Do not forget to specify the terms and dates for payment. The terms will differ for each tester, but the goal is to determine when and how much you will be paid.

### Legal

Be sure to check the legality of the tests before you begin testing. This will depend on the location of the tests.

When testing radio communication for example, be sure to only utilize frequencies allowed in your area.

## Intelligence gathering

The goal of this section is to find out as much information as possible about your target. If you are not working for a client, the following section will have some similarities with the previous one. If you are working for a client, the difference will be that you will perform this section mostly without your client's cooperation. Either way, this section results in a more in-depth understanding of the tested system.

Anytime you discover something new, you should determine whether it is part of the defined scope and potentially discuss it with the client. Analyzing out-of-scope components may cost you a lot of your valuable time. 

### Hardware

Look for any hardware datasheets regarding the tested device. Identify as many components as possible using obtained datasheets and visual inspection. Identify the CPU architecture. 

Obtain the FCC ID of the device and look for any additional information on [fccid.io](https://fccid.io/).

Identify any exposed interfaces and ports.

Which frequencies does the device use for communication?

Is there any temper evidence/resistance technology used?

Try connecting to the serial interface if one is available and identify the baudrate. Find out if there is any shell available through the serial port and whether it is authenticated or not.

### Firmware

Ideally, try to access the codebase of the firmware, as this will greatly help with the following analysis. Look for any current/relevant bug reports, past testing reports, and known vulnerabilities.

Obtain the firmware used on the tested device. This can be a very complex step depending on the situation. Ideally, you would be able to obtain the firmware directly from the vendor or by building it yourself from the source code. If this is not an option, you can try to extract the firmware directly from the device (previous analysis of used interfaces and ports is helpful).

#### Firmware analysis

Use utilities like `file`, `strings`, `binwalk`, `hexdump` and `fdisk` for the initial analysis of the file. You can check the firmware's entropy (e.g., `binwalk -E <bin>`) to try to determine whether the firmware is encrypted or not.

#### Filesystem

Next, try to extract the filesystem from the firmware. You can try extracting it with `binwalk -ev <bin>`. If that does not work, use `binwalk` to find the filesystem's offset, carve it using `dd` and extract the files with an appropriate utility (based on the used filesystem).

Analyze the found files and look for any important files. Automated tools such as [Firmwalker](https://github.com/craigz28/firmwalker) may prove useful.

### Communication protocol

Learn as much information about the communication protocol as possible. This includes the following information:

- radio frequencies
- used ports
- security (authentication, authorization, encryption, etc.)
- default keys and credentials
- known vulnerabilities

## Threat modeling

Threat modeling is an important step when it comes to both testing and developing a product. Its goal is to find specific threats to a system.

### Diagrams

The first step is to understand the system being tested. Using our knowledge from pre-engagement interactions and intelligance gathering, we are able to create a diagram representing the system. This helps to better visualize different components and how they are connected.

### Trust levels

Identify the different levels of access rights to the system. The system will generally have different access levels for an administrator, an authenticated user and an unauthenticated user. There usually are not many trust levels in IoT systems.

### Assets

Next, identify assets - items of interest. These are parts of the system that the attacker might be interested in. These include stuff like login credentials, cryptographic keys and other data associated with the device. For each asset, list all of the associated trust levels that are able to access it.

### Entry points

This step helps describe points of the system through which an entity can interact with it. Previous identification of interfaces will prove useful. Entry points are especially important as these are the points the attacker can use when attacking the system. Again, note the associated trust levels for each entry point.

### Threat identification

When the system is properly modeled and key parts are identified, identify all threats to the system. There are many methodologies focusing on threat modeling/identification but one of the most commonly used ones is STRIDE (spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege). These help identify as well as categorize as many threats as possible.

## Vulnerability analysis

During this phase vulnerabilities are discovered through combination of automated tools and manual testing. Prior threat modeling helps in focusing on specific parts of the system as to not test blindly. 

### Hardware

Generally your goal here is to access the device's firmware/data through the provided interfaces.

Being able to dump the firmware directly from the device may be beneficial because it may contain device specific information, e.g. preprogrammed cryptographic keys.

Also try dumping data from the flash as it may contain sensitive and useful information.

You may alo try modifying the obtained fimrware/data and writing it back on the device. This way, you may alter the expected behaviour of the device.

If you are able to connect to the device's shell, try dumping the firmware, modifying values, checking for persistance across reboots, privileges, etc.

### Firmware

Vulnerability analysis of firmware can be very extensive. Luckily most of it is done through automated tools first.

If you have access to the firmware's source code, analyze it directly for any potential vulnerabilities. [Coverity Scan](https://scan.coverity.com/) is an automated static analysis tool that may be useful during this step.

Next, utilize automated tools like [FACT](https://github.com/fkie-cad/FACT_core), [EMBA](https://github.com/e-m-b-a/emba) or [Bytesweep](https://gitlab.com/bytesweep/bytesweep) to scan the firmware for filesystems, vulnerabilities, suspicious binaries, etc.

Further analyze any suspicious binaries identified during information gathering. As a great first step, use [Checksec](https://github.com/slimm609/checksec) to check for RELRO, stack canaries, etc. If need be, try disassembling the binaries for further analysis.

#### Emulation

For dynamic analysis it is desirable to be able to emulate the device's firmware. Whenever possible, try to perform a full-system emulation. Below are listed some automated tools for automatic emulation. These tools often come with vulnerability scanning ability as well.

- [Firmware Analysis Toolkit](https://github.com/attify/firmware-analysis-toolkit)
- [EMUX](https://github.com/therealsaumil/emux)
- [MIPS-X](https://github.com/getCUJO/MIPS-X)
- [FIRMADYNE](https://github.com/firmadyne/firmadyne)
- [Qltool](https://github.com/qilingframework/qiling#qltool)

If it is not possible to perform a full-system emulation, you can try emulating specific binaries using `qemu` and `chroot`.

#### Dynamic testing

Using the emulated firmware, perform dynamic testing of the bootloader, firmware and applications.

> Some devices may provide a web application as part of its functionality. Testing of such applications is out of scope of this methodology, however [OWASP's Web Security Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) contains detailed steps on how to proceed.

Below is a list of ideas to test:

- bootloader
    - access to the bootloader's shell
    - modifying boot arguments to execute code
    - providing a fake image over the network
- firmware
    - deploying reverse shell
- applications
    - attaching a debugger to the emulated running aplication and closely analyze suspicious applications and functions highlighted during static analysis

### Communication protocol

Analysis of the communication protocol differs based on the used protocol. Below are some things to look for:

- Is it possible to sniff the communication?
- Is encryption used during communication?
- Are well-known keys used for encryption?
- Is replay attack possible?

## Exploitation

### Hardware

### Firmware

### Communication protocol

## Post exploitation

## Reporting
