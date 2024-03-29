# BBS - jforum-2.4.1
采用开源框架 jforum2  二次开发。


#How to use it.

          1.download SourceForge : https://code.google.com/p/jforum2   
          
          2.Export jforum2 to GitHub then download the zip file.    
          
          3.开发工具 intellij idea + Maven + Jetty    
          
          4.将项目以 Maven 的特性导入到开发工具   
          
          5.安装数据库 mysql 字符集 utf-8  
          
          6.开发工具配置 maven-jetty 服务
          
          7.修改配置文件 src/main/config/SystemGlobals.properties   
            i18n.board.default = zh_CN  
            database.driver.name = mysql  
            
          8.修改数据库配置文件 src/main/config/database/mysql/mysql.properties  
          
          9.添加配置文件 src/main/config/ 目录下 jforum-custom.conf  
          
          10.修改配置文件 src/main/config/jforum-custom.conf  
             installed =true  
             
          11.删除安装配置
             
             src/main/config/modulesMapping.properties
             install  
             
             src/main/config/csrf.properties
             checkInformation
             welcome
             doInstall
             finished  
          
          12.初始化数据库   默认管理员 admin/admin
             src/main/config/database/mysql/mysql_db_struct.sql   
             src/main/config/database/mysql/mysql_data_dump.sql   
             
          13.允许jetty maven 配置 jetty:run-war -DskipTests

 
#框架分析
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/jfroum.png?raw=true) 

#Jforum 源码目录
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/jforum-construction.png?raw=true)

#CONF 目录
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/jforum-conf-construction.png?raw=true)

#WEB.XML 处理 Servlet 流程
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/jforum_web_xml.png?raw=true)

#Servlet net.jforum.JForum
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/Jforum-servlet.png?raw=true)

#Service net.jforum.JForum - service
![Aaron Swartz](https://github.com/ittarvin/image/blob/master/image/jforum-servlet-desc.png?raw=true)