# dsor_simulation-ros2
Simulation of DSOR vehicles using ROS2

## Installation

Create a folder to house the colcon workspace and clone this repo:

```bash
mkdir -p ~/colcon_ws_sim/src
git clone --recurse-submodules git@github.com:dsor-isr/dsor_simulation-ros2.git ~/colcon_ws_magicelectric/src/.
```

## Setting up ROS2 and Compiling

Follow the [README](farol2/README.md) for the FAROL 2 submodule, where the system requirements and useful scripts and alias are explained. To compile, simply move to the colcon workspace and build:

```bash
colcon_cd
colcon build --symlink-install
```

After building, source the `~/.bashrc`, which will source all ROS and workspace related setup files:

```bash
source ~/.bashrc
```

## Running

Run:
```
ros2 launch simulation_bringup start_vehicle.launch.py
```