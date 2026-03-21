## Overview
This repository organizes workflows for compiling and running the SHiELD–MOM6–WW3 atmosphere–ocean–wave coupled modeling system. SHiELD–MOM6–WW3 is a coupled modeling framework that integrates:
- **SHiELD** – Atmospheric model ([FV3 dynamical core](https://github.com/NOAA-GFDL/GFDL_atmos_cubed_sphere), [SHiELD physics](https://github.com/NOAA-GFDL/SHiELD_physics))  
- **MOM6** – [Ocean model](https://github.com/NOAA-GFDL/MOM6)
- **SIS2** - [Sea ice moel](https://github.com/NOAA-GFDL/SIS2)
- **WW3** – [WaveWatch III wave model](https://github.com/NOAA-EMC/WW3) 
- **FMS** - [Coupling infrastructure](https://github.com/NOAA-GFDL/FMS)
- **FMScoupler** – [FMS Coupler](https://github.com/NOAA-GFDL/FMScoupler)

At its current stage, this repository primarily serves as a personal reference and working log, documenting the procedures, scripts, and configurations used to compile, configure, and run the coupled system. The content is still under active development and will be gradually expanded and refined to include more standardized workflows.

---

## Build Instructions


### 1. Clone the build repository
To compile SHiELD, the first step is to clone the build repository [build repository](https://github.com/NOAA-GFDL/SHiELD_build). If you want to enable WW3 coupling support, you should check out the following branch:

```bash
git clone -b wave git@github.com:Biao-Zhao/SHiELD_build.git
```

### 2. Download all required source code

```bash
cd SHiELD_build/
./CHECKOUT_code shiewamom
```

This step retrieves all required modules, including FMS, FMScoupler, SHiELD, MOM6, and WW3.

### 3. Build the WW3 coupling libraries
In SHiELD_build directory, run the following command
```bash
./Set_Up_WW3.csh
```

This step compiles WW3 into the library files required by the coupled system.

### 4. Compile the coupled model

```bash
cd Build/
./COMPILE shiewamom nh prod 64bit intel
```

This step builds the full SHiELD–MOM6–WW3 coupled modeling system. If the compilation is successful, an executable file  
`SHiEWaMOM_nh.prod.64bit.intel.x` will be generated

## Running Instructions
To be completed..........
