# ME-AC-ATOMS3LITE

All the gear and no idea.

Connect ESP32 ATOM S3 Lite to your Mitsubishi Electric AC

This worked for me using Atom S3 lite and MSZ-AP25VGD2.

I am no ESP32/HA expert. 

Inspiration from https://github.com/echavet/MitsubishiCN105ESPHome/discussions/83

AC config yaml thanks to https://github.com/fonske/MitsubishiCN105ESPHome/blob/main/me_airco_atom_s3_lite.yaml

## Part list:

- [Atom S3 Lite](https://www.aliexpress.com/item/1005005177952629.html?spm=a2g0o.order_list.order_list_main.17.28bf1802YcbnfM)
- [PAP-05V-S connector](https://www.aliexpress.com/item/1005008331233541.html?spm=a2g0o.order_list.order_list_main.5.28bf1802YcbnfM)
- [4 pin buckled grove cable 5cm](https://www.aliexpress.com/item/32818751577.html?spm=a2g0o.order_list.order_list_main.11.28bf1802YcbnfM)

## Instructions

1. Make the cable, leave pin5 on PAP-05V-S connector with small triangle blank.

     ![Image](https://github.com/user-attachments/assets/1a84040e-bf04-4802-a2e8-7ed63acea3e0)

2.	Install ESPHome compiler in HA. You may need to update HA first. Settings > Add-ons > Add-on store > ESPHome Device Builder add-on > Install.

3. Go to ESPHome compiler tab in HA and click add device, then click OPEN ESPHOME WEB. It'll take you to a new tab.

     ![Image](https://github.com/user-attachments/assets/d98906c4-3bae-406c-bcda-612fdcfcb195)

4. Plug the Atom S3 lite into USB port on your PC. If it's not recognised, install Arduino IDE, or download dodgy drivers from the web.

5. Click connect on the ESPHOME WEB, it will prompt to select the S3 lite over COM port.

     ![Image](https://github.com/user-attachments/assets/f404b590-9ffc-431a-bf0c-81c1dc17180c)

6. Click prepare for first use and install.

     ![Image](https://github.com/user-attachments/assets/f9d4959c-3215-4fca-9700-a81ab20b04ed)

7. Connect to wifi and enter your SSID/Password.

     ![Image](https://github.com/user-attachments/assets/e0675281-9f78-4885-8417-94e4a77fa590)

8. It will now connect to wifi, go back to HA where it's autodiscovered.

     ![Image](https://github.com/user-attachments/assets/6bb662a4-cc85-458e-8069-765e0b5da9ee)

9. HA will discover the device, click show if it’s hidden.

     ![Image](https://github.com/user-attachments/assets/b3aba78b-c2d7-4975-be9d-434e5d3d1e37)

10. Take control of the new discovered device, give it a name.

      ![Image](https://github.com/user-attachments/assets/0c1f4355-c202-4301-963c-002b39869feb)

11. Skip this prompt.

      ![Image](https://github.com/user-attachments/assets/be1dcf6c-88cb-49a4-8b6f-10a073054a4e)

12. Edit the device to paste Mitsubishi Electric Aircon yaml config.

13. Click install and select manual download. It will build and compile the firmware.

      ![image](https://github.com/user-attachments/assets/36c41155-1c52-43f5-bcfb-77c19078961e)

14. Select the “Factory Format, previously modern” to download the firmware.bin file.

      ![image](https://github.com/user-attachments/assets/86a006a8-1b80-4af6-b5d3-1a30ac40b4b9)

15. Go back to web.esphome.io tab where its connected over COM port. Select install and install the firmware.bin file.

      ![image](https://github.com/user-attachments/assets/c8d496b0-294b-4b71-99f7-6141d828ee4d)

16. After flashing, click logs while its powered by USB in ESPHome and see if it connects to wifi.

17. On MSZ-AP25VGD2 indoor unit, remove the front filter flap by opening and pulling it straight out. It uses C clips.

18. Undo the right-hand-side white plastic cover screws, there were two on the front and one at the bottom under the vanes and lift off.

      ![image](https://github.com/user-attachments/assets/d71a47d9-fcb1-49d6-a987-39d2422fa3aa)

20. Remove one screw to remove the metal access panel. Pull the panel to the right then slide forwards. Note 240V AC nearby.

      ![image](https://github.com/user-attachments/assets/948fd217-982f-474f-b977-fb1f8e8a6464)

21. Plug the Atom S3 lite into the CN105 port.

      ![image](https://github.com/user-attachments/assets/23f1c75f-3773-4f3a-9e36-3c914c5f7d68)


22. Go to Devices in HA. Find ESP32 devices and see if it works.

      ![image](https://github.com/user-attachments/assets/ae8e8764-ab9f-4b63-b4e1-6d1ad8f546d5)





