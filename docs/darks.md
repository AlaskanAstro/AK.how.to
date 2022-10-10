# Darks
## What are Darks?
If Bias is the camera’s fingerprint, then Darks are the signature. You can’t change anything about your fingerprints, but you can sign your name larger, smaller, bolder, etc – but it’s still your signature.
 
As you take long exposures with your camera, unwanted signal artifacts can build up over time. These can be caused by a number of sources including heat from electronics. In some cameras these present as a very recognizable starburst pattern. The good news is that like Bias, these patterns are consistent and repeatable. 

<figure markdown>
  ![183 Dark Frame](https://i.imgur.com/j34bG7I.jpg){ width="500" }
  <figcaption>Auto-stretched 240s dark frame from a QHY183. Just bask in this beautiful starburst.</figcaption>
</figure>

Darks also help to remove hot pixels, though dithering does this as well. 

### There are some common misconceptions about things Darks *do not* actually help with. 

> Darks do not remove thermal noise

Thermal noise is random, hence the name: noise. While you can reduce thermal noise by cooling your camera, you cannot remove random noise by subtracting other random noise. The only way to reduce noise of any kind is to reduce the source or to take many images to help average it out. That’s basically the fundamental idea behind stacking.

> Darks may not be helpful if you can’t regulate your camera’s temperature.

Because Darks are affected by temperature, the temperature needs to be within several degrees C to work effectively. How exactly they need to match to work is something you will need to experiment with yourself. If you are using a dedicated AP cam with regulated cooling, this is no issue since you can set the temperature to match exactly. You may need to put your camera in the fridge to take cold enough darks depending on your local weather and camera’s cooling ability, but it is easily achievable. 

## How do we take Darks?

Just like with Bias, our goal is to take a picture of the thing we don’t want so that we can remove it. 

Unlike Bias, Darks are affected by several factors: gain/ISO, time, and temperature. This means that to take an accurate image of what we want to remove, we need to match all these settings to the Light frames we are calibrating. If you took 180s exposures at gain 139 and -10C, your darks need to be 180s long at gain 139 and -10C. 

<figure markdown>
  ![Covered Cameras](https://i.imgur.com/mBixCdJ.jpg){ width="500" }
  <figcaption>Astrocam and DSLR ready to take bias or dark frames. Solid covers are on all light openings (can't see but the DSLR viewfinder has aluminum foil over it. </figcaption>
</figure>

Just like with Bias, this is purely to do with the camera sensor, so we cover our camera and take pictures of nothing, but longer this time.  If you take several different exposure lengths – maybe 180s for broadband and 300s for narrowband, you will need a set of Darks for each time length. The same applies if you use different temperatures in different seasons or different Gain/ISO. Take as many as you like, the more you take, the more accurate and clean your calibration will be. I personally use 30 images for each Master Dark. 

## How do we make a Master Dark

The process to make a **Master Dark** is largely the same as a Master Bias, though you may tweak the rejection settings having fewer subs. Feel free to simply copy these settings for Image Integration. 

- Insert Image of Darks Int

Keep in mind that if you have created several different Master Darks for different exposure lengths, gain/ISO, or temperatures, you will want to save them in an organized manner. Personally I have a folder for the different temperatures I use and then the different exposure lengths inside that. 

Again, we will discuss how to correctly use these Master Darks in the Workflow page. We will also cover something you may have thought of – these Master Darks contain Bias signal. 
