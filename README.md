# 简介

在Windows x64环境中编译的[OpenCC](https://github.com/BYVoid/OpenCC)和[opencc4php](https://github.com/nauxliu/opencc4php)扩展

OpenCC version: 1.1.19

PHP version: 7.4.33 - vc15

PHP-SDK: 2.2.0

编译工具: Visual Studio 2022 Community + CMake + Python 3.13.5


# 安装

1. 将 php_opencc.dll 放入PHP安装目录的ext目录下
2. 将 opencc.dll 放入PHP的根目录下
3. 在 php.ini 中添加 php_opencc.dll（编译自[opencc4php](https://github.com/nauxliu/opencc4php)）扩展
```
[PHP_OPENCC]

extension=php_opencc.dll
```

# 源码编译注意事项

有自己编译需求的，在编译时需要注意你正在使用的PHP版本

测试的PHP 7.4.33，在vc15下编译的

因为我使用的是Visual Studio 2022 Community，从[opencc4php](https://github.com/nauxliu/opencc4php)扩展源码自行编译时，即使安装了MSVC v141 - VS2017 C++ build tools，在不更改其他设置时，还需要修改phpsdk提供的phpsdk_setshell.bat

