# ccminer for ARMv7a on Termux (cortex-a15 cortex-a7)

Based on [https://github.com/monkins1010/ccminer/tree/ARM](https://github.com/monkins1010/ccminer/tree/ARM) and [https://github.com/Oink70/CCminer-ARM-optimized.git](https://github.com/Oink70/CCminer-ARM-optimized.git)
Software AES taken from [https://github.com/turvopit/ccminer.git](https://github.com/turvopit/ccminer.git)

Git and Build Process:
```
pkg update && pkg upgrade -y
pkg install git clang cmake make autoconf automake libtool curl openssl libjansson binutils
git clone [https://github.com/androexp3rt/ccminer-armv7-a.git](https://github.com/androexp3rt/ccminer-armv7-a.git)
cd ccminer-armv7-a
chmod +x build.sh configure.sh autogen.sh
CXX=clang++ CC=clang build.sh
```
After Sucessfull build Run miner using following command:
```
./ccminer -a <coin/algo> -o <Pool Address with port> -u <walletaddress>.<minerName> -p <poolPassword (x for no password)> -t <no. of threads>
```
Example:
```
./ccminer -a verus -o stratum+tcp://pool.verus.io:9999 -u RCNN2BNWKncbkk2aptnLQnJfCruVyrBVgR.GALAXY_NOTE_3 -p x -t 4
```
For specific details on installing clang-16 on your current OS, check: https://apt.llvm.org/
