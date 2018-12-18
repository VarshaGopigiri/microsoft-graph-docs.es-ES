---
title: Obtener deviceConfigurationDeviceOverview
description: Lea las propiedades y las relaciones del objeto deviceConfigurationDeviceOverview.
author: tfitzmac
ms.openlocfilehash: 663c6e4d83b6f573910ba92886d7869840c34265
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344978"
---
# <a name="get-deviceconfigurationdeviceoverview"></a><span data-ttu-id="f717b-103">Obtener deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="f717b-103">Get deviceConfigurationDeviceOverview</span></span>

> <span data-ttu-id="f717b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f717b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f717b-105">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f717b-105">Read properties and relationships of the [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f717b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f717b-106">Prerequisites</span></span>
<span data-ttu-id="f717b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f717b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f717b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f717b-109">Permission type</span></span>|<span data-ttu-id="f717b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f717b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f717b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f717b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f717b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f717b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f717b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f717b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f717b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f717b-114">Not supported.</span></span>|
|<span data-ttu-id="f717b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f717b-115">Application</span></span>|<span data-ttu-id="f717b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f717b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f717b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f717b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f717b-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f717b-118">Optional query parameters</span></span>
<span data-ttu-id="f717b-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f717b-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f717b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f717b-120">Request headers</span></span>
|<span data-ttu-id="f717b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f717b-121">Header</span></span>|<span data-ttu-id="f717b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f717b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f717b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f717b-123">Authorization</span></span>|<span data-ttu-id="f717b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f717b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f717b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f717b-125">Accept</span></span>|<span data-ttu-id="f717b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f717b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f717b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f717b-127">Request body</span></span>
<span data-ttu-id="f717b-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f717b-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f717b-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f717b-129">Response</span></span>
<span data-ttu-id="f717b-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f717b-130">If successful, this method returns a `200 OK` response code and [deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f717b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f717b-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f717b-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f717b-132">Request</span></span>
<span data-ttu-id="f717b-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f717b-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

### <a name="response"></a><span data-ttu-id="f717b-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f717b-134">Response</span></span>
<span data-ttu-id="f717b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f717b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 370

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
    "id": "62d48e3a-8e3a-62d4-3a8e-d4623a8ed462",
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



