# Chimera
This is the header file for Avr programming usng C, by using this header file avr programming will be as simpple as arduino programming

 Instrucions( for Atmel studio)
1. create a new Include file. Rename it as chimera.h
2. copy it's contents to the new include file.
3. Save  it in the include folder, which will be available in the avr folder
  (ex. C:\Program Files (x86)\Atmel\Atmel Toolchain\AVR8 GCC\Native\3.4.1056\avr8-gnu-toolchain\avr\include)
4. while writing the avr program just include chimera.h in the program (#include <chimera.h>). 

  Description
It has delay in milliseconds and microseconds, ADC(analog read), PWM(analog Write) functions.
It can be used for differnt clock frequencies, just define it initially at the start of the program, it shoud terminate by ll(long long)
 ex. for 1Mhz define F_CPU 1000000ll 

NOTE- for this I have used atmega16A with 12Mhz clock.

1. Delay in milliseconds

   Delay(x);  // x is delay in milliseconds.
  
2. Delay in microseconds.

   DelayMicro(x);   //x is in microseconds.
   
3. analod Read, ADC.

   aRPin(x);  //analog Read initializing; x is pin, 0-7 for  ADC0-ADC7 pins. use this before while(1) loop.
   aRead();   //use this in while(1) loop where you want to read. 8 bit resolution
   
4. analog Write, PWM.

   aWPin(x);  //analog Write initialize with pin; x = 0 for OCR0. use it before while(1) loop.
   aWrite(x);  //x is the duty cycle, duty cycle varies from 0 to 255. use it in While(1) loop, where you to read.
   
 
