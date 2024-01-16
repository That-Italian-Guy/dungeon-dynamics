---
title: "Create Roofs in Dungeon Alchemist (for Foundry VTT)"
date: 2024-01-16
excerpt: How to create and edit roofs with Dungeon Alchemist and a Photo editing software.
toc: true
header:
  teaser: /assets/images/video-blogs/automate_complex.webp
categories: 
  - video blog
tags:
  - vtt
  - foundry
  - dungeon alchemist
  - tutorial
---

{% include video id="MRMVdKkGPN4" provider="youtube" %}

{% capture notice-text %}
All the files for this video can be found here:
- [Images](https://imgur.com/a/zx47FnK)
- [JSON file](https://pastebin.com/Y981BZhJ)
- [Full Prefab creation guide](https://youtu.be/k66biGIyED4)
- [Advanced Prefabs #1](https://youtu.be/4e9xosxoBu0)
- [Advanced Prefabs #2](https://www.youtube.com/watch?v=ewHXyRNDnxo)
- Prefab credit to [Baileywiki](https://www.youtube.com/channel/UCg6hyng0ObRKLwfz3QIhcog)https://www.youtube.com/channel/UCg6hyng0ObRKLwfz3QIhcog
- Music: [Tabletop Audio](https://tabletopaudio.com/)
{% endcapture %}
<div class="notice--info">
  {{ notice-text | markdownify }}
</div>

## Text Version
Dungeon Alchemist doesn't currently support levels and, because of that, it doesn't have native roof tiles. So we are going to make our own with these simple steps.
# Create the base image in Dungeon Alchemist
+ Create a 1x1 Castle Hallway on a blank map.
+ Click on Walls > Remove Walls and remove all 4 wall from the Castle Hallway "room".
+ Click on the Rooms tool > Edit Room > Select our single tile and click Edit Room Shape.
+ Add as many tiles as you want your generic roof to be wide and tall as. We are doing a 9x6 roof in the example.
  + Make sure you are using the same pixel size for the DA tiles and the Foundry grid squares to keep things consistent!
  + Make sure to disable AI generation before resizing the room. Alternatively, remove the items placed by the AI in the Castle Hallway "room".

{% include figure image_path="/assets/images/video-blogs/da_roofs_01.webp" caption="This is what your current "room" should look like." %}

+ Switch to the Floor Tiles menu. We are going to use some visual trickery to simulate a 3d roof. Dungeon Alchemist comes with a lot of repeated tiles that are brighter/darker variations of the same pattern.
+ In this example, we are going to replace the tiles in the upper and lower halves with "City pavers dark green" and "City pavers light green" resspectively.

{% include figure image_path="/assets/images/video-blogs/da_roofs_02.webp" caption="The "room" is now a roof covered in shingles!" %}

+ Export the "map" with Ortographic (top down) Perspective and with an Image Quality matching the pixel size of your Foundry grid squares. Set the grid to Off.
## Photo Editing steps
+ Open the image in your favorite photo editor.
+ We have exported the image at 150 pixels per tile, so with a 9x6 size, our roof is precisely 1350x900 pixels in size.
+ We are going to resize the canvas so that it is exaclty the same size of our roof. This will crop out the background and leave the "roof" by itself.
+ It is nice to have the roof overextend over a building by a little bit. We are going to increase the canvas size to add some empty space along the border of our image. Half a square is a good measure so, in our case, we have increased the canvas size by 150 pixels to 1450x1050.
+ Double click our "Background" layer in the "Layers" sidebar and turn it into a Level.
+ Select the Magic Wand tool, click on the white space around the roof and press Delete.

{% include figure image_path="/assets/images/video-blogs/da_roofs_03.webp" caption="Our roof with an empty margin around." %}

### Optional: better looking roofs.
These steps are not fundamental, but they'll improve the overall look of our roof.
+ Turn on the Grid and set it to 25 pixels. In Photoshop, this is under Edit > Preferences > Guides, Grid and Slices. Press _Crtl+,_ to visualize the Grid.
 + Alternatively, you can eyeball it. Roofs are not always that precise anyway!
+ Select the Polygonal Lazo tool and remove two triangles on each side of the roof. The size of these triangles will make the roof look more or less steep.

{% include figure image_path="/assets/images/video-blogs/da_roofs_04.webp" caption="A steeper roof keeps the snow at bay." %}

+ If green roofs are not your thing, clikc the Image menu > Adjustments > Hue/Saturation. Play around with the Hue value until you get a color your like.

{% include figure image_path="/assets/images/video-blogs/da_roofs_05.webp" caption="We opted for red/maroon shingles. Classic!" %}

+ Save your image in a format that supports transparency, like .png or .webp.
+ It is a good idea to save the roof twice: once horizontal, once vertical (you can rotate the image and save it again). This is cause rotating tiles in Foundry is a bit of a headache sometimes.

{% capture notice-text2 %}
**I want even better looking roofs!**
The video has a few additional optional steps to add more decorative elements to the roof, including a chimney, leveraging assets from Dungeon Alchemist.
{% endcapture %}
<div class="notice--info">
  {{ notice-text2 | markdownify }}
</div>

## Foundry usage
There was a tutorial here once, but roofs are now natively supported by Foundry, so you don't need Level/Better Roofs anymore. Simply place your roof on top of the building it was designed for and have fun!

{% include figure image_path="/assets/images/video-blogs/da_roofs_06.webp" caption="What our roof looks like in Foundry from outside and inside." %}
