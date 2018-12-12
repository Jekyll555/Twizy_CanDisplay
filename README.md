# Twizy_CanDisplay
utilizing Arduino components to display CAN vehicle signals on the example of Renault Twizy

![inUsePic](pics/coast_w_light_accel_s.png)  ![componentPic](pics/CanDisplay_desk1_s.png)


This project was born on a Friday evening having a beer and thinking about visualizing a few of the Twizy CAN data by using the omnipresent arduino hardware. 
The first working version took a little longer - mainly to me being unused to designing a display layout with arduino-limitated resources (did you ever do it?).
However in the end it works quite well. The project sources were adjusted
- to use adafruit GFX TFT driver BUT with custom fonts that don't flicker the screen
- the redraw per screen-update was limited to the essential needs

Used components:
1) [arduino Uno](https://de.aliexpress.com/item/2014-the-latest-version-UNO-R3-development-board-FOR-arduino-improved-version-Send-USB-line-and/32248072684.html?spm=a2g0x.search0104.3.134.6d0b1afdoMnAYU&ws_ab_test=searchweb0_0,searchweb201602_1_10320_10152_10321_10065_10151_10344_10068_10342_10547_10343_10322_10340_10548_10341_10193_10696_10194_10084_10083_10618_10304_10307_10302_5711211_10180_10313_10059_10184_10534_100031_10319_10103_10624_10623_443_10622_10186_10621_10620-5711211,searchweb201603_1,ppcSwitch_4&algo_expid=e4e44539-17af-4b11-a1ac-0a23b43cea50-19&algo_pvid=e4e44539-17af-4b11-a1ac-0a23b43cea50&priceBeautifyAB=0) (8EUR)
   or [Mega](https://de.aliexpress.com/item/2014-the-last-new-MEGA-2560-R3-development-board-FOR-arduino-an-improved-version/32247818078.html?spm=a2g0x.search0104.3.8.6d0b1afdoMnAYU&ws_ab_test=searchweb0_0,searchweb201602_1_10320_10152_10321_10065_10151_10344_10068_10342_10547_10343_10322_10340_10548_10341_10193_10696_10194_10084_10083_10618_10304_10307_10302_5711211_10180_10313_10059_10184_10534_100031_10319_10103_10624_10623_443_10622_10186_10621_10620-5711211,searchweb201603_1,ppcSwitch_4&algo_expid=e4e44539-17af-4b11-a1ac-0a23b43cea50-1&algo_pvid=e4e44539-17af-4b11-a1ac-0a23b43cea50&priceBeautifyAB=0) (11EUR, double ROM!)
2) [TFT display](https://de.aliexpress.com/item/Hot-selling-2-8-inch-TFT-Touch-LCD-Screen-Display-Module-for-arduino-UNO-R3-mega2560/32809485905.html?spm=a2g0x.search0104.3.43.203e21a8TddaW8&ws_ab_test=searchweb0_0,searchweb201602_1_10320_10152_10321_10065_10151_10344_10068_10342_10547_10343_10322_10340_10341_10548_10193_10194_10084_10083_10618_10304_10307_10302_5711211_10180_10313_10059_10184_10534_100031_10319_10103_10627_10626_10624_10623_10622_10186_5722411_10621_10620_5711311-normal#cfs,searchweb201603_25,ppcSwitch_4&algo_expid=857043ee-847e-459b-9e99-53bd0180b3b1-6&algo_pvid=857043ee-847e-459b-9e99-53bd0180b3b1&transAbTest=ae803_3&priceBeautifyAB=0)
 ~8.4EUR 
3) [Can shield ](https://de.aliexpress.com/item/1Set-MCP2515-Can-Bus-Shield-Board-SPI-Interface-9-Pins-Standard-Sub-D-Connector-Expansion-Module/32819242555.html?spm=a2g0x.search0104.3.2.422e7f6fe72rXb&ws_ab_test=searchweb0_0,searchweb201602_1_10320_10152_10321_10065_10151_10344_10068_10342_10547_10343_10322_10340_10341_10548_10193_10194_10084_10083_10618_10304_10307_10302_5711211_10180_10313_10059_10184_10534_100031_10319_10103_10627_10626_10624_10623_10622_10186_5722411_10621_10620_5711311,searchweb201603_25,ppcSwitch_4&algo_expid=91f26e02-d7cb-4589-9694-d072f3432757-0&algo_pvid=91f26e02-d7cb-4589-9694-d072f3432757&transAbTest=ae803_3&priceBeautifyAB=0)
(self-solder connectors, 5EUR)
4) [OBD Adapter 10$](https://www.seeedstudio.com/DB9-to-OBD2-Cable-With-Switch-p-2872.html)
   , lock for the _pinout_ when searching alternatives 
   DB9 CAN (for above CAN shield): High Pin3, Low Pin5 !! OVMS adapter does NOT fit~! :(

you should be able to use an arduino mega as well, it holds double the flash for your fonts etc... pin-compatible, slightly longer PCB. 
I didn't have one for testing yet.
The cheap CAN shields come with a hard-wired 120Ohms resistor. This didn't make trouble during my testing. Possibly you want to remove it (unsolder or 'destroy').

Printing (or building) a casing for this CAN display is planed. You have an STL file matching this job (it should be ?

mediate level: checkout yourself options for bigger TFT (up to 3.5" on _AVR_ or going to where the music plays: who is the first for esp8266/32? - but that is like an OVMS display isn't it :D )

And here we go for another posibility for improvements.
[![Feature Requests](http://feathub.com/Jekyll555/Twizy_CanDisplay?format=svg)](http://feathub.com/Jekyll555/Twizy_CanDisplay)
