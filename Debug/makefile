################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (11.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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


BUILD_ARTIFACT_NAME := PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.elf \

MAP_FILES += \
PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.list \


# All Target
all: main-build

# Main-build Target
main-build: PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.elf secondary-outputs

# Tool invocations
PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.elf PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.map: $(OBJS) $(USER_OBJS) D:\Universidad\Sexto\ semestre\Estructuras\ computacionales\Parcial\ #1\STM32L476RGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\Universidad\Sexto semestre\Estructuras computacionales\Parcial #1\STM32L476RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.elf PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.list PARCIAL_1_ESTRUCTURAS_COMPUTACIONALES.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
