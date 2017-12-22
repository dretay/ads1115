# ADS1115 for STM32


Invoke Like this:

```c
	ADS1115_CHANNEL_CONFIG ads1115_channel_configs[2];
	ads1115_channel_configs[0].idx = 0;
	ads1115_channel_configs[0].ratio = 1;//3.125;
	ads1115_channel_configs[0].differential = true;
	ads1115_channel_configs[0].parameter = CURRENT; 
	
	ads1115_channel_configs[1].idx = 1;
	ads1115_channel_configs[1].ratio = 8.0645;
	ads1115_channel_configs[1].parameter = VOLTAGE;
	ads1115_channel_configs[1].differential = true;


	ADS1115_CONFIG ads1115_configs[1];
	ads1115_configs[0].addr = 0x90;
	ads1115_configs[0].p_i2c = &hi2c2;
	ads1115_configs[0].channel_cnt = 2;
	ads1115_configs[0].channel_configs = ads1115_channel_configs;
	
        ADS1115.configure(ads1115_configs, 2);

```
