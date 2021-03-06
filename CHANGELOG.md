# ChangeLog
Change log for jQuery-Mapael

## 2.0.0 - Not released yet

- Feature : Added 'showElementsInRange' event to filter the elements to show on the map depending on values intervals ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/a634d2d731a070b0369f4d7cd55109c05c8ac579))
- Refactoring : Move default options inside prototype to allow overriding ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/c17c0de61a90581e1a88aace64fd2b97fbcb1bb1))
- Refactoring : Refactored internal structure of the plugin (Indigo744)
- Misc : Added many new code examples (Indigo744)
- Misc : Added unit tests (Indigo744)
- Refactoring : New update event signature ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/3ad903b8e38bcc7dd5e3d368f07c1d379a0e19d4))
- Bugfix : Fixed leaking when removing plots/links ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/2c9aa9bdbec554286c3f69d8b194bac3a23b5602))
- Feature : tooltip.content accept function ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/489cad8f93fc1d328a6e76d5d0fd824af6eec00d))
- Bugfix : handleClickOnLegendElem take into account other legends ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/23419ccbc522b497831478a2f827819460e1b6fd))
- Bugfix : Set default size when no size is set on slices ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/2f4fa5c6dddacf52cb1308ae261e94239791fceb))
- Bugfix : Fixed target for zoom related events 'mousewheel', 'touchstart' and 'touchmove' ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/b3f8ab04ed76c13aa0c3dc97dff582e612ebb503))
- Feature : Delete all plots/links in 'update' event ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/822a1caa322c5c0e422447e204b7624c5e3e1885))
- Refactoring : Set legend slice max value inclusive ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/68f95555858bfc9e3afcea96d95d00c3d573e34b))
- Bugfix : hide/show elements only on current map ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/dc1994c0c92e14e6a1356dfb514b051acbdc7067))
- Feature : Allow to update legend in the update event ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/191149446d0fe3cb34910ef44e430ed960b6b08e))
- Feature : Added AMD and CommonJS compatibility to mapael and mapel maps ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/56f941f5ce03254a4cb65963860a9868a6813da9))
- Feature : Added animDuration option to 'zoom' event and set it to 0 by default for initial zoom ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/bbcecae471e31c1b37aa62d7ed83842550837ae6))
- Refactoring : Removed map.tooltip.target option ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/f1e8758b91504f399392e4af390ed020ad935bdf))
- Feature : Added tooltip.overflow.right and tooltip.overflow.bottom options to allow tooltip overflow from the container ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/476fbbad7a23f622bc49e80f6be47413f585cf31))
- Bugfix : Fixed raphael.safari() call with laster version of Raphael.js ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/f458ea8af781a57d6d3b77e1dd6b52bbfb8332ed))
- Bugfix : Fixed legend display when no title is defined ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/3d8200706548a9bbd0710d3dd6829d767c7d2ffc))
- Refactoring : Tooltip position is computed as absolute instead of fixed ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/7907701a46ae7a270d68a7f6ac9c9be96d95f8df))
- Bugfix : Fixed IE8 js error on map update ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/44798289cc28ff5150e3f94dbe11c02b5d0bc33c))
- Feature : Added legend.(area|plot).hideElemsOnClick.animDuration option ([Indigo744](https://github.com/neveldo/jQuery-Mapael/commit/52eef6549b70ea09d982ccfc78a5b8f6ea944d8a))
- Bugfix : Fixed current zoomX and zommY values set in container’ data. ([neveldo](https://github.com/neveldo/jQuery-Mapael/commit/438858423f5eb816124d9171806030f6be1261a7))

## 1.1.0 - 31 August 2015
Minor version release.

### New features
- Added support for animated zoom through the new option map.zoom.animDuration (200 by default, set to 0 in order to disable it). The option map.zoom.animEasing allows to set the easing function to animate the zoom action
- Panning is now allowed through touch event (it can be disabled through the option map.zoom.touch)
- Zooming is now allowed through pinch touch event (it can also be disabled through the option map.zoom.touch)
- In addition to 'circle', 'square' and 'image' plotted point types, the new 'svg' type allows to add SVG paths on the map
- Links can now be updated through the 'update' event : they can be edited or deleted and new links can be added to the map
- New legend.exclusive option allows the user to activate only one item from the legend at a time
- New ‘clicked’ option in order to initialize the legend item in the 'clicked' state on the map load
- Added hook 'beforeInit' hook that is called right after the initialization of the areas
- New map.tooltip.target option allows to specify a container where to append the tooltip div
- The new option 'cssClass' allows to set additional CSS class(es) the tooltip for a specific area or a plotted point
- Added events afterZoom and ‘afterPanning’

### Bugfixes & other
- Upgraded Raphael.js dependency to v2.1.4
- Fixed horizontal legend display with squares
- Fixed tooltip position

## 1.0.1 - 17 May 2015
Bugfix version release.
- Fixed undeclared variable in drawLegend function. IE >10 wasn't able to display the map legend.

## 1.0.0 - 4 January 2015
Major version release with breaking change.
### New features
- You can now add curved links between two cities, between two points defined by a latitude and a longitude, or between two points defined by a x and y coordinates
- jQuery Mapael now handles multiple criteria legends. Each point or each area can be associated with one or several values
- You can use non-vector images in order to plot locations on your map.Moreover, non-vector images can be used in the legends
- The legend can be displayed horizontally or vertically
- The jQuery mousewheel is now fully integrated with jQuery mapael and zoom on mousewheel features have been improved. Zoom is now focused on the cursor position
- The target of each link on the map can be specified
- You can define each slice of a legend with a single value or with a minimum and a maximum values
- You can display a map with an initial zoom level that is focused on a particular location
- Dependencies are now included through Bower packages manager.
- Mapael allows users to set specific attributes for the elements in the legend independently from the attributes for the matching elements on the map
- A new tutorial that explain how to create a map for jQuery Mapael is now available. It comes with some useful online tools.

### Breaking changes 
Here are the changes that are not compatible with the 0.7.1:
- If you have overloaded $.fn.mapael.defaultOptions, note that the default Mapael options (previously stored in $.fn.mapael.defaultOptions) are now stored in two different variables : $.fn.mapael.defaultOptions and $.fn.mapael.legendDefaultOptions . The last one is specific to legends options.
- Legends 'display' option is now set to true by default instead of false

## 0.7.1 - 23 January 2014
Bugfix version release:
- Fixed legend colorisation with zero values in slices definition
- Don't animate areas and plots in the legend on mouse hover
- afterUpdate call : fixed undefined opt

## 0.7.0 - 17 November 2013
### Improvements
- Improved zooming feature. You can now trigger a 'zoom' event on the container (required parameter : level, optional parameters : x, y in order to zoom on a specific area). The current zoom level is now stored as data. Example of use : http://jsfiddle.net/neveldo/RahvT/
- Added two new hooks in order to allow custom processing on map initialization and map update ('update' event) : afterInit and afterUpdate. Here is an example with the afterInit() hook : http://jsfiddle.net/neveldo/8Ke69/
- Added labelAttrsHover option for the plots and areas legend that allows to customize the attributes of the labels in the legend on mouse hover.
- prevent the tooltip to overflow from the container
- 'update' event' now allows to update attrsHover for plots and area (bugfix)

## 0.6.0 - **29 September 2013**

### Improvements
- Added missing Michigan state on the USA map
- New map of France with equirectangular projection for better cities location
- Upgraded to version 2.1.2 of Raphael.js
- Truely hide the elements when user clicks on the legend and hideElems.OnClick.opacity is set to 0
- Squares and circles in the legend take account the scale of the map in order to draw them at the same scale
- Newattribute 'data-id' added to plots and areas's nodes
- New option 'display' that allows to display or hide a specific element from the legend
- Improved event handling (with the new option 'eventHandlers'). You can now attach handlers to all events from jQuery.
- Improved 'update' event that now allows to add or delete plot from the map, update text attributes (content, position, ...) and the contents of the tooltips
- New option text.margin that allows to customize the margin between the plot and its associated label
- Miscellaneous bug fixes

### Incompatible changes with 0.5.1
- Event handlers for plots and areas (previously set by options 'onclick', 'onmouseover' and 'onmouseout') now have to be defined with the option 'eventHandlers'. It contains the list of handlers (function(e, id, mapElem, textElem) { ...}) that will be called when events occur on elements. The key must match the event name (example : 'click', 'dblclick', ...). See documentation and examples for more information.
- Parameters for the update event are now the followings : updatedOptions, newPlots, deletedPlots, and opt. Example : $(".container").trigger('update', [updatedOptions, newPlots, deletedPlots, opt]);. See documentation and examples for more information.
- The options for the texts (previously text, textAttrs, textHoverAttrs and textPosition) are now the followings : text.content, text.attrs, text.attrsHover and text.position. See documentation and examples for more information.

## 0.5.1 - 24 August 2013
Fourth version

## 0.4.0 - 29 July 2013
Third version

## 0.3.0 - 15 July 2013
Second version

## 0.2.2 - 2 July 2013
First version
