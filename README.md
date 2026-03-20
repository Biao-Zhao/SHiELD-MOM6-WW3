# SHiELD–MOM6–WW3 Coupled Modeling System

This repository organizes the components and workflows for the SHiELD–MOM6–WW3 atmosphere–ocean–wave coupled modeling system.

---

## Overview

SHiELD–MOM6–WW3 is a high-resolution coupled modeling framework that integrates:

- **SHiELD** – Atmospheric model  
- **MOM6** – Ocean model  
- **WW3** – Wave model  
- **FMS / FMScoupler** – Coupling infrastructure  

---

## Build Instructions

To build the SHiELD–MOM6–WW3 coupled modeling system:

### 1. Clone the build repository

```bash
git clone -b wave git@github.com:Biao-Zhao/SHiELD_build.git


2. Download all required source code

./CHECKOUT_code

This step retrieves all required modules, including FMS, FMScoupler, SHiELD, MOM6, and WW3.

3. Build the WW3 coupling libraries

./Set_Up_WW3.csh

This step compiles WW3 into the library files required by the coupled system.

4. Compile the coupled model

cd SHiELD_build/Build/
./COMPILE shiewamom nh prod 64bit intel

This step builds the full SHiELD–MOM6–WW3 coupled modeling system.
