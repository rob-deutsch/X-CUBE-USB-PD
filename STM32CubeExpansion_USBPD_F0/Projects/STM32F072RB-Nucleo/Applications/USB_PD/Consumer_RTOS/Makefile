##########################################################################################################################
# File automatically-generated by tool: [projectgenerator] version: [3.3.0] date: [Mon Jul 15 23:38:50 AEST 2019]
##########################################################################################################################

# ------------------------------------------------
# Generic Makefile (based on gcc)
#
# ChangeLog :
#	2017-02-10 - Several enhancements + project update mode
#   2015-07-22 - first version
# ------------------------------------------------

######################################
# target
######################################
TARGET = poopy


######################################
# building variables
######################################
# debug build?
DEBUG = 1
# optimization
OPT = -Og


#######################################
# paths
#######################################
# Build path
BUILD_DIR = build

######################################
# source
######################################
# C sources
DRIVERS = ../../../../../Drivers
DRIVER_HAL = $(DRIVERS)/STM32F0xx_HAL_Driver
RTOS = ../../../../../Middlewares/Third_Party/FreeRTOS/Source
USBPD = ../../../../../Middlewares/ST/STM32_USBPD_Library
LED_SERVER = ../../../../../Utilities/LED_SERVER

C_SOURCES =  \
Src/main.c \
Src/stm32f0xx_it.c \
Src/stm32f0xx_hal_msp.c \
Src/usbpd_dpm_user.c \
Src/usbpd_pwr_if.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_tim.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_tim_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_uart.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_uart_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_rcc.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_rcc_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_i2c.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_i2c_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_gpio.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_dma.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_cortex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_pwr.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_pwr_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_flash.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_flash_ex.c \
Src/system_stm32f0xx.c  \
$(USBPD)/Devices/STM32F072/src/usbpd_hw_if_it.c \
$(USBPD)/Devices/STM32F072/src/usbpd_phy_hw_if.c \
$(USBPD)/Devices/STM32F072/src/usbpd_timersserver.c \
$(USBPD)/Devices/STM32F072/src/usbpd_pwr_hw_if.c \
$(USBPD)/Devices/STM32F072/src/usbpd_phy.c \
$(USBPD)/Devices/STM32F072/src/bmc.c \
$(USBPD)/Devices/STM32F072/src/usbpd_cad_hw_if.c \
$(USBPD)/Core/src/usbpd_dpm_core.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_crc.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_crc_ex.c \
$(DRIVER_HAL)/Src/stm32f0xx_ll_utils.c \
$(DRIVER_HAL)/Src/stm32f0xx_hal_comp.c \
$(RTOS)/CMSIS_RTOS/cmsis_os.c \
$(RTOS)/portable/GCC/ARM_CM0/port.c \
$(RTOS)/tasks.c \
$(RTOS)/list.c \
$(RTOS)/portable/MemMang/heap_4.c \
$(RTOS)/queue.c \
$(LED_SERVER)/led_server.c \
$(DRIVERS)/BSP/P-NUCLEO-USB001/p-nucleo-usb001.c

# ASM sources
ASM_SOURCES =  \
SW4STM32/startup_stm32f072xb.s


#######################################
# binaries
#######################################
PREFIX = arm-none-eabi-
# The gcc compiler bin path can be either defined in make command via GCC_PATH variable (> make GCC_PATH=xxx)
# either it can be added to the PATH environment variable.
ifdef GCC_PATH
CC = $(GCC_PATH)/$(PREFIX)gcc
AS = $(GCC_PATH)/$(PREFIX)gcc -x assembler-with-cpp
CP = $(GCC_PATH)/$(PREFIX)objcopy
SZ = $(GCC_PATH)/$(PREFIX)size
else
CC = $(PREFIX)gcc
AS = $(PREFIX)gcc -x assembler-with-cpp
CP = $(PREFIX)objcopy
SZ = $(PREFIX)size
endif
HEX = $(CP) -O ihex
BIN = $(CP) -O binary -S
 
#######################################
# CFLAGS
#######################################
# cpu
CPU = -mcpu=cortex-m0

# fpu
# NONE for Cortex-M0/M0+/M3

# float-abi


# mcu
MCU = $(CPU) -mthumb $(FPU) $(FLOAT-ABI)

# macros for gcc
# AS defines
AS_DEFS = 

# C defines
C_DEFS =  \
-DUSE_HAL_DRIVER \
-DSTM32F072xB \
-DUSE_HAL_DRIVER \
-DSTM32F072xB \
-DUSE_STM32F0XX_NUCLEO \
-D_RTOS \
-DUSBPD_LED_SERVER \
-DUSBPD_PORT_COUNT=1 \
-D_SNK \
-DUSBPDCORE_LIB_PD2_CONFIG_1 \
-D_TRACE_NA

# AS includes
AS_INCLUDES = 

# C includes
C_INCLUDES =  \
-IInc \
-I$(DRIVER_HAL)/Inc \
-I$(DRIVER_HAL)/Inc/Legacy \
-I$(DRIVERS)/CMSIS/Device/ST/STM32F0xx/Include \
-I$(DRIVERS)/CMSIS/Include \
-I$(DRIVERS)/CMSIS/Include \
-I$(DRIVERS)/BSP/P-NUCLEO-USB001 \
-I$(DRIVERS)/BSP/STM32F0xx-Nucleo \
-I$(DRIVERS)/BSP/Components/Common \
-I$(RTOS)/CMSIS_RTOS \
-I$(RTOS)/include \
-I$(RTOS)/portable/GCC/ARM_CM0 \
-I$(USBPD)/Core/inc \
-I$(USBPD)/Devices/STM32F072/inc \
-I$(LED_SERVER)

# -I$(DRIVERS)/BSP/Components/fusb307


# compile gcc flags
ASFLAGS = $(MCU) $(AS_DEFS) $(AS_INCLUDES) $(OPT) -Wall -fdata-sections -ffunction-sections

CFLAGS = $(MCU) $(C_DEFS) $(C_INCLUDES) $(OPT) -Wall -fdata-sections -ffunction-sections

ifeq ($(DEBUG), 1)
CFLAGS += -g -gdwarf-2
endif


# Generate dependency information
CFLAGS += -MMD -MP -MF"$(@:%.o=%.d)"


#######################################
# LDFLAGS
#######################################
# link script
LDSCRIPT = SW4STM32/STM32F072RB-Nucleo_Consumer_RTOS/STM32F072RBTx_FLASH.ld

# libraries
LIBS = -lc -lm -lnosys \
-l:USBPDCORE_PD2_CONFIG_1_CM0_wc32.a
LIBDIR = -L$(USBPD)/Core/lib
LDFLAGS = $(MCU) -specs=nosys.specs -specs=nano.specs -T$(LDSCRIPT) $(LIBDIR) $(LIBS) -Wl,-Map=$(BUILD_DIR)/$(TARGET).map,--cref -Wl,--gc-sections

# default action: build all
all: $(BUILD_DIR)/$(TARGET).elf $(BUILD_DIR)/$(TARGET).hex $(BUILD_DIR)/$(TARGET).bin


#######################################
# build the application
#######################################
# list of objects
OBJECTS = $(addprefix $(BUILD_DIR)/,$(notdir $(C_SOURCES:.c=.o)))
vpath %.c $(sort $(dir $(C_SOURCES)))
# list of ASM program objects
OBJECTS += $(addprefix $(BUILD_DIR)/,$(notdir $(ASM_SOURCES:.s=.o)))
vpath %.s $(sort $(dir $(ASM_SOURCES)))

$(BUILD_DIR)/%.o: %.c Makefile | $(BUILD_DIR) 
	$(CC) -c $(CFLAGS) -Wa,-a,-ad,-alms=$(BUILD_DIR)/$(notdir $(<:.c=.lst)) $< -o $@

$(BUILD_DIR)/%.o: %.s Makefile | $(BUILD_DIR)
	$(AS) -c $(CFLAGS) $< -o $@

$(BUILD_DIR)/$(TARGET).elf: $(OBJECTS) Makefile
	$(CC) $(OBJECTS) $(LDFLAGS) -o $@
	$(SZ) $@

$(BUILD_DIR)/%.hex: $(BUILD_DIR)/%.elf | $(BUILD_DIR)
	$(HEX) $< $@
	
$(BUILD_DIR)/%.bin: $(BUILD_DIR)/%.elf | $(BUILD_DIR)
	$(BIN) $< $@	
	
$(BUILD_DIR):
	mkdir $@		

#######################################
# clean up
#######################################
clean:
	-rm -fR $(BUILD_DIR)
  
#######################################
# dependencies
#######################################
-include $(wildcard $(BUILD_DIR)/*.d)

# *** EOF ***
