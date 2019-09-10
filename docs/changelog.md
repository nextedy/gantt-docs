# Release Notes

## Changelog

### 1.7 <small>- Sep 9, 2019 </small>
* New property **Advanced > Show Today Marker** - if true, a today marker is added to the gantt.
* New property **Advanced > Start Field is End Date (calculate from end)** - this one is tricky, if it is true, than the **Start Field** will be actually treated as end date. What? Simply read more at [How to configure the gantt to compute the start date from end/due date?]()
* `widgetContext` object ([Class Javadoc](https://almdemo.polarion.com/polarion/sdk/doc/javadoc-rendering/com/polarion/alm/shared/api/model/rp/widget/RichPageWidgetRenderingContext.html)) has been added to **Markers Script**. It can be used to e.g. access the project context via `widgetContext.getDisplayedScope().projectId()`
* **Progress coloring added** - the gantt will now mark the tasks that end in the past and are unresolved as red, and those with planned progress date in a past as orange. If you do not like this behaviour, you can turn it off by adding `gantt.config.show_progress_colors=false;` into `Advanced > Gantt Config Script`. We do not want to add a widget property to control this behaviour to restrict number of properties.

![gantt-progress-colors](img/gantt-progress-colors.png)


### 1.6.2 <small>- August 28, 2019 </small>
* Fix for ugly bug that custom field of type Date-Time was not supported for Start/End dates. We still recomend to use Date-only but some customers prefere Date-Time.

### 1.6.1 <small>- August 27, 2019 </small>

* Support for velocity scripting in *Advanced > Gantt Script* parameter, see use case here: [How to set the Gantt time range?](https://nextedy.freshdesk.com/support/solutions/articles/48000063422-how-to-set-the-gantt-time-range-)

### 1.6.0 <small>- August 23, 2019 </small>

* Support for Markers Script, see [How to add Markers via Marker Script?](https://nextedy.freshdesk.com/solution/articles/48000862790-how-to-add-markers-via-marker-script)
* Regular bug-fixing
* Update of documementation (split of widget documentation pages for Work Items and Plans Gantt)


### 1.5.0 <small>- July 1, 2019</small>

* Big release with many customer enhancements and with addition of *Plans Gantt Widget* (added for free) justifies the big shift on version number.
* Support for duration fields in DurationTime format (converts to days only)
* Compare actual vs planned (requires Task Script to configure how to load the original schedule)

!!! warning
    Due to major refactoring (as we were adding support for Plans data type), the widget needs to be reconfigured when you update from 1.0 to 1.5. This shall not happen in the future versions. This was agreed upfront with paying customers.
    

![Gantt-menu](img/gantt-versioning.gif)


### 1.0.3 <small>- May 29, 2019</small>
* Action menu added
* Refresh action to reload the Gantt
* Drag children control - add an option to turn on/off drag children instantly on Gantt, the widget property  holds the default
* Today Marker - add marker for today + scroll to today
* Set Scale - add an option to set the timeline scale instantly on Gantt, the widget property would hold the default.

![Gantt-menu](img/gantt-menu.png)


### 1.0.2 <small>- May 28, 2019 17:20</small>
* Documentation improvements
* Script support added to decorate a task based on work item properties, see Widget > Task Script
* Infinite loop on parent links (should not happen in Polarion) does not cause gantt to fail (but data do not load).
* Project style support (via Task Script)
* License at polarion/polarion/gantt-lic.json


### 1.0.1 <small>- May 15, 2019</small>

* Published on extensions.polarion.com
* New Work Items Gantt widget icon.
* Widget tags configured -  "Work Items", "Charts" 
* `gantt.config.round-dnd-dates`  reflected when dragging children
    
### 1.0.0 <small>- May 5, 2019</small>
*  After couple of months of development and use in several customer projects we officially release the public version 1.0.0.

## Roadmap / TODO
	
* **Markers** - support for release/milestone markers (timepoints, plans, ...)
	* It is covered now since 1.6 with `Advanced > Markers Script`, but we are still considering a native support
* **Readonly** - add widget property to mark Gantt read-only
* **Start/End Dates** - add direct support for Start/End dates. 
	* Currently possible with scripting: [How to set the Gantt time range?](https://nextedy.freshdesk.com/support/solutions/articles/48000063422-how-to-set-the-gantt-time-range-), we are considering adding a dedicated parameters
* **Drag Project** - support for moving tass of type 'project'
* **Server Side Scripted Tooltip** - add widget property - a script - to hold a generation of tooltip on the server side ...
	* It is possible using a script since 1.0.2 with `Task Script`
* **Item Colors based on Type** - make it possible to color the tasks based on item type.
	* It is possible using a script since 1.0.2 with `Task Script`
* **Working Time** - derived from the Polarion calendar.

## Known Issues
* When you collapse a left side Polarion navigator, the empty place appears on the right (collapse/drag fixes it)
