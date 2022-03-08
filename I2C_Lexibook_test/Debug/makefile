################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32WBxx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
I2C_Lexibook_test.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
I2C_Lexibook_test.list \

OBJCOPY_HEX += \
I2C_Lexibook_test.hex \

OBJCOPY_BIN += \
I2C_Lexibook_test.bin \


# All Target
all: I2C_Lexibook_test.elf secondary-outputs

# Tool invocations
I2C_Lexibook_test.elf: $(OBJS) $(USER_OBJS) C:\Users\lemin\STM32CubeIDE\Minh_Examples\I2C_Lexibook_test\STM32WB55RGVX_FLASH.ld
	arm-none-eabi-gcc -o "I2C_Lexibook_test.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\lemin\STM32CubeIDE\Minh_Examples\I2C_Lexibook_test\STM32WB55RGVX_FLASH.ld" --specs=nosys.specs -Wl,-Map="I2C_Lexibook_test.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

I2C_Lexibook_test.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "I2C_Lexibook_test.list"
	@echo 'Finished building: $@'
	@echo ' '

I2C_Lexibook_test.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "I2C_Lexibook_test.hex"
	@echo 'Finished building: $@'
	@echo ' '

I2C_Lexibook_test.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "I2C_Lexibook_test.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
