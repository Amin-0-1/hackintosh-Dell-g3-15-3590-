
There are 2 methods to make touchpad work
1- interrupt GPIO pinning
2- polling 

As the voodooi2c docs says it is preferable that your are running interrupt GPIO pinning as it use a little resources (ram and cpu) , in contradiction with polling mode which is using lots of resources


Use the attached kexts as they have some changes for making interrupt GPIO working properly , also note that , your Voodoops2Controller should not has any plugin kexts except voodoops2keyboar , delete all of that (mouse,trackpad) and make sure there is no voodooinput too


https://voodooi2c.github.io/


