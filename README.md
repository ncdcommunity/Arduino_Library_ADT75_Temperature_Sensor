
[![ADT75](ADT75_I2C.png)](https://store.ncd.io/product/adt75-temperature-sensor-%C2%B11c-12-bit-with-3-address-lines-i2c-mini-module/).

# ADT75
ADT75 is a Temperature Sensor ±1°C 12-Bit with 3 Address Lines I2C Mini Module.
This Device is available from www.ncd.io 

[SKU: ADT75_I2CS]

(https://store.ncd.io/product/adt75-temperature-sensor-%C2%B11c-12-bit-with-3-address-lines-i2c-mini-module/)
This Sample code can be used with Arduino.

Hardware needed to interface ADT75 temperature sensor with Arduino
1. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-nano/">Arduino Nano</a>
2. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-micro-with-i2c-expansion-port/">Arduino Micro</a>
3. <a href="https://store.ncd.io/product/i2c-shield-for-arduino-uno/">Arduino uno</a>
4. <a href="https://store.ncd.io/product/dual-i2c-shield-for-arduino-due-with-modular-communications-interface/">Arduino Due</a>
5. <a href="https://store.ncd.io/product/adt75-temperature-sensor-%C2%B11c-12-bit-with-3-address-lines-i2c-mini-module/">ADT75 Temperature Sensor </a>
6. <a href="https://store.ncd.io/product/i%C2%B2c-cable/">I2C Cable</a>

ADT75 :

ADT75 The ADT75 is a complete temperature monitoring system in 8-lead MSOP and SOIC packages. It contains a band gap temperature sensor and a 12-bit analog-to-digital converter
(ADC) to monitor and digitize the temperature to a resolution of 0.0625°C.

Applications:

•Isolated sensors

•Environmental control systems

•Computer thermal monitoring

•Thermal protection

•Industrial process control

•Power-system monitors

•Hand-held applications

## Arduino
Download and install Arduino Software (IDE) on your machine. Steps to install Arduino are provided at:

https://www.arduino.cc/en/Main/Software

Download (or git pull) the code and double click the file to run the program.
Compile and upload the code on Arduino IDE and see the output on Serial Monitor.

How to Use the ADT75 Arduino Library
The ADT75 has a number of settings, which can be configured based on user requirements.
1.The SMBus Alert:The OS/ALERT pin can behave as a SMBus alert pin when the SMBus alert function is enabled by setting Bit D7 in the configuration register. 

    adt.setSM(SM_DISABLED);               // Disabled
    
2.The One-Shot Mode:In normal conversion mode, the internal clock oscillator is reset after every read or write operation. This causes the device to start a temperature conversion, the result of which is typically available 60 ms later

     adt.setOneShot(ONESHOT_NORMAL);         // Normal
     
    // adt.setOneShot(ONESHOT_ENABLED);     // Enabled
    
3. Shutdown Mode: The ADT75 can be placed in shutdown mode via the configuration register, in which case the on-chip oscillator is shut down and no further conversions are initiated until the ADT75 is taken out of shutdown mode. T
     
       adt.setShutdown(SHUTDOWN_DISABLE);      // Disable
    
       // adt.setShutdown(SHUTDOWN_ENABLE);    // Enable
    
4. Temperature Measurement:The temperature can be measured using the following command:

       temp = adt.Measure_Temp();    
    
