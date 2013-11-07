GLYPHICONS Sprite Generator (NOT for Bootstrap!!!)
=========================================
The GLYPHICONS Sprite Generator allows you to change the size and colors of the
Free or Pro versions of GLYPHICONS.

The generator was developed for a Bootstrap audience, but I really dislike Bootstrap's
css class names.  Therefore, I tweaked this with saner classes which lead to a smaller
stylesheet and will lead to a smaller html file.

Since you are not using Bootstrap, you will have to link back to [GLYPHICONS](http://glyphicons.com/)
if you use the free icon set.  No need for backlinks if you paid.

New CSS and PNG sprites are generated from the icon set.

Dependencies
------------
The only required non-standard-library package that is needed is the Python
Imaging Library. To install this simply run "easy_install pil" or
"pip install pil"

How to use sprite-generator.py
------------------------------

 1. Download the type of GLYPICONS distribution and extract the zip file
 2. Copy sprite-generator.py into the extracted glypicons_free or glyphicons pro folder
 3. Check to see if you want to change any of the constants at the top of the
    script (size, preview background, etc)
 4. Run sprite-generator.py, if everything worked property, sprite-generator.py will
    have generated the following files in the "sprites" directory:

    - glyphicons.css         CSS Overrides
    - glyphicons.html        Preview HTML
    - glyphicons.png         Black Icons
    - glyphicons-alt.png   White (or colorized) icons

 5. Open sprites/glyphicons.html in your browser (if you're on a Mac, it will try and do so itself)

How to use in your project
------------------------------------
1. Copy the glyphicons.png and glyphicons-alt.png to the project img directory.
2. Include the glyphicons.css file
3. Edit glyphicons.css, fixing the paths to the image files in the background-image directives.
4. Example icon <i class="icon address-book"></i>
5. Example alternate icon <i class="icon alt address-book"></i>
6. Example alternate-on-hover behavior <a class="hinvert"><i class="icon address-book"></i></a>

How to change the icon sizes or colors
--------------------------------------
In sprite-generator.py are three variables you can use to impact the generated
sprites: WHITE, PREVIEW_BACKGROUND and ICON_SIZE.

The WHITE variable controls the RGB values of the foreground of the icons. Change any of the
three values to any number between 0 and 255:

     # Make the icons red
     WHITE = (255, 0, 0)

The PREVIEW_BACKGROUND variable only impacts the glyphicons.html file and can be used to
tweak icon colors against different backgrounds. This is an RGB triplet without the
hash symbol (#).

     # Change the preview background to yellow
     PREVIEW_BACKGROUND = 'FF0'

The ICON_SIZE changes the dimensions of the icons in the sprites and in the CSS. This
should be two values representing the width and height:

    # Change to big icons!
    ICON_SIZE = 58,58

Using Glyphicons
----------------
Since you're here and if you plan on using this, you should support the designer
who made GLYPHICONS and pay the modest license fee for the Pro version. Not only
do you get more icons out of it, but whatever you're using this for will get
higher quality icons out of it. If you use the Pro icons as a source, the higher
resolution icons will be used.
