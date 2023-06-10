# rosrelatedqueries

## ROS_Installation
- If you get this error *failed : package not found* something like this after doing **sudo apt update** while installing ros-noetic ninjemys then follow these steps

`sudo apt-key del 421C365BD9FF1F717815A3895523BAEEB01FA116 `

`sudo -E apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654`

- if this results in errors (similar to "gpg: keyserver receive failed: End of file" or others indicating the key server could not be reached), an alternative would be (make sure curl is installed):

`curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -`

- if second command didn't result in errors then directly execute this command

`sudo apt clean && sudo apt update`

---

- *libqt5webkit5 not found*. So resolve this issue paste this on your browser and a debian file will be downloaded

`http://ports.ubuntu.com/ubuntu-ports/pool/universe/q/qtwebkit-opensource-src/libqt5webkit5_5.212.0~alpha4-1ubuntu2_arm64.deb`

- go to downloaded file location and then install it using dpkg -i command

`sudo dpkg -i <file_name>.deb`

- you might face issue after this regarding dependencies not installed so to resolve this use the below command

`sudo apt-get install -f`

- again try installing the debian package

`sudo dpkg -i <file_name>.deb`

---
