---
title: Enumerar windowsUpdateForBusinessConfigurations
description: Enumere las propiedades y las relaciones de los objetos windowsUpdateForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4bcc2ffd2d39bd9b759578fd8786fc0675555e95
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889064"
---
# <a name="list-windowsupdateforbusinessconfigurations"></a><span data-ttu-id="6f817-103">Enumerar windowsUpdateForBusinessConfigurations</span><span class="sxs-lookup"><span data-stu-id="6f817-103">List windowsUpdateForBusinessConfigurations</span></span>

> <span data-ttu-id="6f817-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6f817-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6f817-105">Enumere las propiedades y las relaciones de los objetos [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="6f817-105">List properties and relationships of the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6f817-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6f817-106">Prerequisites</span></span>
<span data-ttu-id="6f817-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6f817-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6f817-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f817-109">Permission type</span></span>|<span data-ttu-id="6f817-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f817-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6f817-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f817-111">Delegated (work or school account)</span></span>|<span data-ttu-id="6f817-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="6f817-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="6f817-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f817-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6f817-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f817-114">Not supported.</span></span>|
|<span data-ttu-id="6f817-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f817-115">Application</span></span>|<span data-ttu-id="6f817-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f817-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6f817-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f817-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="6f817-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f817-118">Request headers</span></span>
|<span data-ttu-id="6f817-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f817-119">Header</span></span>|<span data-ttu-id="6f817-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6f817-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6f817-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="6f817-121">Authorization</span></span>|<span data-ttu-id="6f817-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6f817-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6f817-123">Accept</span><span class="sxs-lookup"><span data-stu-id="6f817-123">Accept</span></span>|<span data-ttu-id="6f817-124">application/json</span><span class="sxs-lookup"><span data-stu-id="6f817-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6f817-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f817-125">Request body</span></span>
<span data-ttu-id="6f817-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6f817-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6f817-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f817-127">Response</span></span>
<span data-ttu-id="6f817-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f817-128">If successful, this method returns a `200 OK` response code and a collection of [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f817-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f817-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="6f817-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f817-130">Request</span></span>
<span data-ttu-id="6f817-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f817-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="6f817-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f817-132">Response</span></span>
<span data-ttu-id="6f817-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f817-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1211

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
      "id": "4928dd6a-dd6a-4928-6add-28496add2849",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "deliveryOptimizationMode": "httpOnly",
      "prereleaseFeatures": "settingsOnly",
      "automaticUpdateMode": "notifyDownload",
      "microsoftUpdateServiceAllowed": true,
      "driversExcluded": true,
      "installationSchedule": {
        "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
        "scheduledInstallDay": "everyday",
        "scheduledInstallTime": "11:59:31.3170000"
      },
      "qualityUpdatesDeferralPeriodInDays": 2,
      "featureUpdatesDeferralPeriodInDays": 2,
      "qualityUpdatesPaused": true,
      "featureUpdatesPaused": true,
      "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
      "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
      "businessReadyUpdatesOnly": "all"
    }
  ]
}
```



