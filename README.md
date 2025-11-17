✅ Step 1: Install Arduino IDE

If not installed:
https://www.arduino.cc/en/software


✅ Step 2: Add ESP8266 Board URL

Open Arduino IDE

Go to Preferences

Find the field: Additional Boards Manager URLs

Paste this URL:

http://arduino.esp8266.com/stable/package_esp8266com_index.json


Click OK


✅ Step 3: Install ESP8266 Board

Go to Tools → Board → Boards Manager

Search: ESP8266

Install "esp8266 by ESP8266 Community"


✅ Step 4: Select NodeMCU Board

Go to Tools → Board

Scroll down and select:

NodeMCU 1.0 (ESP-12E Module)


✅ Step 5: Select Port

Connect your NodeMCU using USB

Go to Tools → Port

Select something like:

/dev/cu.SLAB_USBtoUART   (for CP2102 chip)
or
/dev/cu.wchusbserial     (for CH340 chip)


If no port shows → you need drivers.

Install drivers on Mac:

CH340 Driver: https://github.com/adrianmihalko/ch340g-ch34g-ch34x-mac-os-x-driver

CP2102 Driver: https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers


✅ Step 6: Test with Blink Code

Upload this example to verify your NodeMCU works:

void setup() {
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop() {
  digitalWrite(LED_BUILTIN, LOW);  
  delay(1000);
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000);
}


If the blue LED blinks → setup is correct.


🎉 DONE

Your NodeMCU is ready to upload IoT programs.

