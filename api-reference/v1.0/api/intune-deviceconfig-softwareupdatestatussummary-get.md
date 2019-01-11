---
title: Obtener softwareUpdateStatusSummary
description: Lea las propiedades y las relaciones del objeto softwareUpdateStatusSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3c03096e64b75df89f131a01344e1adb6a1bee44
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890275"
---
# <a name="get-softwareupdatestatussummary"></a><span data-ttu-id="9ec4f-103">Obtener softwareUpdateStatusSummary</span><span class="sxs-lookup"><span data-stu-id="9ec4f-103">Get softwareUpdateStatusSummary</span></span>

> <span data-ttu-id="9ec4f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ec4f-105">Lea las propiedades y las relaciones del objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md).</span><span class="sxs-lookup"><span data-stu-id="9ec4f-105">Read properties and relationships of the [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9ec4f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9ec4f-106">Prerequisites</span></span>
<span data-ttu-id="9ec4f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9ec4f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9ec4f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ec4f-109">Permission type</span></span>|<span data-ttu-id="9ec4f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ec4f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9ec4f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ec4f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9ec4f-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9ec4f-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9ec4f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ec4f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9ec4f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-114">Not supported.</span></span>|
|<span data-ttu-id="9ec4f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ec4f-115">Application</span></span>|<span data-ttu-id="9ec4f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9ec4f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ec4f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/softwareUpdateStatusSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9ec4f-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9ec4f-118">Optional query parameters</span></span>
<span data-ttu-id="9ec4f-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9ec4f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ec4f-120">Request headers</span></span>
|<span data-ttu-id="9ec4f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9ec4f-121">Header</span></span>|<span data-ttu-id="9ec4f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ec4f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9ec4f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9ec4f-123">Authorization</span></span>|<span data-ttu-id="9ec4f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9ec4f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="9ec4f-125">Accept</span></span>|<span data-ttu-id="9ec4f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9ec4f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ec4f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ec4f-127">Request body</span></span>
<span data-ttu-id="9ec4f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9ec4f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ec4f-129">Response</span></span>
<span data-ttu-id="9ec4f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-130">If successful, this method returns a `200 OK` response code and [softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ec4f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ec4f-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="9ec4f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ec4f-132">Request</span></span>
<span data-ttu-id="9ec4f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/softwareUpdateStatusSummary
```

### <a name="response"></a><span data-ttu-id="9ec4f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ec4f-134">Response</span></span>
<span data-ttu-id="9ec4f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9ec4f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 620

{
  "value": {
    "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
    "id": "4f71421f-421f-4f71-1f42-714f1f42714f",
    "displayName": "Display Name value",
    "compliantDeviceCount": 4,
    "nonCompliantDeviceCount": 7,
    "remediatedDeviceCount": 5,
    "errorDeviceCount": 0,
    "unknownDeviceCount": 2,
    "conflictDeviceCount": 3,
    "notApplicableDeviceCount": 8,
    "compliantUserCount": 2,
    "nonCompliantUserCount": 5,
    "remediatedUserCount": 3,
    "errorUserCount": 14,
    "unknownUserCount": 0,
    "conflictUserCount": 1,
    "notApplicableUserCount": 6
  }
}
```



