+++
title = "Configure Visio TimeLine Shapes" 
description = "" 
weight = 12026 
+++

Aspose.Diagram for .NET : Configure Visio TimeLine Shapes  

# Aspose.Diagram for .NET : Configure Visio TimeLine Shapes


{{< panel title="Contents Summary" style="primary" >}}
*   1 [Set Milestone Shape Properties](#ConfigureVisioTimeLineShapes-SetMilestoneShapeProperties)
    *   1.1 [Setting Milestone Date, Date Format, Auto Update Flag and Type](#ConfigureVisioTimeLineShapes-SettingMilestoneDate,DateFormat,AutoUpdateFlagandType)
        *   1.1.1 [Set Milestone Programming Sample](#ConfigureVisioTimeLineShapes-SetMilestoneProgrammingSample)
*   2 [Set Time Period and Date Format of Timeline Shape](#ConfigureVisioTimeLineShapes-SetTimePeriodandDateFormatofTimelineShape)
    *   2.1 [Setting Time Period and Date Format](#ConfigureVisioTimeLineShapes-SettingTimePeriodandDateFormat)
        *   2.1.1 [Set Time Period and Date Programming Sample](#ConfigureVisioTimeLineShapes-SetTimePeriodandDateProgrammingSample)
*   3 [Refresh Milestones on the Timeline in Visio](#ConfigureVisioTimeLineShapes-RefreshMilestonesontheTimelineinVisio)
    *   3.1 [Refresh Milestones on the Timeline using TimeLineHelper class](#ConfigureVisioTimeLineShapes-RefreshMilestonesontheTimelineusingTimeLineHelperclass)
        *   3.1.1 [Refresh Milestones using TimeLineHelper Programming Sample](#ConfigureVisioTimeLineShapes-RefreshMilestonesusingTimeLineHelperProgrammingSample)
    *   3.2 [Refresh Milestones on the Timeline using MilestoneHelper class](#ConfigureVisioTimeLineShapes-RefreshMilestonesontheTimelineusingMilestoneHelperclass)
        *   3.2.1 [Refresh Milestones using MilestoneHelper Programming Sample](#ConfigureVisioTimeLineShapes-RefreshMilestonesusingMilestoneHelperProgrammingSample)
{{< /panel >}}
 

 

## Set Milestone Shape Properties

Aspose.Diagram allows developers to set milestone properties. This article shows how to set the milestone date, date format, auto update flag and type.

### Setting Milestone Date, Date Format, Auto Update Flag and Type

The [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) class takes a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object while initializing the [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) object. The code example in this article sets the milestone date, date format, auto update flag and milestone type properties.

The process for updating the milestone date, date format, auto update flag and milestone type:

1.  Load a diagram.
2.  Find a particular shape.
3.  Initialize the `MilestoneHelper` object.
4.  Set a milestone date.
5.  Set the milestone date format.
6.  Set an auto update flag.
7.  Set the milestone type
8.  Save the Visio drawing to any supported format.

#### Set Milestone Programming Sample

  
Table of date format values:

{{< table style="table-striped" >}}
|Value|Format String|
|:----|:----|
|0|dddd, yyyy-M-d|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|yyyy/M/d|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|M-d-yy|
|11|M-d|
|12|d MMMM, yyyy|
|13|d MMM, yyyy|
|14|d-M-yy|
|15|d-M|
|16|yy-M-d|
|17|yyyy-M-d|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|yy|
|25|yyyy|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
{{< /table >}}

## Set Time Period and Date Format of Timeline Shape

Aspose.Diagram allows developers to configure the timeline programmatically. This explains how to adjust the time period and date format of timeline shapes (block, line, ruler, divided, or cylindrical).

### Setting Time Period and Date Format

The [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) class takes a [Shape](http://www.aspose.com/api/net/diagram/aspose.diagram/shape) object when initializing the [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) object. The code example in this article sets the time period start, end and date format values.

The process for updating time period start, end and date format is:

1.  Load a diagram.
2.  Find a particular shape.
3.  Initialize the `TimeLineHelper` object.
4.  Set the time period start.
5.  Set the time period end.
6.  Set a date format.
7.  Save the Visio drawing to any supported format.

#### Set Time Period and Date Programming Sample

  
Table of date format values:

{{< table style="table-striped" >}}
|Value|Format String|
|:----|:----|
|0|dddd, yyyy-M-d|
|1|yyyy-MM-dd|
|2|yy-MMM-d|
|3|yyyy/M/d|
|4|yy-MMM.-d|
|5|d MMMM yyyy|
|6|yy-M|
|7|MMM-yy|
|8|MMMM d, yyyy|
|9|MMM d, yyyy|
|10|M-d-yy|
|11|M-d|
|12|d MMMM, yyyy|
|13|d MMM, yyyy|
|14|d-M-yy|
|15|d-M|
|16|yy-M-d|
|17|yyyy-M-d|
|18|M-yy|
|19|M-yyyy|
|20|MMMM yyyy|
|21|MMMM yy|
|22|MMM yyyy|
|23|MMM yy|
|24|yy|
|25|yyyy|
|26|d|
|27|MMMM|
|28|MMM|
|29|M|
{{< /table >}}

## Refresh Milestones on the Timeline in Visio

Aspose.Diagram allows developers to adjust milestones on the timeline shapes (block, line, ruler, divided, or cylindrical) according to the time period change.

### Refresh Milestones on the Timeline using TimeLineHelper class

The `RefreshTimeLine` method exposed by the [TimeLineHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/timelinehelper) class can be used to revive milestones on the timeline.

The code below shows how to:

1.  load a sample diagram.
2.  get a timeline shape.
3.  initialize the TimeLineHelper object.
4.  set the time period start.
5.  set the time period end.
6.  set date format (optional).
7.  call RefreshTimeLine method of the TimeLineHelper object.
8.  save diagram

#### Refresh Milestones using TimeLineHelper Programming Sample

Use the following code in your .NET application to revive milestones on the timeline using Aspose.Diagram for .NET.

### Refresh Milestones on the Timeline using MilestoneHelper class

The `RefreshMilestone` method exposed by the [MilestoneHelper](http://www.aspose.com/api/net/diagram/aspose.diagram/milestonehelper) class can be used to refresh milestones on the timeline.

The code below shows how to:

1.  load a sample diagram.
2.  get a timeline shape.
3.  add Shape in Visio diagram using AddShape method.
4.  initialize the MilestoneHelper object.
5.  set Milestone Date.
6.  set Milstone's IsAutoUpdate property to true.
7.  call RefreshMilestone method of the MilestoneHelper object.
8.  save diagram

#### Refresh Milestones using MilestoneHelper Programming Sample

Use the following code in your .NET application to refresh milestones on the timeline using Aspose.Diagram for .NET.

## Attachments:

![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 01.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547230.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 02.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547231.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 03.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546738.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 04.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546739.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Milestone Shape Properties 01.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546740.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Milestone Shape Properties 02.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546741.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [cMJQNch.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547239.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [nHth3W8.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547238.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 01.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546736.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [Set Time Period and Date Format of TimeLine Shape 02.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18546737.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [TxFKc1K.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547228.png) (image/png)  
![](https://docs2.aspose.com/diagram/net/images/icons/bullet_blue.gif) [XulWyBC.png](https://docs2.aspose.com/diagram/net/attachments/18350185/18547229.png) (image/png)  

