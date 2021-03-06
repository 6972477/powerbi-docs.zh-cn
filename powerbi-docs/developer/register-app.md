---
title: "注册应用以便嵌入 Power BI 内容"
description: "了解如何在 Azure Active Directory 中注册应用程序，用于嵌入 Power BI 内容。"
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 10/05/2017
ms.author: maghan
ms.openlocfilehash: cc9a4c7a29ddb84e6230d42f31a9c6a0427008f1
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2018
---
# <a name="register-an-azure-ad-app-to-embed-power-bi-content"></a>注册 Azure AD 应用以便嵌入 Power BI 内容
了解如何在 Azure Active Directory (Azure AD) 中注册应用程序，用于嵌入 Power BI 内容。

使用 Azure AD 注册应用程序后，应用程序将能够访问 Power BI REST API。 此操作能够为应用程序建立标识，并指定对 Power BI REST 资源的权限。

> [!IMPORTANT]
> 注册 Power BI 应用之前，需要一个 [Azure Active Directory 租户和一个组织用户](create-an-azure-active-directory-tenant.md)。 如果尚未以租户中的用户身份注册 Power BI，则无法成功完成应用注册。
> 
> 

注册应用程序有两种方法。 第一种方法是使用 [Power BI 应用注册工具](https://dev.powerbi.com/apps/)，第二种方法是直接在 Azure 门户中注册。 Power BI 应用注册工具只需填充几个字段即可，是最简单的注册方式。 若要更改应用，请使用 Azure 门户。

## <a name="register-with-the-power-bi-app-registration-tool"></a>使用 Power BI 应用注册工具注册
需要在 **Azure Active Directory** 中注册你的应用程序，以便为应用程序建立标识，并指定对 Power BI REST 资源的权限。 注册控制台应用或网站等应用程序时，你会收到一个标识符，应用程序使用该标识符向被请求权限的用户标识自己的身份。

下面介绍如何使用 Power BI 应用注册工具注册应用程序：

1. 转到 [dev.powerbi.com/apps](https://dev.powerbi.com/apps)。
2. 选择“使用现有帐户登录”。
3. 提供“应用名称”。
4. 应用类型选择将取决于你使用的应用程序的类型。
   
   * 对 Web 应用或 Web API 使用“服务器端 Web 应用”。
   * 对在客户端设备上运行的应用使用“本机应用”。 ***若要为客户嵌入内容，而不考虑实际应用，也请选择“原生应用”。甚至对于 Web 应用，也是如此。***
5. 为“重定向 URL”和“主页 URL”输入一个值。 任何有效的 URL 都可用。
   
    只有将应用程序类型选择为“服务器端 Web 应用”，“主页 URL”才可用。
   
    对于“为客户嵌入内容”和 integrate-dashboard-web-app 示例，重定向 URL 为 `http://localhost:13526/redirect`。 对于报表和磁贴示例，重定向 URL 为 `http://localhost:13526/`。
6. 选择此应用程序将有权访问的 API。 有关 Power BI 访问权限的详细信息，请参阅 [Power BI 权限](power-bi-permissions.md)。
   
    ![](media/register-app/app-registration-apis.png)
7. 选择“注册应用”。
   
    你将收到一个“客户端 ID”。 如果选择“服务器端 Web 应用”，还会收到“客户端密码”。 如有需要，稍后可以从 Azure 门户中检索客户端 ID。 如果忘记了客户端密码，将需要在 Azure 门户中新建一个密码。

现在，可以将注册的应用用作自定义应用的一部分，从而与 Power BI 服务进行交互。

> [!IMPORTANT]
> 若要为客户嵌入内容，需要在 Azure 门户中配置其他权限。 有关详细信息，请参阅[向应用授予权限](#apply-permissions-to-your-application)。
> 
> 

## <a name="register-with-the-azure-portal"></a>使用 Azure 门户注册
注册应用程序还有另一种选择，即直接在 Azure 门户中注册。 请按照下列步骤注册你的应用程序。

1. 接受 [Microsoft Power BI API 条款](https://powerbi.microsoft.com/api-terms)。
2. 登录到 [Azure 门户](https://portal.azure.com)。
3. 在页面右上角选择你的帐户，从而选择你的 Azure AD 租户。
4. 在左侧导航窗格中，依次选择“更多服务”、“安全性 + 标识”下的“应用注册”和“新应用注册”。
   
    ![](media/register-app/azuread-new-app-registration.png)
5. 按照提示进行操作，并创建新的应用程序。
   
   * 对于 Web 应用，请输入“登录 URL”，即用户可以登录的应用基 URL（例如，http://localhost:13526）。
   * 对于本机应用程序，请提供“重定向 URI”，Azure AD 用其返回令牌响应。 输入应用的专属值（例如，http://myapplication/redirect）

有关如何在 Azure Active Directory 中注册应用程序的详细信息，请参阅 [Azure Active Directory 集成应用程序](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications)

## <a name="how-to-get-the-client-id"></a>如何获取客户端 ID
注册应用程序时，你将收到一个“客户端 ID”。  应用程序使用**客户端 ID** 向其请求权限的用户标识其自身。

下面介绍了如何获取客户端 ID：

1. 登录到 [Azure 门户](https://portal.azure.com)。
2. 在页面右上角选择你的帐户，从而选择你的 Azure AD 租户。
3. 在左侧导航栏中，选择依次“更多服务”和“应用注册”。
4. 选择需为其检索客户端 ID 的应用程序。
5. 此时，“应用 ID”列为 GUID。 这就是该应用程序的客户端 ID。
   
    ![“应用注册”内列为应用 ID 的客户端 ID](media/register-app/powerbi-embedded-app-registration-client-id.png)

## <a name="apply-permissions-to-your-application-within-azure-ad"></a>在 Azure AD 中向应用授予权限
> [!IMPORTANT]
> 此部分只适用于为组织嵌入内容的应用。
> 
> 

除了应用注册页中提供的权限之外，还需要对应用程序启用其他权限。 可以通过 Azure AD 门户或以编程方式完成此操作。

需要使用用于嵌入内容的主帐户登录，或使用全局管理员帐户登录。

### <a name="using-the-azure-ad-portal"></a>使用 Azure AD 门户
1. 在 Azure 门户中，转到[应用注册](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ApplicationsListBlade)，再选择要用于嵌入内容的应用。
   
    ![](media/register-app/powerbi-embedded-azuread-registered-apps.png)
2. 在“API 访问权限”下选择“所需权限”。
   
    ![](media/register-app/powerbi-embedded-azuread-app-required-permissions.png)
3. 选择“Windows Azure Active Directory”并请务必选中“以登录用户身份访问目录”。 选择“保存”。
   
    ![](media/register-app/powerbi-embedded-azuread-app-permissions01.png)
4. 在“所需权限”中，选择“Power BI 服务 (Power BI)”。
   
    ![](media/register-app/powerbi-embedded-azuread-app-permissions03.png)
   
   > [!NOTE]
   > 如果直接在 Azure AD 门户中创建了应用，可能看不到“Power BI 服务(Power BI)”。 如果不存在，请选择“+ 添加”，然后选择“1 选择和 API”。 在 API 列表中选择“Power BI 服务”，然后选择“选择”。  如果“+ 添加”中没有“Power BI 服务(Power BI)”，请至少使用一个用户注册 Power BI。
   > 
   > 
5. 选择“委派权限”下的所有权限。 需要逐一选中这些选项才能保存所做的选择。 完成时选择“保存”。
   
    ![](media/register-app/powerbi-embedded-azuread-app-permissions04.png)
6. 在“所需权限”中，选择“授予权限”。
   
    必须为“主帐户”调用“授予权限”操作，以免 Azure AD 提示提供内容。 如果执行此操作的帐户是全局管理员，将向组织内此应用的所有用户授予权限。 如果执行此操作的帐户是主帐户，而不是全局管理员，将仅向此应用的主帐户授予权限。
   
    ![“必需权限”对话框中的“授予权限”](media/register-app/powerbi-embedded-azuread-app-grant-permissions.png)

### <a name="applying-permissions-programmatically"></a>以编程方式应用权限
1. 需要获取租户中的现有服务主体（用户）。 有关如何执行该操作的信息，请参阅 [Get servicePrincipal](https://developer.microsoft.com/en-us/graph/docs/api-reference/beta/api/serviceprincipal_get)。
   
    你可以调用 *Get servicePrincipal* API 而无需使用 {id}，这将使你获取租户中的所有服务主体。
2. 使用作为 **appId** 属性的应用客户端 ID 检查服务主体。
3. 如果应用缺少服务计划，请新建一个。
   
    ```
    Post https://graph.microsoft.com/beta/servicePrincipals
    Authorization: Bearer ey..qw
    Content-Type: application/json
    {
    "accountEnabled" : true,
    "appId" : "{App_Client_ID}",
    "displayName" : "{App_DisplayName}"
    }
    ```
4. 向 Power BI API 授予应用权限
   
    ```
    Post https://graph.microsoft.com/beta/OAuth2PermissionGrants
    Authorization: Bearer ey..qw
    Content-Type: application/json
    { 
    "clientId":"{Service_Plan_ID}",
    "consentType":"AllPrincipals",
    "resourceId":"c78b2585-1df6-41de-95f7-dc5aeb7dc98e",
    "scope":"Dataset.ReadWrite.All Dashboard.Read.All Report.Read.All Group.Read Group.Read.All Content.Create Metadata.View_Any Dataset.Read.All Data.Alter_Any",
    "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
    "startTime":"2017-03-29T14:35:32.4933413+03:00"
    }
    ```
5. 向 AAD 授予应用权限
   
    “consentType”的值具体取决于执行请求的用户。 可以提供 AllPrincipals 或 Principal。 AllPrincipals 只能由管理员使用，用于向所有用户授予权限。 Principal 用于向特定用户授予权限。 
   
    必须为“主帐户”调用“授予权限”操作，以免 Azure AD 提示提供内容。 
   
    如果使用的是现有租户，并且不希望向所有租户用户授予权限，可以将 contentType 值替换为 Principal，向特定用户授予权限。
   
    ```
    Post https://graph.microsoft.com/beta/OAuth2PermissionGrants
    Authorization: Bearer ey..qw
    Content-Type: application/json
    { 
    "clientId":"{Service_Plan_ID}",
    "consentType":"AllPrincipals",
    "resourceId":"61e57743-d5cf-41ba-bd1a-2b381390a3f1",
    "scope":"User.Read Directory.AccessAsUser.All",
    "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
    "startTime":"2017-03-29T14:35:32.4933413+03:00"
    }
    ```

## <a name="next-steps"></a>后续步骤
至此，已在 Azure AD 中注册了应用，需要在应用中对用户进行身份验证了。 若要了解详细信息，请参阅[对用户进行身份验证，并获取 Power BI 应用的 Azure AD 访问令牌](get-azuread-access-token.md)。

更多问题？ [尝试咨询 Power BI 社区](http://community.powerbi.com/)

