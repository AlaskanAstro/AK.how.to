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

<figure markdown>
  ![Bias Integration](https://i.imgur.com/4AEVGm8.jpg){ width="500" }
  <figcaption>Settings for Image Integration in PixInsight to create Master Dark</figcaption>
</figure>

Keep in mind that if you have created several different Master Darks for different exposure lengths, gain/ISO, or temperatures, you will want to save them in an organized manner. Personally I have a folder for the different temperatures I use and then the different exposure lengths inside that. 

Again, we will discuss how to correctly use these Master Darks in the Workflow page. We will also cover something you may have thought of – these Master Darks contain Bias signal. 

## Do I actually need Darks?
Depending on your camera, the answer may be: no. There are two ends of the spectrum where you may not want darks. 

### You have a DSLR
The first is **if you cannot regulate the temperature of your camera**, most commonly, using a DSLR. Because the temperature changes throughout the night and your camera may build up heat over time, there is no way to regulate the temperature of a DSLR without heavy DIY modification. If your temperatures are fairly steady through the night, darks may be of some benefit but remember three things:
> Darks only remove characteristic sensor glow and hot pixels

If you DSLR does not have a patterned sensor glow, there is not much you will remove. If your temperature does not match closely enough you will end up adding or over-subtracting this pattern into your Light subs.
> Never waste precious clear dark skies to take darks

Because you can’t regulate your temperature, you will almost certainly need to take darks immediately after imaging before the weather changes. Never waste clear skies to take darks, it’s just not worth it. The benefit of taking more Light subs will far outweigh un-regulated Darks. 
> You will need to make new darks nearly every night

Unless your night time temperatures are constant all night long over multiple days, you will need to make a fresh Master Dark every imaging session. This sounds like a royal pain to me. 

### You have a latest generation AP Cam

The other end of the spectrum is the latest generation of sensors in popular AP cams. These new Sony sensors do not exhibit any characteristic sensor glow so there is nothing to remove in the first place. Darks can still help with hot pixels, though again, dithering does this as well. For these cams, I would call darks *optional* but personally consider it a waste of time and effort. 

Common cameras with this lovely feature are the QHY/ZWO 533, QHY268/ASI2600, and the QHY600/ASI6200. 

Ultimately, you can always experiment yourself and see if Darks benefit your specific gear. Personally, I think they are a waste of time and effort unless you have a dedicated AP cam with regulated cooling and a distinct sensor glow that needs to be removed. 
