---
title: "报表编辑器...教程"
description: "报表编辑器...教程。"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
featuredvideoid: IkJda4O7oGs
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/30/2017
ms.author: mihart
ms.openlocfilehash: e5ee6db22fe0fa7fd1e61ebbfb7dbee9d3458159
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2017
---
# <a name="the-report-editortake-a-tour"></a>报表编辑器...教程
Power BI 服务中的报表编辑器和 Power BI Desktop 中的报表编辑器非常相似。 该视频演示的是 Power BI Desktop 中的报表编辑器，而本文介绍的是 Power BI 服务中的报表编辑器。 

<iframe width="560" height="315" src="https://www.youtube.com/embed/IkJda4O7oGs" frameborder="0" allowfullscreen></iframe>

在 Power BI 服务中，报表编辑器仅在[编辑视图](service-reading-view-and-editing-view.md)中可用。 若要在“编辑视图”中打开报表，必须是报表所有者身份。

Power BI 报表编辑器由 3 部分组成：  

1. “字段”、“可视化效果”和“筛选器”窗格
2. 顶部导航栏    
3. 报表画布     

![](media/service-the-report-editor-take-a-tour/power-bi-report-canvas.png)

## <a name="1-the-report-editor-panes"></a>1.报表编辑器窗格
![](media/service-the-report-editor-take-a-tour/power-bi-report-panes.png)

首次打开报表时可看到 3 个窗格：“可视化效果”、“筛选器”和“字段”。 左侧窗格“可视化效果”和“筛选器”可控制可视化效果的外观，其中包括类型、字体、筛选、格式设置。  而右侧窗格上的“字段”则可管理将用于可视化效果的基础数据。 

报告编辑器中显示的内容会随报表画布中选择的内容不同而异。  例如，如果选择单个视觉对象， 

|  |  |
| --- | --- |
| ![](media/service-the-report-editor-take-a-tour/power-bi-panes.png) |<ul><li>“可视化效果”窗格顶部会标识出正在使用的视觉对象类型；在本例中，就是簇状柱形图。<br><br></li> <li>“可视化效果”窗格底部（可能需要向下滚动）则会显示视觉对象中正在使用的字段。 此图使用 FiscalMonth、DistrictManager 和 Total Sales Variance。 <br><br></li><li>“筛选器”窗格（可能需要向下滚动）将显示已应用的所有筛选器。 <br><br></li><li>“字段”窗格中列出可用的表，如果展开表的名称，还会列出构成该表的字段。 黄色字体告诉用户可视化效果中至少正在使用该表格中的一个字段。<br><br></li><li>![](media/service-the-report-editor-take-a-tour/power-bi-paint-roller-icon.png)要显示“格式设置”窗格，请为所选的可视化效果选择滚筒刷图标。<br><br></li><li>![](media/service-the-report-editor-take-a-tour/power-bi-magnifying-icon.png) 若要显示“分析”窗格，请选择放大镜图标。</ul> |
|  | |

## <a name="the-visualizations-pane-from-top-to-bottom"></a>可视化效果窗格（从上到下）
![](media/service-the-report-editor-take-a-tour/selectviz.png)

在此处选择可视化效果类型。 小图片称为*模板*。 在上图中，已选择“簇状条形图”。 如果未首先选择可视化效果类型，而是通过选择字段开始生成可视化效果，则 Power BI 将为你选择可视化效果类型。 你可以保留 Power BI 的选择或通过选择不同的模板更改类型。 可以根据需要进行多次切换，找到最能代表你的数据的可视化效果类型。

### <a name="manage-the-fields-used-in-your-visual"></a>管理视觉对象中使用的字段。
![](media/service-the-report-editor-take-a-tour/power-bi-field-list.png)

此窗格中显示的存储桶（有时称为*井*）根据所选择的可视化效果类型而有所不同。  例如，如果选择的是条形图，则会看到以下存储桶：值、轴和图例。 当选择某个字段时，或将其拖到画布上时，Power BI 会将该字段添加到其中一个存储桶。  也可以直接将“字段”列表中的字段拖动到存储桶中。  某些存储桶仅限于特定类型的数据。  例如，**值**将不会接受非数字字段。 因此，如果将**员工姓名**字段拖入**值**存储桶，Power BI 会将其更改为**员工姓名计数**。

### <a name="remove-a-field"></a>删除字段
若要从可视化效果中删除字段，请选择字段名称右侧的“X”。

![](media/service-the-report-editor-take-a-tour/deletefield.png)

有关详细信息，请参阅[向 Power BI 报表添加可视化效果](power-bi-report-add-visualizations-i.md)。

### <a name="format-your-visuals"></a>格式化视觉对象
选择滚动油漆刷图标，以显示“格式设置”窗格。 可用的选项取决于所选可视化效果的类型。

![](media/service-the-report-editor-take-a-tour/power-bi-formatting.png)

几乎可以进行任何格式设置。  若要了解详细信息，可以自行探索或参阅以下文章：

* [自定义可视化效果的标题、背景和图例](power-bi-visualization-customize-title-background-and-legend.md)
* [颜色格式](service-getting-started-with-color-formatting-and-axis-properties.md)
* [自定义 X 轴和 Y 轴属性](power-bi-visualization-customize-x-axis-and-y-axis.md)

### <a name="add-analytics-to-your-visualizations"></a>将分析添加到可视化效果
选择放大镜图标以显示“分析”窗格。 可用的选项取决于所选可视化效果的类型。

![](media/service-the-report-editor-take-a-tour/power-bi-analytics.png)    
通过 Power BI 服务中的“分析”窗格，可以将动态参考行添加到可视化效果，并重点关注重要趋势或见解。 若要了解详细信息，请参阅 [Power BI 服务中的“分析”窗格](service-analytics-pane.md)或 [Power BI Desktop 中的“分析”窗格](desktop-analytics-pane.md)。

- - -
## <a name="the-filters-pane"></a>“筛选器”窗格
查看、设置并修改页、报表、钻取和视觉对象级别筛选器。

![](media/service-the-report-editor-take-a-tour/power-bi-formatting-pane.png)

有关详细信息，请参阅[向报表添加筛选器](power-bi-report-add-filter.md)。

- - -
## <a name="the-fields-pane"></a>“字段”窗格
“字段”窗格显示数据中存在的表和字段，可供你创建可视化效果。

|  |  |
| --- | --- |
| ![](media/service-the-report-editor-take-a-tour/reportfields.png) |<ul><li>将字段拖到页上，以启动一个新的可视化效果。  还可以将字段拖动到现有可视化效果，以将字段添加到该可视化效果。<br><br></li> <li>添加某一字段旁的选中标记时，Power BI 会将该字段添加到活动（或新的）可视化效果中。 它还决定将该字段放入哪个存储桶。  例如，该字段应用于图例、轴还是值？ Power BI 进行最佳推测，如有必要，可以将其从一个存储桶移动到另一个。 <br><br></li><li>无论哪种方式，每个所选的字段都会被添加到报表编辑器中的可视化效果窗格。</li></ul> |

**注意**：如果使用的是 Power BI Desktop，则还可以选择显示/隐藏字段、添加计算等。

### <a name="what-do-the-field-icons-mean"></a>字段图标的涵义
* **∑ 聚合**聚合是一个数值，例如，可对其求和或求平均值。 聚合随数据一起导入（在报表所基于的数据模型中定义）。
  有关详细信息，请参阅 [Power BI 报表中的聚合函数](service-aggregates.md)。
* ![](media/service-the-report-editor-take-a-tour/pbi_calculated_icon.png)**计算度量值（亦称为“计算字段”）**  
   各个计算字段都具有其自己的硬编码公式。 不能更改此计算，例如，如果该计算是求和，则只能进行求和。 有关详细信息，请参阅[了解度量值](desktop-measures.md)
* ![](media/service-the-report-editor-take-a-tour/icon.png)唯一字段  
   具有此图标的字段是从 Excel 导入的，因此将被设置为显示全部值，即使它们具有重复项也是如此。 例如，你的数据可能有两条人名为 John Smith 的记录，每一条都将被视为唯一（不会总结这两条）。  
* **![](media/service-the-report-editor-take-a-tour/pbi_geo_icon.png) 地理位置字段**  
   地理字段可用于创建地图可视化效果。 
* **![](media/service-the-report-editor-take-a-tour/power-bi-hierarchy-icon.png) 层次结构**  
   选择箭头以显示构成层次结构的字段。 

- - -
## <a name="2-the-top-navigation-bar"></a>2.顶部导航栏
顶部导航栏中可用的操作有很多；新操作一直在增加。 有关特定操作的信息，请使用 Power BI 文档目录或搜索框。

## <a name="3-the-report-canvas"></a>3.报表画布
报表画布是显示工作内容的地方。 使用“字段”、“筛选器”和“可视化效果”窗格创建视觉对象时，将在报表画布中生成和显示这些视觉对象。 画布底部的各个选项卡表示报表中的页。 选择某个选项卡将打开该页。 

## <a name="next-steps"></a>后续步骤：
[创建报表](service-report-create-new.md)

[编辑报表](service-interact-with-a-report-in-editing-view.md)

了解有关 [Power BI 中的报表](service-reports.md)的详细信息

[Power BI 入门](service-get-started.md)

[Power BI - 基本概念](service-basic-concepts.md)

更多问题？ [尝试参与 Power BI 社区](http://community.powerbi.com/)

