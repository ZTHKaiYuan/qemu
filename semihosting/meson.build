specific_ss.add(when: 'CONFIG_SEMIHOSTING', if_true: files(
  'guestfd.c',
  'syscalls.c',
))

common_ss.add(when: 'CONFIG_SEMIHOSTING', if_false: files('stubs-all.c'))
user_ss.add(when: 'CONFIG_SEMIHOSTING', if_true: files('user.c'))
system_ss.add(when: 'CONFIG_SEMIHOSTING', if_true: files(
  'config.c',
  'console.c',
  'uaccess.c',
), if_false: files(
  'stubs-system.c',
))

specific_ss.add(when: ['CONFIG_ARM_COMPATIBLE_SEMIHOSTING'],
		if_true: files('arm-compat-semi.c'))
