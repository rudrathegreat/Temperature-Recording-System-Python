# The Temperature Recording System
## Receiving
### The BBC Micro:bit

When the BBC Microbit without the sensor recevies the data, it then processes it onto Scratch. But first, it needs to be transferred back into an integer.

```Python

from microbit import *
import radio

radio.config(channel = 76)
radio.on()

while True:
  incoming == radio.receive():
  
  if incoming == None:
    display.show('-')
    pass
  else:
    display.scroll(incoming)
    print(int(incoming))
  
  display.show('-')
  
```

### Scratch

This data is then passed into this program aka intepreter to then be processed onto Scratch.
