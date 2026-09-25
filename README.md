# Dear students,  you can use either VSCODE or Arduino to run the VSDSquadron Mini board 
### VSDSquadron Mini is a compact RISC-V based development board built around the CH32V003 microcontroller, used for embedded C programming, GPIO control, UART communication, and hardware development.

<img width="710" height="460" alt="image" src="https://github.com/user-attachments/assets/26eb6574-3482-4a48-a641-30aeb8a0e6d0" />

### Pin configuration : VSDSquadron Mini Pin Diagram 

<img width="940" height="613" alt="image" src="https://github.com/user-attachments/assets/f7dfc09b-0afb-43c5-b66b-d3d9af175489" />


### tabular Form 

<img width="879" height="934" alt="image" src="https://github.com/user-attachments/assets/ce850c18-5c19-47f5-8c25-a4b5e13bdff6" />


### Mostly used 


<img width="326" height="517" alt="image" src="https://github.com/user-attachments/assets/3c6cdcd8-7fbc-45b1-88ba-222c156eda87" />


### You will See device when connected if not then you need to install the driven from the '[link https://zadig.akeo.ie/](https://github.com/Community-PIO-CH32V/wchlink-driver-windows)' (**Here the actual board must be physically required**)

```
https://github.com/Community-PIO-CH32V/wchlink-driver-windows
```


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
- The Pdf is attached in the folder to make the installtion easy and simple in the same link.
### Steps in Nutshell given Link 
```
https://www.vlsisystemdesign.com/docs/vsdsquadronminidatasheet/installation-and-settings/
```
<img width="1332" height="414" alt="image" src="https://github.com/user-attachments/assets/dc7afe20-3e6a-4ad2-8eba-1cf8873085c9" />

### Install VSCode
- Download and install VSCode from https://code.visualstudio.com

### Install PlatformIO

<img width="458" height="329" alt="image" src="https://github.com/user-attachments/assets/b0bcc562-9933-411e-a80c-d1b8ba1b251e" />

- Open the ”Extensions” sidebar in VSCode, as shown in Figure.
- Search for ”PlatformIO” and click ”install”, as shown in Figure.

### Install CH32V Platform
- Expand the PlatformIO sidebar (ant icon) and click ”PIO Home” as shown in Figure below.

<img width="679" height="1024" alt="image" src="https://github.com/user-attachments/assets/8499b9b3-498e-4d33-949c-e171219d0c31" />


- In the PIO Home window, click on the ”Platforms” sidebar and choose “Advanced Installation” as shown in Figure.


<img width="1024" height="741" alt="image" src="https://github.com/user-attachments/assets/50c99bf4-94e2-44e5-afa4-6fbf3e31fb87" />


- Enter the following repository URL when prompted and press ”Install,” as shown in Figure below: 'https://github.com/vsdip/vsdsquadron pio'
  
<img width="1024" height="807" alt="image" src="https://github.com/user-attachments/assets/24b8bbc3-b0e5-40f4-bee9-237e3a643b59" />

  

### Uploading blink example
- Click on ”Platforms” 
- Click on ”VSDSquadron”

  <img width="1024" height="595" alt="image" src="https://github.com/user-attachments/assets/8612f64d-8c63-4351-aa35-61fdd4a32c10" />


- Click on ”Examples” as shown in Figure

<img width="1024" height="604" alt="image" src="https://github.com/user-attachments/assets/7b2f1033-88ba-4879-ab3b-a62332ea412e" />


- Click on ”Import” as shown in Figure
- You should see ”vsdsquadronmini” under ”Project Tasks” as shown in Figure
- Click on ”Build” and ”Upload” button as shown in Figure

<img width="1024" height="442" alt="image" src="https://github.com/user-attachments/assets/00a33bf7-7a84-4788-a878-d3cfd75619f4" />



# Credits to Mr. Kunal Ghosh Sir !!
<img width="639" height="304" alt="image" src="https://github.com/user-attachments/assets/c5e0cd14-8480-4241-ac75-7e26c3240cd5" />

# Thank you !!




