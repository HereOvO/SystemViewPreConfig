# 使用SystemView的前置配置

## 需要包含的文件

需要包含`SystemViewCroppedVer`目录下除了/Inc/*.s都需要包含入工程(.h包含路径即可)



其中`SEGGER_SYSVIEW_Config_FreeRTOS.c`和`SEGGER_SYSVIEW_FreeRTOS.c`两个文件的版本必须**根据使用freertos的版本修改**,相应文件放在`SysView_README\SystemView-main.zip\SystemView-main\Sample`中. (现在文件夹里的是适合freertos v10版本的文件,版本可以在自己原工程中task.c中的说明行查看)

## 需要修改的freertos源文件

进入文件夹backup2中的`freertosconfig.h`和`task.c`文件,,搜索:`sysview修改`,对照修改你自己的工程文件



需要在main()中包含`#include "SEGGER_SYSVIEW.h"`



## 其它文件说明

`RTT-main`,`SystemView-main中存放的是官方提供的最新的使用SystemView时需要移植的文件(2026年1月),其中有一部分是在`SystemViewCroppedVer`中没有使用的,但如果需要使用,可以在目录下找,应该是全的