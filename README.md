# rpi-cpu-stress

## Overview
We conducted a stress test on `NASPi` to check the heat dissipation of the product

We use rpi cpu stress to stress test the Raspberry Pi 4 2GB version, the OS is 2021-05-07-raspios-buster-armhf.img, and the charger used is type-c Huawei 65W fast charger， program running time exceeds 30 minutes

## How to test?

```
git clone https://github.com/geekworm-com/rpi-cpu-stress
cd rpi-cpu-stress
chmod +x stress.sh
sudo ./stress.sh
```

Use the `htop` command to monitor the task manager, you can see that all 4 processors are full.
```
sudo htop
```

The following is the log output of the program, temp divided by 1000 is the current CPU temperature

![the result of htop](https://wiki.geekworm.com/images/0/0f/Rpi-cpu-stress-1.png)

![log out](https://wiki.geekworm.com/images/0/0f/Rpi-cpu-stress-1.png)

## Test result
The 4 CPU cores are running at full load, the maximum temperature of the CPU core does not exceed 75 degrees, and the surface of the shell does not generate heat, which meets the design requirements.