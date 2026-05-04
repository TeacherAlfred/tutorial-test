# Glowy Lights Tutorial

## Introduction @unplugged
Learn how to control colorful LEDs using the **NeoPixel** extension! We will set up a strip of 8 lights and turn them all red when you press Button A.

## Step 1
Drag the ``||neopixel:set strip to NeoPixel at pin P0||`` block into the ``||basic:on start||`` block.
```blocks
let strip = neopixel.create(DigitalPin.P0, 8, NeoPixelMode.RGB)
```

## Step 2

Now, let's make the lights turn red.

Add an ``||input:on button A pressed||`` block. Inside it, place the ``||neopixel:show color red||`` block.

Code snippet

```blocks
input.onButtonPressed(Button.A, function () {
    strip.showColor(neopixel.colors(NeoPixelColors.Red))
})
```

## Step 3

Finally, let's make a way to turn the lights off.

Add an `||input:on button B pressed||` block and put a `||neopixel:clear||` block inside it, followed by `||neopixel:show||`.

Code snippet

```blocks
input.onButtonPressed(Button.B, function () {
    strip.clear()
    strip.show()
})
```

## Done! @unplugged

You've finished! Download this to your micro:bit and press **A** to see the glow and **B** to turn it off.

Code snippet

```package
neopixel
```