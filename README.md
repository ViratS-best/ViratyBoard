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
