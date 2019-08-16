# Work Items Gantt

The *Work Item Gantt* widget is listed under  *Work Items* tag:

![Gantt](img/gantt-widget-add.png)

!!! info
    Currently, it is possible to have only one Work Item Gantt widget on a page.

## Widget Parameters 

* `Work Items` - a standard data set parameter, select what work items you want to see on your Gantt chart.

* `Sort by` -  the sort criteria to sort the top level work items.

* `Load Children` - define how many levels of child items should be traversed and added to the list in addition to the items from `Work Items` date set parameter. 
    
    Zero (0) means that no additional items are shown.
    
* `Show Unplanned` - click on `no` to hide all the work items that do not have the `Start Field` set. 

    If you keep it set to `yes`, such tasks will be in the list, scheduled for 'Today', and marked by gray color. 

* `Scale ( D || W || M )` -  configures the scale of the timeline.   Values are: 
    + 'D' - day
    + 'W' - week
    + 'M' - Month

* `Parent Role` - select what Work Item link roles should be used to detect the parent-child relationships. If empty, no hierarchy is shown.

* `Dependency Role` - select what Work Item link roles should be used to detect Depends-on relationships. If empty, no dependencies will be shown. 

    If you select multiple link roles, the first role is used when creating new links.


## Advanced Parameters

* `Maximize View` -  configure if the widget should expand its content over the full working area. See [Setup](../setup/).

* `Drag Children` -  configure if you want the child items to be rescheduled when dragging their parent's item.

* `Start Field` -  the name of the custom field, that stores the information when the work item starts. 

	The type of the custom field can be any of these: Date, Date-Time or String. 
	
	If such custom field does not exist, the value will be stored in String ad-hoc custom field. For production use, we recommend using a Date (Only) custom field.

* `Duration Field` -  the name of the custom field, that stores the information about the work item duration as the number of days. 

	The type of the custom field can be any of these: Integer or String.  
	
	If such custom field does not exist, the value will be stored in String ad-hoc custom field. For production use, we recommend using an Integer custom field.

* `Progress Field` - the name of the custom field, that stores the progress of the work item progress as Float (multiply by 100 to get % of completion). 

	The type of the custom field can be any of these: Float or String.  
	
	If such custom field does not exist, the value will be stored in String ad-hoc custom field. For production use, we recommend using a Float custom field.


* `Max Items` -  (Integer) limits the maximum number of work items loaded into the Gantt view.

### Gantt Config Script

You can add additional Gantt javascript configuration options, e.g.:

``` 

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
### Task Script 
You can add a server side  javascript (executed on server) to decorate the task based on the work item properties.
You have two variables defined:

*  `task` of type `com.nextedy.polarion.gantt.model.Task`
*  `wi` of type `com.polarion.alm.tracker.model.IWorkItem` 

See following example, that changes type of the task to `project` if the Work Item Type in Polarion is `capability`. 

```
if(wi.type.id==='capability'){
    task.color='green';
    task.getFields().put("isCapability",true);
}else{
    task.getFields().put("isCapability",false);
}
```

You can access a `Task.class` definition bellow. 

```
public class Task  {
    public String id;
    public String text;
    public Date start_date;
    public int duration = Integer.getInteger("nextedy.gantt.default.task_duration",10);
    public float progress ;
    public String parent;
    public String type ;	
    public String url;
    public String itemId;
    public String projectId;
    public boolean readonly;
    public boolean unplanned = false;
    public boolean open = !Boolean.getBoolean("nextedy.gantt.default.do_expand");
    public String color = System.getProperty("nextedy.gantt.default.task_color",null);
    
    private Map<String,String> fields = new HashMap<String, String>();

	public Map<String, String> getFields() {
		return fields;
	}

	public void setFields(Map<String, String> fields) {
		this.fields = fields;
	}
    
}
```

As you can see, you can store the additional information in fields map, and use it e.g. when configuring the actual tooltip in `Gantt Config Script` (experts only).

```
gantt.templates.rightside_text = function(start, end, task){
    return  "Capability: <b>"+task.fields.isCapability+"</b>";
};
```
