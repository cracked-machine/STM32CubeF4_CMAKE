# build STM32 LL as static lib. 
# includes must be PUBLIC because they are used when building dependents
    
    add_library(STM32CubeLib STATIC "")
    target_sources(STM32CubeLib PUBLIC
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cortex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_exti.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash_ramfunc.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_gpio.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2s.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2s_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim_ex.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_adc.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_dma.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_exti.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_gpio.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_rcc.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_tim.c
        Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_utils.c

    )
    target_include_directories(STM32CubeLib PUBLIC 
    
        Drivers/STM32F4xx_HAL_Driver/Inc
        Drivers/STM32F4xx_HAL_Driver/Inc/Legacy
        Drivers/CMSIS/Include
        Drivers/CMSIS/Device/ST/STM32F4xx/Include
        Core/Inc
        
        ${CMAKE_SOURCE_DIR}/cube_workspace/STM32F405RG/Core/Inc
    )       
        




