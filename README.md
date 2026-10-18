# ViratyBoard

A RP2040 board! My second-ever PCB!!!

[![View PCB on KiCanvas](https://hack.club/pcb-badge)](https://kicanvas.org/?repo=https://github.com/ViratS-best/ViratyBoard)

I made this devboard because I really wanted to learn how to integrate a chip, and maybe later I could make compute modules with this knowledge! I know this is really basic compared to a 6-8 layer chip CM, but it's a start I hope to build on! 

This is mainly built using the RP2040 datasheet and this guide: https://github.com/KaiPereira/build-a-devboard

<img width="459" height="528" alt="image" src="https://github.com/user-attachments/assets/52d1dd4a-474a-41f9-a41c-60574e132774" />
<img width="813" height="1143" alt="image" src="https://github.com/user-attachments/assets/28f2eee1-4f94-4383-abea-95747b253da9" />

## What makes my devboard unique?

* **Battery & USB** Accepts both USB power and a battery connection!

  <img width="693" height="562" alt="Screenshot 2026-10-05 174123" src="https://github.com/user-attachments/assets/3a03f2a9-fae2-4a43-b277-6be4fff3c73c" />

# How I built it:

I started by looking over the build-a-devboard GitHub repository, and I followed the guide as well.

Next, I looked over the datasheet for the RP2040, hopefully to find the same image the GitHub repository referenced that showed the result.

So I started developing the board.

First, I set up the decoupling capacitors:

<img width="945" height="286" alt="image" src="https://github.com/user-attachments/assets/d5fd77d7-dc20-4e9e-bd72-a36c1be8eae6" />

Then I continued by labling the whole RP2040:

<img width="455" height="515" alt="image" src="https://github.com/user-attachments/assets/24f9b3f3-ebad-4c4f-9e77-70104d53821d" />

I also added the USB power source and programmer:

<img width="700" height="565" alt="image" src="https://github.com/user-attachments/assets/37d61425-d4bc-41e8-9ddd-32409ec04fc9" />

Then I added the crystal oscillator to make the RP2040 actually work:

<img width="378" height="183" alt="image" src="https://github.com/user-attachments/assets/83432de9-675b-46cf-8377-cff80ea41ac7" />

As well as the flash storage:

<img width="339" height="321" alt="image" src="https://github.com/user-attachments/assets/ec560121-574f-4cac-81fd-32d5b904c1c4" />

And lastly made the pin headers:

<img width="267" height="344" alt="image" src="https://github.com/user-attachments/assets/e7efc268-3629-4f75-b580-8d2703aa5770" />

OH NO!!!

I kept the wrong voltage regulator!!

Thankfully it was an easy fix:

<img width="232" height="227" alt="image" src="https://github.com/user-attachments/assets/5fa59f21-7e0b-44d2-873a-8b2501371b8c" />

But then I thought I should also add something original, like battery power instead of USB... so I added that:

<img width="693" height="562" alt="image" src="https://github.com/user-attachments/assets/2ebb0950-f6ec-42dc-9427-258332b1eefe" />

So... now it accepts both BATTERY AND USB!!!

Plug in BOTH: The USB power instantly turns the MOSFET OFF, completely disconnecting the AA batteries so they don't get accidentally charged or drained!

Next I attached all the footprints:

<img width="621" height="432" alt="image" src="https://github.com/user-attachments/assets/8082cfba-0bf5-45fd-aa0f-cbb061117e18" />

and looked at my final schematic:

<img width="935" height="573" alt="image" src="https://github.com/user-attachments/assets/ee460f0b-4421-401d-ad6c-a3141bbf3446" />

Only routing and PCB design left!

Now this is where it got hard...

## Where did I get stuck at?

This devboard is 4 layers... It's not 2, because, due to the battery mechanism, routing it in 2 layers became really hard and complicated, so I had to switch to 4 layers. This could be done in 2 layers, but I just couldn't manage to, and I was really confused about how to do it, so I was stuck with this. **I asked about routing on Reddit**:
 
 <img width="724" height="239" alt="Screenshot 2026-10-11 114151" src="https://github.com/user-attachments/assets/fc6380bd-d2c4-4ac0-9259-4981979cecc2" />

This was a place where I got stuck during 2-layer routing:

<img width="387" height="359" alt="Screenshot 2026-10-10 102857" src="https://github.com/user-attachments/assets/87837329-9d10-4b5b-ade4-f5a81f631eea" />

And another place I got stuck at:

<img width="397" height="551" alt="image" src="https://github.com/user-attachments/assets/1b7d0c5a-40ad-4fe1-a51c-2ad8ce90a158" />

So it became a 4-Layer project:

<img width="959" height="582" alt="image" src="https://github.com/user-attachments/assets/3a7a1306-9d01-49b0-a9b7-736ac2ec92ae" />

I finally made good progress:

<img width="412" height="521" alt="image" src="https://github.com/user-attachments/assets/efd68bf0-2802-4bff-819e-e5bb984644ef" />

But I ran into an issue on one of the last things:

<img width="618" height="464" alt="image" src="https://github.com/user-attachments/assets/a9f466e8-ff47-43d5-a440-4becdfe3e1f3" />

So I fixed it using:

<img width="751" height="252" alt="image" src="https://github.com/user-attachments/assets/32f2bf24-f533-420f-a202-f79ddacee94d" />

Then I filled for Signal & for Ground on the other two layers!

Just like that I am **DONE**!

<img width="459" height="528" alt="image" src="https://github.com/user-attachments/assets/d83d6882-a056-4b33-a7a9-64665f664789" />


## Project Structure

```text
README.md
devboard.kicad_pcb
devboard.kicad_pro
devboard.kicad_sch
devboard.zip    # Gerber
bom.csv
submit.ino
```

## BOM:

| Part | Qty | Unit | Total | Vendor |
| ---- | ----- | ----- | ----- | ---- |
| [PCB Devboard] | 1 | $66.63 | $66.63 | [JLCPCB](https://www.jlcpcb.com) |
| Tax & shipping for the whole order |  |  | $0.05 |  |
| **Total** | | | **$66.68** | |
