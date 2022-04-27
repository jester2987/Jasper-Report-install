# Jasper-Report-install
## ขั้นตอนการดาวน์โหลดและติดตั้งและ Jasper Report

พิมพ์คำสั่งเพื่อติดตั้ง chromium เพื่อใช้งานร่วมกับ Jasper Report
~~~
sudo apt install chromium-browser
~~~
พิมพ์คำสั่งเพื่อดาวน์โหลดไฟล์ Jasper Report
~~~
wget https://sourceforge.net/projects/jasperserver/files/JasperServer/JasperReports%20Server%20Community%20edition%208.0.0/TIB_js-jrs-cp_8.0.0_linux_x86_64.run
~~~
รอจนเสร็จสิ้น จะแสดง
~~~
TIB_js-jrs-cp_8.0.0_linux_x86 100%[=================================================>] 369.98M  7.70MB/s    in 57s
2022-04-25 07:58:57 (6.49 MB/s) - ‘TIB_js-jrs-cp_8.0.0_linux_x86_64.run’ saved [387947913/387947913]
~~~
เปลี่ยนสิทธิ์ให้กับไฟล์ที่ติดตั้ง
~~~
chmod a+x TIB_js-jrs-cp_8.0.0_linux_x86_64.run
~~~
รันคำสั่งติดตั้ง
~~~
sudo ./TIB_js-jrs-cp_8.0.0_linux_x86_64.run
~~~
โปรแกรมจะถามข้อกำหนดการใช้งาน License สำหรับใช้งานบนเครื่อง Server กด Enter ไปเรื่อยๆ เพื่อยืนยัน
พิมพ์ y เพื่อยืนยันการใช้ license
~~~
Do you accept this license? [y/N]: y  
~~~
โปรแกรมจะถามเรื่องพื้นที่ในการติดตั้ง พิมพ์ 1 เพื่อยืนยันการติดตั้งแบบ defualt
JasperReports Server Installation
~~~
Please choose an install option below:
[1] Install All Components and Samples (requires disk space of: 1.5 GB)
[2] Custom Install
Please choose an option [1] : 1     
~~~
โปรแกรมจะให้เลือกโฟลเดอร์ที่ทำการติดตั้ง tomcat อยู่ กด enter
~~~
Installation folder
Please, choose a folder to install JasperReports Server CP 8.0.0
Select a folder [/opt/jasperreports-server-cp-8.0.0]:
~~~
โปรแกรมจะถามหา Chromium browser เพื่อใช้งานกับโปรแกรม กด Enter เพื่อยืนยัน
~~~
Do you want to use Chromium? [Y/n]: Y
Chromium folder
Click Next to acknowledge this warning and continue with the installation.
Press [Enter] to continue:
https://community.jaspersoft.com/wiki/keystore-management-and-repair/ [Y/n]: Y
~~~
โปรแกรมจะให้กด Y เพื่อทำการติดตั้งโปรแกรม
~~~
Setup is now ready to begin installing JasperReports Server CP 8.0.0 on your
computer.
Do you want to continue? [Y/n]: Y
~~~
รอจนเสร็จจะแสดง 
~~~
Completing the JasperReports Server CP 8.0.0 Setup Wizard
For release notes and further documentation please see,
/opt/jasperreports-server-cp-8.0.0/docs. Our full documentation is also
available at http://community.jaspersoft.com/documentation
----------------------------------------------------------------------------
Setup has finished installing JasperReports Server CP 8.0.0 on your computer.
~~~
พิมพ์คำสั่งเพื่อเปิด Jasper Report
~~~
sudo /opt/jasperreports-server-cp-8.0.0/ctlscript.sh start
~~~
จะแสดง
~~~
waiting for server to start.... done
server started
/opt/jasperreports-server-cp-8.0.0/postgresql/scripts/ctl.sh : postgresql  started at port 5432
Using CATALINA_BASE:   /opt/jasperreports-server-cp-8.0.0/apache-tomcat
Using CATALINA_HOME:   /opt/jasperreports-server-cp-8.0.0/apache-tomcat
Using CATALINA_TMPDIR: /opt/jasperreports-server-cp-8.0.0/apache-tomcat/temp
Using JRE_HOME:        /opt/jasperreports-server-cp-8.0.0/java
Using CLASSPATH:       /opt/jasperreports-server-cp-8.0.0/apache-tomcat/bin/bootstrap.jar:/opt/jasperreports-server-cp-8.0.0/apache-tomcat/bin/tomcat-juli.jar
Using CATALINA_OPTS:
Using CATALINA_PID:    /opt/jasperreports-server-cp-8.0.0/apache-tomcat/temp/catalina.pid
Tomcat started.
/opt/jasperreports-server-cp-8.0.0/apache-tomcat/scripts/ctl.sh : tomcat started
~~~
เสร็จสิ้นการติดตั้ง
