# CUSTOM ICONS GENERATION

## Usage

FontCustom generates icons from svg files. 
Drop new svgs correctly named, regenerate the icons and push your changes.

The svgs are in folder `/svg` and generated fonts and web assets in `/fontcustom`

A css file is generated as well where icon classes follow the svg filename such that the icon `/svg/gear.svg` is usable as `.icon-gear`



## Dependencies

To install [FontCustom](http://fontcustom.com):

[XQuartz](http://xquartz.macosforge.org/landing/) must be installed first.

then:

	brew install fontforge --with-python
	brew install eot-utils
	gem install fontcustom
	

## Regenerate

	. gen-icons.sh




