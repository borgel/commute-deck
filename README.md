# What?
A mechanical keyboard, Raspberry-Pi 2, battery and display all in one 24" wide box. Think of it as a [deck](https://www.google.com/search?q=neuromancer+deck) (some sort of poorly defined computing device full of 90's nostalgia) from William Gibson's [Sprawl Trilogy](https://en.wikipedia.org/wiki/Sprawl_trilogy).

It was built to make it comfortable to work in a UNIX terminal on the train. Though it turns out that staring straight down at the display isn't great long term.

# What's it Made Of?
The big pieces are
* Laser cut plywood (there's a list of how many of each with the [mechanicals](/mechanicals)).
* A Raspberry-Pi (a Pi 2 in v1, but anything with HDMI should work).
* A 7" 720p screen
* A Teensy 2 running a modified version of the [tmk keyboard firmware](https://github.com/tmk/tmk_keyboard) and connected to the key matrix. It emulates a keyboard and mouse to the Pi.
* A 10,000 mAh LiPo battery (ripped apart and rearranged).
* Two USB hubs (one inside, one outside). WiFi and Bluetooth dongles attached inside.

## How To Build One
Ping me. Twitter is easiest (use my GitHub username) and we can start an email thread.

That out of the way... the high level is:
1. Laser cut the chassis using the DXFs in [mechanicals](/mechanicals).
2. Put the switches in the plywood.
3. Bite the bullet and hand wire the key matrix. This part sucks. There are [many](https://deskthority.net/workshop-f7/brownfox-step-by-step-t6050.html) excellent [guides](https://github.com/technomancy/atreus/wiki/BuildLogs) on assembling keyboards by hand. When I built this one, I copied from those and debugged until it worked.
4. Pull apart the battery if needed, and relocate it's charging/regulaton hardware/LEDs somewhere they are accessible from outside.
5. Bolt the battery, Pi, etc onto the bottom plate.
6. There is a top plate (which holds the switches), and a layer above that which mostly protects the edges of the keys. I glued mine together, which I think made it a bit more durable. If you'd like, you can glue together the three layers which include the handle. If you chose to glue things together, make sure to thread the bolts through to hold things in place!
7. Bolt the display between the front acrylic and the plate assembly from 6.
8. Connect the now large number of wires.
9. Slot everything together and tighten the bolts to hold it together!

## Parts
* Plywood, acrylic, or similar. Something which can be laser cut. If you choose plywood, it should be extremely cheap. Personally I prefer the lighter weight and look of (ply)wood.
* A small section of acrylic (I chose something marketed as abrasion resistant) to cover and hold in the display.
* A display. Mine was 7" and 720p (https://www.amazon.com/gp/product/B00JOY5PGM/). You will need both the display AND a control board. I'd get both together to make sure they work together.
* Key switches for a mechanical keyboard is a while thing. Here's a [disturbingly thurough guide](https://input.club/the-comparative-guide-to-mechanical-switches/). There are many places to get them, but I got mine from [mechanicalkeyboards.com](https://mechanicalkeyboards.com/shop/index.php?l=product_list&c=107).
* Key caps for the switches. Again, many places to get them, but [mechanicalkeyboards.com](https://mechanicalkeyboards.com/shop/index.php?l=product_list&c=40) works well.
* A Raspberry-Pi (version doesn't matter as long as it can connect to the display)
* A battery. Again, pretty much anything works, but here's the one I used [https://www.amazon.com/gp/product/B00ITILPZ4]. At the time I chose it because it was thinish.
* A Teensy 2.0 (https://www.pjrc.com/store/teensy.html). Other micros will work too, but if you're planning to use the `tmk` firmware it needs to be at ATMEGA of some sort. The Teensy 2.0 is a populat choice. Note: Newer Teensy's are much more powerful, but don't have ATMEGAs!
* Fasteners. Uhhh, need to find a list of these
* A 12" HDMI cable to connect the Pi and display. If you move the Pi, changing the length might not hurt. I got my cable from [Monoprice](https://www.monoprice.com/).

