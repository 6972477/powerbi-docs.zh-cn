---
title: 合并 Power BI Desktop 中的文件（二进制文件）
description: 轻松合并 Power BI Desktop 中的文件（二进制文件）数据源
services: powerbi
documentationcenter: ''
author: davidiseminger
manager: kfile
backup: ''
editor: ''
tags: ''
qualityfocus: no
qualitydate: ''
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 04/24/2018
ms.author: davidi
LocalizationGroup: Transform and shape data
ms.openlocfilehash: 4996b7485cb9514b9378982d2149ef5380e8fdc9
ms.sourcegitcommit: 3f2f254f6e8d18137bae879ddea0784e56b66895
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="combine-files-binaries-in-power-bi-desktop"></a>合并 Power BI Desktop 中的文件（二进制文件）
向 **Power BI Desktop** 导入数据的一个强大的方法是将具有同一架构的多个文件合并到一个逻辑表中。 随着 2016 年 11 月 **Power BI Desktop**（及后续版本）的发行，这一方便且受欢迎的方法变得更为便捷并被更广泛地使用，如本文中所述。

若要从同一文件夹中启动合并文件的过程，请选择“获取数据”>“文件”>“文件夹”。

![](media/desktop-combine-binaries/combine-binaries_1.png)

## <a name="previous-combine-files-binaries-behavior"></a>之前合并文件（文件）的行为
在 2016 年 11 月发布的 Power BI Desktop 之前，此功能称为“合并二进制文件”，并且可以使用合并二进制文件转换功能来合并某些文件类型，但存在限制：

* 在将文件合并到一个单个表前，不会考虑转换每个单独的文件。 为此，通常需要合并文件，然后通过筛选行删选掉标头值，作为编辑过程的一部分。
* **合并二进制文件**转换仅适用于文本或 CSV 文件，对其他受支持的文件格式（如 Excel 工作簿、JSON 文件等）不适用。

客户要求更直观的合并二进制文件操作，因此我们增强了转换功能并将其重命名为“合并文件”。

## <a name="current-combine-files-behavior"></a>当前合并文件的行为
Power BI Desktop 现在可以更有效地合并文件（二进制文件）。 首先，从“查询编辑器”中的“主页”功能区选项卡或从列本身选择“合并文件”。

![](media/desktop-combine-binaries/combine-binaries_2a.png)

合并文件转换现在执行如下操作：

* 合并文件转换分析每个输入文件，并确定要使用的正确文件格式，如文本或 Excel 工作簿或 JSON 文件。
* 借助转换，可以从第一个文件选择特定对象，例如，要提取的 Excel 工作簿。
  
  ![](media/desktop-combine-binaries/combine-binaries_3.png)
* 合并文件然后会自动执行以下查询：
  
  * 创建在单个文件中执行所有所需提取步骤的示例查询。
  * 创建功能查询，该功能查询将参数化示例查询的文件/二进制文件输入。 将示例查询和功能查询进行链接，以在功能查询中反映对示例查询所做的更改。
  * 使用输入二进制文件（如文件夹查询）将功能查询应用于原始查询，以使其应用于每一行的二进制文件输入的功能查询，然后将生成的数据提取扩展为顶级列。
    
    ![](media/desktop-combine-binaries/combine-binaries_4.png)

随着合并文件的新行为，可以在给定文件夹内轻松合并所有文件，因为它们具有同一文件类型和结构（如同一列）。

此外，还可以通过修改自动创建的示例查询轻松应用其他转换或提取步骤，而无需担心修改或创建其他功能查询步骤。 对示例查询所做的任何更改都会在链接的功能查询中自动生成。

## <a name="next-steps"></a>后续步骤
你可以使用 Power BI Desktop 连接到各种数据。 有关数据源的详细信息，请参阅下列资源：

* [Power BI Desktop 入门](desktop-getting-started.md)
* [Power BI Desktop 中的数据源](desktop-data-sources.md)
* [使用 Power BI Desktop 调整和合并数据](desktop-shape-and-combine-data.md)
* [通过 Power BI Desktop 连接到 CSV 文件](desktop-connect-csv.md)   
* [直接将数据输入到 Power BI Desktop 中](desktop-enter-data-directly-into-desktop.md)   

