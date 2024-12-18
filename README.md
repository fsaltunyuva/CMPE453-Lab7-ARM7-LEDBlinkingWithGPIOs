# CMPE453-Lab7-LEDBlinkingWithGPIOs
Using Proteus (Demo Version) to design circuit and use it for LED blinking for the Lab of the CMPE453 (Embedded Systems) Course.

1. Please add one led to PB6 for 1 second blink, and add the screenshot of the circuit.

**Answer:** ![placeholder]()

2. What changes were made to add the new LED? Please write the code parts according to 
that and explain in detail.

**Answer:** To add LED to PB6 and have blink with 1 second delay, we should have the code: 
```c
while (1) 
{ 
    HAL_GPIO_TogglePin(Ld2_GPIO_Port, Ld2_Pin); //Toggle LED 
    HAL_Delay(1000); //Delay 1 Seconds 
} 
```
```Ld2_GPIO_Port``` should be Port B and Ld2_Pin should be Pin 6. (Assuming GPIO_PORT_B and PIN6 are defined appropriately, ```HAL_GPIO_TogglePin(GPIO_PORT_B, PIN6);```) 

3. What happens if the ```HAL_Delay(1000)``` value is modified? Give examples and explain. 

**Answer:** The delay between blinks will change to that ms. For example, if we use 
```HAL_Delay(3000)```, the LED will wait for 3 seconds before the next blink.

4. What does the ```HAL_GPIO_TogglePin``` function do? What parameters does it take?

**Answer:** It toggles the GPIO pin whose port is stated in the parameters. The function 
comes from the header file. It takes the parameters GPIOx and GPIO_Pin which are the 
port of the pin to be toggled and the pin number respectively.