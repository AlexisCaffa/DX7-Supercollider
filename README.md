# DX7-Supercollider
My accurate Yamaha DX-7 clone. Programmed in Supercollider.

This is a super-exact clone of DX7 in SC environment. This project started with my internship at the STEIM during last year,, I was able to get my hands on an original DX7 synth and eventually found out that this instrument has this mystic / marvelous sound.  So I started fiddling with it and made some experiments with Supercollider. After a while, it became an obsession to play with it and started to copy parts of its synth mechanism just to flex my DSP muscles. Sooner, I found myself in this huge project to clone the entire thing. After 2-3 months of implementing process and lots of sleepless nights. I was able to clone the entire DX7 engine with very high accurate results. Other than the DX7’s vintage sound hiss, it is hard to distinguish between the clone and the original one on the same presets. For my own use, I collected some 16384 (2^14) DX7 sysex bank presets from the internet and converted it to some integer sequences to read it from Supercollider. I am also combining this clone with this 16384 preset package. Currently, I am using it with my sequencers to modulate its parameters but for everyone's ease of use, I implemented a very basic function call. Which calls notes with this format: [Midi note, velocity, preset number]. Additional documentation is in the file. It is very easy to run but one requirement is to put my own collected DX7 presets files in the same directory as the DX7.scd patch and the other requirement is to have SC3plugins because I implemented it with FM7.ar Ugen. For the current version, it is not possible to put your own DX7 patches or modulate its parameters (I will add them in the future). But I think this synth has enough interesting presets and sounds to find some use in the different projects. 
You can download the zip of DX7.scd and preset file from this link: egegonul.com/dx7.zip I also added it to sccode.org. Have fun!

Running instructions:

You don't need to open DX7.afx file. It just needs to be in the same directory as DX7.scd. Just open DX7.scd in Supercollider and run the big chunk of code starting from the line 35 and it's ready to use. Then run the mainCaller functions for new notes and to close notes send zero velocity from the mainCaller functions. The only requirement is to install SC3-Plugins Ugen library because I use FM7.ar Ugen at the heart of all operation.

Here is a sound example which calls a random preset for each new node:

https://soundcloud.com/ewbta/dx-7-sc-clone-demo-2

