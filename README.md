# INURA
guide of image INURA 


# Requirements 

* Raspberry pi
* mazizone_v1 image . You can download from these link http://nitlab.inf.uth.gr/mazi-guides/download.html

# Set up

* At  **/home/pi** directory
**$ sudo git clone https://github.com/mazi-project/guides.git**                                                                 
Now you have all scripts from INURA image into the file **/INURA**                                                             
Rename it to  mazi                                                                                                             
**$ sudo mv /INURA /mazi**

* Go to dnsmasq.conf file                                                                                                       
**$ cd  /etc/dnsmasq.conf**                                                                                                  
Add the follow code at line 541                                                                                                 
**hcp-script=/home/pi/mazi/check.sh**                                                                                           

* Make inot2.sh to run every time the system starts                                                                             
Make it executable                                                                                                             
**$ chmod ugo+x /etc/init.d/internet-forward**         
Configure the init system to run this script at startup.                                                                       
**$ update-rc.d internet-forward defaults**
