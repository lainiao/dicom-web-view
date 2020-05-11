

Although GitHub was registered very early in 2010, it has basically not been used. The reason why I plan to use Github this time is to expect to complete this project with everyone.

# dicom-web-view

It is planned to implement a Dicom reading system based on Web technology. The initial plan is to realize the basic Dcm file display, window adjustment, rotation, zoom, mark, basic measurement and other functions. The system plans to support both PC and Mobile at the same time.


The project plans to use Springboot as the Server, Mysql as the database, MINIO as the storage middleware used offline, and Ali OSS as the storage middleware supported online. The front-end reading plugin currently plans to use cornerstone.js

cornerstone.js, this plugin is used because it is currently a relatively mature plugin in open source, but it is not excluded to write it later, because I am not satisfied with the use of the original DCM file for front-end reading. The factor is that the DCM file is large. The second factor is that the front-end parsing of the DCM file is actually more computationally intensive. If the project is completed, see if there is time to write an implementation, turn the DCM file into a special picture, and read it in the front end. The reason why it needs to be converted into a special picture is because the existing DCM to picture conversion will convert the DCM file into a picture with a fixed window width and window level, and map it to a picture with only 256 grayscales, which will be lost The original image information has lost the meaning of reading. If it is converted into this special picture, the pixel information will not be lost. However, the information of up to 65536 gray levels can still be maintained, and the image information will not be lost. Of course, this is said later, first realize the function, this is the optimization level Function.

 
Because I am lazy, I slowly updated this project and put my own ideas first.
 
Mind Mapping
------------
 
![image](https://github.com/lainiao/dicom-web-view/blob/master/document/img/1.png)
 
DataBase
-----------

![image](https://github.com/lainiao/dicom-web-view/blob/master/document/img/2.png)

Main Flow
-------------

![image](https://github.com/lainiao/dicom-web-view/blob/master/document/img/3.png)


