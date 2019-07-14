- 不要尝试在 osx 上编译，没有 arm-gcc
- linux 交叉编译失败， ld 时 so 文件错误. 直接在 arm 板上编译
- 在pi上编译 
```
sudo aptitude install libedbus-dev
./tools/build.py --target-arch=arm --target-os=linux  --buildtype=release  --target-board=rpi2  --static
```
- shdownode 包含 child_process, iot.js 不包含。
- 即使添加 --static, bus.so 还是动态