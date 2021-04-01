# Karma_tutorial

#create a folder for the project that you are about to write the unit tests for 

#You can name it “basicUT”

#Open the Visual studio code inbuilt terminal window, 

#click the ‘View menu’, and then 

#select the integrated terminal sub-menu

#In the terminal window, type ‘npminit’ as shown in the below figure


![image](https://user-images.githubusercontent.com/79251268/113264737-eebb7100-92f0-11eb-8949-3b2d5291350b.png)

#This command guides you to automatically set up the ‘package.json’ file which every node-based application must-have


# Overview Of Karma.conf.js File Configuration Options

This configuration file can be created manually or automatically by using the command

       karma init
       
It starts to display different questions for you to answer, and Karma uses the answers that you provide to set up the configuration file.

If karma init’, gives the error as shown in the figure

 ![IMG_20210401_142549](https://user-images.githubusercontent.com/79251268/113270191-dc443600-92f6-11eb-9f8f-0e16527d4f10.jpg)
 
 To fix this error, we need to install Karma globally which is Karma-cli. Simply run the command
 
     npm install -g karma-cli
 
 ![IMG_20210401_142623](https://user-images.githubusercontent.com/79251268/113270275-ecf4ac00-92f6-11eb-81d7-cb5ff8642324.jpg)
    
Now re-run karma init

![IMG_20210401_142717](https://user-images.githubusercontent.com/79251268/113270241-e5350780-92f6-11eb-8a9f-b5a820429c3d.jpg)

During tests any package installed should be instaled using -save-dev option to instruct npm to install the package as a development dependency & not as a project dependency.

     npm install karma --save-dev

![IMG_20210401_142815](https://user-images.githubusercontent.com/79251268/113270252-e6663480-92f6-11eb-9377-f1055a6d88a9.jpg)


Now re-run the command karma-init, and you can see the questions as shown in the below figure. When you answer each question and press the ‘ENTER’ key, the next question will come up.

![IMG_20210401_142403](https://user-images.githubusercontent.com/79251268/113270229-e2d2ad80-92f6-11eb-92d0-ce49f2c70e16.jpg)
