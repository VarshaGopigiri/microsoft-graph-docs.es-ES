---
title: Enumerar windows81GeneralConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows81GeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 42e17464ab42dec12921b3e4db879d274b09e430
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880370"
---
# <a name="list-windows81generalconfigurations"></a><span data-ttu-id="e3fd8-103">Enumerar windows81GeneralConfigurations</span><span class="sxs-lookup"><span data-stu-id="e3fd8-103">List windows81GeneralConfigurations</span></span>

> <span data-ttu-id="e3fd8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3fd8-105">Enumere las propiedades y las relaciones de los objetos [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e3fd8-105">List properties and relationships of the [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e3fd8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e3fd8-106">Prerequisites</span></span>
<span data-ttu-id="e3fd8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3fd8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3fd8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3fd8-109">Permission type</span></span>|<span data-ttu-id="e3fd8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3fd8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e3fd8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3fd8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e3fd8-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="e3fd8-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="e3fd8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3fd8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e3fd8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-114">Not supported.</span></span>|
|<span data-ttu-id="e3fd8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3fd8-115">Application</span></span>|<span data-ttu-id="e3fd8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e3fd8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3fd8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="e3fd8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3fd8-118">Request headers</span></span>
|<span data-ttu-id="e3fd8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3fd8-119">Header</span></span>|<span data-ttu-id="e3fd8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3fd8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e3fd8-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e3fd8-121">Authorization</span></span>|<span data-ttu-id="e3fd8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e3fd8-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e3fd8-123">Accept</span></span>|<span data-ttu-id="e3fd8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e3fd8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3fd8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3fd8-125">Request body</span></span>
<span data-ttu-id="e3fd8-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e3fd8-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3fd8-127">Response</span></span>
<span data-ttu-id="e3fd8-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-128">If successful, this method returns a `200 OK` response code and a collection of [windows81GeneralConfiguration](../resources/intune-deviceconfig-windows81generalconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3fd8-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3fd8-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e3fd8-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3fd8-130">Request</span></span>
<span data-ttu-id="e3fd8-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="e3fd8-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3fd8-132">Response</span></span>
<span data-ttu-id="e3fd8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3fd8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2058

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windows81GeneralConfiguration",
      "id": "0e9285b5-85b5-0e92-b585-920eb585920e",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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
      "updatesRequireAutomaticUpdates": true,
      "userAccountControlSettings": "alwaysNotify",
      "workFoldersUrl": "https://example.com/workFoldersUrl/"
    }
  ]
}
```



