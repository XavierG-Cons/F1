# ROS

## 1.安装ROS

sudo sh -c '. /etc/lsb-release && echo "deb http://mirrors.ustc.edu.cn/ros/ubuntu/ `lsb_release -cs` main" > /etc/apt/sources.list.d/ros-latest.list'

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

sudo apt update

sudo apt install ros-melodic-desktop-full

sudo rosdep init				//问题一   问题二
rosdep update

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc

sudo apt install python-rosinstall python-rosinstall-generator python-wstool build-essential

## 2.SSH

```shell
ls -al ~/.ssh

ssh-keygen -t rsa -C "1906492408@qq.com"

ls -al ~/.ssh

cat /home/lv/.ssh/id_rsa.pub
```



# Problem

## 1.sudo: rosdep：找不到命令

sudo rosdep init
sudo: rosdep：找不到命令
sudo apt-get install python-rosdep

## 2.ERROR: cannot download default sources list from

（1）换源

（2）

如果提示的是 ERROR: unable to process source https://raw.githubusercontent.com/ros/rosdistro/master/rosdep/xxxxx 之类的错误，同时保证自己机器可以上百度的前提下，此时可能是因为raw.githubusercontent.com网站被墙了。
解决办法是修改hosts文件，添加这个网站的ip地址

#打开hosts文件
sudo gedit /etc/hosts
#在文件末尾添加
151.101.84.133  raw.githubusercontent.com
#保存后退出再尝试



# 安装软件

## 1.Typora

```
# or run:
# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -

# add Typora's repository
sudo add-apt-repository 'deb https://typora.io/linux ./'
sudo apt-get update

# install typora
sudo apt-get install typora
```

## 2.TMUX

```
sudo apt-get install tmux
```

## 3.Python3.7虚拟环境

```
sudo apt install python3.7-venv
python3.7 -m venv projectA
source ./projectA/bin/activate
deactivate
```

[https://blog.csdn.net/heww/article/details/92803938](https://blog.csdn.net/heww/article/details/92803938)

# 命令

## 1.touch    mkdir





# BITFSD2020

## 1.     ./update_dependencies.sh

1.sudo apt install checkinstall

Checkinstall 是一个能从 tar.gz 类的源代码自动生成 RPM／Debian 或Slackware 安装包的程序。通过 CheckInstall，你就能用几乎所有的 tar.gz 类的源代码来生成“干净”的安装或者卸载包。

2.sudo apt-get install python-catkin-tools

3.sudo apt install libgoogle-glog-dev

4.sudo apt-get install ros-kinetic-geographic-msgs（Ubuntu16.04）或sudo apt-get install ros-melodic-geographic-msgs（Ubuntu18.04）

## 2.ACADOtoolkit

```
git clone https://github.com/acado/acado.git -b stable ACADOtoolkit

//修改install_ACADO.sh文件第一行

source install_ACADO.sh
```

```
 bash auto_build.sh 
```

```
最后catkin build
```

# Offline_Tools

```
sudo apt install python-pip
pip install numpy -i https://pypi.tuna.tsinghua.edu.cn/simple
pip install matplotlib -i https://pypi.tuna.tsinghua.edu.cn/simple 
sudo apt-get install python3-tk
```

