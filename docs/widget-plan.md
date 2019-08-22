# Plans Gantt Widget

The *Plans Gantt* widget is listed under  *Plans* tag. It shows Polarion Plans as items on the Gantt chartt.

!!! info
    Currently, it is possible to have only one Work Item Gantt widget on a page.

## Widget Parameters 


* **`Plans`** - a standard data set parameter. Select what plans you want to see on your Gantt chart.

* **`Sort by`** -  the sort criteria to sort the plans.

* **`Load Children`** - define how many levels of child plans should be traversed and added to the list in addition to the items from Plans` date set parameter. 
    
    Zero (0) means that no additional items are shown.
    
* **`Show Unplanned`** - click on `no` to hide all the plans that do not have the start date set. 

    If you keep it set to `yes`, such tasks will be in the list, scheduled for 'Today', and marked by *gray* color. 

* **`Scale ( D || W || M )`** -  configures the scale of the Gantt timeline. Values are: 
    + 'D' - day
    + 'W' - week
    + 'M' - Month


## Advanced Parameters

* **`Maximize View`** -  configure if the widget should expand its content over the full working area. See [Setup](../setup/).

* **`Drag Children`** -  configure if you want the child items to be rescheduled when dragging their parent's item.

* **`Max Items`** -  (Integer) limits the maximum number of plans loaded into the Gantt view.

* **`Gantt Config Script`** - a optional javascript snippet executed on the client, usually used to add additional Gantt configuration options.

	Example: [How to set the Gantt time range?](https://nextedy.freshdesk.com/support/solutions/articles/48000063422-how-to-set-the-gantt-time-range-).

* **`Item Script`** - a server side javascript snippet executed on the server to decorate the task based on the work item properties. 

	Example: [How to change text on right?](https://nextedy.freshdesk.com/support/solutions/articles/48000064501-how-to-change-text-on-right-)


<!-- Start of HubSpot Embed Code -->
<script type="text/javascript" id="hs-script-loader" async defer src="//js.hs-scripts.com/6265870.js"></script>
<!-- End of HubSpot Embed Code -->
