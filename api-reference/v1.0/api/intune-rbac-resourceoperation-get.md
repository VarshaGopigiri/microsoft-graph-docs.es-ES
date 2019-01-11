---
title: Obtener resourceOperation
description: Lea las propiedades y las relaciones del objeto resourceOperation.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 97090b8a93a26d6e28689586602bb065bc7eaba6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27840624"
---
# <a name="get-resourceoperation"></a><span data-ttu-id="46eee-103">Obtener resourceOperation</span><span class="sxs-lookup"><span data-stu-id="46eee-103">Get resourceOperation</span></span>

> <span data-ttu-id="46eee-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46eee-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46eee-105">Lea las propiedades y las relaciones del objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="46eee-105">Read properties and relationships of the [resourceOperation](../resources/intune-rbac-resourceoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46eee-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46eee-106">Prerequisites</span></span>
<span data-ttu-id="46eee-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46eee-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46eee-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46eee-109">Permission type</span></span>|<span data-ttu-id="46eee-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46eee-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46eee-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46eee-111">Delegated (work or school account)</span></span>|<span data-ttu-id="46eee-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="46eee-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="46eee-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46eee-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46eee-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46eee-114">Not supported.</span></span>|
|<span data-ttu-id="46eee-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46eee-115">Application</span></span>|<span data-ttu-id="46eee-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46eee-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46eee-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46eee-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/resourceOperations/{resourceOperationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="46eee-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="46eee-118">Optional query parameters</span></span>
<span data-ttu-id="46eee-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46eee-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="46eee-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46eee-120">Request headers</span></span>
|<span data-ttu-id="46eee-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46eee-121">Header</span></span>|<span data-ttu-id="46eee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46eee-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46eee-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="46eee-123">Authorization</span></span>|<span data-ttu-id="46eee-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46eee-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46eee-125">Accept</span><span class="sxs-lookup"><span data-stu-id="46eee-125">Accept</span></span>|<span data-ttu-id="46eee-126">application/json</span><span class="sxs-lookup"><span data-stu-id="46eee-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46eee-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46eee-127">Request body</span></span>
<span data-ttu-id="46eee-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="46eee-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="46eee-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46eee-129">Response</span></span>
<span data-ttu-id="46eee-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46eee-130">If successful, this method returns a `200 OK` response code and [resourceOperation](../resources/intune-rbac-resourceoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46eee-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46eee-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="46eee-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46eee-132">Request</span></span>
<span data-ttu-id="46eee-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46eee-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/resourceOperations/{resourceOperationId}
```

### <a name="response"></a><span data-ttu-id="46eee-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46eee-134">Response</span></span>
<span data-ttu-id="46eee-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46eee-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 256

{
  "value": {
    "@odata.type": "#microsoft.graph.resourceOperation",
    "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
    "resourceName": "Resource Name value",
    "actionName": "Action Name value",
    "description": "Description value"
  }
}
```



