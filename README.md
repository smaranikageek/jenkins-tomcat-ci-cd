  
Jenkins Installation  

1. First we have to create instances for Jenkins and tomcat.
   
2. Next we have to connect the Jenkins instance with port number 8080.
   
3. Install Java-17 version and git and maven.     
using command:-  sudo yum install java-17 -y   
                 Sudo yum install git -y   
                Sudo yum install maven -y
      
4. Search for Jenkins on Aws in  web page , in that there some Jenkins  
  
installation commands will display. Write vi filename.sh ,Copy that links and paste it in amazon linux.  
  
5. After completing all installation of Jenkins , copy the public ipv4 address and paste it in webpage using port number :8080. It  will display page.  
  
6. copy that file of the server and paste it in amazon linux using sudo cat it will  
  
give password of that file, copy that and paste it in unlock Jenkins page.  
7. After click on plugins it will show to give us personal details like  (Name, mail, username, password).  
--------------------Jenkin installation completed --------------------
TOMCAT installation
   
1. First we have to create instance for tomcat same as Jenkins and connect it.   
2. Search for tomcat install in software in webpage.    
3.	In that copy the link of tar.gz and paste that link in amazon linux using wget .   
  
  
   
4.	After that we have to extract the tar.gz file.   
Using cmd:- 
tar -zxvf filename   
5. After extraction of the file , we will change the name of extract file using mv .    
6. Next connect with tomcat in that open bin file in that we make bash startup.sh .    
  
  
7. Copy the public id of tomcat instance and paste it in webpage using port number :8080.   
  
   
8. Click on manager app , it show’s 403 Access Denied    
    
9. For to rectify this error    
Install locate---- sudo yum install locate   updatedb   locate context.xml   
    
10. copy the last line path and paste it , next vi context.xml    In that delete Valve content and next do conf    
 11. In conf we have to edit vi users.xml in this we have to edit roles.   
12. After that do bash startup.sh and next reload the web page  of tomcat.    
    
   
13. It will show user login details.   
   
  
   
14. After give sign in details we logging into tomcat web application.   
  
  
   
   
----------------------Tomcat installation completed --------------------   
 
PROJECT STEPS   
1. open Jenkins manage settings for to login.   
2. Go to plugings in that available plugins , search for deploy to container install it . Back to Jenkins home page.   
3. Create new item give any name , check in freestyle ,and click ok .   
  
  
4. click on configure any description   
     Next source code management in that we have to git    
              After selection git it display  url of rep we have to give that.   
5. click on Build steps select invoke type -level maven target             Nextwe have give goal as clean package.   
   
  
   
6. click on post -build actions  select deploy war/ear to a container.           
   Nextwar/ear files give target/*.war and next we have to give                              
Context path (any name)   
    
7. Add containers in that we have to give user name and password of tomcat , Next we have to give tomcat url and apply and save. click on build now.   
   
   
  
8. This screen shot shows the status of build.  
9. It shows that our project application.   
 
   
 10. Click on that project name file what we give it will display the content  
.  
   
  
  
  

