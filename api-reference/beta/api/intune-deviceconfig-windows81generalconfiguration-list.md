---
title: Enumerar windows81GeneralConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows81GeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 219ca47840efe36bbe9ebd00ad92669a1a76391b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924135"
---
# <a name="list-windows81generalconfigurations"></a><span data-ttu-id="45ced-103">Enumerar windows81GeneralConfigurations</span><span class="sxs-lookup"><span data-stu-id="45ced-103">List windows81GeneralConfigurations</span></span>

> <span data-ttu-id="45ced-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45ced-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45ced-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45ced-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="45ced-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="45ced-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="45ced-107">Enumere las propiedades y las relaciones de los objetos [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="45ced-107">List properties and relationships of the [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="45ced-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="45ced-108">Prerequisites</span></span>
<span data-ttu-id="45ced-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="45ced-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="45ced-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="45ced-111">Permission type</span></span>|<span data-ttu-id="45ced-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="45ced-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="45ced-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="45ced-113">Delegated (work or school account)</span></span>|<span data-ttu-id="45ced-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="45ced-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="45ced-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="45ced-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="45ced-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45ced-116">Not supported.</span></span>|
|<span data-ttu-id="45ced-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="45ced-117">Application</span></span>|<span data-ttu-id="45ced-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="45ced-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="45ced-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="45ced-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="45ced-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="45ced-120">Request headers</span></span>
|<span data-ttu-id="45ced-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45ced-121">Header</span></span>|<span data-ttu-id="45ced-122">Valor</span><span class="sxs-lookup"><span data-stu-id="45ced-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="45ced-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="45ced-123">Authorization</span></span>|<span data-ttu-id="45ced-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="45ced-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="45ced-125">Accept</span><span class="sxs-lookup"><span data-stu-id="45ced-125">Accept</span></span>|<span data-ttu-id="45ced-126">application/json</span><span class="sxs-lookup"><span data-stu-id="45ced-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="45ced-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="45ced-127">Request body</span></span>
<span data-ttu-id="45ced-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="45ced-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="45ced-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45ced-129">Response</span></span>
<span data-ttu-id="45ced-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="45ced-130">If successful, this method returns a `200 OK` response code and a collection of [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="45ced-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="45ced-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="45ced-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="45ced-132">Request</span></span>
<span data-ttu-id="45ced-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="45ced-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="45ced-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="45ced-134">Response</span></span>
<span data-ttu-id="45ced-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="45ced-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2313

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
      "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "accountsBlockAddingNonMicrosoftAccountEmail": true,
      "applyOnlyToWindows81": true,
      "browserBlockAutofill": true,
      "browserBlockAutomaticDetectionOfIntranetSites": true,
      "browserBlockEnterpriseModeAccess": true,
      "browserBlockJavaScript": true,
      "browserBlockPlugins": true,
      "browserBlockPopups": true,
      "browserBlockSendingDoNotTrackHeader": true,
      "browserBlockSingleWordEntryOnIntranetSites": true,
      "browserRequireSmartScreen": true,
      "browserEnterpriseModeSiteListLocation": "Browser Enterprise Mode Site List Location value",
      "browserInternetSecurityLevel": "medium",
      "browserIntranetSecurityLevel": "low",
      "browserLoggingReportLocation": "Browser Logging Report Location value",
      "browserRequireHighSecurityForRestrictedSites": true,
      "browserRequireFirewall": true,
      "browserRequireFraudWarning": true,
      "browserTrustedSitesSecurityLevel": "low",
      "cellularBlockDataRoaming": true,
      "diagnosticsBlockDataSubmission": true,
      "passwordBlockPicturePasswordAndPin": true,
      "passwordExpirationDays": 6,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
      "passwordMinimumCharacterSetCount": 0,
      "passwordPreviousPasswordBlockCount": 2,
      "passwordRequiredType": "alphanumeric",
      "passwordSignInFailureCountBeforeFactoryReset": 12,
      "storageRequireDeviceEncryption": true,
      "minimumAutoInstallClassification": "recommendedAndImportant",
      "updatesMinimumAutoInstallClassification": "recommendedAndImportant",
      "updatesRequireAutomaticUpdates": true,
      "userAccountControlSettings": "alwaysNotify",
      "workFoldersUrl": "https://example.com/workFoldersUrl/"
    }
  ]
}
```





