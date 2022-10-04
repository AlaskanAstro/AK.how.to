# Bias

## What is it?

Every time your camera takes an image, it leaves an electronic fingerprint. The process of reading the information off the sensor and saving it produces a very faint characteristic pattern on every image. This is the Bias signal. The bias signal is identical for a set gain or ISO setting (like how you actually have 10 unique fingerprints), regardless of any other factors like image length or temperature. Every image you take with your camera has bias signal in it. Since this signal is just part of the camera electronics, we don’t want to see it in our finished image. 

<figure markdown>
  ![268 Bias Frame](https://i.imgur.com/IIEfk74.jpg){ width="300" }
  <figcaption>An overstretched bias image from a QHY268M. Note the pattern of vertical lines. This is the "fingerprint" it leaves on every image. </figcaption>
</figure>

## How do we take a bias image?

We’re going to talk about this idea for each of the calibration frame types – once we know what the frame is, how do we remove it from our finished product? To be able to remove it, we need to capture a very clean idea of what it is that we’re actually getting rid of. 

Since bias is in every image and isn’t affected by length, we want to isolate just the bias signal as much as we can. We do that by taking a picture of… nothing! Capturing bias frames is the easiest calibration process. All you need to do is put a very light-proof cap on your camera and take a large amount of very short exposures. Remember we’re trying to take a picture of *just the electronic signature of taking and saving an image*. Because many astro-cams enter a different video mode at too-short exposures, I recommend making your bias images 0.2s long. Taking 200 is not an unreasonable start. As you’ll see we really only need to do this once and then can reuse the files many times in the future. 

So take your 200, very short images of nothing at the same ISO or gain that you took your lights at. Temperature doesn’t matter because there’s no time for thermal noise to build up so quickly. The lens or telescope obviously doesn’t matter because we aren’t letting any light in. 

## How do we make a Master Bias?

Great, now you have a bunch of pictures of nothing. That was easy. Now we want to turn this into something useful. Simply put we’re going to average them together to eliminate as much noise as possible and get the truest most accurate idea of what the bias signal really looks like. 

Here are the settings I use in PixInsight with the image integration process– they’re the same that WBPP would automatically choose for you anyway. The only fancy bit is the pixel rejection which just looks at outlier values and doesn’t bother averaging them into the final image because they’re so far off from the other 199 samples. 

Once we’ve run image integration we’re left with our **Master Bias**. This should be a very accurate picture of our camera’s signature. Save it with the following settings and we can reuse it for many months. We’ll use this Master Bias when we begin the actual calibration workflow to remove the bias signal from all our images. 
