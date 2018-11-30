---
title: Obtener managedDeviceMobileAppConfigurationDeviceSummary
description: Lea las propiedades y las relaciones del objeto managedDeviceMobileAppConfigurationDeviceSummary.
ms.openlocfilehash: 810a65825e1e7932cabd0bacf023f2ef95392234
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032335"
---
# <a name="get-manageddevicemobileappconfigurationdevicesummary"></a><span data-ttu-id="e6174-103">Obtener managedDeviceMobileAppConfigurationDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="e6174-103">Get managedDeviceMobileAppConfigurationDeviceSummary</span></span>

> <span data-ttu-id="e6174-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6174-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6174-105">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="e6174-105">Read properties and relationships of the [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6174-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6174-106">Prerequisites</span></span>
<span data-ttu-id="e6174-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e6174-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e6174-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6174-109">Permission type</span></span>|<span data-ttu-id="e6174-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6174-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6174-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6174-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e6174-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="e6174-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="e6174-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6174-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6174-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6174-114">Not supported.</span></span>|
|<span data-ttu-id="e6174-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6174-115">Application</span></span>|<span data-ttu-id="e6174-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6174-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6174-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6174-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e6174-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e6174-118">Optional query parameters</span></span>
<span data-ttu-id="e6174-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6174-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e6174-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6174-120">Request headers</span></span>
|<span data-ttu-id="e6174-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6174-121">Header</span></span>|<span data-ttu-id="e6174-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e6174-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6174-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e6174-123">Authorization</span></span>|<span data-ttu-id="e6174-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6174-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e6174-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6174-125">Accept</span></span>|<span data-ttu-id="e6174-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e6174-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6174-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6174-127">Request body</span></span>
<span data-ttu-id="e6174-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e6174-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e6174-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6174-129">Response</span></span>
<span data-ttu-id="e6174-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6174-130">If successful, this method returns a `200 OK` response code and [managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6174-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6174-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6174-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6174-132">Request</span></span>
<span data-ttu-id="e6174-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6174-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatusSummary
```

### <a name="response"></a><span data-ttu-id="e6174-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6174-134">Response</span></span>
<span data-ttu-id="e6174-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6174-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 385

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceSummary",
    "id": "9997c455-c455-9997-55c4-979955c49799",
    "pendingCount": 12,
    "notApplicableCount": 2,
    "successCount": 12,
    "errorCount": 10,
    "failedCount": 11,
    "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
    "configurationVersion": 4
  }
}
```



