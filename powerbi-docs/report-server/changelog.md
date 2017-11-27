---
title: "Power BI 报表服务器的更改日志"
description: "此更改日志适用于 Power BI 报表服务器，并列出了新项和每次发布版本的 bug 修复。"
services: powerbi
documentationcenter: 
author: jtarquino
manager: jonhp
backup: maggies
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 11/17/2017
ms.author: jaimeta
ms.openlocfilehash: e56976943e58aba8c9ef36c576a16ab5eba4c796
ms.sourcegitcommit: 7d4ad2ba92a932d7cc6637348e0774be6623559e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2017
---
# <a name="changelog-for-power-bi-report-server"></a>Power BI 报表服务器的更改日志

此更改日志适用于 Power BI 报表服务器，并列出了新项和每次发布版本的 bug 修复。

有关新功能的详细信息，请参阅[Power BI 报表服务器中的新增功能](whats-new.md)。

## <a name="october-2017"></a>2017 年 10 月

- **Power BI 报表服务器**
    - 2017 年 11 月 17 日发布的版本 1.1.6530.30789（生成号 14.0.600.437）
        - Bug 修复
            - 针对基本身份验证方案进行了修复 
            - 修复了以下问题：无法在门户上“订阅”、“缓存刷新计划”和“历史记录快照”的计划页上选择工作日
            - 对于分页报表 (RDL)，修复了以下问题：如果文本框中的表达式将 CanGrow 属性设为 False，则会导致值不显示颜色且字体不正确
            - 对于 Power BI 报表 (PBIX)，修复了以下问题：向折线图添加图例会导致呈现的视觉对象为空

    - 版本 1.1.6514.9163（内部版本 14.0.600.434），发布日期：2017 年 11 月 1 日
        - Bug 修复
            - 对超过 500MB 的 PBIX 报表的上传可靠性问题的修复
            - 对超过 1GB 的 PBIX 报表的数据上传问题的修复

    - 版本 1.1.6513.3500（内部版本 14.0.600.433），发布日期：2017 年 10 月 31 日
        - 功能
            - 嵌入数据模型支持
            - Excel 工作簿查看（已启用 Office Online Server 集成）
            - 计划的数据刷新 (PBIX)
            - 直接查询支持
            - 大文件支持（最大 2 GB）
            - 公用 REST API
            - Power BI Desktop 中的共享数据集支持（通过 oData）
            - URL 参数 支持 PBIX 文件
            - 辅助功能改进

- Power BI Desktop（已针对 Power BI 报表服务器进行优化）
    - 2017 年 11 月 17 日发布的版本 2.51.4885.1423（2017 年 10 月）
        - Bug 修复
            - 修复了以下问题：32 位 Power BI Desktop 无法在 x86 OS 上运行
            - 对于 Power BI 报表 (PBIX)，修复了 X 轴网格线的显示问题
            - 其他次要缺陷修复

    - 版本：2.51.4885.1041（2017 年 10 月），发布时间：2017 年 10 月 31 日
        - 功能
            - 包含与 Power BI 报表服务器连接所需的更改（2017 年 10 月）

## <a name="june-2017"></a>2017 年 6 月

- **Power BI 报表服务器**
    - 内部版本 14.0.600.305，发布日期：2017 年 9 月 19 日  
        - Bug 修复
            - 更新到最新的[必应地图 Web 控件](https://msdn.microsoft.com/library/mt712542.aspx)

    - 内部版本 14.0.600.301，发布日期：2017 年 7 月 11 日
        - Bug 修复
            - {{UserId}} 标记解析为存储的凭据，而不是在 Power BI 报表中执行报表的用户
            - 某些图像无法在 Power BI 报表服务器报表中呈现
            - 无法在 Power BI 报表服务器中更改 Power BI 报表的名称
            - 无法在 Power BI 移动应用程序中加载自定义视觉对象（需要重新安装移动应用以清除本地缓存）

    - 内部版本 14.0.600.271，发布日期：2017 年 6 月 12 日
        - Power BI 报表服务器初始版本

## <a name="next-steps"></a>后续步骤

[用户手册](user-handbook-overview.md)  
[管理员手册](admin-handbook-overview.md)  
[快速入门：安装 Power BI 报表服务器](quickstart-install-report-server.md)  
[安装报表生成器](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[下载 SQL Server Data Tools (SSDT)](http://go.microsoft.com/fwlink/?LinkID=616714)

更多问题？ [尝试咨询 Power BI 社区](https://community.powerbi.com/)