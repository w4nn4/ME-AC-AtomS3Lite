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

     ![image](https://github.com/user-attachments/assets/5b239f4f-34c9-49b4-b12e-bdae60e25cfd)

2.	Install ESPHome compiler in HA. You may need to update HA first. Settings > Add-ons > Add-on store > ESPHome Device Builder add-on > Install.

3. Go to ESPHome compiler tab in HA and click add device, then click OPEN ESPHOME WEB. It'll take you to a new tab.

     ![image](https://github.com/user-attachments/assets/10bf9ff1-3a33-4b89-bcd5-dde52846beab)

4. Plug the Atom S3 lite into USB port on your PC. If it's not recognised, install Arduino IDE, or download dodgy drivers from the web.

5. Click connect on the ESPHOME WEB, it will prompt to select the S3 lite over COM port.

     ![image](https://github.com/user-attachments/assets/e8945f51-e537-4bc1-b366-839c59f638cb)

6. Click prepare for first use and install.

     ![image](https://github.com/user-attachments/assets/906b0141-5c39-48ad-9493-f3f6fd40b06e)

7. Connect to wifi and enter your SSID/Password.

     ![image](https://github.com/user-attachments/assets/939ee67f-e6e1-43b8-86c6-89553344155f)

8. It will now connect to wifi, go back to HA where it's autodiscovered.

     ![image](https://github.com/user-attachments/assets/fe067502-d1ad-40b1-8f07-082f1d411070)

9. HA will discover the device, click show if it’s hidden.

     ![image](https://github.com/user-attachments/assets/27465531-7452-45b4-9634-6fcd0b8df8b4)

10. Take control of the new discovered device, give it a name.

      ![image](https://github.com/user-attachments/assets/f8468c38-e84e-472f-9acb-a7f283f4e14b)

11. Skip this prompt.

      ![image](https://github.com/user-attachments/assets/d305c3b6-24ba-4945-b70e-c054546b0420)

12. Edit the device to paste Mitsubishi Electric Aircon yaml config.

13. Click install and select manual download. It will build and compile the firmware.

      ![image](https://github.com/user-attachments/assets/e1e01593-38ec-4dff-9863-e6c7ed59882c)

14. Select the “Factory Format, previously modern” to download the firmware.bin file.

      ![image](https://github.com/user-attachments/assets/0d7af673-f64e-440d-aa64-e8f07225b2ad)

15. Go back to web.esphome.io tab where its connected over COM port. Select install and install the firmware.bin file.

      ![image](https://github.com/user-attachments/assets/4e2e10c9-d69c-4feb-ad87-e6d6ac76cff7)

16. After flashing, click logs while its powered by USB in ESPHome and see if it connects to wifi.

17. On MSZ-AP25VGD2 indoor unit, remove the front filter flap by opening and pulling it straight out. It uses C clips.

18. Undo the right-hand-side white plastic cover screws, there were two on the front and one at the bottom under the vanes and lift off.

      ![image](https://github.com/user-attachments/assets/10bf9345-b019-46e2-bb2e-9ae52bcf0219)

19. Remove one screw to remove the metal access panel. Pull the panel to the right then slide forwards. Note 240V AC nearby.

      ![image](https://github.com/user-attachments/assets/47767191-68d6-466c-96ad-8cb3e31e239d)

20. Plug the Atom S3 lite into the CN105 port.

      ![image](https://github.com/user-attachments/assets/5205cff0-2343-4f23-914a-6b5aa3e4b6a9)

21. Go to Devices in HA. Find ESP32 devices and see if it works.

      ![image](https://github.com/user-attachments/assets/cb879cad-a990-4d60-8518-ceddc25c76ee)



