
### --- driver brightness

		sudo add-apt-repository ppa:apandada1/brightness-controller
		sudo apt-get update
		sudo apt-get install brightness-controller-simple
		sudo apt-get install brightness-controller

### --- additional OS

		sudo usermod -a -G dialout $USER
		sudo reboot
		sudo apt install net-tools
		sudo apt install openssh-server
		sudo apt install apache2
		sudo apt install g++ git
		sudo apt install curl

### --- dynamixelsdk
> https://emanual.robotis.com/docs/en/software/dynamixel/dynamixel_sdk/library_setup/cpp_linux/

		$ sudo apt-get install gcc-5
		$ sudo apt-get install build-essential
		$ sudo apt-get install gcc-multilib g++-multilib

		/DynamixelSDK/c++/build/linux64$ make

Copy (Install) the Library to the Root Directory

		/DynamixelSDK/c++/build/linux64$ sudo make install
example

		DynamixelSDK/c++/example/protocol1.0/read_write/linux64$ make && ./read_write

### --- OP3_patch
> https://emanual.robotis.com/docs/en/platform/op3/recovery/#recovery-of-robotis-op3
	
		$ sudo apt-get update
		$ sudo apt install samba samba-common python-glade2 system-config-samba
#####  Samba

	Installation


		$ sudo apt install samba samba-common python-glade2 system-config-samba

   
	Configuration

		$ sudo touch /etc/libuser.conf
		$ sudo system-config-samba

		Go to Preferences > Samba Users…
		    Click Add User button
		    Select the Unix Username (ex : rscuad)
		    Enter the Windows Username (ex : rscuad)
		    Enter the Password (ex : rscuad)
		Click Add Share button
		    In the Basic tab
		        Enter / in the Directory.
		        Check on the Writable / Visible option.
		    In the Access tab
		        Select Only allow access to specific users
		        Select samba user

##### ros
> http://wiki.ros.org/melodic/Installation/Ubuntu


##### Installing additional applications 
	
		$ sudo apt install v4l-utils
		$ sudo apt install madplay mpg321

##### Installing ROS packages 
		
		$ cd ~/catkin_ws/src
		$ git clone https://github.com/ROBOTIS-GIT/face_detection.git
		$ cd ~/catkin_ws
		$ catkin_make
robot_upstart

		$ sudo apt install ros-melodic-robot-upstart

usb_cam

		$ cd ~/catkin_ws/src
		$ git clone https://github.com/bosch-ros-pkg/usb_cam.git
		$ cd ~/catkin_ws
		$ catkin_make
		$ sudo apt install v4l-utils
qt_ros


		$ sudo apt install ros-melodic-qt-ros

Package for footstep planner.
Install prerequisite packages

		$ sudo apt-get install ros-melodic-map-server
		$ sudo apt-get install ros-melodic-humanoid-nav-msgs [ paket tidak ada ]


patch manual

		cd ~/catkin_ws/src/
		git clone https://github.com/ahornung/humanoid_msgs.git
		cd ../
		catkin_make 
		
		cd ~/catkin_ws/src/
		$ sudo apt-get install ros-melodic-nav-msgs
		$ sudo apt-get install ros-melodic-octomap
		$ sudo apt-get install ros-melodic-octomap-msgs
		$ sudo apt-get install ros-melodic-octomap-ros
		$ sudo apt-get install ros-melodic-octomap-server

humanoid_navigation
> https://github.com/sbpl/sbpl

		$ sudo apt-get install ros-melodic-sbpl

Install humanoid_navigation

		$ cd ~/catkin_ws/src
		$ git clone https://github.com/ROBOTIS-GIT/humanoid_navigation.git
		$ cd ~/catkin_ws

Packages for web_setting_tool

		$ sudo apt install ros-melodic-rosbridge-server ros-melodic-web-video-server

Download sources from Github. 

		$ cd ~/catkin_ws/src
		$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-Framework.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-Framework-msgs.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-Math.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-OP3.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-OP3-Demo.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-OP3-msgs.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-OP3-Tools.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-OP3-Common.git
		$ git clone https://github.com/ROBOTIS-GIT/ROBOTIS-Utility.git
		$ cd ~/catkin_ws
		$ catkin_make
ETC Setting
 
		$ cd ~/catkin_ws/src/ROBOTIS-OP3-Tools/op3_web_setting_tool
		$ sudo cp -r ./html /var/www


