# INSTAGLYPH GENERATION

## Usage

FontCustom generates icons from svg files. 
Drop new svgs correctly named, regenerate the icons and push your changes.

The svgs are in folder `/svg` and generated fonts in `/fonts`

A css file is generated in `/css`. Icon classes follow the svg filename such that the icon `/svg/gear.svg` is usable as `.ig-gear`

## Dependencies

[FontCustom](http://fontcustom.com), [XQuartz](http://xquartz.macosforge.org/landing/) must be installed first.

Then:

  Old way

    brew install fontforge --with-python
    brew install eot-utils
    gem install fontcustom

  With latest version of brew

    brew tap bramstein/webfonttools
    brew install woff2 sfnt2woff eot-utils
    brew install --cask fontforge (or for old Mac OS: "brew cask install fontforge")
    sudo gem install fontcustom

  Be sure that in your path /etc/paths you have

  /usr/local/lib/ruby/gems/2.6.0/bin
  /Applications/FontForge.app/Contents/Resources/opt/local/bin

## Tips

* `“FontForge” cannot be opened because the developer cannot be verified.`: allow the App "FontForge" from System Preferences panel "Security"

## Steps to add an icon without pain

In icons:
1) search an svg for the new icon from web (for example https://www.materialui.co/icons / https://materialdesignicons.com / https://material-ui.com/components/material-icons) or Instaply designer
2) copy/paste the svg text into a new file .svg file with future css name into directory ./svg
3) run the script sh gen-icons.sh
4) open instaply-preview.html and check rendering is ok
5) commit & push everything into a branch / create PR / review / merge it
6) generate new tag in github

Then in old webapp:
1) point to new tag & refresh this package install
2) update in some .jade and .css to use the new icon
