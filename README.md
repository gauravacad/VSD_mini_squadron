# Dear students,  you can use either VSCODE or Arduino to run the VSDSquadron Mini board 
### VSDSquadron Mini is a compact RISC-V based development board built around the CH32V003 microcontroller, used for embedded C programming, GPIO control, UART communication, and hardware development.

<img width="710" height="460" alt="image" src="https://github.com/user-attachments/assets/26eb6574-3482-4a48-a641-30aeb8a0e6d0" />

### Pin configuration : VSDSquadron Mini Pin Diagram 

<img width="940" height="613" alt="image" src="https://github.com/user-attachments/assets/f7dfc09b-0afb-43c5-b66b-d3d9af175489" />


### tabular Form 

<img width="879" height="934" alt="image" src="https://github.com/user-attachments/assets/ce850c18-5c19-47f5-8c25-a4b5e13bdff6" />


### Mostly used 


<img width="326" height="517" alt="image" src="https://github.com/user-attachments/assets/3c6cdcd8-7fbc-45b1-88ba-222c156eda87" />


### You will See device when connected if not then you need to install the driven from the 'link https://zadig.akeo.ie/' (**Here the actual board must be physically required**)

 <img width="589" height="260" alt="image" src="https://github.com/user-attachments/assets/687a6ec9-16b7-4599-bb41-ca2f1692818a" />


### 

<img width="463" height="595" alt="image" src="https://github.com/user-attachments/assets/7bb7765a-26d1-451a-8447-9a478d14dbc6" />



# First Method for VSD_mini_squadron With Arduino on Windows 
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


### Step 2  Write the Code for Blink LED

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

<img width="727" height="360" alt="image" src="https://github.com/user-attachments/assets/d6181996-dbdf-440c-9068-62df832392bd" />


- More experiments :- https://www.vlsisystemdesign.com/vsdsquadronmini/



## Now second Method: with Platformio on VScode 
- Vscode can be either on Linux (it can be standalone Linux ubuntu or Using Oracle VirtualBox) or Standalone Windows 


# Credits to Mr. Kunal Ghosh Sir !!
<img width="639" height="304" alt="image" src="https://github.com/user-attachments/assets/c5e0cd14-8480-4241-ac75-7e26c3240cd5" />

# Thank you !!




