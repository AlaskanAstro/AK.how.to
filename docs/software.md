# Astrophotography Software

This is a list of every piece of software you *should* need for a brand new astrophotography setup. And the best part? Other than some of the processing software, it's all completely free! (of course a lot of it is useless without the hardware but oh well.)

Depending on what specific gear you have, you may only need some of these programs. Note this list assumes you are running a Windows PC, as this is by far the most supported platform for AP. 

Install them before your first night out; keep them up to date. These links were all correct and working as of Nov 2022, please let me know if anything is broken.

## Foundation - ASCOM

ASCOM is the glue that holds everything together. It's a foundational software package that installs a language and framework for all the other softwares to talk to each other. There are some diagnostic tools included but if everything goes according to plan, you should never actually have to interact with ASCOM itself. It just runs in the background. 

<a href="https://ascom-standards.org/Downloads/Index.htm" target="_blank">ASCOM</a>

> A quick note: ASCOM (and NINA) should install any .NET Windows dependencies, but if an issue comes up, google is your friend.

## Imaging - NINA

NINA is an all in one image aquisition suite that controls and coordinates all your astrophotography gear, prioritized for Deep Sky Imaging. It is a free, open source project with a vibrant developer community and is rich with new and useful features. It's so good we named our dog after it. Really. 

The latest stable releases can completely automate your night of imaging depending on what gear you have, in addition to its many useful planning, framing, and gear fine tuning and setup features. It also has a plugin system that is constantly expanding the already amazing feature set. I won't bother listing any other deep sky imaging software as NINA truly is all you need today.

<a href="https://nighttime-imaging.eu/download/" target="_blank">NINA Imaging</a>

There are a few large optional database downloads you can choose to enhance NINA. One is the offline HiPS framing catalog which lets you see where faint nebula are while framing without an internet connection. The other is the object catalog which simply adds pretty preview pictures for many common targets. They are both on the same download page. 

### Platesolving - ASTAP

A core function of NINA is platesolving which relies on an additional free software. Platesolving looks at the stars in your image and precisely figures out where your mount is pointing (and fixes if it's pointing the wrong way). Far and away the best option for this is ASTAP. You will also need to download the correct star catalog for your setup's focal length (H17 or H18). 

<a href="https://www.hnsky.org/astap.htm" target="_blank">ASTAP Plate Solver</a>

## Camera Drivers

You will need to install the latest drivers for your PC to be able to see and talk to your camera. Once installed though, you should never need to interact with the driver. NINA will do all the controlling. Here are links to the most common camera manufacturer's driver pages. 

### ZWO/ASI

<a href="https://astronomy-imaging-camera.com/software-drivers" target="_blank">ZWO Drivers</a>

### QHY

Note that you may need to download the beta driver for some latest model cameras. 


<a href="https://www.qhyccd.com/download/" target="_blank">QHY Drivers</a>

### Player One

<a href="https://player-one-astronomy.com/service/software/" target="_blank">Player One Drivers</a>

### DSLR/Mirrorless - Canon, Nikon, Sony

NINA is able to natively control some Canon and Nikon cameras. For others and for most Sony cameras, this 3rd party ASCOM driver has been developed. From what I've heard, it it is functional. Give it a try. 

<a href="https://www.cloudynights.com/topic/707662-ascomdslr-ascom-driver-for-dslr-cameras-canon-nikon-pentax-sony/" target="_blank">DSLR ASCOM Driver</a>

## Mount Drivers

Like cameras, your PC needs a driver to see and talk to the camera. However, most of these drivers do require a little bit of setup the first time you connect your mount. Most also allow some manual control of your mount without any other software. 

### GSS - Green Swamp Server

GSS is a free 3rd party driver for Synta mounts, that is Sky-Watcher and Orion branded mounts like the HEQ5, Atlas, EQ6-r, AZ-GTi, and more. Most settings out of the box are pretty good. You may need to search for the correct COM port or adjust baud rate depending on your mount. Be sure to find and check the "reverse dec guiding after meridian flip" setting in PHD2 if you use GSS. 

<a href="https://greenswamp.org/?page_id=834" target="blank">GSS</a>

### EQMOD

EQMOD is another 3rd part synta driver. Be sure to set your guide rate to 0.5x or 0.9x depending on your mount.

<a href="https://sourceforge.net/projects/eq-mod/files/EQASCOM/" target="blank">EQMOD</a>

### iOptron

iOptron mounts have their own drivers I guess?

<a href="https://www.ioptron.com/category-s/138.htm" target="blank">iOptron Mounts</a>

### ZWO

Same deal with ZWO's AM5 mount.

<a href="https://astronomy-imaging-camera.com/software-drivers" target="blank">ZWO Mounts</a>

## Autoguiding - PHD2

Autoguiding makes your mount less bad. I'll have another page explaining what autoguiding is in more detail and how to set it up and troubleshoot at this <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="blank">non-existant and definitely non-functional link</a>. Simply put, autoguiding uses a small secondary camera to lock onto a reference star and tell your mount when it's moving the wrong way and how to stop doing that. 

PHD2 is a free software that... does that. It will connect and communicate with your mount, guide camera, and imaging software. Once you use the easy Setup Wizard and calibrate, NINA should do most of the talking to PHD2, including coordinating dithers. 

<a href="https://openphdguiding.org/downloads/" target="blank">PHD2 Guiding</a>

### PHD2 Log Viewer

This simple and helpful bit of software lets you view the log files that PHD2 automatically spits out. It's useful for troubleshooting, seeing your PA error, and bragging about how good your mount performs. 

<a href="https://adgsoftware.com/phd2utils/" target="blank">PHD2 Log Viewer</a>

## Accessory Drivers

Depending on what accessories you have, you may need to install additional drivers. Some are packaged with camera drivers, some are stand alone, some are part of a suite, and some accessories are plug and play in Windows.

### ZWO

ZWO has an autofocuser and many filter wheels.

<a href="https://astronomy-imaging-camera.com/software-drivers" target="blank">ZWO Drivers</a>

### Pegasus Astro

Pegasus makes a great deal of accessories, including autofocus, power distribution, filterwheels, and more. They are all managed through one driver app, Pegasus Unity. Once connected in NINA however, you shouldn't need to deal with Unity unless you want to. It has pretty graphs, so like, you might want to. 

<a href="https://pegasusastro.com/download/" target="blank">Pegasus Astro Accessories</a>

### QHY

The QHY filter wheel drivers should be included with their all-in-one camera driver package but QHY drivers are weird so check the site. 

<a href="https://www.qhyccd.com/download/" target="_blank">QHY Drivers</a>

## Polar Alignment

Electronic Polar Alignment uses your camera, scope, and mount to assist you in accurately aligning your mount to the celestial pole for accurate tracking. When done correctly it's quick, easy, and saves you breaking your back. 

### TPPA in NINA

Three Point Polar Align is a free plugin available in NINA. If you can connect your camera to NINA it should be all you need to successfully Polar Align. It also carries the huge advantage of not needing a clear view of the pole. 

It is found in the plugin menu. 

### SharpCap Pro

If for some reason TPPA doesn't work for you, SharpCap Pro is another good, accurate option. Unfortunately, this feature is only availble with a paid (~$20/yr) subscription to SCP. 

<a href="https://www.sharpcap.co.uk/sharpcap/downloads" target="_blank">SharpCap Pro</a>

Planetarium - Stellarium

Stellarium is a wonderful, free software that among many other features, helps you visualize what objects are up in the sky for your location. It is great for planning your targets days, weeks, and even years in advance and is just a joy to explore around. It can be <a href="https://youtu.be/v2gROUlPRhw" target="_blank">connected to NINA</a>
as well. 

<a href="https://stellarium.org" target="_blank">Stellarium</a>

## Remote Access

Who wants to sit outside in the cold all night, hunched over your laptop? I sure don't. Thankfully there are great options to connect to your imaging PC from another PC, phone, or tablet. Personally I think RDP is best, especially if you are on your own local network. If you need to connect to your imaging PC that is truly remote or you're away from your house, Chrome Remote Desktop is a lot more simple to set up and works great as well. 

### RDP - baked into Windows

Remote Desktop Protocol is incredibly efficient as it simply sends information about what needs to be updated and rendered on your screen. It is baked into certain versions of Windows. There are native apps to control RDP on Android, iPhone, and of course Windows.

Here is <a href="https://darkskies.space/mobile-remote-imaging/" target="_blank">a great article</a> on how to set things up and what additional hardware you may need. If you are at home, all you should need it for your imaging PC to be connected to your network. 

### Chrome Remote Desktop

Chrome Remote Desktop essentially streams a video of your screen. It is very simple to set up and use from anywhere. It can be controlled through your web browser or an app.

<a href="https://remotedesktop.google.com/access/" target="_blank">Chrome Remote Desktop</a>

## Weather

Not exactly software persay, but knowing what's going on with the weather is critical to planning your night of Astrophotography. 

### Astropheric

An excellent website and app which presents cloud forecasts as well as many other layers of relevant AP weather info. I have personally found it to be very accurate. The pro version (only 99¢/mo) lets you view multiple weather models at once. North America only currently. 

<a href="https://www.astrospheric.com/" target="_blank">Astropheric</a>

### Clear Outside

Ah the classic red bingo. Clear Outside presents the hourly forecast in an easy to interpret Green/Orange/Red grid. It's more accurate for some than others. 

<a href="https://clearoutside.com/" target="_blank">Clear Outside</a>

### Weather Underground

Personally I find WU's cloud forecast to be quite accurate. 

<a href="https://www.wunderground.com/" target="_blank">Wunderground</a>

### RAMMB GOES Viewer

There is often no better forecast than looking at what the weather is doing right now. This viewer uses the GOES satellites to show recent visual (or IR) cloud images even at night. Gives you a good heads up of what's headed your way.

<a href="https://www.rammb-slider.cira.colostate.edu/" target="_blank">GOES Viewer</a>

## Processing

### PixInsight

#### Plugins

GHS
EZ Suite
Starnet 2

### SiriL
### Deep Sky Stacker
### AutoStakert3

