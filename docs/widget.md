# Widget

You will find widget under the "workitems" tag:

![Gantt](img/gantt-widget-add.png)

!!! info
	Currently it is possible to have only one Work Item Gantt widget on a page.

## Widget Parameters 



* `Work Items` - a standard data set parameter, where you define what are work items you want to see on your gantt.

* `Parent Role` - Select what Work Item link roles should be used to detect the parent-child relationships. If empty, no hierarchy is shown.

* `Dependency Role` - Select what Work Item link roles should be used to detect the Depends-on relationships. If empty, no dependencies will be shown. If you select multiple link roles, the first role is used when creating new links.

* `Load Children` - define how many levels of child items should be traversed and added to the list in addition to the items from 'Work Items' attributes. Zero (0) means that no additional items are shown.

* `Show Unplanned` - click on 'no' to hide all the work items that do not have the start field set. If you keep it set to 'yes', such tasks will be in the list, scheduled for 'Today', marked by gray color. 

* `Drag Children` - To allow dragging children when the user is dragging their parent's task, set this property to 'yes'


### Advanced

* `Maximize View` -  configure if the widget should expand the over the full working area. See [Setup](../setup/).

* `Start Field` -  the name of the custom field, that holds when the work item starts. It can be any of: Date, Date-Time or String. DIf such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use a Date (Only) custom field.

* `Duration Field` -  the name of the custom field, that holds when the work item duration as number of days. It can be any of: Integer or String.  If such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use an Integer custom field.

* `Progress Field` - the name of the custom field, that holds when the work item progress as float (if you multiple by 100 you get % of completion). It can be any of: Float or String.  If such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use a Float custom field.

* `Sort by` -  the sort criteria to sort the top level work items.

* `Scale ( D || W || M )` -  configures the scale of the timeline.   Values are: 
    + 'D' - day
    + 'W' - week
    + 'M' - Month

* `Max Items` -  (Integer) limmits the maximum number of work items loaded into the gantt view.

### Additional Script

You can add additional DHTMLX Gantt javascript configuration options, e.g.:

``` python

    gantt.config.start_date = new Date(2018, 12, 10);
    gantt.config.end_date = new Date(2020, 08, 20);

    gantt.config.scale_unit = "month";
    gantt.config.step = 1;
    gantt.config.date_scale = "%F, %Y";
    gantt.config.min_column_width = 50;

    gantt.config.scale_height = 90;

    var weekScaleTemplate = function (date) {
        var dateToStr = gantt.date.date_to_str("%d %M");
        var endDate = gantt.date.add(gantt.date.add(date, 1, "week"), -1, "day");
        return dateToStr(date) + " - " + dateToStr(endDate);
        };

    var daysStyle = function(date){
        var dateToStr = gantt.date.date_to_str("%D");
        if (dateToStr(date) == "Sun"||dateToStr(date) == "Sat")  return "weekend";
        return "";
        };

    gantt.config.subscales = [
        {unit: "week", step: 1, template: weekScaleTemplate},
        {unit:"day", step:1, date:"%D", css:daysStyle }
        ];
```

