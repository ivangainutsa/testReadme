# project NBG ![alt text][logo]

## Servers:
***
#### tomcat7x : Local Development
	http://localhost:8080


## 	Management:
***
	
#### DB: NBG
See **`hibernate.cfg.xml`**

Credentials for management : 
>See **`filter_values_development.properties` :** `fv.jdbc.username` , `fv.jdbc.password` , `fv.db.name`

#### solr: NBG
Credentials for management : 
>See **`filter_values_production.properties`** : `fv.jdbc.username` , `fv.jdbc.password` , `fv.db.name`

#### Rest API documentation: NBG
	http://localhost:8080/NBG/swagger

	
## 	install project in local:
***
1. clone project in computer
2. downloads and install program Workbench [link](https://dev.mysql.com/downloads/workbench/)
3. downloads and install SQL [link](https://drive.google.com/drive/folders/0B4alBSKMwoHLMFhvRnZGY3c1WGM)  
 a. create new_schema from name `fv.db.name`  
 b. rewrite your login and password in the file **`filter_values_development.properties`** to those indicated in Workbench  
4. downloads solr-4.10.4 [link](https://drive.google.com/drive/folders/0B4alBSKMwoHLMFhvRnZGY3c1WGM)  
 a. unzip the program solr-4.10.4  
 b. run the file `start.bat` **`"С:\solr-4.10.4\example\start.bat"`**  
5. downloads and install set to jdk1.8.0_152 in Eclipse [link] (https://drive.google.com/file/d/1HayaRxt7HRTBpXlgQf0yzhbnEr2X1oC1/view) 
6. finish

## 	run project in local:
*** 
1. open project in Eclipse
2. remove javascript errors from the project `Markers` -> `Delete`
3. run solr `start.bat` **`"С:\solr-4.10.4\example\start.bat"`** but don't close the console
4. `Run as` this file `NBG_DEV.launch` 
5. url project http://localhost:8080/NBG/login  
 a. login and password take from DB in table `app_user` 
6. to work with Rest API you needy install Postman [link](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop?hl=ru)  
 a. run Postman  
 b. insert url http://localhost:8080/NBG/rest/????  
 c. type selected **"Basic Auth"** you needy insert login and password take from DB in table `app_user`  
7. finish

## 	move the project to Java 8:
*** 
1. downloads and install set to jdk1.8.0_152 in Eclipse [link](https://drive.google.com/file/d/1HayaRxt7HRTBpXlgQf0yzhbnEr2X1oC1/view)  
2. `Maven` -> `Update project...`  
3. `Properties` -> `Java Compiler` -> `Installed JREs` -> `Add` -> `Next` -> `Directory` **C:\Program Files\Java\jdk1.8.0_152** -> `Finish` -> select **jdk1.8.0_152** -> `Apply and Close` -> `Apply and Close`  
4. restart Eclipse 
5. `Run As` -> `Maven clean` the project
6. `Maven` -> `Update project...` 
8. finish

## 	How to resolve Libraries problem:
*** 
1. `Run As` -> `Maven clean` the project
2. `Maven` -> `Update project...` 
3. remove javascript errors from the project

  

## 	for now we are waiting for:
*** 
maven build - production:
	
	clean compile war:war -DbuildTarget=production

1)In Eclipse set to jdk1.7.0_79



[logo]: https://github.com/ivangainutsa/testReadme/blob/master/favicon.ico "Logo"
