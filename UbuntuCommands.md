---------------
UBUNTU
-------------

1. I've recently come to like setsid. It starts off looking like you're just running something from the terminal but you can disconnect (close the terminal) and it just keeps going.

setsid gnome-calculator

2. avoid overheating

sudo tlp start

3. Kill unresponsive app

xkill

4. Ubuntu open terminal in current folder with shortcut

RIGHT-CLICK KEY + E
"Shift + F10" and then + "E"

5. Fix resolution
xrandr -s 0

6. change title of pdf
exiftool -Title="This is the Title" -Author="Happy Man" -Subject="PDF Metadata" drawing.pdf


--------------
CUSTOM
-----------

1. xkill

ctrl+alt+shift+delete

2. custom terminal alerts

notify-send 'Updates Complete' 'Your system updated successfully!' -u normal -t 7500 -i checkbox-checked-symbolic

alias lmk="..."

3. open project folders in vscode

	code /home/dheeraj/E\ drive/app-ui
	Ctrl + R ->  arya		
	Ctrl + D ->  admin-ui	
	Ctrl + P ->  app-ui

4. GMAIL

	Alt + G -> /opt/google/chrome/google-chrome "--profile-directory=Profile 1" --app-id=pjkljhegncpnkpknbcohdijeoejaedia

5. Yakyak

	Alt + Y
---------------
IMAGEMAGICK
---------------

1. Color invert
convert input.png -channel RGB -negate output.png

2. black and white

convert source.jpg -colorspace Gray destination.jpg (true grayscale only)
convert source.jpg -monochrome destination.jpg (true black and white)
convert source.jpg -separate destination.jpg (separate into gray channels)
If you don't care about losing the original file: mogrify -colorspace Gray file'.

3. invert to BW
mogrify -channel RGB -negate input3.jpg && mogrify -monochrome input3.jpg

