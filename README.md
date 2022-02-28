# vsomeip-for-qnx
vsomeip(3.1.20) library patched for qnxnto

Ubuntu 18.04 x86_64
cmake 3.10.2

make sure you have install qnx700 sdp and qcc is vaild before compiling.

1. source your_qnx700/qnxsdp-env.sh

you can set target build arch using QNX_ARCH environment variable.

2. export QNX_ARCH=aarch64le

3. cd vsomeip-master
4. mkdir build && cd build
5. cmake ../ -DCMAKE_TOOLCHAIN_FILE=../../qnx.cmake
6. make

of course, i removed 'netlink' function call, and 'socket credentials', for modified details, please diff with original vsomeip project. 
