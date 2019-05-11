from building import *

cwd     = GetCurrentDir()
src     = Split('''
kendryte-standalone-sdk/lib/bsp/sleep.c
kendryte-standalone-sdk/lib/bsp/entry.c
kendryte-standalone-sdk/lib/bsp/entry_user.c
kendryte-standalone-sdk/lib/drivers/aes.c
kendryte-standalone-sdk/lib/drivers/clint.c
kendryte-standalone-sdk/lib/drivers/dmac.c
kendryte-standalone-sdk/lib/drivers/dvp.c
kendryte-standalone-sdk/lib/drivers/fft.c
kendryte-standalone-sdk/lib/drivers/fpioa.c
kendryte-standalone-sdk/lib/drivers/gpio.c
kendryte-standalone-sdk/lib/drivers/gpiohs.c
kendryte-standalone-sdk/lib/drivers/i2c.c
kendryte-standalone-sdk/lib/drivers/i2s.c
kendryte-standalone-sdk/lib/drivers/kpu.c
kendryte-standalone-sdk/lib/drivers/plic.c
kendryte-standalone-sdk/lib/drivers/pwm.c
kendryte-standalone-sdk/lib/drivers/rtc.c
kendryte-standalone-sdk/lib/drivers/sha256.c
kendryte-standalone-sdk/lib/drivers/spi.c
kendryte-standalone-sdk/lib/drivers/sysctl.c
kendryte-standalone-sdk/lib/drivers/timer.c
kendryte-standalone-sdk/lib/drivers/uart.c
kendryte-standalone-sdk/lib/drivers/uarths.c
kendryte-standalone-sdk/lib/drivers/utils.c
kendryte-standalone-sdk/lib/drivers/wdt.c
''')
CPPPATH = [cwd + '/kendryte-standalone-sdk/lib/drivers/include', 
cwd + '/kendryte-standalone-sdk/lib/bsp/include',
cwd + '/kendryte-standalone-sdk/lib/utils/include']
CPPDEFINES = ['CONFIG_LOG_COLORS', 'CONFIG_LOG_ENABLE', 'CONFIG_LOG_LEVEL=LOG_VERBOSE', 'FPGA_PLL', 'LOG_KERNEL', '__riscv64']

group = DefineGroup('SDK', src, depend = ['PKG_USING_KENDRYTE_SDK'], CPPPATH = CPPPATH, LOCAL_CPPDEFINES = CPPDEFINES)

Return('group')
