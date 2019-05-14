# Setup

!!! info "Installation"
    In this document we describe how to configure Polarion to display the Work Item Gantt. 
    We suppose the plugin is already installed.
    If you look for the the plugin installation instructions you will find them in the distribution zip file.

## Widget

The Work Item Gantt is implemented as standard Polarion widget.

![Gantt](img/gantt-widget-add.png)

All the configuration options are described on [Widget Parameters](../widget/#widget-parameters) page.

## Display Modes

You have two options how to display the Gantt widget.

1.	Setup Gantt as Full-Report view
	
	OR
	
2.	Add Gantt to an existing report


###  Full Report Gantt

The most common approach to show *Work Items Gantt* is to create a single LiveReport page, call it for example *Gantt*, and put the *Work Items Gantt Widget* as single widget there.

In this case we recommend to activate following widget property:

* `Advanced` >  `Maximize` - set the Maximize property of the widget to 'yes'

This will make the widget size equal to working area size.

Please make sure there are no additional empty paragraphs or other whitespace content around the widget.

![Gantt Maximize Widget Property](img/gantt-max-property.png)


###  Gantt as Widget

Sometimes it is more useful to embed the Gantt widget to an existing reports, together with other reporting widgets. In such case make sure that `Maximize` property is turned off.

* `Advanced` >  `Maximize` - set the Maximize property of the widget to 'no'

!!! warning
	Currently it is possible to have only one Work Item Gantt widget on a page. Please do not add more of them on a single page.


## Data Mapping

Once you have the widget on your page, you need to configure where to store scheduling informations. The gantt model is storing following data:

* Start Date (Date)
* Duration (Number of days)
* Progress (Float from 0 .. 1)

You can configure the mapping using the Advanced Widget parameters:

* `Start Field` -  the name of the custom field, that holds when the work item starts. It can be any of: Date, Date-Time or String. If such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use a Date (Only) custom field.

* `Duration Field` -  the name of the custom field, that holds when the work item duration as number of days. It can be any of: Integer or String.  If such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use an Integer custom field.

* `Progress Field` - the name of the custom field, that holds when the work item progress as float (if you multiple by 100 you get % of completion). It can be any of: Float or String.  If such custom fields does not exists, the value will be stored in String ad-hoc custom fields. For production use we recommend to use a Float custom field.

## Hierarchy

The hierarchy of items on the gantt chart is derived from work item links. This is controlled by `Parent Role` widget parameter:

* `Parent Role` - select what Work Item link roles should be used to detect the parent-child relationships. If empty, no hierarchy is shown.

## Dependencies

The dependency links are also derived from the work item links. This is controlled by `Dependency Role` widget parameter:

* `Dependency Role` - select what Work Item link roles should be used to detect the Depends-on relationships. If empty, no dependencies will be shown. If you select multiple link roles, the first role is used when creating new links.

## More 

There a lot more configuration options, see [Widget Parameters](../widget/#widget-parameters) page for the full list. 




