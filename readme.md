# ***Server Setup in Linux***

***Step 1: Install VirtualBox according to your Operating System from Url:https://www.virtualbox.org/wiki/Downloads***
---
**Download VirtualBox Platform Packages \& VirtualBox Extension Pack**
![alt text](img/image.png)
---
**Click "Next"**
![alt text](img/image-3.png)
---
**Click "Next"**
![alt text](img/image-4.png)
---
**Click "Next"**
![alt text](img/image-17.png)
---
**Click "Yes"**
![alt text](img/image-18.png)

---

**To fix this run cmd as administator and run py -m pip install pywin32 and Click "Yes"**
![alt text](img/image-5.png)
![alt text](img/image-31.png)
---
**Click "Next"**
![alt text](img/image-6.png)
---
**Click "Finish"**
![alt text](img/image-7.png)
---
***Step 2: Download Centos from Url:https://drive.google.com/file/d/1QXdagFhT5kchGL-iLlDSkcN2RqIskLmX/view or Url:https://www.centos.org/download/***

![alt text](img/image-16.png)
---
***Step 3: Extract the Centos Iso \& Double Click the Iso file. The VM will automatically run the Centos.***
---
![alt text](img/image-1.png)
---
![alt text](img/image-2.png)
---
![alt text](img/image-8.png)
---
![alt text](img/image-24.png)
---
![alt text](img/image-19.png)
---
***Step 4: Setup network in VM Box and Starting centos***
---
**Open Settings**
![alt text](img/image-20.png)
---
**Open network settings and click Expert**
![alt text](img/image-21.png)
---
**Click Port Forwarding**
![alt text](img/image-22.png)
---
**Set http values as shown in the Image**
![alt text](img/image-23.png)
---
**Click Start**
![alt text](img/image-25.png)
---

***Step 5: Enter "centos" for LocalHost login and password.***
---
![alt text](img/image-10.png)
---

***Step 6: Open terminal or Command prompt by Right clicking in desktop or search "terminal" or "CMD" in windows search.***
---
![alt text](img/image-11.png)
![alt text](img/image-12.png)
**or**
![alt text](img/image-32.png)
![alt text](img/image-33.png)
---
***Step 7: Type the following commands***
---


# ***Note***

   ***If you see "lines 1-20/20 (END)" Press " q "***
   ***This Exit the log***
---


***Connect to VM centos From windows terminal***
---
```sh
ssh centos@localhost
```
![alt text](img/image-26.png)
---
***Password*** 
---
```sh
centos
```
![alt text](img/image-27.png)
---
***Start the Lab Environment*** 
---
```sh
startlab1
```
![alt text](img/image-13.png)
---

***Check if httpd is installed***
---
```sh
sudo systemctl status httpd
```
![alt text](img/image-28.png)
**Press q to Exit Log**
---

***Install Httpd(If not installed)***
---
```sh
sudo yum install httpd -y
```


***Start Apache (httpd) Service***
---
```sh
sudo systemctl start httpd
```
![alt text](img/image-29.png)

***Press q to Exit Log***
---

***Enable Apache to start on boot (Optional).***
***This makes Apache start on every boot.***
---
```sh
sudo systemctl enable httpd
```
***Check status***
---
```sh
sudo systemctl status httpd
```
![alt text](img/image-15.png)
---

***You should see:***
***Active: active (running)***
---

***Step 8: Open your Windows browser and go to:***
---
```sh
http://localhost:8080/
```
![alt text](img/image-14.png)
---

***Troubleshooting***
---
## *Stop firewall temporarily (so Windows can access Apache Server )*
---
```sh
sudo systemctl stop firewalld
```

***Congratulations you  have successfully started the server.***
===


