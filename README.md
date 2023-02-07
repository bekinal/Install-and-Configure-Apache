<h1>Install & Configure Apache</h1>

<h2>Description</h2>
Project consists of installing the Apache2 service using Packet Manager. Apache2 is then configured to manage local web server access options. The status of the service is then verified, and restarted
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b>
- <b>Debian Environment</b>
- <b>Terminal</b>
- <b>Apache2</b>
- <b>Netstat</b>

<h2>Install and Configure Apache2:</h2>
Under the root user the service --status-all command is run. Apache2 is noted to be absent from the system:<br/>
<img src="https://imagizer.imageshack.com/img922/3638/clLd4l.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Netstat -l is used to listen to all open ports in the operating system to check if the HTTP protocol is listening. It can be noted that port 80 is not listening:<br/>
<img src="https://imagizer.imageshack.com/img922/1551/Hhl1LZ.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The apt install apache2 -y command is executed to install HTTP server Apache2:<br/>
<img src="https://imagizer.imageshack.com/img923/6229/JARyAc.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The service start command is used to start the Apache2 service. The service is then verified as running with the service status command:<br/>
<img src="https://imagizer.imageshack.com/img924/8793/n0UHrd.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Netstat -l is used again. This time, Apache2 appears on the system:<br/>
<img src="https://imagizer.imageshack.com/img922/9601/e54meL.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The firefox browser is opened:<br/>
<img src="https://imagizer.imageshack.com/img923/2361/3mPwqF.png" alt="Disk Sanitization Steps"/>
<br />
<br />
After browsing to 127.0.0.1, it can be noted that the local server is up and running:<br/>
<img src="https://imagizer.imageshack.com/img923/7762/YB9Xxr.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Nano is used to open the Apache2 configuration file:<br/>
<img src="https://imagizer.imageshack.com/img922/6104/kiIrYr.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The Listen port number is changed from HTTP to HTTP-alt. The file is saved and exited:<br/>
<img src="https://imagizer.imageshack.com/img924/3862/fU7zt8.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The Apache2 server is restarted amd verified as running:<br/>
<img src="https://imagizer.imageshack.com/img923/5978/GTKpCR.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Lsof -i and grep are used to check if port 8080 is listening:<br/>
<img src="https://imagizer.imageshack.com/img923/3791/eo8Z9R.png" alt="Disk Sanitization Steps"/>
<br />
<br />
127.0.0.1 is browsed again. This time, the webpage does not respond:<br/>
<img src="https://imagizer.imageshack.com/img922/849/LTeGPM.png" alt="Disk Sanitization Steps"/>
<br />
<br />
Instead, 127.0.0.1:8080 is entered into the search bar. The page loads as HTTP-alt:<br/>
<img src="https://imagizer.imageshack.com/img923/3890/Q33SwE.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The listening port is changed back to 80:<br/>
<img src="https://imagizer.imageshack.com/img923/5056/4pn0WK.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The Apache2 service is restarted:<br/>
<img src="https://imagizer.imageshack.com/img924/8498/qDss9L.png" alt="Disk Sanitization Steps"/>
<br />
<br />
The Apache2 default page can now be reached with its normal HHTP address:<br/>
<img src="https://imagizer.imageshack.com/img923/305/S8d7L5.png" alt="Disk Sanitization Steps"/>
<br />
<br />



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
