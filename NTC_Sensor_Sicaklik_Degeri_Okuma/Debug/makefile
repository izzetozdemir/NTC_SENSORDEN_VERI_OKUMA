################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (9-2020-q2-update)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := NTC_Sensor_Sicaklik_Degeri_Okuma
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
NTC_Sensor_Sicaklik_Degeri_Okuma.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
NTC_Sensor_Sicaklik_Degeri_Okuma.list \

OBJCOPY_BIN += \
NTC_Sensor_Sicaklik_Degeri_Okuma.bin \


# All Target
all: main-build

# Main-build Target
main-build: NTC_Sensor_Sicaklik_Degeri_Okuma.elf secondary-outputs

# Tool invocations
NTC_Sensor_Sicaklik_Degeri_Okuma.elf: $(OBJS) $(USER_OBJS) D:\Stm32f407Yeni\NTC_Sensor_Sicaklik_Degeri_Okuma\STM32F407VGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "NTC_Sensor_Sicaklik_Degeri_Okuma.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Stm32f407Yeni\NTC_Sensor_Sicaklik_Degeri_Okuma\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="NTC_Sensor_Sicaklik_Degeri_Okuma.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

NTC_Sensor_Sicaklik_Degeri_Okuma.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "NTC_Sensor_Sicaklik_Degeri_Okuma.list"
	@echo 'Finished building: $@'
	@echo ' '

NTC_Sensor_Sicaklik_Degeri_Okuma.bin: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "NTC_Sensor_Sicaklik_Degeri_Okuma.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) NTC_Sensor_Sicaklik_Degeri_Okuma.bin NTC_Sensor_Sicaklik_Degeri_Okuma.elf NTC_Sensor_Sicaklik_Degeri_Okuma.list default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
