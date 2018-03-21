# The Temperature Recording System
## Sensoring
### The Temperature Sensor

------------------------------------------------------------------------------------------------------------------------------------------

The temperature sensor is behind all of the sensing. Attached to a BBC Microbit to transmit the data and for power, the temperature sensor just sits there and senses the temperature.

------------------------------------------------------------------------------------------------------------------------------------------

### The BBC Micro:bit

------------------------------------------------------------------------------------------------------------------------------------------

The BBC Microbit with the attached sensor receives the data and then transmits it to the other BBC Microbit via radio. But the input the BBC Microbit with the attached sensor is receiving is in a form of an integer. So the BBC Microbit translates that integer into a string for it to be sent.

```Python

from microbit import *
import radio

radio.config(channel = 76)
radio.on()

temperature = 20.523

while True:
  if button_a.is_pressed():
    radio.send(str(temperature))
    display.scroll('Sent')
    sleep(1000)
  
  display.show('-')

```

----------------------------------------------------------------------------------------------------------------------------------------

### Power

----------------------------------------------------------------------------------------------------------------------------------------

The power is four lithium-ion batteries. They are long-lasting. They are connected to the BBC Microbit via the motor-driver board attached to the BBC Microbit.

----------------------------------------------------------------------------------------------------------------------------------------
