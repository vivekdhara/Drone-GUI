<h1 align="center">
  <a href="https://github.com/vivekdhara/drone-gui">
    <!-- Please provide path to your logo here -->
    <img src="docs/images/logo.svg" alt="Logo" width="100" height="100">
  </a>
</h1>

<div align="center">
  Drone GUI
  <br />
  <a href="#about"><strong>Explore the screenshots »</strong></a>
  <br />
  <br />
  <a href="https://github.com/vivekdhara/drone-gui/issues/new?assignees=&labels=bug&template=01_BUG_REPORT.md&title=bug%3A+">Report a Bug</a>
  ·
  <a href="https://github.com/vivekdhara/drone-gui/issues/new?assignees=&labels=enhancement&template=02_FEATURE_REQUEST.md&title=feat%3A+">Request a Feature</a>
  .<a href="https://github.com/vivekdhara/drone-gui/discussions">Ask a Question</a>
</div>

<div align="center">
<br />

[![Project license](https://img.shields.io/github/license/vivekdhara/drone-gui.svg?style=flat-square)](LICENSE)

[![Pull Requests welcome](https://img.shields.io/badge/PRs-welcome-ff69b4.svg?style=flat-square)](https://github.com/vivekdhara/drone-gui/issues?q=is%3Aissue+is%3Aopen+label%3A%22help+wanted%22)
[![code with love by vivekdhara](https://img.shields.io/badge/%3C%2F%3E%20with%20%E2%99%A5%20by-vivekdhara-ff1414.svg?style=flat-square)](https://github.com/vivekdhara)

</div>

<details open="open">
<summary>Table of Contents</summary>

- [About](#about)
  - [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Roadmap](#roadmap)
- [License](#license)
- [Acknowledgements](#acknowledgements)

</details>

---

## About

<table><tr><td>

> **[?]**
> Provide general information about your project here.
> What problem does it (intend to) solve?
> What is the purpose of your project?
> Why did you undertake it?
> You don't have to answer all the questions -- just the ones relevant to your project.

<details>
<summary>Screenshots</summary>
<br>

> **[?]**
> Please provide your screenshots here.

|                               Home Page                               |                               Login Page                               |
| :-------------------------------------------------------------------: | :--------------------------------------------------------------------: |
| <img src="docs/images/screenshot.png" title="Home Page" width="100%"> | <img src="docs/images/screenshot.png" title="Login Page" width="100%"> |

</details>

</td></tr></table>

### Built With

> **[?]**
> Please provide the technologies that are used in the project.

## Getting Started

### Prerequisites

Tested With Ardupilot Stable Release on Ubuntu 18.04.

### Installation


#### 1. Gazebo, and Web Dependecies
Gazebo is an open-source 3D robotics simulator. Gzweb is a WebGL client for Gazebo. It is a front-end graphical interface to gazebo and provides visualization of the simulation even on mobile devices

```
sudo apt install gazebo9 libgazebo9-dev
```

```
sudo apt install curl
` curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
sudo apt install
libjansson-dev libboost-dev imagemagick libtinyxml-dev mercurial cmake build-essential
nvm install 8
source ~/.bashrc
sudo apt install git
cd ~; git clone https://github.com/osrf/gzweb
cd ~/gzweb
git checkout gzweb_1.4.1
echo "source /usr/share/gazebo/setup.sh" >> ~/.bashrc
npm run deploy --- -m
```

### 2. ROS 

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt update
sudo apt install ros-melodic-ros-base
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc
source /opt/ros/melodic/setup.bash
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
sudo rosdep init
rosdep update
```

### 3.MAVROS

```
sudo apt-get install ros-melodic-mavros ros-melodic-mavros-extras ros-melodic-mavros-msgs
wget https://raw.githubusercontent.com/mavlink/mavros/master/mavros/scripts/install_geographiclib_datasets.sh
sudo bash ./install_geographiclib_datasets.sh   
```


### 4. Ardupilot

```
git clone https://github.com/r0chin/ardupilot
git config --global url."https://github.com".insteadOf git://github
cd ardupilot/
git submodule update --init --recursive
sudo Tools/scripts/install-prereqs-ubuntu.sh -y
sudo ~/.profile
sim_vehicle.py -v ArduCopter -f gazebo-iris --map --console```
```

### 5. Ardupilot Gazebo Plugin

```
git clone https://github.com/khancyr/ardupilot_gazebo
cd ardupilot_gazebo
mkdir build
cd build
cmake ..
make -j4
sudo make install
echo 'source /usr/share/gazebo/setup.sh' >> ~/.bashrc
echo 'export GAZEBO_RESOURCE_PATH=~/ardupilot_gazebo/worlds:${GAZEBO_RESOURCE_PATH}' >> ~/.bashrc
source ~/.bashrc
```



### 6. Packages (Conda)
```
bash radioconda-2023.07.26-Linux-x86_64.sh
mamba install numpy h5py Flask flask-socketio geopy folium simplekml branca simple-websocket pykml tornado rospkg
```

## Usage

```
./run ; localhost:5000

```


## Contributing

First off, thanks for taking the time to contribute! Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make will benefit everybody else and are **greatly appreciated**.


Please read [our contribution guidelines](docs/CONTRIBUTING.md), and thank you for being involved!
, see [the contributors page](https://github.com/vivekdhara/drone-gui/contributors).


## License

This project is licensed under the **MIT license**.

See [LICENSE](LICENSE) for more information.

## Acknowledgements

> **[?]**
> If your work was funded by any organization or institution, acknowledge their support here.
> In addition, if your work relies on other software libraries, or was inspired by looking at other work, it is appropriate to acknowledge this intellectual debt too.
