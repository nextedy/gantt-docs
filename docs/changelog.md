# Release Notes


## Changelog

!!! info
    The latest plugin distribution is available [here](https://nextedy.github.io/gantt-docs/download/work_items_gantt.zip)
    
    For those who read this documentation embedded in Polarion: you can check the online version for up-to-date changelog:
    <https://nextedy.github.io/gantt-docs/changelog/>

### 1.0.2 <small>_ May 28, 2019</small>
* Documentation improvements
* Script support added to decorate a task based on work item properties, see Widget > Task Script
* Infinite loop on parent links (should not happen in Polarion) does not cause gantt to fail (but data do not load).
* Project style support (via Task Script)
* License at polarion/polarion/gantt-lic.json


### 1.0.1 <small>_ May 15, 2019</small>

* Published on extensions.polarion.com
* New Work Items Gantt widget icon.
* Widget tags configured -  "Work Items", "Charts" 
* `gantt.config.round_dnd_dates`  reflected when dragging children
    
### 1.0.0 <small>_ May 5, 2019</small>
*  After couple of months of development and use in several customer projects we officially release the public version 1.0.0.

## TODO

* **Refresh** - refresh action to reload the Gantt
* **Drag children control** - add an option to turn on/off drag children instantly on Gantt, the widget property would hold the default
* **Today** - add marker for today + scroll to today
* **Readonly** - add widget property to mark Gantt read-only
* **Server Side Scripted Tooltip** - add widget property - a script - to hold a generation of tooltip on the server side ...
	* Partially possibly in 1.0.2 with `Task Script`
* **Item Colors based on Type** - make it possible to color the tasks based on item type.
	* Partially possibly in 1.0.2 with `Task Script`
* **Set Scale control** - add an option to set the timeline scale instantly on Gantt, the widget property would hold the default.

## Known Issues
* When you collapse a left side Polarion navigator, the empty place appears on the right (collapse/drag fixes it)


28-May-2019 17:20

