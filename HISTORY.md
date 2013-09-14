## 0.6.0 (2013-09-14)

* First pass to update all themes to bootswatch version 3.0
* Included variables.less for default theme
* Removed spruce and superhero
* Updated Rakefile to point to bootswatch3 and CONVERSION.md for bootswatch3

## 0.5.0 (2013-05-21)

* Update all themes to current bootswatch versions (2.3.2)
* Add Flatly theme
* Add script for determining variables that need to be rearranged
* Add list of conversions to do manually (CONVERSION.md)

## 0.4.0 (2013-02-22)

* Update all themes to current bootswatch versions (2.3.0)

## 0.3.2 (2013-01-23)

* Escape complex arguments to box-shadow in Simplex (reported @murtra)
* Make glyphicon links rails-friendly by default (reported @nysalor)

## 0.3.1 (2013-01-14)

* Add !default to all bootswatch variables, making them overridable

## 0.3.0 (2013-01-13)

* Add a converter script for most of the repetitive less/sass conversion work
* Add bootswatch project as a submodule
* Add a rake task that auto-converts less files from submodule into scss
* Convert all latest bootswatches to scss
* Stop using percentage -> percentile conversion, it seems to only break things
