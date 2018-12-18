---
title: Obtener roleAssignment
description: Lea las propiedades y las relaciones del objeto roleAssignment.
author: tfitzmac
ms.openlocfilehash: 916e673da74f9da0fe8d678e2d8f763ac9842cae
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360910"
---
# <a name="get-roleassignment"></a><span data-ttu-id="1dfeb-103">Obtener roleAssignment</span><span class="sxs-lookup"><span data-stu-id="1dfeb-103">Get roleAssignment</span></span>

> <span data-ttu-id="1dfeb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1dfeb-105">Lea las propiedades y las relaciones del objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="1dfeb-105">Read properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1dfeb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1dfeb-106">Prerequisites</span></span>
<span data-ttu-id="1dfeb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1dfeb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1dfeb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1dfeb-109">Permission type</span></span>|<span data-ttu-id="1dfeb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1dfeb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1dfeb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1dfeb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1dfeb-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="1dfeb-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="1dfeb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1dfeb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1dfeb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-114">Not supported.</span></span>|
|<span data-ttu-id="1dfeb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1dfeb-115">Application</span></span>|<span data-ttu-id="1dfeb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1dfeb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1dfeb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1dfeb-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1dfeb-118">Optional query parameters</span></span>
<span data-ttu-id="1dfeb-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1dfeb-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1dfeb-120">Request headers</span></span>
|<span data-ttu-id="1dfeb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dfeb-121">Header</span></span>|<span data-ttu-id="1dfeb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1dfeb-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1dfeb-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="1dfeb-123">Authorization</span></span>|<span data-ttu-id="1dfeb-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1dfeb-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1dfeb-125">Accept</span></span>|<span data-ttu-id="1dfeb-126">application/json</span><span class="sxs-lookup"><span data-stu-id="1dfeb-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1dfeb-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1dfeb-127">Request body</span></span>
<span data-ttu-id="1dfeb-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1dfeb-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1dfeb-129">Response</span></span>
<span data-ttu-id="1dfeb-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [roleAssignment](../resources/intune-rbac-roleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-130">If successful, this method returns a `200 OK` response code and [roleAssignment](../resources/intune-rbac-roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1dfeb-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1dfeb-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="1dfeb-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1dfeb-132">Request</span></span>
<span data-ttu-id="1dfeb-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}
```

### <a name="response"></a><span data-ttu-id="1dfeb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1dfeb-134">Response</span></span>
<span data-ttu-id="1dfeb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1dfeb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 275

{
  "value": {
    "@odata.type": "#microsoft.graph.roleAssignment",
    "id": "b3234d24-4d24-b323-244d-23b3244d23b3",
    "displayName": "Display Name value",
    "description": "Description value",
    "resourceScopes": [
      "Resource Scopes value"
    ]
  }
}
```



