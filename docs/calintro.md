# Pre-Processing Workflow Introduction
In this section we’ll be looking at a typical, modern, calibration and stacking workflow for a CMOS camera.

> Calibrating and stacking (also called pre-processing) your images correctly is absolutely essential to get the most out of your AP experience. 

The classic guide for calibration in PixInsight at LightVortex has been a mainstay for many years, however it hasn’t been updated since 2018 and has some directions that are more for CCD imaging, which can be confusing. 

Before we even begin let me also say: using the WBPP (weighted batch pre-processing) script in PixInsight will do everything nearly the same as in this explanation, automatically. The PixInsight team has shown that they are committed to making WBPP the standard way to pre-process and even stack your images. However, I think there is still value in knowing what is going on behind the scenes for 2 reasons: 
1)	You can feed WBPP the correct files and tweak it to your liking
2)	You know what to do when things go wrong

With that lets begin. We’ll also be looking at what each of these calibration file types is as we progress. Please take a look at the nav bar on the left to jump between sections. We’ll be starting with bias frames, talking about flats, working with darks, then how we apply them all together, correctly. 
