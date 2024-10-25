# Gergo 
Gram's ergonomic keyboard is based on Klor and Kaly42 keyboards. Uses a 40-key layout, with splay from Klor and the thumb cluster found in Kaly with some small modifications. The graphic found on both the front and back depicts a morning glory flower, a flower that grew in the backyard of my childhood home :)

![IMG_2381 (1)](https://github.com/user-attachments/assets/bae146b6-9161-4e91-84f1-cff75f1e9980)

# Materials needed:
this keyboard requires some level of experience with soldering and requires the following materials in addition to the PCB:
2x Elite-C MCU (atmega32u4)

40x Cherry mx compatible key switches

40x Cherry mx compatible keycaps

2x TRRS jacks (PJ-320A) *

40x 1N4148 Diodes

1x TRRS cable *


(TRS may be used, however, I will get to that later, I would recommend TRRS as that is what I am currently using and it is known to work)

Optional:

40x Kailh hot swap sockets (while not technically needed, it is a nice feature to have. I opted for clear HS sockets)

2x EC11 Rotary Encoder (not required however they have been very fun to play with and I would recommend them)

Rubber/ Silicone bump-ons (allow the PCB to be used bare without any sliding around without a case)

2x key-switch plate (the one pictured is laser cut acrylic so you can still see PCB graphics, 3D printing would work as well but I feel it would take away from the aesthetics

2x reset switch (I am putting this in optional because the Elite-C has an onboard reset switch, and since the controller is exposed you can also short the RST pin. I don't have reset switches on my current build.)

rubber/silicone bump-ons mentioned above:
![silicone (1)](https://github.com/user-attachments/assets/c576f748-5b0e-4545-98a6-9f643065ed00)


# Notes:
For my specific build:

I used Gateron beer switches which I have come to love, they are somewhat lighter than holy pandas but still feel amazing. The keycaps were resin printed, however, they came out somewhat consistent. I will likely remake a new set at some point. The plate is 1.5mm clear acrylic, 1.5mm thickness is necessary for this build as the plate is held up by the switches alone so the switches must click into the plate. PCB was ordered from JLC and I had a great experience with them. 

In hindsight, I wish I had used a pro-micro footprint so I could try out Bluetooth and ZMK without having to design a new board, as the PCB is compatible ONLY with the Elite-C as well as I am aware. Having diode clusters looks nice but routing them isn't nice, I am unsure if I will continue to include them in further designs. Originally, I had planned for the two halves to communicate using I2C, which was changed to serial, so pins D0 and D1 can be used for serial communications between the two halves. The current PCB also includes a place for pull-up resistors on the right half but if you plan to build this keyboard in serial (which I would recommend), just ignore them. I had read somewhere that I2C was faster, however, was having trouble with the firmware and decided to switch to serial. At some point I may design a full case which will be added to this repository but for now I recommend adding rubber feet to the bare PCB and potentially adding a plate.

# Future Plans
I am very happy with how this keyboard came out and have been playing around with different keymaps for awhile. In the future, I want to try Kailh low-profile switches and maybe a 38-key layout similar to the totem. Features I have been looking into including in my next project are OLED, some sort of tenting solution, Bluetooth + ZMK, and integrated MCU. 

