INCLUDE(CMakeForceCompiler)

# CROSS COMPILER SETTING
SET(CMAKE_SYSTEM_NAME Generic)
CMAKE_MINIMUM_REQUIRED (VERSION 2.6)

# THE VERSION NUMBER
SET (Tutorial_VERSION_MAJOR 1)
SET (Tutorial_VERSION_MINOR 0)

# ENABLE ASM
ENABLE_LANGUAGE(ASM)

SET(CMAKE_STATIC_LIBRARY_PREFIX)
SET(CMAKE_STATIC_LIBRARY_SUFFIX)

SET(CMAKE_EXECUTABLE_LIBRARY_PREFIX)
SET(CMAKE_EXECUTABLE_LIBRARY_SUFFIX)

 
# CURRENT DIRECTORY
SET(ProjDirPath ${CMAKE_CURRENT_SOURCE_DIR})

# DEBUG LINK FILE
set(CMAKE_EXE_LINKER_FLAGS_DEBUG "${CMAKE_EXE_LINKER_FLAGS_DEBUG} -T${ProjDirPath}/../../../../../platform/devices/MKV31F51212/linker/gcc/MKV31F512xxx12_flash.ld  -static")

# RELEASE LINK FILE
set(CMAKE_EXE_LINKER_FLAGS_RELEASE "${CMAKE_EXE_LINKER_FLAGS_RELEASE} -T${ProjDirPath}/../../../../../platform/devices/MKV31F51212/linker/gcc/MKV31F512xxx12_flash.ld  -static")

# DEBUG ASM FLAGS
SET(CMAKE_ASM_FLAGS_DEBUG "${CMAKE_ASM_FLAGS_DEBUG} -g  -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  -mthumb  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mapcs  -std=gnu99")

# DEBUG C FLAGS
SET(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -g  -O0  -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  -mthumb  -MMD  -MP  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mapcs  -std=gnu99")

# DEBUG LD FLAGS
SET(CMAKE_EXE_LINKER_FLAGS_DEBUG "${CMAKE_EXE_LINKER_FLAGS_DEBUG} -g  -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  --specs=nano.specs  -lm  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mthumb  -mapcs  -Xlinker --gc-sections  -Xlinker -static  -Xlinker -z  -Xlinker muldefs  -Xlinker --defsym=__stack_size__=0x2000  -Xlinker --defsym=__heap_size__=0x2000")

# RELEASE ASM FLAGS
SET(CMAKE_ASM_FLAGS_RELEASE "${CMAKE_ASM_FLAGS_RELEASE} -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  -mthumb  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mapcs  -std=gnu99")

# RELEASE C FLAGS
SET(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -Os  -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  -mthumb  -MMD  -MP  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mapcs  -std=gnu99")

# RELEASE LD FLAGS
SET(CMAKE_EXE_LINKER_FLAGS_RELEASE "${CMAKE_EXE_LINKER_FLAGS_RELEASE} -mcpu=cortex-m4  -mfloat-abi=hard  -mfpu=fpv4-sp-d16  -mtune=cortex-m4  --specs=nano.specs  -lm  -Wall  -fno-common  -ffunction-sections  -fdata-sections  -ffreestanding  -fno-builtin  -mthumb  -mapcs  -Xlinker --gc-sections  -Xlinker -static  -Xlinker -z  -Xlinker muldefs  -Xlinker --defsym=__stack_size__=0x2000  -Xlinker --defsym=__heap_size__=0x2000")

# ASM MACRO
SET(CMAKE_ASM_FLAGS_DEBUG "${CMAKE_ASM_FLAGS_DEBUG}  -DDEBUG")

# C MACRO
SET(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG}  -DDEBUG")
SET(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG}  -DCPU_MKV31F512VLL12")
SET(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG}  -DFRDM_KV31F")
SET(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG}  -DFREEDOM")
SET(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE}  -DNDEBUG")
SET(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE}  -DCPU_MKV31F512VLL12")
SET(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE}  -DFRDM_KV31F")
SET(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE}  -DFREEDOM")

# CXX MACRO

# INCLUDE_DIRECTORIES
IF(CMAKE_BUILD_TYPE MATCHES Debug)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/osa/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/utilities/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/CMSIS/Include)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices/MKV31F51212/include)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices/MKV31F51212/startup)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/hal/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/adc16)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/cmp)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/crc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/dac)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/dspi)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/edma)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/ewm)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/flexbus)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/ftm)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/gpio)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/i2c)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/lptmr)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/lpuart)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/pdb)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/pit)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/rnga)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/uart)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/vref)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/wdog)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/smartcard)
    INCLUDE_DIRECTORIES(${ProjDirPath}/..)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../board)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/system/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../..)
ELSEIF(CMAKE_BUILD_TYPE MATCHES Release)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/osa/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/utilities/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/CMSIS/Include)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices/MKV31F51212/include)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/devices/MKV31F51212/startup)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/hal/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/adc16)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/cmp)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/crc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/dac)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/dspi)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/edma)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/ewm)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/flexbus)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/ftm)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/gpio)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/i2c)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/lptmr)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/lpuart)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/pdb)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/pit)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/rnga)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/uart)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/vref)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/wdog)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/drivers/src/smartcard)
    INCLUDE_DIRECTORIES(${ProjDirPath}/..)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../board)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../../../../platform/system/inc)
    INCLUDE_DIRECTORIES(${ProjDirPath}/../../..)
ENDIF()

# ADD_EXECUTABLE
ADD_EXECUTABLE(FreedomKV31F 
    "${ProjDirPath}/../../../../../platform/utilities/src/fsl_misc_utilities.c"
    "${ProjDirPath}/../../../../../platform/devices/MKV31F51212/startup/gcc/startup_MKV31F51212.S"
    "${ProjDirPath}/../main.c"
    "${ProjDirPath}/../main.h"
    "${ProjDirPath}/../hardware_init.c"
    "${ProjDirPath}/../board/gpio_pins.c"
    "${ProjDirPath}/../board/gpio_pins.h"
    "${ProjDirPath}/../board/pin_mux.c"
    "${ProjDirPath}/../board/pin_mux.h"
    "${ProjDirPath}/../board/board.c"
    "${ProjDirPath}/../board/board.h"
    "${ProjDirPath}/../../../../../platform/utilities/src/fsl_debug_console.c"
    "${ProjDirPath}/../../../../../platform/utilities/inc/fsl_debug_console.h"
    "${ProjDirPath}/../../../../../platform/utilities/src/print_scan.c"
    "${ProjDirPath}/../../../../../platform/utilities/src/print_scan.h"
    "${ProjDirPath}/../../../../../platform/devices/MKV31F51212/startup/system_MKV31F51212.c"
    "${ProjDirPath}/../../../../../platform/devices/MKV31F51212/startup/system_MKV31F51212.h"
    "${ProjDirPath}/../../../../../platform/devices/startup.c"
    "${ProjDirPath}/../../../../../platform/devices/startup.h"
)
SET_TARGET_PROPERTIES(FreedomKV31F PROPERTIES OUTPUT_NAME "FreedomKV31F.elf")

TARGET_LINK_LIBRARIES(FreedomKV31F -Wl,--start-group)
# LIBRARIES
IF(CMAKE_BUILD_TYPE MATCHES Debug)
    TARGET_LINK_LIBRARIES(FreedomKV31F ${ProjDirPath}/../../../../../lib/ksdk_platform_lib/armgcc/KV31F51212/debug/libksdk_platform.a)
ELSEIF(CMAKE_BUILD_TYPE MATCHES Release)
    TARGET_LINK_LIBRARIES(FreedomKV31F ${ProjDirPath}/../../../../../lib/ksdk_platform_lib/armgcc/KV31F51212/release/libksdk_platform.a)
ENDIF()

# SYSTEM LIBRARIES
TARGET_LINK_LIBRARIES(FreedomKV31F m)
TARGET_LINK_LIBRARIES(FreedomKV31F c)
TARGET_LINK_LIBRARIES(FreedomKV31F gcc)
TARGET_LINK_LIBRARIES(FreedomKV31F nosys)
TARGET_LINK_LIBRARIES(FreedomKV31F -Wl,--end-group)

# MAP FILE
SET(CMAKE_EXE_LINKER_FLAGS_DEBUG "${CMAKE_EXE_LINKER_FLAGS_DEBUG}  -Xlinker -Map=debug/FreedomKV31F.map")
SET(CMAKE_EXE_LINKER_FLAGS_RELEASE "${CMAKE_EXE_LINKER_FLAGS_RELEASE}  -Xlinker -Map=release/FreedomKV31F.map")

# BIN AND HEX
ADD_CUSTOM_COMMAND(TARGET FreedomKV31F POST_BUILD COMMAND ${CMAKE_OBJCOPY} -Oihex ${EXECUTABLE_OUTPUT_PATH}/FreedomKV31F.elf ${EXECUTABLE_OUTPUT_PATH}/FreedomKV31F.hex)
ADD_CUSTOM_COMMAND(TARGET FreedomKV31F POST_BUILD COMMAND ${CMAKE_OBJCOPY} -Obinary ${EXECUTABLE_OUTPUT_PATH}/FreedomKV31F.elf ${EXECUTABLE_OUTPUT_PATH}/FreedomKV31F.bin)
