---
title: Enumerar roleAssignments
description: Enumere las propiedades y las relaciones de los objetos roleAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 4b0aa8f8894ac378aa009f188887e31a4a5e1525
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808305"
---
# <a name="list-roleassignments"></a><span data-ttu-id="3ab55-103">Enumerar roleAssignments</span><span class="sxs-lookup"><span data-stu-id="3ab55-103">List roleAssignments</span></span>

> <span data-ttu-id="3ab55-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3ab55-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3ab55-105">Enumere las propiedades y las relaciones de los objetos [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3ab55-105">List properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3ab55-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3ab55-106">Prerequisites</span></span>
<span data-ttu-id="3ab55-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ab55-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3ab55-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ab55-109">Permission type</span></span>|<span data-ttu-id="3ab55-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ab55-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3ab55-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ab55-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3ab55-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="3ab55-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="3ab55-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ab55-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3ab55-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ab55-114">Not supported.</span></span>|
|<span data-ttu-id="3ab55-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ab55-115">Application</span></span>|<span data-ttu-id="3ab55-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ab55-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3ab55-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ab55-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="3ab55-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ab55-118">Request headers</span></span>
|<span data-ttu-id="3ab55-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ab55-119">Header</span></span>|<span data-ttu-id="3ab55-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3ab55-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3ab55-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3ab55-121">Authorization</span></span>|<span data-ttu-id="3ab55-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3ab55-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3ab55-123">Accept</span><span class="sxs-lookup"><span data-stu-id="3ab55-123">Accept</span></span>|<span data-ttu-id="3ab55-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3ab55-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3ab55-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3ab55-125">Request body</span></span>
<span data-ttu-id="3ab55-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3ab55-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3ab55-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ab55-127">Response</span></span>
<span data-ttu-id="3ab55-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos de [roleAssignment](../resources/intune-rbac-roleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ab55-128">If successful, this method returns a `200 OK` response code and a collection of [roleAssignment](../resources/intune-rbac-roleassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ab55-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ab55-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="3ab55-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ab55-130">Request</span></span>
<span data-ttu-id="3ab55-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ab55-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
```

### <a name="response"></a><span data-ttu-id="3ab55-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ab55-132">Response</span></span>
<span data-ttu-id="3ab55-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ab55-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 303

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.roleAssignment",
      "id": "b3234d24-4d24-b323-244d-23b3244d23b3",
      "displayName": "Display Name value",
      "description": "Description value",
      "resourceScopes": [
        "Resource Scopes value"
      ]
    }
  ]
}
```



