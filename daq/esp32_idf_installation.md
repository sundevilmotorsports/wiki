# ESP32 Installation for IDF Toolchain

## Two Options - IDF or Arduino
We choose IDF because it enables us to have more control over our ESP32 rather than deal with the abstractions that the arduino library provides us. Also, to put it bluntly, it tests us as engineers because its harder.


## Install Repo
In a folder of your choice, I chose `C:\Users\ryans`. Take note, wherever you install this toolchain, you need to have your projects within this directory. For instance a project directory I would have would be `c:\Users\ryans\esp-idf\projects\blink`

Run in your terminal: 
`git clone --recursive https://github.com/espressif/esp-idf.git`

### Enter directory
Enter the cloned directory: `cd esp-idf`

### Run the install script: 
- windows: `install.bat`
- linux/mac: `install.sh`

### Run the export script (add to PATH)
- windows: `export.bat`
- linux/mac: `export.sh`

### Create projects directory
You can call it whatever you like but this is what I did

 Run:
 1. `mkdir projects`

 2. `cd projects`

Check that the installation is working:

Run: `idf.py`

## Create blink project
Run: `idf.py create-project blink`

Run: `cd blink`

Open it in your text editor or ide of choice. I use VSCode and so I just run: `code .` to open the entire directory.

### Configure Project 
Depending on which esp32 you are using esp32 or esp32s2 or esp32c3, change the target in the command, for now:

Run: `idf.py set-target esp32`

Run: `idf.py build`. This will take a while :)

## Write code:
In your blink.c file put this code:
```c
#include <stdio.h>
#include "freertos/FreeRTOS.h"
#include "freertos/task.h"
#include "driver/gpio.h"
#include "sdkconfig.h"

// Define the GPIO pin for the LED (GPIO 2 is common for onboard LEDs)
#define BLINK_GPIO 2

void app_main(void)
{
    // Configure the GPIO pin
    gpio_reset_pin(BLINK_GPIO);
    gpio_set_direction(BLINK_GPIO, GPIO_MODE_OUTPUT);

    // Blink loop
    while (1) {
        // Turn LED ON
        printf("LED ON\n");
        gpio_set_level(BLINK_GPIO, 1);
        vTaskDelay(1000 / portTICK_PERIOD_MS); // Delay 1 second

        // Turn LED OFF
        printf("LED OFF\n");
        gpio_set_level(BLINK_GPIO, 0);
        vTaskDelay(1000 / portTICK_PERIOD_MS); // Delay 1 second
    }
}
```

### There you go!
You have a working blink code for esp32!🚀🚀🚀



## Espressif VSCode Extension

If you want to use the vscode extension to code your esp32. Install the extension and when you enter the setup wizard, make sure you install from existing version. The main ESP-IDF PATH for me was `C:\Users\ryans\esp-idf` and the TOOLS PATH was `C:\Users\ryans\.espressif`



## Errors from C/C++ Extension
Make you you go to the command palette. On windows, its ctrl + shift + p and type `ESP-IDF Add .vscode Configuration Folder`. This fixed the errors for me and should fix them for you as well.