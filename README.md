# Autonomous-of-drone-using-raspi
me and my team done a project on drone and my role is to make drone autonomous. here i mention my methrod that i used to perfrom automation onn drone 
Frist you have to connect raspi and pixhawk as mention in given image 
Then you have to setup raspi 
  1- Install raspi os 64bit in a memory card of 32gb using Raspberry Pi Imager link: https://www.raspberrypi.com/software/
  2- As soon as it install setup VNC in raspi with your laptop
  3- After that install below mention library in raspi
     run below mention command on raspi terminal 
        sudo apt-get update
        sudo apt-get install python3-dev python3-opencv python3-wxgtk4.0 python3-pip python3-matplotlib python3-lxml python3-pygame
        pip3 install PyYAML mavproxy --user
        sudo pip install pymavlink
        sudo pip install mavproxy
  4- After that you have to enable serial port and disable serial control
     for that you have to go to terminal and run sudo rapi-confi 
     that you pop up a window in that go to
     Interfacing option ----->  Serial ----->  no ----->  yes ----->  finish
     after that restart your raspi 
  5- After that you have to edit config file of raspi
     for that you have to run command on raspi terminal 
      nano /boot/config.txt
     after that you have to mention below given line in file last line
      start_x=1
      gpu_mem=128
      enable_uart=1
      dtoverlay=pi3-disable-bt
   Now you raspi is setup
Now you have to opean misson planner and in that you have to set baudrate of telemetery2 as 921600
      
      
      
      
        
        
