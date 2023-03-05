# Ubuntu Core on Xilinx Kria
This repository contains the required snaps, assertions to build an Ubuntu Core image for Xilinx Kria boards.

## Dependencies
```
sudo apt install wget git snapd
sudo snap install snapcraft --classic
sudo snap install ubuntu-image --classic
git clone https://github.com/talhaHavadar/ubuntu-core-kria-assertions.git && cd ubuntu-core-kria-assertions
```

## Build

To build the ubuntu core image, first we need to download the kernel and gadget snaps.

```
wget https://github.com/talhaHavadar/ubuntu-core-kria-assertions/releases/download/v0.0.1-pre-release/kria-kv260_22-1_arm64.snap
wget https://github.com/talhaHavadar/ubuntu-core-kria-assertions/releases/download/v0.0.1-pre-release/zynqmp-kernel_5.15.0-1018.20_arm64.snap
```

Once you have the required files to build, you can run the following command to build your own Ubuntu Core image and voila! Enjoy the UC.
```
ubuntu-image snap my-model.model --snap kria-kv260_22-1_arm64.snap --snap zynqmp-kernel_5.15.0-1018.20_arm64.snap
```

