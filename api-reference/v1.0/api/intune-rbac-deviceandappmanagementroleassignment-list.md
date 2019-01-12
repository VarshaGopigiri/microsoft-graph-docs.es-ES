---
title: Enumerar deviceAndAppManagementRoleAssignments
description: Enumere las propiedades y las relaciones de los objetos deviceAndAppManagementRoleAssignment.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 62a68a75c9e1d8eb6bf78070be75d56fe0f9b7cb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984944"
---
# <a name="list-deviceandappmanagementroleassignments"></a><span data-ttu-id="f9617-103">Enumerar deviceAndAppManagementRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="f9617-103">List deviceAndAppManagementRoleAssignments</span></span>

> <span data-ttu-id="f9617-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9617-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9617-105">Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="f9617-105">List properties and relationships of the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9617-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9617-106">Prerequisites</span></span>
<span data-ttu-id="f9617-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9617-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9617-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9617-109">Permission type</span></span>|<span data-ttu-id="f9617-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9617-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9617-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9617-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f9617-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9617-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="f9617-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9617-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9617-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9617-114">Not supported.</span></span>|
|<span data-ttu-id="f9617-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9617-115">Application</span></span>|<span data-ttu-id="f9617-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9617-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9617-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9617-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="f9617-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9617-118">Request headers</span></span>
|<span data-ttu-id="f9617-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9617-119">Header</span></span>|<span data-ttu-id="f9617-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9617-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9617-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9617-121">Authorization</span></span>|<span data-ttu-id="f9617-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9617-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9617-123">Accept</span><span class="sxs-lookup"><span data-stu-id="f9617-123">Accept</span></span>|<span data-ttu-id="f9617-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f9617-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9617-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9617-125">Request body</span></span>
<span data-ttu-id="f9617-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9617-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9617-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9617-127">Response</span></span>
<span data-ttu-id="f9617-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9617-128">If successful, this method returns a `200 OK` response code and a collection of [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9617-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9617-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9617-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9617-130">Request</span></span>
<span data-ttu-id="f9617-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9617-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments
```

### <a name="response"></a><span data-ttu-id="f9617-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9617-132">Response</span></span>
<span data-ttu-id="f9617-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9617-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 380

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
      "id": "a12e8ebb-8ebb-a12e-bb8e-2ea1bb8e2ea1",
      "displayName": "Display Name value",
      "description": "Description value",
      "resourceScopes": [
        "Resource Scopes value"
      ],
      "members": [
        "Members value"
      ]
    }
  ]
}
```



