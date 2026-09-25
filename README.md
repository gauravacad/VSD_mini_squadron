# VSD_mini_squadron
Installtion for Windows 

# Download and install Arduino IDE
-Download the latest release - 'https://downloads.arduino.cc/arduino-ide/arduino-ide_latest_Windows_64bit.exe'
-Double-click the executable (.exe) file.
-Follow the instructions in the installation guide.
-When completing the setup, leave Run Arduino IDE ticked to launch the application, or launch it later from the Start Menu.


# Access the borad CH32V003F4U6 RISC-V MCU 

## Need to Install in Arduino 'File -> Prefrences' as shown below

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1aa1c85e-f081-4fc8-ba1d-6256bcb4f0d4" />


##Now, add the link 'https://github.com/openwch/board_manager_files/raw/main/package_ch32v_index.json'

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/c7ae38e1-f586-42f4-9986-23210710ef69" />

## Now to add the Board via board manager

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/79995e10-eb0e-4677-a3c3-0c7f34ee9dda" />


## Then search Ch32, You need to install, In my case it is already done so update is coming

<img width="789" height="451" alt="image" src="https://github.com/user-attachments/assets/06618732-710f-4cd7-9524-60515ceb8521" />

# Now Your First Program to Blink the LED
### Step 1 File -> New program 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f22e9945-0aeb-4261-bb69-a6b6f8b5302c" />


### Step 2 
```
void setup() {
    pinMode(PD6, OUTPUT);

    //Serial.begin(115200);
}

void loop() {
    digitalWrite(PD6, HIGH);
    //Serial.println("LED ON");
    delay(500);

    digitalWrite(PD6, LOW);
    //Serial.println("LED OFF");
    delay(500);
}
```
'Here PD 6 is builtin LED of the Board, No need of External'

### Step 3 Board selection 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/22b71e38-c207-4bb7-a565-378cbf514a2a" />

### Step 4 Select the appropriate detected COM port

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/65ebd29c-5a55-40d4-a66f-650b6fca098f" />

### Finally Compile and upload You will see the output on the console as shown in figure 

<img width="865" height="483" alt="image" src="https://github.com/user-attachments/assets/e31a0f60-7b02-4675-b1f3-cae1aac15850" />

### You will see the led blinking on your board. 
More experiments :- https://www.vlsisystemdesign.com/vsdsquadronmini/


# Credits to Mr. Kunal Ghosh Sir !!
<img width="639" height="304" alt="image" src="https://github.com/user-attachments/assets/c5e0cd14-8480-4241-ac75-7e26c3240cd5" />






