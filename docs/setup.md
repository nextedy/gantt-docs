# Setup

!!! info "Installation"
    In this document we describe how to configure Polarion to display the Work Item Gantt. 
    We suppose the plugin is already installed.
    If you look for the the plugin installation instructions you will find them in the distribution zip file.

You have two options:

1.	Setup Gantt as full report view
	
	OR
	
2.	Add interactive Gantt to an existing report


##  Full report gantt

The most common approach to display *Work Items Gantt* is to create a single LiveReport page, call it for example *Gantt*, and put the *Work Items Gantt Widget* as single widget there.

In this case we recommend to activate following widget property:

* `Advanced` >  `Maximize` - set the Maximize property of the widget to 'yes'

This will make the widget size equal to working area size.

Please make sure there are no additional empty paragraphs or other whitespace content around the widget.

![Gantt Maximize Widget Property](img/gantt-max-property.png)


##  Gantt as widget

Sometimes it is more useful to embed the Gantt widget to an existing reports, together with other reporting widgets. In such case make sure that `Maximize` property is turned off.

* `Advanced` >  `Maximize` - set the Maximize property of the widget to 'no'

!!! warning
	Currently it is possible to have only one Work Item Gantt widget on a page. Please do not add more of them on a single page.



