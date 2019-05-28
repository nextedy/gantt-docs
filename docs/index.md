# Work Items Gantt 

*Work Items Gantt* brings the interactive high-level project planning & scheduling to Polarion ALM. 

Interactive drag & drop enabled Gantt chart widget provides unique capabilities to expose the standard Work Items (such as Features, Epics, Objectives, ...) as micro projects in a visually appealing way and perform various operations easily and efficiently.

![Gantt Screenshot](img/gantt-overall.png)

## Adjust Schedule

You can easily adjust the project schedule, including re-scheduling of the subtasks when the parent project schedule is adjusted:

![Replan](img/gantt-drag-children.gif)

## Manage Dependencies

The Management of project and task dependencies is another common task. Just start a link on start item and finish it on target item:

![Dependencies](img/gantt-drag-dependency-link.gif)

## Project Types

Sometimes the task schedule should be derivered from the children, this is exactly what is covered by `project` type. (Task Script needs to be used to configure what work items are of type `project`

![Projects](img/gantt-projects.gif)



## Storing Data

You can fully configure what work item custom fields are used to store the Gantt information, See Widget  > [Advanced Properties](./widget/#advanced). 
