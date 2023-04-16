# stayboogy_DellBrightnessKeys

## initial commit from multiple repos here: https://github.com/acidanthera

User's source would not build without a broken header and library setup they use on their personal machine to build BrightnessKeys.kext from, so I found all the necessary files in their git and patched together this repo.

I am working with this broken mess of a kext for OpenCore that uses ADB opcodes which are now obsolete, but has somehow broken brightness keys for Dell Hackintosh Laptops to where even with Function Keys on in BIOS where one has to press Fn+F1 to access F1 keypress and where Mute on F1 is the default keypress, one has to press Fn+S and Fn+B to decrease and increase brightness respectively.  

Even after setting F11 and F12 to Display Brightness Controls in Keyboard Shortcut Settings of MacOS Ventura, the Fn key must still be pressed to access what should be the standard function according the BIOS settings above.

My Goal in this is to get this kext working with 1) BIOS of Dell Laptop set to Function On, and the Brightness Down and Up keys work just like the media keys do in MacOS Ventura without having to press Fn key first, and 2) hardcode Brightness Down/Up to their actual keys instead of F14/F15 like the creator of said broken kext has, which still doesn't actually work as F14 would be "Insert" and F15 would "delete" but instead it requires Fn+S and Fn+B, and 3) learn some about creating kexts as DSDT patching is more complicated than it looks to get the desired results in modern Dell Laptops.

# 
