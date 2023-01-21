# Pocket-SDVX-Pico-THT-Release
An ultra budget mini Sound Voltex controller with through hole components. Intended to fit within AllPCB's free prototype size.

Join the discord for discussion and support! https://discord.gg/MmuKd73XbY

My blurb regarding this controller's design: https://youtu.be/ZNcycQQxNAY

Side Note: This design really needs to have 2 10nF capacitors on each encoder(CH-A -> GND, CH-B -> GND), totalling 4 capacitors.  You can maybe bodge in some small ones where the encoder pins meet the pcb or on the pi pico's gpio 0, 1, 2, 3 pins.  Without it, the encoders might skip a lot even with software debouncing turned on.

![Pocket SDVX Pico THT 1](pics/20210724_023411.jpg)

- This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.

## Parts Required
- 1x Case, 3D Printed
- 1x PCB, 5 free ones via AllPCB's 2021 Free Prototyping (1/mo/user, same gerber can only be made once a week between all users)
- 7x MX-Style switches of your choice
- 2x Bourns PEC16-2015F-N0024 Encoders (can get different shaft lengths if this one is OOS, follow the format PEC16-20##F-N0024 where ## is the shaft length in mm)
- 1x Raspberry Pi Pico
- 2x Knobs with an inner diameter of 6mm and an outer diameter of between 20-25mm.  Can purchase or 3D print, preferably via resin.  Knob takes a m4x12 setscrew/grubscrew or shorter.  Probably go m4x10.  Or omit it entirely, it's a very tight fit.
- 7x MX-compatible keycaps, in the sizes: 1x 1u, 4x 1.25/1.5u, 2x 2u.  Can purchase or 3D print, preferably via resin.
- 4x small rubber feet, 10mm diameter
- 1x USB micro to USB type A cable, you likely have dozens of these already.

## Optional Parts/Upgrades
- 2x 2u Cherry MX Clip-in Stabilizers CHERRY 0G990224: https://www.mouser.com/ProductDetail/540-G99-0224 (Screw in stabs might fit as well, untested)
- 7x LEDs of your color choice, choose between 2x3x4mm, 1.8mm, or 3mm flangeless LEDs - anything that will fit with MX switches
- 7x 1/4w resistors, choose between 100-220Ohm for Bright->Less Bright

## Order & Build Instructions
- ~~ ORDERING ~~
- AllPCB has free prototype boards: https://www.allpcb.com/activity/free-pcb-prototype-2021.html.  Create an account, claim the free prototype coupon, and go to Instant PCB Quote.  Their site is a little jank and sometimes the PCB quote won't show $0 when you login.  Can e-mail support and they might be able to help you out.
- EDIT: FREE PROTOTYPE BOARDS DEAD AS OF 2022.  RIP.  Can order PCBs off JLCPCB, AllPCB, or basically any other pcb manufacturer though.
- Leave everything as default except for Dimensions(100.8 x 131 mm), Quantity(5), Solder Mask(Cold White), Silkscreen(Black)[this should change automatically once you select solder mask]
- Quote now, choose the cheapest option.  I think it should say free if you did it correctly.  Add to cart, checkout, and then upload Pocket-SDVX-Pico-THT-1-2-Gerbers.zip to the order.  You're done ordering your PCBs now!
- Print case_v2_1.STL on a FDM printer in whatever plastic you want as long as it prints nice and flat.  Bring your own keycaps and knobs or print the ones here - tested on a resin 3d printer and NOT FDM, YMMV.
- Get the other stuff listed in the BOM above.
- ~~ ASSEMBLY --
- Flash your Pi Pico with https://github.com/speedypotato/Pico-Game-Controller.  You may have to change the encoder PPR from the default 600 to 24.  If you don't need to change anything, I've provided a precompiled Pico_Game_Controller.uf2 you can use.  Just hold down the small button on the Pi Pico when plugging it in, and drag the .uf2 file directly into the drive that pops up.  EDIT: I now recommend going here https://github.com/speedypotato/Pico-Game-Controller/tree/release/pocket-sdvx-pico/build_uf2 and picking up the latest build for Pocket SDVX Pico as the pinouts that matter on THT should always match up.
- ![Pocket SDVX Pico THT 2](pics/20210722_215100.jpg)
- Add your 2u stabilizers to the case.  I always forget, so just do it now.
- Solder in your LED resistors if you have them.  This is the side with the rectangles and Rasis.  Clip the legs.
- Solder your Pi Pico directly onto the board.  This is the side with the rectangular pads and Rasis.  Lookup soldering castellated pins on youtube if you need help.
- ![Pocket SDVX Pico THT 3](pics/20210722_220145.jpg)
- NOTE: ONLY DO THIS IF YOUR SWITCH HAS A HOLE FOR THE WHOLE LED.  IF IT DOESNT, SOLDER THESE AFTER YOU SOLDER SWITCHES.  Solder in the LEDs.  The light part is on the same side as the resistors/pi pico/Rasis.  Be sure to match up the shorter lead(negative) with the square pad.  Clip the legs.
- ![Pocket SDVX Pico THT 4](pics/20210722_200532.jpg)
- ![Pocket SDVX Pico THT 5](pics/20210722_200616.jpg)
- Your board should now look like this(ignore the little green wires sticking out at the corner of the board)
- ![Pocket SDVX Pico THT 6](pics/20210722_201329.jpg)
- Slot in the encoders onto the edge of the PCB.  The 3 pins should touch the 3 pads directly, and then insert it all into the case.  Ignore the green wires, v1.2 pcb and up should be able to be soldered directly.  Screw them onto the case with their washer and solder them in.
- ![Pocket SDVX Pico THT 7](pics/20210722_203214.jpg)
- Your controller should look like this now.
- ![Pocket SDVX Pico THT 8](pics/20210722_203224.jpg)
- Add your switches to all the sockets, making sure they are pushed in all the way.  Solder them in.
- ![Pocket SDVX Pico THT 9](pics/20210722_213212.jpg)
- Add your rubber feet.
- Add keycaps and knobs.  Your con is now complete!  Grab a micro-usb cable and plug it into the Pi Pico.  Route the wire up through the channel and start playing!
- ![Pocket SDVX Pico THT 10](pics/20210724_023411.jpg)


<!--
## Probably your BOM, FYI I haven't bought these yet so YMMV
- $12 - 1x Case printed at a library, makerspace, or maybe try https://www.reddit.com/r/3Dprintmything/
- $0 - 5x PCB free from AllPCB https://www.allpcb.com/activity/free-pcb-prototype-2021.html
- $6.86 - 7x switches, e.g. gateron yellows from ebay https://www.ebay.com/itm/114844081593?
- $10.39 - 2x Bourns PEC162015F-N0024 where shipping is 7.99 for me
- $4.00 - 1x Raspberry Pi Pico, should be available everywhere eventually
- $3.88 - 2x knobs, Dia Black Aluminum Rotary Control Potentiometer Knob 20mm x 15.5mm GN_T6 https://www.ebay.com/itm/294227590591?hash=item448154bdbf:g:9tcAAOSwkklZo4D3
- $15 - 7x keycaps, get 4x 2u and 4x 1.25u https://www.aliexpress.com/item/4001241957677.html or spend a little more and get a 1u for the start button as well https://www.aliexpress.com/item/32850729893.html?spm=a2g0o.cart.0.0.44a23c00ztfS3E&mp=1 or save a big chunk of change and settle for 3d printed ones
- $0.40 - 2x 2U Cherry MX Clip in Stabs, assuming you buy this with the encoders
- $4.00 - 7x LEDs, here's 100 red for 4 bucks https://www.ebay.com/itm/201172208103?
- $2.07 - 7x resistors, but just pick up 100 for 2 bucks tbh https://www.ebay.com/itm/192076577170?hash=item2cb8a7f992:g:XUsAAOSwUKxYl9tT
- $2.19 - 4x rubber feet, but you get 50 for 2 bucks ish https://www.ebay.com/itm/124679886620

The sum: $60.79 plus tax
-->

## BOM 
| Name             |Order Qty.  |Price (USD)|Ext.: (USD)|Manufacturer Num.  |Manufacturer|Description                                                                 |
|------------------|------------|-----------|-----------|-------------------|------------|----------------------------------------------------------------------------|
|Encoders          |2           |$2.00      |$4.00      |PEC16-2015F-N0024  |Bourns      |Encoders 15 MM SHAFT NO SWITCH NO DET                                       |
|Pi Pico           |1           |$4.00      |$4.00      |SC0915             |Raspberry Pi|Single Board Computers Raspberry Pi Pico (No Headers)                       |
|19mmx20mm Knobs   |2           |$5.08      |$10.16     |KB700B14AL         |Apem        |Knobs & Dials Machined Alumin Knob                                          |
|MX 2U Stabilizers |2           |$0.23      |$0.46      |0G990224           |CHERRY      |Switch Hardware 1x2 KEYCAP W/FRAME                                          |
|Knob LEDs         |2           |$0.36      |$0.72      |WP914IDT           |Kingbright  |Standard LEDs - Through Hole **Red** 625nm Diffused 8mcd. 2x3x4mm           |
|Button LEDs       |5           |$0.37      |$1.85      |WP914GDT           |Kingbright  |Standard LEDs - Through Hole **Green** 568nm Diffused 6mcd. 2x3x4mm         |
|Resistors         |7           |$0.32      |$2.24      |MOS1/2CT52R101J    |KOA Speer   |Metal Oxide Resistors 1/2W 100 5%                                           |
|Capacitors        |4           |$0.22      |$0.88      |K103K10X7RF5UL2    |Vishay      |Multilayer Ceramic Capacitors MLCC - Leaded K 50V 10NF +/-10% X7R AMMO E3   |
|MX Switches       |7           |$1.59      |$11.13     |MX3A-11NA          |CHERRY      |Cherry MX **Black**, clear housing  (Buy whatever switch type you prefer)   |
|Keycaps           |1 (set)     |$19.99     |$19.99     | N/A               | N/A        |Need 5x 1u for BT, 2x 2u for FX. (Optimally 4x 1.5u, 2x 2.5u, 1x 1u)        |
|USB Cable         |1           |$7.50      |$7.50      | N/A               | N/A        |USB Type A Male to Micro USB male. Purchase off Amazon or electronics store |
|Rubber Feet       |100 (need 4)|$0.052     |$12.87     | N/A               | N/A        |Adhesive rubber pads. 3/8" diameter (~9.5mm). Try Amazon, or hardware store |
|Case              |1           |$19.96     |$19.96     | N/A               | N/A        |Print at library or makerspace. PLA Price quote from https://www.hubs.com/. ABS may have fitment issues with switches. Resin is optimal but 2-3x the price.      |
|PCB               |5 (need 1)  |$9.00      |$45.00     | N/A               | N/A        |MINIMUM sets of 5 PCBs. Price quote from https://www.allpcb.com/            |


Sum (excluding shipping and tax): $140.76

All components with a listed Manufacturer Number has an uploadable BOM to Mouser and/or Digikey found in `bom/`. Components which do not have a listed number must be ordered wherever you can find them.

## Reduced Cost BOM
While the original sum may seem pricey, a majority of the cost is from the Case, Keycaps, and Knobs (all of which can be 3D printed) as well as the PCBs (which can be subsidized if you or someone you know makes more than one Pico THT). Additional cost savings can be accounted for if you already own these components, or buy them in bulk (such as the MX switches). Below is a more accurate projection of price per controller assuming you:
1. Have access to a large enough FDM 3D printer which prints in PLA filament, or SLA printer which prints in resin. These have costs about $25.00 per 1kg spool/container.
2. Obtained a spare PCB from a friend or acquaintance, or got lucky and found a manufacturer promotion for free PCBs.
3. Bought or own the MX Switches, and Rubber Feet in bulk from a previous project and/or plan to use them in other projects.
4. Have a surplus of USB cables.

Changes are bolded and marked in `[#]`

| Name             |Order Qty.  |Price (USD)|Ext.: (USD)|Manufacturer Num.  |Manufacturer|Description                                                                 |
|------------------|------------|-----------|-----------|-------------------|------------|----------------------------------------------------------------------------|
|Encoders          |2           |$2.00      |$4.00      |PEC16-2015F-N0024  |Bourns      |Encoders 15 MM SHAFT NO SWITCH NO DET                                       |
|Pi Pico           |1           |$4.00      |$4.00      |SC0915             |Raspberry Pi|Single Board Computers Raspberry Pi Pico (No Headers)                       |
|**22mmx20mm Knobs [1]**|2      |**$0.35**  |**$0.70**  | N/A (3D)          |N/A (3D)    |3D printed, ~14g = ~1/71 of a spool/container.                              |
|MX 2U Stabilizers |2           |$0.23      |$0.46      |0G990224           |CHERRY      |Switch Hardware 1x2 KEYCAP W/FRAME                                          |
|Knob LEDs         |2           |$0.36      |$0.72      |WP914IDT           |Kingbright  |Standard LEDs - Through Hole **Red** 625nm Diffused 8mcd. 2x3x4mm           |
|Button LEDs       |5           |$0.37      |$1.85      |WP914GDT           |Kingbright  |Standard LEDs - Through Hole **Green** 568nm Diffused 6mcd. 2x3x4mm         |
|Resistors         |7           |$0.32      |$2.24      |MOS1/2CT52R101J    |KOA Speer   |Metal Oxide Resistors 1/2W 100 5%                                           |
|Capacitors        |4           |$0.22      |$0.88      |K103K10X7RF5UL2    |Vishay      |Multilayer Ceramic Capacitors MLCC - Leaded K 50V 10NF +/-10% X7R AMMO E3   |
|**MX Switches [1]**|7          |**$0.27**  |**$2.40**  | (Gateron Yellows) |Gateron     |Most switches at ~$0.27 when buying in 100+. or ~$0.35 for 50+.             |
|**Keycaps  [1]**  |1 (set)     |**$0.36**  |**$0.36**  | N/A (3D)          | N/A (3D)   |3D printed (4x 1.5u, 2x 2.5u, 1x 1u), ~14.5g = ~1/69 of a spool/container.  |
|**USB Cable [4]** |1           |**$0.00**  |**$0.00**  | N/A               | N/A        |You probably have lots. Be sure they arent USB power only (no data transmit)|
|**Rubber Feet [3]**|4          |**$0.052** |**$0.21**  | N/A               | N/A        |Adhesive rubber pads. 3/8" diameter (~9.5mm). Try Amazon, or hardware store.|
|**Case   [1]**    |1           |**$2.25**  |**$2.25**  | N/A (3D)          | N/A (3D)   |3D printer, ~90g = ~1/11 of a spool/container.                              |
|**PCB    [2]**    |1           |**$0.00**  |**$0.00**  | N/A               | N/A        |Obtained from friend or acquaintence, or a manufacturer had a free promo.   |

Sum (excluding shipping and tax): $1​7.83

Parts from either BOM can be modified as seen fit, for example keeping aluminum knobs for their feel or going to commericial 3D printing solutions if your print bed isnt big enough to 3D print the case. 
<!--
## My BOM
- $0 - 1x Case printed free at my local library
- $0 - 5x PCB free from AllPCB
- $1.82 - 7x switches, technically these are mx blue clones harvested from prebuilts but I'll calculate gateron prices here at around 26c/switch
- $2.49 - 2x Bourns PEC162015F-N0024, which I bought 20 of as well as some 2u MX stabilizers to offset shipping. ((35.97/27.98)*19.38)/10
- $2.11 - 1x Raspberry Pi Pico from a microcenter sale when the pi pico first launched
- $7.42 - 2x knobs, 25mmx15mm Black Aluminum which I got off amazon
- $0 - 7x keycaps, cheating because I'm borrowing from my Pocket-SDVX
- $0.44 - 2x 2U Cherry MX Clip in Stabs, ordered 50 to offset shipping. ((35.97/27.98)*8.60)/25
- $0.14 - 7x LEDs, (4.03/200)*7
- $0.09 - 7x resistors (1.29/100)*7
- $0.08 - 4x feet (1/50)*4

The sum: $14.59, half of which is overpriced knobs
-->