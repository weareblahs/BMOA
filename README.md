# BIOA: Batch Multimedia Overlay Adder
This script allows you to add transparent images on top of another media file (image / video). Uses FFMPEG to process images over files.

## Background story
~~Maybe you shouldn't read it and get into the next step~~
One time, when I was shopping at Shopee, then I think about: How they actually put the same watermark / overlay graphics on an image while it's time consuming?

## Before you use
Download / copy FFMPEG at the same directory as the script's location. If you didn't know how to download it, just double-click on `download_ffmpeg.bat` at the root directory of this script. TL;DR:
<details>
<summary>Uhh, how to download it manually?</summary>
1.  Download FFMPEG [here](https://www.gyan.dev/ffmpeg/builds/ffmpeg-git-essentials.7z) (Direct link).
<br>
2. Unzip it then copy ffmpeg.exe under the bin directory to the same directory with this script.
</details>
<details>
<summary>Got FFMPEG?</summary>
Just copy it to the same directory where this repo is located. That's all.
</details>
<details>
<summary>FFMPEG under PATH?</summary>
Proceed to the next step. You don't have to setup FFMPEG.
</details>

## Step 2: Create overlay image
Basically, create an image with **the same width and height as the image you're going to process**, and importantly, **make it transparent**. After editing it, export as PNG. Guides coming soon.

## Step 3: Modify configuration files
First, open the `config.ini` file for editing. Use whatever editor you want. Edit this line:
```
general_overlay_image=overlay.png
```
by changing `overlay.png` to the complete path of the file. 
(more easier: just rename it to "overlay.png" then put it at the same directory as the script's location)
### Finetuning FFMPEG settings? Let me explain first:
`quality`: Change quality properties for FFMPEG image encoding. If you're exporting JPEG, then I recommend you to not change the quality property, as the JPEG file ~~will look more JPEG than usual~~ will become "blocky".
`x` and `y`: Change the X-axis and Y-axis of the overlay file on the image.
`outformat`: Change output format of image file. See [here](https://www.ffmpeg.org/general.html#toc-Image-Formats) for file formats (if it's X for encoding then it supports that fileformat for exporting).
`custom_args` (under `ffmpeg_finetune_image_advanced`): Arguments before the output name. Advanced users only.
# To-do
[ ] Video support
