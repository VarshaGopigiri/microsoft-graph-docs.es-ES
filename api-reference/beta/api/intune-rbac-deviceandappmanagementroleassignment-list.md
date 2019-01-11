---
title: Enumerar deviceAndAppManagementRoleAssignments
description: Enumere las propiedades y las relaciones de los objetos deviceAndAppManagementRoleAssignment.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8dc9307ed69c977b3d312f63e3d2a1e1ed9814b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27848408"
---
# <a name="list-deviceandappmanagementroleassignments"></a><span data-ttu-id="d12ba-103">Enumerar deviceAndAppManagementRoleAssignments</span><span class="sxs-lookup"><span data-stu-id="d12ba-103">List deviceAndAppManagementRoleAssignments</span></span>

> <span data-ttu-id="d12ba-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d12ba-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d12ba-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d12ba-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d12ba-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d12ba-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d12ba-107">Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d12ba-107">List properties and relationships of the [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d12ba-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d12ba-108">Prerequisites</span></span>
<span data-ttu-id="d12ba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d12ba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d12ba-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d12ba-111">Permission type</span></span>|<span data-ttu-id="d12ba-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d12ba-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d12ba-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d12ba-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d12ba-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="d12ba-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="d12ba-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d12ba-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d12ba-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d12ba-116">Not supported.</span></span>|
|<span data-ttu-id="d12ba-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d12ba-117">Application</span></span>|<span data-ttu-id="d12ba-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d12ba-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d12ba-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d12ba-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="d12ba-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d12ba-120">Request headers</span></span>
|<span data-ttu-id="d12ba-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d12ba-121">Header</span></span>|<span data-ttu-id="d12ba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d12ba-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d12ba-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d12ba-123">Authorization</span></span>|<span data-ttu-id="d12ba-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d12ba-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d12ba-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d12ba-125">Accept</span></span>|<span data-ttu-id="d12ba-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d12ba-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d12ba-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d12ba-127">Request body</span></span>
<span data-ttu-id="d12ba-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d12ba-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d12ba-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d12ba-129">Response</span></span>
<span data-ttu-id="d12ba-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d12ba-130">If successful, this method returns a `200 OK` response code and a collection of [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d12ba-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d12ba-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="d12ba-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d12ba-132">Request</span></span>
<span data-ttu-id="d12ba-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d12ba-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/roleAssignments
```

### <a name="response"></a><span data-ttu-id="d12ba-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d12ba-134">Response</span></span>
<span data-ttu-id="d12ba-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d12ba-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 480

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
      "id": "a12e8ebb-8ebb-a12e-bb8e-2ea1bb8e2ea1",
      "displayName": "Display Name value",
      "description": "Description value",
      "scopeMembers": [
        "Scope Members value"
      ],
      "scopeType": "allDevices",
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





