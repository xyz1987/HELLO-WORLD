# HELLO-WORLD

ESP32-C3 Hello World 示例程序。

## 简介

这是一个基于 ESP-IDF 框架的 ESP32-C3 Hello World 程序。程序启动后会：

1. 打印 "Hello world!"
2. 打印芯片信息（型号、CPU 核心数、WiFi/BT 功能、硅版本、Flash 大小等）
3. 打印最小可用堆内存大小
4. 倒计时 10 秒后重启

## 环境要求

- [ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/esp32c3/get-started/index.html) v5.0 或更高版本

## 编译和烧录

1. 设置 ESP-IDF 环境：

   ```bash
   . $IDF_PATH/export.sh
   ```

2. 设置目标芯片为 ESP32-C3：

   ```bash
   idf.py set-target esp32c3
   ```

3. 编译项目：

   ```bash
   idf.py build
   ```

4. 烧录到设备（将 `PORT` 替换为实际串口号）：

   ```bash
   idf.py -p PORT flash
   ```

5. 查看串口输出：

   ```bash
   idf.py -p PORT monitor
   ```

## 项目结构

```
├── CMakeLists.txt          # 顶层 CMake 配置文件
├── main
│   ├── CMakeLists.txt      # 主组件 CMake 配置文件
│   └── hello_world_main.c  # 主程序源文件
├── sdkconfig.defaults      # 默认 SDK 配置（目标芯片 ESP32-C3）
└── README.md               # 项目说明文件
```
