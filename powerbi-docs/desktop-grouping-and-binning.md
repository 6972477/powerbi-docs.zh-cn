---
title: "在 Power BI Desktop 中使用分组和装箱"
description: "了解如何在 Power BI Desktop 中对元素进行分组和装箱"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/19/2018
ms.author: davidi
LocalizationGroup: Create reports
ms.openlocfilehash: ec663e61a6cb5281500e605fda35ecb81d7b71a2
ms.sourcegitcommit: 88c8ba8dee4384ea7bff5cedcad67fce784d92b0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/24/2018
---
# <a name="use-grouping-and-binning-in-power-bi-desktop"></a>在 Power BI Desktop 中使用分组和装箱
在创建视觉对象后，**Power BI Desktop** 会根据基础数据中的值，将数据分入各区块（或**组**）。 这通常不会出现问题，但你有时可能会想要优化这些区块的显示方式。 例如，你可能想要在一个更宽泛的类别（ *组* ）中设置三个产品类别。 或者，你可能希望将销售额数据按 1,000,000 美元大小进行装箱，而不是等分 923,983 美元。

在 Power BI Desktop 中，你可以对数据点进行**分组**，以便更清楚地查看、分析和浏览视觉对象中的数据和趋势。 你还可以定义**装箱大小**（通常称为**装箱**），将值归入大小相同的组，更有助于你执行合理的数据可视化。

### <a name="using-grouping"></a>使用分组
若要使用**分组**，请在按住 CTRL 的同时单击选择多个元素，从而选择视觉对象上的两个或多个元素。 然后，右键单击所选多个元素中的一个，并从随即显示的菜单中选择“ *分组* ”。

![](media/desktop-grouping-and-binning/grouping-binning_1.png)

创建的组会被添加到视觉对象的“**图例**”存储桶中，并且还会显示在“**字段**”列表中。

![](media/desktop-grouping-and-binning/grouping-binning_2.png)

创建组后，可以右键单击“ **图例** ”存储桶或“ **字段** ”列表中的字段，然后选择“ *编辑组* ”，从而轻松编辑该组的成员。

![](media/desktop-grouping-and-binning/grouping-binning_3.png)

在随即显示的“**组**”窗口中，可以新建组，也可以修改现有组。 还可以 *重命名* 任意组，只需双击“ **组和成员** ”框中的“ **组** ”标题，然后键入一个新名称即可。

在此窗口中，可以对组执行各种操作。 可以将“**未分组值**”列表中的项添加到一个新组或现有组中。 若要新建组，请从“**未分组值**”框中选择两个或多个项（按住 CTRL 的同时单击），然后单击该框下方的“**组**”按钮。

可以将未分组值添加到现有组，只需选择未分组值，选择要在其中添加此值的现有组，然后单击“**组**”按钮。 若要删除组中的项，请在“**组和成员**”框中选择相应项，然后单击“**取消分组**”。 你还可以选择是应将未分组的类别归入**其他**组，还是应保留未分组状态。

![](media/desktop-grouping-and-binning/grouping-binning_4.png)

> [!NOTE]
> 也可以为“字段”中的任意字段创建组，而无需选择现有视觉对象中的多个元素。 只需右键单击相应字段，然后从随即显示的菜单中选择“**组**”即可。
> 
> 

### <a name="using-binning"></a>使用装箱
可以在 **Power BI Desktop** 中设置数字和时间字段的装箱大小。 借助装箱，可以合理精简 **Power BI Desktop** 显示的数据。

若要应用装箱大小，请右键单击“**字段**”，然后选择“**组**”。

![](media/desktop-grouping-and-binning/grouping-binning_5.png)

在“**组**”窗口中，设置所需的“**装箱大小**”。

![](media/desktop-grouping-and-binning/grouping-binning_6.png)

选择“ **确定** ”后，你会发现“ **字段** ”窗格中显示一个新字段，且后跟“ *（装箱）* ”一词。 然后，可以将该字段拖到画布上，以在视觉对象中使用此装箱大小。

![](media/desktop-grouping-and-binning/grouping-binning_7.png)

若要了解**装箱**的运作方式，请观看此[视频](https://www.youtube.com/watch?v=BRvdZSfO0DY)。

一切就是这么简单！使用**分组**和**装箱**可以确保报表中的视觉对象按你所需的方式显示数据。

