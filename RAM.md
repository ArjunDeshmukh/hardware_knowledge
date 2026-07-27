# Board's RAM memory chip (LPDDR4X SDRAM)

## Why "Rayson"?
Raspberry Pi uses multiple certified component suppliers (such as Micron, Winbond, CXMT, and Rayson) to manufacture memory chips for their boards. In official Product Change Notifications (PCN 46), Raspberry Pi Ltd introduced Rayson as an approved alternative RAM supplier alongside Micron to maintain a steady production supply chain.

## Key Details
* **Component Type:** LPDDR4X SDRAM

* **Role:** High-speed system memory used by the BCM2712 processor and VideoCore VII GPU.

* **Capacity:** Depending on your Raspberry Pi 5 model, the Rayson chip will be either 2GB, 4GB, or 8GB.

Tip: You can check the exact amount of RAM installed on your board in the command line by running free -h or checking the small RAM indicator resistor pad labeled on the top corner of the Pi 5 PCB.