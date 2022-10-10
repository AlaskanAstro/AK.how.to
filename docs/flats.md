# Flats

## What are Flats
Unlike Darks and Bias, Flats are entirely to do with the optical train of our telescope. Flats take an image of what’s wrong with our telescope and accessories and help correct it. 

The two main things that flats correct for are **dust** and **vignetting**. 

**Dust** is simply that: dots of dust that end up on our scope’s optical surfaces or more often on our filters or even the window right in front of our camera sensor. These show up as dark circles on our Light images. The size is a factor of many things especially how close the dust is to the camera sensor. 

**Vignetting** is the natural light fall-off towards the edges and corners of your image. This is caused by a number of factors and flats help even it out, making processing much easier. 

Just like with Darks and Bias, we want to take a picture only of what we don’t want so we can remove it from our Light subs. 

## How do we take Flats?

To take a picture of the optical issues, we take several images of an evenly lit field that covers the whole field of view of our scope. A *flat field* if you will. 

There are several different techniques for this depending on your equipment and situation. The basic idea is the same though. We want to take an image that doesn’t get clipped on the dark or light end of our histogram. We want our light source to be perfectly even with nothing that can be resolved by the scope or lens. See the sidebar for different Flat methods.

> Critically, everything in the imaging train needs to be the same as the Lights.

This means that anything adjustable like f-stop, filter position, zoom if using a camera lens, and physical position of the dirt, all needs to be in the exact same place as when taking your Lights. Depending on your gear, focus may or may not be critical but try to be as close as you can. 

### White T-Shirt Method (sky)

This is a classic and simple way to take flats with equipment almost anyone has. Simply place a <a href="https://youtu.be/h_m-BjrxmgI">Plain White T</a> over the front of your scope and aim it at zenith (straight up). The morning or even afternoon sky is a great even source of illumination. **Please do no point your scope at the sun.** With a DSLR, set your mode dial to Av (Aperture Priority) mode and take 12-30 images. Again make sure your f-stop stays the same. 

With a dedicated AP cam you’ll need to use your control software of choice (it’s NINA) to find an exposure length that roughly centers the histogram. With NINA’s Flat Wizard, this can be done automatically. Like with Bias, I do recommend keeping the minimum exposure length above 0.2s to avoid weird video readout modes. You may need to experiment with more or fewer layers of T shirt to get a reasonable length exposure. Take a set of Flats for each filter. 

-Insert T-Shirt

### Tracing Pad

My favorite mid-ground between the “correct” gear and price is using an LED tracing panel. Just like the T-Shirt method, place your tracing panel on top of your scope, set the brightness to a workable level, and take your images with the same method. You may need to add or remove sheets of printer paper or other suitable material to dim the light and help diffuse it. 
Some large scopes in observatories use a similar method by placing a very large flat field source on a tripod or wall near the scope and aim at that to take flats.

-Insert Tracing Pad Pic
### Bare Sky-Flats

This technique is basically the same as the White T-Shirt method except there is no diffuse material. Because of this, especially if it close to dawn, your camera may pick up some stars. You can take several seconds in between each exposure and make sure your mount isn’t tracking to help reject stars that may come through. This method can be used as a last resort or for very very large scopes that are hard to cover easily. 

-Insert… telescope?

### Flippy-Flatty

The method with the best consistency and cool factor is definitely an automatic flipping cover. These are sold under different names like “Flip Flat” or their technical ASCOM device name “Calibration Cover” as they double as a lens cap when not shooting. 

The biggest advantage of these light panels, other than the obvious fact that they can automatically be taken on and off, is that the light source is controllable via your imaging software. This means the intensity can be adjusted and saved and your flats can be exactly the same settings every time. This greatly helps automation. 

### Synthetic Flats

I don’t condone such base activities. 


## How do we make Master Flats
This section will be a quick preview of the full calibration workflow because to properly make a Master Flat, we need to remember what is in the Flat frame. Going back to the first section on Bias, Bias signal is in *every* frame we take. That means Flats contain Bias, and we need to do something about that. (Spoiler alert - it’s simply subtracting the Master Bias from each Flat sub)

We’ll see how this plays into the complete calibration workflow. There are some things to make note of, for instance the fact that Flats do not need to match Gain/ISO of the Lights to work correctly.

Once we do have properly-calibrated Flats, we combine them with Image Integration again but with some slightly different settings. 

It’s best practice to take new Flats every time you change anything about the optical train of your camera. That includes the location of dust, so if you move your scope when you image or break down any pieces, it is best practice to take fresh Flats every imaging session.

## How do I know my Flats work?

