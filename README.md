# HELLO-WORLD
第一个

## ESP32C3 Hello World

这是一个基于 ESP-IDF 框架的 ESP32C3 Hello World 示例程序。

### 硬件要求

- ESP32-C3 开发板

### 环境要求

- [ESP-IDF](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32c3/get-started/index.html) v5.0 或更高版本

### 构建与烧录

```bash
# 设置目标芯片
idf.py set-target esp32c3

# 编译
idf.py build

# 烧录并监视串口输出
idf.py -p PORT flash monitor
```

将 `PORT` 替换为实际的串口设备（如 `/dev/ttyUSB0` 或 `COM3`）。

按下 `Ctrl+]` 退出串口监视器。

### 程序说明

程序启动后会：
1. 打印 "Hello World! ESP32C3"
2. 显示芯片信息（CPU核心数、WiFi/BLE支持、Flash大小等）
3. 倒计时 10 秒后重启
