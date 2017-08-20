# BatoCRT, an EmulationStation theme for Recalbox/Batocera/RetroPie
A simple EmulationStation theme for Recalbox/Batocera/RetroPie. Based on the CRT theme by Anthony that was originally based on the Carbon theme by Eric Hettervik; then tweaked to work with Recalbox/Batocera.

---

### Updates

*20/08/2017*
- Moved things around in `_inc/templates` to allow this theme to support both Recalbox/Batocera and RetroPie.
 - Templates are split in to `_inc/templates/recalbox` and `_inc/templates/retropie`. See the [customizing layout section](#customizing-layout) below.
- Added a 16x9-no_desc.xml template for RetroPie.
- Adjusted `retropie/theme.xml` to disable aditional md_lbl elements that would appear in 16x9-no_desc.xml template.

*07/08/2017*
- Initial fork and edit of CRT Theme.
- Removed unsupport ES theme items such as video/z-index/etc as they do not work in Recalbox/Batocera.
- Add support for favorite, fba_libretro & pcenginecd.
- Created templates with and without the CRT bezel for artwork, default template is 16x9 with no CRT bezel.

---

## Preview
TBC

## Details

- Has support for system, basic, detailed and video views
- Displays the following metadata on detailed view:
 - rating
 - description
 - number of players
 - genre
 - publish date
 - last played
- 16x9 layouts currently tested on 1080p resolutions
- 4x3 and 16x10 layouts currently untested

## How to use

### Installation
Copy the theme directory to `\\RECALBOX\share\system\.emulationstation\themes\` and then select the theme in the UI settings menu.

### Customizing Layout
In `theme.xml` you can uncomment the layout template you wish to use. The default layout is 16x9 with no bezel.

~~~
<theme>
   <formatVersion>4</formatVersion>
   <!--
   Uncomment the template vesion below that you want to use...
   -->
   <!-- This Section for Recalbox/Batocera templates... -->
   <!-- <include>./_inc/templates/recalbox/4x3.xml</include> -->
   <!-- <include>./_inc/templates/recalbox/16x9-no_desc.xml</include> -->
   <!-- <include>./_inc/templates/recalbox/16x10.xml</include> -->
   <!-- <include>./_inc/templates/recalbox/4x3-bezel.xml</include> -->
   <!-- <include>./_inc/templates/recalbox/16x9-bezel.xml</include> -->
   <!-- <include>./_inc/templates/recalbox/16x10-bezel.xml</include> -->


   <!-- This Section for RetroPie templates... -->
   <!-- <include>./_inc/templates/retropie/4x3.xml</include> -->
   <!-- <include>./_inc/templates/retropie/16x9.xml</include> -->
   <include>./_inc/templates/retropie/16x9-no_desc.xml</include>
   <!-- <include>./_inc/templates/retropie/16x10.xml</include> -->
</theme>
~~~

## Acknowledgments

- Based on the EmulationStation CRT theme by Anthony (see: https://github.com/anthonycaccese/es-theme-crt)
- All Logo graphics are from the default Carbon theme made by Eric Hettervik (see: https://github.com/RetroPie/es-theme-carbon/)
- Theme tutorial written by mattrixk was a huge help in learning how to build this (see: https://github.com/RetroPie/RetroPie-Setup/wiki/Creating-Your-Own-EmulationStation-Theme)
