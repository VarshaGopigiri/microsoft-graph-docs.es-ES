---
title: Enumerar deviceAndAppManagementRoleDefinitions
description: Enumere las propiedades y las relaciones de los objetos deviceAndAppManagementRoleDefinition.
ms.openlocfilehash: 5cefb4694c3faf481ac6122356e879ec103469a1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030347"
---
# <a name="list-deviceandappmanagementroledefinitions"></a><span data-ttu-id="4cd62-103">Enumerar deviceAndAppManagementRoleDefinitions</span><span class="sxs-lookup"><span data-stu-id="4cd62-103">List deviceAndAppManagementRoleDefinitions</span></span>

> <span data-ttu-id="4cd62-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4cd62-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4cd62-105">Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="4cd62-105">List properties and relationships of the [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4cd62-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4cd62-106">Prerequisites</span></span>
<span data-ttu-id="4cd62-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4cd62-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4cd62-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4cd62-109">Permission type</span></span>|<span data-ttu-id="4cd62-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4cd62-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4cd62-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4cd62-111">Delegated (work or school account)</span></span>|<span data-ttu-id="4cd62-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="4cd62-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="4cd62-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4cd62-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4cd62-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4cd62-114">Not supported.</span></span>|
|<span data-ttu-id="4cd62-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4cd62-115">Application</span></span>|<span data-ttu-id="4cd62-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4cd62-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4cd62-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4cd62-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="4cd62-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4cd62-118">Request headers</span></span>
|<span data-ttu-id="4cd62-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cd62-119">Header</span></span>|<span data-ttu-id="4cd62-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4cd62-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4cd62-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="4cd62-121">Authorization</span></span>|<span data-ttu-id="4cd62-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4cd62-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4cd62-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4cd62-123">Accept</span></span>|<span data-ttu-id="4cd62-124">application/json</span><span class="sxs-lookup"><span data-stu-id="4cd62-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4cd62-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4cd62-125">Request body</span></span>
<span data-ttu-id="4cd62-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4cd62-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4cd62-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cd62-127">Response</span></span>
<span data-ttu-id="4cd62-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4cd62-128">If successful, this method returns a `200 OK` response code and a collection of [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4cd62-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4cd62-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="4cd62-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4cd62-130">Request</span></span>
<span data-ttu-id="4cd62-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4cd62-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions
```

### <a name="response"></a><span data-ttu-id="4cd62-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4cd62-132">Response</span></span>
<span data-ttu-id="4cd62-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4cd62-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 768

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
      "id": "bca1dfb5-dfb5-bca1-b5df-a1bcb5dfa1bc",
      "displayName": "Display Name value",
      "description": "Description value",
      "rolePermissions": [
        {
          "@odata.type": "microsoft.graph.rolePermission",
          "resourceActions": [
            {
              "@odata.type": "microsoft.graph.resourceAction",
              "allowedResourceActions": [
                "Allowed Resource Actions value"
              ],
              "notAllowedResourceActions": [
                "Not Allowed Resource Actions value"
              ]
            }
          ]
        }
      ],
      "isBuiltIn": true
    }
  ]
}
```



