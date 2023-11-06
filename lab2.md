# Lab Report 2

## StringServer

**StringServer.java**

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/94b04e5e-03d4-4ec8-9f11-729f998189b9)

* /add-message?s=Hello
  
![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/7dec67ee-82de-4342-b622-7e1c31bf03d2)

* /add-message?s=How are you

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/88030008-94b2-4a23-94fd-a3175ca2c438)

so the method handleRequest gets called, therefore the stringSearch field is initalized to an empty string and the field numAdd is initialized to 0. Therefore when you are calling the getPath /add-message, with the query s=, it icremenets in the numAdd by one, it takes the argument of the query split which is the message after the s= which means I also have a value of a string thats initalized to an empty string which will be part of the inside if statement, which is a empty string. Therefore I have a try catch to decode the query split which contains the message, then it gets concatened in a string format for the stringSearch field with the field value and field numAdd increment which is returned.

**ls into private key of ssh**

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/287e650b-6183-447d-86a2-5d2a7263148c)

the public key starts with the file extension .pub meanwhile the private key does not have .pub therefore it is id_rsa

**path to the public key**

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/30eefa7e-8971-4860-9724-59325b3069d4)

**terminal without password**

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/a915088c-1239-4e5a-9202-e16ea9bab499)


This week I learned how to use SSH and understand how to make a new directory, these are the things I have never used in my daily life, therefore understanding these commands have taught me how to remote into a server, giving me more knowledge on how SSH works.
