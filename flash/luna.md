### 1. Put Luna in Download Mode

To put Toradex Luna in Download mode: short, put a jumper, on the `USB-BOOT` pins:

![](https://raw.githubusercontent.com/gaiaBuildSystem/phobos-docs/refs/heads/main/assets/img/flashLunaStep1.png)

![](https://raw.githubusercontent.com/gaiaBuildSystem/phobos-docs/refs/heads/main/assets/img/flashLunaStep2.png)

### 2. Connect Luna USB to a Host Computer

![](https://raw.githubusercontent.com/gaiaBuildSystem/phobos-docs/refs/heads/main/assets/img/flashLunaStep3.png)

### 3. Download Flashing Tool & PhobOS Image

Download the compacted flashing tool and the PhobOS image from the following link:

- [https://github.com/gaiaBuildSystem/cookbook-phobos/releases/download/v0.2.0.0-luna/PhobOS-luna-emmc-ota-0-2-0.flash.zip](https://github.com/gaiaBuildSystem/cookbook-phobos/releases/download/v0.2.0.0-luna/PhobOS-luna-emmc-ota-0-2-0.flash.zip)

### 4. Extract the Flashing Tool & PhobOS Image

Extract the downloaded ZIP file to a convenient location on your host computer. You should see the flashing tool and the PhobOS image inside the extracted folder.

### 5. Run the Flashing Tool

From the extracted folder, run the flashing tool wrapper:

- For Windows users, from inside a PowerShell terminal, run the following command:
    ```bash
    ./flash-windows.ps1
    ```
- For Linux users, from inside a terminal, run the following command:
    ```bash
    chmod +x ./flash-linux.sh
    ./flash-linux.sh
    ```
The flashing tool will start to listen for the Luna device in Download mode. It will automatically detect it as soon as it is turned on.

> [!WARNING]
If the board is already turned on, the flashing tool will not be able to detect it. Make sure the board is powered off before running the flashing tool.

### 6. Power On the Luna Board

Toggle the power switch to turn on the Luna board. A green LED will light up. The flashing tool should detect the board and start the flashing process automatically.

![](https://raw.githubusercontent.com/gaiaBuildSystem/phobos-docs/refs/heads/main/assets/img/flashLunaStep4.png)

### 7. Wait for the Flashing Process to Complete

The flashing process may take a few minutes. Wait until the flashing tool indicates that the process was 100% completed.

### 8. Power Off the Luna Board

Toggle the power switch to turn off the Luna board.

### 9. Remove the Jumper from the USB-BOOT Pins

![](https://raw.githubusercontent.com/gaiaBuildSystem/phobos-docs/refs/heads/main/assets/img/flashLunaStep2.png)

### 10. Power On the Luna Board

Switch the power back on. The Luna board should now boot into PhobOS. The default user is `phobos` and the default password is `phobos`.

> [!WARNING]
The pre-built PhobOS images are meant for development purposes only. It is recommended to use [Opus](https://github.com/gaiaBuildSystem/opus) to create hardened and production-ready PhobOS images for your Luna board.
