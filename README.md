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

When describing scope of hardware testing, determine wether it is needed in the first place and if so, which specific components need to be tested. For all tested components try to acquire the corresponding documentation and schematics.

Determine wether to test the device's firmware and try to obtain it as well as any documentation or source code associated with it. You may also choose to specify parts of the firmware to be omitted.

If the device's communication protocol is in-scope determine what layers of the protocol needs testing and acquire the documentation.

If multiple devices are to be tested together, you need to repeat the steps for each device.

### Denial of service

Denial of service (DoS) testing is among the areas to be discussed prior to testing. While it is a valid thing to test, the findings are oftentimes not fixable anyway so you may be able to shorten the time required for testing. Not to mention that there may occur irreversible damage to the device itself.

### Third parties

Oftentimes IoT devices rely on cloud services to be able to control them. Ensure that you do not interfere with these services or have a written permission stating what testing you are able to perform toward the cloud.

### Compliance

When testing a device, you may also check for compliance. Keep in mind that this should not be the primary goal of your testing as compliance does not imply security.

### Contact

> This section is only relevant if you are testing a device for a client.

Establish proper, safe lines of communication with the client. You will generally need two contact types: normal and emergency.

Emergency contacts are for emergencies - that is they are to be used only when a critical flaw is found and it is necessary to report it immediately.

For all contacts you need to establish reliable and secure line of communication. Use only encrypted channels to transfer any sensitive data.

You should also set up regular status reports with the client where you will go through the curent status of testing. These do not need to be as often as with non-IoT testing as you generally do not need client's cooperation.

### Time

Before the testing begins, it is important to specify when the testing starts and when it ends. This step is imprtant mainly when dealing with a client and a budget but can be helpful when testing for own use as well.

It can also be helpful to prepare a more detailed timeline showing when each part of testing will take place. 

When dealing with a client explicitly stating start and end dates helps with managing expectations. When it comes to budget, it ensures that you do not work more than the budget allows for. If there is a need for more work to be done make sure that it is paid for.

If you are only testing for your own use, setting time boundaries can help not getting stuck on testing.

### Payment

> This section is only relevant if you are testing a device for a client.

Do not forget to specify the terms and dates for payment. The terms will differ for each tester but the goal is to determine when and how much you will be paid.

### Legal

Be sure to check the legality of the tests before you begin testing. This will depend on the location of the tests.

When testing radio communication for example, be sure to only utilize frequencies allowed in your area.

## Intelligence gathering

## Threat modeling

## Vulnerability analysis

### Hardware

### Firmware

### Communication protocol

## Exploitation

### Hardware

### Firmware

### Communication protocol

## Post exploitation

## Reporting

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque lectus elit, egestas quis urna non, condimentum posuere quam. Praesent et condimentum quam. Donec dignissim neque nunc, quis scelerisque ex accumsan sit amet. Quisque sed semper ante. Maecenas tincidunt justo sapien, eu scelerisque magna facilisis eget. Integer mauris ex, euismod at nisi at, maximus posuere leo. Praesent pharetra tincidunt ultricies. Donec bibendum ornare sem, id sodales odio. Vestibulum mollis lorem at est ornare, a interdum sapien ornare. Duis et neque ornare tellus lacinia egestas. Praesent sit amet risus ipsum. Ut vitae nisi a lacus hendrerit laoreet.

Cras cursus bibendum odio, in lobortis velit dapibus vel. Proin suscipit sem quis tincidunt sagittis. Sed a faucibus ligula. Quisque sollicitudin posuere ex, in facilisis lectus egestas id. Nam dolor justo, blandit quis venenatis ut, auctor et libero. Nullam ac convallis augue, vel malesuada orci. Cras placerat velit ultricies faucibus malesuada. Sed facilisis, lacus in lacinia molestie, nibh nulla dapibus diam, quis rutrum erat massa et tortor. Vestibulum lacus dolor, condimentum ac ornare nec, porta in velit. Nunc pharetra elementum libero. Vestibulum est dolor, ullamcorper ac dui in, viverra pulvinar eros. Aliquam semper placerat metus. Aenean eget rutrum sem. Praesent tristique lacus non ipsum porta congue.

Mauris eu euismod enim, at viverra risus. Donec vitae nibh eget tortor convallis pharetra. Nunc erat ante, tincidunt et purus vel, lacinia accumsan urna. Morbi semper quis dolor lacinia ultrices. Nulla condimentum ligula nisi, ac egestas nisl malesuada vitae. Integer viverra elementum ante in tristique. Phasellus lacinia diam pharetra sem suscipit fringilla. Nullam at enim urna. Nulla efficitur metus eu nunc ultrices finibus. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aliquam fringilla convallis magna sit amet dictum. Quisque gravida malesuada neque ac dignissim. Suspendisse potenti. Vestibulum hendrerit nulla ac risus pharetra aliquet. Suspendisse luctus est ipsum, quis placerat est ultricies vel.

Pellentesque sodales mattis vulputate. In volutpat turpis sed tellus ultrices, id euismod ipsum consectetur. Mauris in tristique nisi. Phasellus purus magna, tempus quis lacus euismod, pretium eleifend elit. Phasellus feugiat lectus vel eros suscipit finibus. Etiam vel tortor orci. Curabitur sit amet fermentum augue. Donec nec magna magna. Mauris viverra, orci ac sagittis iaculis, lectus eros fringilla libero, vitae eleifend ex tellus ultricies lorem. Etiam non erat condimentum, aliquet nunc quis, tempor nibh. Maecenas tempor lorem sit amet arcu volutpat, eget aliquam mauris hendrerit. Donec at sodales libero. Nam hendrerit egestas vulputate. Maecenas non semper risus, ac mattis justo. Donec urna urna, pharetra sit amet sapien tempor, ultrices tincidunt ligula.

Etiam dui metus, molestie malesuada lobortis vel, cursus egestas ipsum. Praesent eleifend lacus non urna imperdiet vulputate. Sed sit amet viverra magna, at condimentum neque. Cras quis orci et felis commodo ultricies in ac felis. Duis nec tempor dui. Proin aliquet ante non erat aliquam, ut dictum turpis tempor. Pellentesque sed sapien nec elit porta vehicula id eget diam. In sit amet molestie nisi. Proin erat arcu, imperdiet eget dapibus et, volutpat eu mauris. In sed fringilla metus, eu porttitor nisi. Integer rhoncus mattis massa porttitor pulvinar. Nunc id quam sed odio blandit lobortis quis eget diam. Aliquam aliquam, nunc eget euismod pulvinar, leo velit sagittis lectus, non dictum lacus mi eget magna. Suspendisse erat velit, malesuada eget hendrerit eget, pretium sit amet metus. Nullam at nisl nisl.

Proin pretium fringilla urna, in suscipit diam molestie et. Nulla congue lectus id libero ultrices, et rhoncus ligula tempus. Proin diam mauris, pretium at lectus sed, aliquet feugiat neque. Pellentesque iaculis placerat neque, vitae ultrices leo bibendum non. Sed pretium ex ligula, ut finibus dui consectetur at. Proin pharetra mauris et mi gravida, vitae posuere dolor eleifend. Sed pulvinar velit blandit, semper tortor id, pharetra lorem. Aliquam vestibulum mauris leo, vel aliquam enim semper ac. Nulla tempus risus sapien, in fermentum nisl aliquet a. In in tellus vulputate, pretium lacus et, consequat mauris. Curabitur at lacinia ex. Nunc leo leo, iaculis vitae ligula sit amet, tincidunt vestibulum augue. Quisque ipsum nibh, fermentum a ex sit amet, tempor consectetur eros. Mauris vulputate auctor velit.

Phasellus ultrices diam eget vestibulum ullamcorper. Pellentesque nec sem hendrerit, tempor enim vel, dapibus purus. Pellentesque at arcu dignissim libero convallis rhoncus at ut nulla. Curabitur velit est, volutpat eu sapien non, vulputate tincidunt neque. Quisque sed scelerisque urna. Donec auctor lorem sed malesuada tincidunt. Aliquam erat volutpat. Etiam vehicula ullamcorper mauris non sodales. Sed faucibus risus nisi, et mollis ex convallis at. Suspendisse sit amet porttitor ex. Nulla a urna ut odio laoreet dignissim vitae sed augue. In hac habitasse platea dictumst.

Sed sed turpis a libero bibendum luctus. Cras vehicula, lacus sed varius condimentum, purus tellus commodo libero, in hendrerit dui ipsum ac tellus. Phasellus facilisis ac enim ut feugiat. Maecenas finibus sagittis enim, id rhoncus augue viverra sed. Nullam sit amet elit a tortor consectetur dignissim. Sed non interdum orci. Proin lobortis mi enim. Praesent quis posuere dolor. Integer sodales commodo felis, ac suscipit quam ullamcorper sed. Sed ipsum nunc, placerat condimentum odio vel, ornare auctor dui. Maecenas varius porta fermentum. Vivamus magna velit, sagittis eu ultricies ac, pharetra ac purus. Donec mauris nulla, hendrerit ac mollis auctor, lobortis ac arcu. Vestibulum tortor neque, laoreet feugiat convallis in, volutpat vitae arcu.

Donec eget mattis purus. Nam aliquam at turpis a mollis. Curabitur eu posuere orci, lacinia lacinia sem. Etiam et quam et ex sollicitudin ullamcorper. Donec ut imperdiet nulla, non facilisis lorem. Praesent tincidunt quis felis in egestas. Nam blandit mi at lacus bibendum, at dignissim ligula consectetur. Praesent et libero suscipit, vestibulum nulla ut, placerat augue. In maximus consequat felis eu convallis. Praesent lacus mauris, suscipit id sagittis eu, iaculis ac nisl. Nam eget accumsan turpis, eu consectetur nibh.

Cras porttitor nulla nec velit dignissim cursus eget vitae mauris. Nam consectetur quis est at sagittis. Nunc mattis ligula faucibus, mollis tellus in, fermentum est. Donec id augue id mi ultrices iaculis a aliquet mi. Curabitur sit amet libero non ex hendrerit eleifend. Vestibulum ac maximus dui, sit amet condimentum leo. Suspendisse potenti. Morbi consequat arcu odio, id feugiat lorem suscipit sed. Donec eu volutpat ex. Cras consectetur tempus arcu, eget efficitur leo mattis eget.

Fusce suscipit imperdiet risus, at ultricies est. Pellentesque id erat sed mauris lobortis maximus. Duis ornare elit id sapien dictum, semper auctor tortor fringilla. Duis euismod a nulla vulputate aliquam. Pellentesque porta leo lectus, sed efficitur justo consequat porta. Quisque id posuere erat, et consectetur sem. Sed vel pulvinar felis. Nam in mattis arcu, id varius diam. Vestibulum interdum, sapien ut egestas commodo, nibh tellus ultricies enim, auctor hendrerit est elit vitae felis. Vestibulum sed diam erat. Nulla elementum, nulla eget consequat tempus, magna metus convallis eros, vel posuere sem arcu eu eros. Ut blandit lectus eu lorem pellentesque, vel mattis lorem vulputate.

Vestibulum nulla tellus, hendrerit sit amet ligula sodales, maximus dictum sapien. Vivamus sollicitudin dapibus sapien, aliquet finibus tellus dapibus tempus. Suspendisse imperdiet erat tellus, ac faucibus tortor dictum eget. Etiam viverra neque vitae tortor maximus, ac rutrum ligula accumsan. Proin a massa ultricies, sollicitudin libero sit amet, dapibus ipsum. In turpis metus, mollis id massa sit amet, condimentum convallis arcu. Quisque non purus sit amet lectus aliquam elementum. Praesent convallis consequat enim id euismod. Morbi imperdiet nisi ex, quis pellentesque dui fringilla sed. Sed dolor arcu, vehicula sed pellentesque sed, varius id augue. Sed tempus diam a efficitur fermentum. Aenean sit amet dolor laoreet, aliquet velit id, dictum ex. Etiam eget erat elit. Proin eget convallis nulla. Praesent non metus sagittis, iaculis est quis, pretium tellus.

Mauris in volutpat nisl. Cras rutrum interdum nisl sit amet volutpat. Integer vel leo ligula. Cras sodales sapien at risus cursus, egestas ornare lacus posuere. In blandit euismod enim semper egestas. Ut imperdiet consequat eros, sit amet euismod lectus euismod sit amet. Ut vehicula sagittis velit nec efficitur. Quisque suscipit diam lorem, non luctus lorem eleifend tincidunt. Suspendisse potenti. Proin eget lacus scelerisque, ullamcorper lectus feugiat, cursus est. Sed in purus sed nisl viverra ornare in sit amet magna. Aenean nec ligula ex. Etiam urna lorem, dictum a mi vitae, sollicitudin finibus lorem. Integer tincidunt at lorem at efficitur. Cras efficitur leo lacus, suscipit tristique nibh malesuada at. Aenean convallis velit sed nulla consequat pulvinar.

Sed cursus felis sit amet tellus sagittis ultricies. Donec lacus orci, venenatis maximus tristique eget, blandit vitae dolor. Phasellus at velit eu quam malesuada mattis. Donec elementum tortor non tellus lacinia pretium. Praesent eget nibh eget ipsum rutrum dignissim sed sit amet nulla. Sed maximus ligula ac eros semper euismod. Ut suscipit neque nec nisi sodales, eget auctor lectus interdum. Curabitur faucibus posuere nulla, sit amet dapibus quam hendrerit vulputate. Sed mollis et ante eget dictum. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Mauris id vulputate sem. Praesent varius, justo eget vehicula fermentum, quam est placerat orci, id pretium nunc nulla sit amet turpis. Nulla tempor sem eros, nec fermentum ipsum iaculis vel. Vestibulum et sagittis ante, quis semper metus. Curabitur quis tempus est, eu accumsan justo.

Duis pretium dictum urna nec tincidunt. Etiam imperdiet nibh sed tellus aliquam, nec hendrerit ipsum suscipit. Etiam nisi massa, luctus in odio nec, venenatis commodo velit. Ut sem dolor, vestibulum quis eleifend et, tempor nec mi. Nunc rutrum ligula id diam congue sagittis. Donec ac placerat dolor. Morbi a fringilla orci. Mauris sit amet risus urna.

Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Maecenas enim nibh, iaculis sed accumsan ac, lobortis vitae libero. Curabitur varius vulputate porttitor. Phasellus consequat ligula felis. In interdum turpis metus, a commodo mi tempor nec. Donec interdum felis eu nibh varius consectetur. Sed sed leo in lectus convallis imperdiet. Integer venenatis, tortor eu lacinia bibendum, erat felis tristique risus, ac ultrices dui ante a magna. Nunc ac placerat sapien. Curabitur bibendum mauris lacinia, tincidunt libero a, sodales massa. Nam ac vehicula odio. Aliquam vel magna tristique, viverra augue in, dapibus eros. Nunc imperdiet vel sem et fermentum. Nullam sollicitudin sed mauris id congue. Donec rutrum, sapien a porta convallis, nibh turpis elementum purus, non mollis lorem massa ac nulla. In hac habitasse platea dictumst.

Curabitur velit leo, placerat eu gravida non, accumsan eget urna. Vivamus bibendum lobortis magna in lobortis. In hac habitasse platea dictumst. Vivamus tristique ultricies mauris, eget maximus dolor scelerisque eu. Sed vulputate suscipit nisl, at vehicula est venenatis sit amet. Proin rhoncus nisi posuere diam molestie, in laoreet felis placerat. Nunc erat enim, volutpat non dictum ac, tristique in purus. Nullam vulputate pretium nisl feugiat tristique. Quisque pharetra magna ligula, eu vestibulum neque lacinia tincidunt. Aliquam aliquet leo arcu, sed tristique urna bibendum sit amet. Vestibulum at blandit arcu.

Pellentesque pulvinar nunc non mollis pharetra. Vestibulum ac nisi enim. Mauris in varius nunc, ac ullamcorper libero. Mauris non sapien cursus, scelerisque augue ullamcorper, placerat neque. Sed pulvinar felis vitae nunc ultrices, consectetur imperdiet metus dictum. Phasellus ut ante vestibulum, faucibus augue at, tincidunt turpis. Integer euismod odio in mi ornare blandit. Donec aliquam et sem id elementum. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vivamus sollicitudin, diam ut pellentesque venenatis, lacus erat placerat nibh, vel vehicula est elit pellentesque nisl. Donec fermentum gravida hendrerit. Quisque mollis turpis in sem sagittis, eu maximus dolor auctor. Nunc at feugiat sem.

Pellentesque euismod nulla nec libero tincidunt semper. Phasellus sed lacus consequat, mollis erat vitae, rhoncus urna. Aenean iaculis, purus eget aliquam aliquet, arcu lectus dictum orci, sit amet venenatis magna neque at magna. Etiam feugiat euismod fermentum. Ut vel cursus nulla. Nulla lectus sem, tincidunt ut tempor at, ornare id sem. In lacinia ligula vitae dui viverra pharetra. Nullam vestibulum scelerisque sem quis molestie. Maecenas elementum erat et libero convallis, eu aliquet nisl vulputate. Donec ac ante orci.

Aliquam laoreet mollis lorem eget dignissim. Donec posuere ornare felis in imperdiet. In hac habitasse platea dictumst. Suspendisse tristique accumsan mi et vestibulum. Duis laoreet mauris id sapien commodo facilisis. Aliquam gravida arcu accumsan est cursus, vitae commodo risus consequat. Vivamus luctus finibus ante vitae scelerisque. Mauris pulvinar magna non luctus porttitor. Vestibulum in sapien ut mauris fermentum lacinia sed quis lorem. Aenean facilisis velit quam, sed eleifend magna eleifend sit amet.
