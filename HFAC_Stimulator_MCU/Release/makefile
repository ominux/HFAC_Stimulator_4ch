################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Sources/subdir.mk
-include SDK/devices/MK64F12/gcc/subdir.mk
-include SDK/devices/MK64F12/drivers/subdir.mk
-include SDK/devices/MK64F12/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
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
SECONDARY_FLASH += \
HFAC_Stimulator_MCU.hex \

SECONDARY_SIZE += \
HFAC_Stimulator_MCU.siz \


# All Target
all: HFAC_Stimulator_MCU.elf secondary-outputs

# Tool invocations
HFAC_Stimulator_MCU.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM Cross C Linker'
	arm-none-eabi-gcc -mcpu=cortex-m4 -mthumb -mfloat-abi=hard -mfpu=fpv4-sp-d16 -Os -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections  -g -T MK64FN1M0xxx12_flash.ld -Xlinker --gc-sections -L"C:\Users\adrien\MCU Programming\K64F_SDK_NoDebugConsole/devices/MK64F12" -L"C:\Users\adrien\MCU Programming\K64F_SDK_NoDebugConsole/devices/MK64F12/drivers" -L"C:\Users\adrien\MCU Programming\K64F_SDK_NoDebugConsole/devices/MK64F12/gcc" -Wl,-Map,"HFAC_Stimulator_MCU.map" --specs=nano.specs --specs=nosys.specs -o "HFAC_Stimulator_MCU.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

HFAC_Stimulator_MCU.hex: HFAC_Stimulator_MCU.elf
	@echo 'Invoking: GNU ARM Cross Create Flash Image'
	arm-none-eabi-objcopy -O ihex "HFAC_Stimulator_MCU.elf"  "HFAC_Stimulator_MCU.hex"
	@echo 'Finished building: $@'
	@echo ' '

HFAC_Stimulator_MCU.siz: HFAC_Stimulator_MCU.elf
	@echo 'Invoking: GNU ARM Cross Print Size'
	arm-none-eabi-size --format=berkeley "HFAC_Stimulator_MCU.elf"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(SECONDARY_FLASH)$(SECONDARY_SIZE)$(ASM_DEPS)$(S_UPPER_DEPS)$(C_DEPS) HFAC_Stimulator_MCU.elf
	-@echo ' '

secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_SIZE)

.PHONY: all clean dependents

-include ../makefile.targets
