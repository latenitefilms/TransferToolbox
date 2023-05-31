# How To Use

### Introduction

Simply drag and drop your **Final Cut Pro (for Mac) library** into the drop zone:

![_Screenshot of Transfer Toolbox_](static/homepage.png)

You will be presented with a Open Panel to grant sandbox access to that library:

![_Screenshot of Transfer Toolbox_](static/grant-access.png)

After clicking **Grant Access**, you'll be presented with a success message:

![_Screenshot of Transfer Toolbox_](static/victory.png)

You'll now find a `.fcpproj` file in the same folder as your `.fcpbundle`:

![_Screenshot of Transfer Toolbox_](static/result-files.png)

You can now use [Airdrop](https://support.apple.com/en-au/HT203106#:~:text=Select%20AirDrop%20in%20the%20sidebar,recipient%20shown%20in%20the%20window.), [iCloud Drive](https://support.apple.com/en-au/guide/mac-help/mchle5a61431/mac) or other means (such as putting on an external hard drive) to move the project from your Mac to your iPad.

---

### Supported Media in Final Cut Pro for iPad

#### Video Formats

- Apple ProRes
- Apple ProRes RAW and Apple ProRes RAW HQ
- H.264
- HEVC
- MXF (Apple ProRes)

#### Audio Formats

- AAC
- AIFF
- BWF
- CAF
- MP3
- MP4
- WAV

#### Still-image Formats

- Apple ProRAW
- BMP
- GIF
- HEIF
- JPEG
- PNG
- PSD
- RAW
- TGA
- TIFF

You can also find this information on [Apple's website](https://support.apple.com/en-au/guide/final-cut-pro-ipad/dev3f1bb94c2/ipados).

---

### Tips & Gottchas

Some important things to keep in mind:

- Transfer Toolbox requires Final Cut Pro 10.6.6 or later.
- You should ensure your library only has a single event.
- Transfer Toolbox will warn you if it detects more than one event, but it still allows you to proceed.
- All project timecode should start at **00:00:00:00**.
- All Motion Content and Media should be contained within the Library (or on the [same external drive](https://transfertoolbox.io/how-to-use/#storing-media-externally)).
- Your Final Cut Pro (for Mac) timeline/project cannot have any **Stabilisation or Rolling Shutter** effects enabled. If you do, the iPad will just say "Import Failed".
- If you have **custom fonts** on the Mac Final Cut Pro library, you should manually install them on the iPad before importing the project.
- Not all Motion Templates will work on the iPad. For example, some Titles using the **Match Move Behaviour** don't appear correctly on Final Cut Pro (for iPad) - the positions are all wrong.
- **FxPlug4** effects (such as [BRAW Toolbox](https://brawtoolbox.io)) will not work at all on the iPad. Whilst Final Cut Pro (for iPad) does seem to have FxPlug4 Frameworks, there's currently no mechanism for third party to add FxPlug4 to iPad.
- Final Cut Pro (for iPad) will always **ignore proxy files** - it will always use the Original high-quality media files.
- **Soundtracks** will come across from iPad to Mac. However, they're not "normal" audio clips, and won't appear if you export a FCPXML.
- Some users have reported that when you AirDrop from Mac to iPad, it can take a few minutes for the project to appear in Final Cut Pro for iPad. We haven't been able to reproduce this on a 12.9inch iPad Pro, so it may be hardware dependant. Basically... be patient if using older devices.
- **Compound Clips** will come across correctly, however you cannot modify them in Final Cut Pro for iPad.
- **Multicam Clips** with more than 4 angles will come across correctly, however you still only have access to the first 4 angles in Final Cut Pro for iPad.

If you find any other issues/limitations, [please let us know](https://transfertoolbox.io/support/).

---

### Storing Media Externally

Interestingly, it is actually possible to "link" to media on an external hard drive.

However, even though Final Cut Pro (for iPad) will "link" to the external drive initially, and when you first start editing, you'll be editing off the external drive - in the background, Final Cut Pro will start copying everything across to the internal drive.

As far as we can tell, there's currently no way to stop Final Cut Pro from importing the footage to your iPad's internal drive.

This works slightly differently to DaVinci Resolve (for iPad) and LumaFusion, which both support "linking" to external drives without having a local/internal copy.

With that in mind, if you still want to "link" to your media initially, you'll need to create the Final Cut Pro library on macOS, and make sure you keep the media **external** to the library.

As long as both the generated Final Cut Pro (for iPad) project and media are on the same external hard drive, in the same location as they were on the Mac, everything will work.

The reason for this is that internally Final Cut Pro (for Mac) created document-scope security-scoped bookmarks to each media file, which Final Cut Pro (for iPad) can also use to get access to the files, even in a sandboxed environment.

After creating a new Final Cut Pro (for iPad) project using Transfer Toolbox, you may need to open the library back up on the Mac, to update all the bookmarks.

Simply right-click on the new Final Cut Pro (for iPad) project in Finder and select **Show Package Contents**.

![_Screenshot of Finder_](static/show-package-contents.png)

Within the package contents, two folders deep, you'll find the Final Cut Pro (for Mac) library that you can now open on your Mac.

![_Screenshot of Finder_](static/inside-project.png)

Once you open it, and allow Background Tasks to complete, you can then close it, as the document-scope security-scoped bookmarks should now be updated.

We will investigate automating this process in a future update.

You can then import Final Cut Pro (for iPad) libraries via the home screen:

![_Screenshot of Final Cut Pro (for iPad)_](static/import-ipad.jpeg)

Just select the project on your external drive:

![_Screenshot of Final Cut Pro (for iPad)_](static/external-ssd.jpeg)