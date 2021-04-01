#  Implementing The Project Using Jasmine Standalone Distribution And Gulp

The Jasmine standalone distribution thas the directory structure as shown below:

Directory Structure Of Jasmine Standalone Distribution Zip File
![Screenshot from 2021-04-01 15-48-29](https://user-images.githubusercontent.com/79251268/113281774-a48fbb00-9303-11eb-9169-c5a6d3c858df.png)

In the above image, you can see the SpecRunner.html file. This file displays the results of the tests in the browser.
As this file needs to be displayed in a web browser, there is a need to configure a server. The gulp package helps us with the need for configuring the server.

The lib folder --> Jasmine library files that facilitate the specRunner to display the output of the tests. 
The spec folder--> the test files and the src folder contains the javascript source codes that are required to make the tests pass.

#Note that the standalone distribution still needs the Jasmine package installed with npm for it to work.

#  1. Modifying SpecRunner.html And Directory Structure
Now, we need to delete the default files from the test folder and src folder and then create our own files. 
We also need to create our own folder called ‘JSON’ which will contain the course object in a JSON file. Hence, create a JSON file named ‘courses.json’.

As we have changed the directory structure, we need to modify our specRunner.html as well to make it as the code shown below:

![Screenshot from 2021-04-01 16-14-04](https://user-images.githubusercontent.com/79251268/113283256-b1151300-9305-11eb-9bd9-9869805f2f16.png)
Note that in the code, the Cgpa.js source file (that contains all our functions) is loaded first before the spec file, as the CgpaSpec.js file depends on Cgpa.js. Hence it must be specified first for the browser to load it first.
Now copy the absolute path of your specRunner.html and paste it into your browser address bar
You will discover the specRunner informing you that “no spec was found” as we included the spec file in the head tag.

# Writing The gulpfile.js File
we will use gulp to create a server on which we will always start our specRunner, browserify (our spec file) and then add it to our specRunner.html and further watch for changes in any of the files and continue to repeat the bundling.

