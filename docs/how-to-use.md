# How To Use

## Introduction

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

## Tips & Gottchas

Some important things to keep in mind:

- Transfer Toolbox requires Final Cut Pro 10.6.6 or later.
- You should ensure your library only has a single event.
- Transfer Toolbox will warn you if it detects more than one event, but it still allows you to proceed.
- All project timecode should start at **00:00:00:00**.
- All Motion Content and Media should be contained within the Library (or on the [same external drive](https://transfertoolbox.io/how-to-use/#storing-media-externally)).
- If you have custom fonts on the Mac Final Cut Pro library, you should manually install them on the iPad before importing the project.
- Not all Motion Templates will work on the iPad. For example, some Titles using the Match Move behaviour don't appear correctly on Final Cut Pro (for iPad).
- FxPlug4 effects (such as [BRAW Toolbox](https://brawtoolbox.io)) will not work at all on the iPad.
- Final Cut Pro (for iPad) will always ignore proxy files - it will always use the Original high-quality media files.
- Soundtracks will come across from iPad to Mac. However, they're not "normal" audio clips, and won't appear if you export a FCPXML.

---

## Storing Media Externally

!!!
**NOTE:** As Final Cut Pro for iPad is very new - this is all very experimental. Explore with caution!
!!!

Surprisingly, it is actually possible to store media on an external hard drive.

You need to create the Final Cut Pro library on macOS, and make sure you keep the media **external** to the library.

As long as both the generated Final Cut Pro (for iPad) project and media are on the same external hard drive, in the same location as they were on the Mac, everything will work.

The reason for this is that internally Final Cut Pro (for Mac) created document-scope security-scoped bookmarks to each media file, which Final Cut Pro (for iPad) can also use to get access to the files, even in a sandboxed environment.

After creating a new Final Cut Pro (for iPad) project using Transfer Toolbox, you may need to open the library back up on the Mac, to update all the bookmarks.

Right-click on the new Final Cut Pro (for iPad) project in Finder and select **Show Package Contents**.

![_Screenshot of Finder_](static/show-package-contents.png)

Within the package contents, two folders deep, you'll find the Final Cut Pro (for Mac) library that you can now open on your Mac.

![_Screenshot of Finder_](static/inside-project.png)

Once you open it, and allow Background Tasks to complete, you can then close it, as the document-scope security-scoped bookmarks should now be updated.

We will investigate automating this process in a future update.

You can then import Final Cut Pro (for iPad) libraries via the home screen:

![_Screenshot of Final Cut Pro (for iPad)_](static/import-ipad.jpeg)

Just select the project on your external drive:

![_Screenshot of Final Cut Pro (for iPad)_](static/external-ssd.jpeg)