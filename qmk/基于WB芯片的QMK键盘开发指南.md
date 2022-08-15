## 资源介绍

### 开发 DEMO

- [owlt87-spi flash](https://github.com/WestberryTech/qmk_firmware/tree/demo/keyboards/owl/owlt87)

- [owlt87-embedded flash](https://github.com/WestberryTech/qmk_firmware/tree/demo/keyboards/owl/owlt87_vendor) [^1]

[^1]: 上电后等待工作时间较长，可在`mcuconf.h`中添加`#define WB32_FLASH_PROGRAM_NO_ERASE`定义

### 文档及固件更新工具

- QMK文档: [https://docs.qmk.fm](https://docs.qmk.fm)

- QMK已支持 WB32 MCU 列表: [点击查看](https://docs.qmk.fm/#/compatible_microcontrollers?id=westberrytech-wb32)
- 下载: [qmk_toolbox](https://github.com/qmk/qmk_toolbox/releases)
- 下载: [wb32-dfu-updater-windows](https://packages.msys2.org/package/mingw-w64-x86_64-wb32-dfu-updater?repo=mingw64)

- 下载: [wb32-dfu-updater-mac/linux](https://formulae.brew.sh/formula/wb32-dfu-updater_cli#default)

### VIA 支持

- VIA 软件[下载](https://github.com/WestBerryVIA/via-releases/releases)
- 线上 [VIA](https://via.evove.top)
- vial-gui[下载](https://github.com/WestBerryVIA/vial-gui/releases)
- 键盘提交[仓库](https://github.com/WestBerryVIA/keyboards)

### QMK 已支持的基于 WB32 MCU 的键盘
- [GMMK PRO V2](https://github.com/qmk/qmk_firmware/tree/develop/keyboards/gmmk/pro/rev2)
- [GMMK V2 96%](https://github.com/qmk/qmk_firmware/tree/develop/keyboards/gmmk/gmmk2/p96)

### 注意事项

- QMK中不支持多个Master[^2]的存在，如有多个Slave可以通过CS/Address的方式控制，硬件设计时一定要注意。
- 推荐使用外挂 SPI Flash 或者 EEPROM 来保存数据。若使用内置Flash并且做了[^1]的处理，需要承担一定的风险。

### 注解

[^1]: 上电后等待工作时间较长，可在`mcuconf.h`中添加`#define WB32_FLASH_PROGRAM_NO_ERASE`定义
[^2]: 比如 SPI Master / I2C Master ... 