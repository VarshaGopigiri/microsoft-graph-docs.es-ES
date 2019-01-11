---
title: Obtener windowsUpdateForBusinessConfiguration
description: Lea las propiedades y las relaciones del objeto windowsUpdateForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b13f12c48d9a3bf5fdfc8d50874be07906b39220
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809264"
---
# <a name="get-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="06ace-103">Obtener windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="06ace-103">Get windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="06ace-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06ace-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06ace-105">Lea las propiedades y las relaciones del objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="06ace-105">Read properties and relationships of the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="06ace-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="06ace-106">Prerequisites</span></span>
<span data-ttu-id="06ace-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06ace-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06ace-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06ace-109">Permission type</span></span>|<span data-ttu-id="06ace-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06ace-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="06ace-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06ace-111">Delegated (work or school account)</span></span>|<span data-ttu-id="06ace-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="06ace-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="06ace-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06ace-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06ace-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06ace-114">Not supported.</span></span>|
|<span data-ttu-id="06ace-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06ace-115">Application</span></span>|<span data-ttu-id="06ace-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06ace-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06ace-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06ace-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="06ace-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="06ace-118">Optional query parameters</span></span>
<span data-ttu-id="06ace-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06ace-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="06ace-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06ace-120">Request headers</span></span>
|<span data-ttu-id="06ace-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06ace-121">Header</span></span>|<span data-ttu-id="06ace-122">Valor</span><span class="sxs-lookup"><span data-stu-id="06ace-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06ace-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="06ace-123">Authorization</span></span>|<span data-ttu-id="06ace-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="06ace-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06ace-125">Accept</span><span class="sxs-lookup"><span data-stu-id="06ace-125">Accept</span></span>|<span data-ttu-id="06ace-126">application/json</span><span class="sxs-lookup"><span data-stu-id="06ace-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06ace-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06ace-127">Request body</span></span>
<span data-ttu-id="06ace-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="06ace-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="06ace-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06ace-129">Response</span></span>
<span data-ttu-id="06ace-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06ace-130">If successful, this method returns a `200 OK` response code and [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06ace-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06ace-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="06ace-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06ace-132">Request</span></span>
<span data-ttu-id="06ace-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06ace-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="06ace-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06ace-134">Response</span></span>
<span data-ttu-id="06ace-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06ace-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1149

{
  "value": {
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
}
```



