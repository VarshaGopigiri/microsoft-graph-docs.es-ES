---
title: Obtener roleDefinition
description: Lea las propiedades y las relaciones del objeto roleDefinition.
author: tfitzmac
ms.openlocfilehash: 77087011f30f5cdc261074bc58e1afe48a3f9d27
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27303314"
---
# <a name="get-roledefinition"></a><span data-ttu-id="eaa53-103">Obtener roleDefinition</span><span class="sxs-lookup"><span data-stu-id="eaa53-103">Get roleDefinition</span></span>

> <span data-ttu-id="eaa53-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eaa53-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eaa53-105">Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="eaa53-105">Read properties and relationships of the [roleDefinition](../resources/intune-rbac-roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eaa53-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eaa53-106">Prerequisites</span></span>
<span data-ttu-id="eaa53-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eaa53-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eaa53-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eaa53-109">Permission type</span></span>|<span data-ttu-id="eaa53-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eaa53-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eaa53-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eaa53-111">Delegated (work or school account)</span></span>|<span data-ttu-id="eaa53-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="eaa53-112">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="eaa53-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eaa53-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eaa53-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaa53-114">Not supported.</span></span>|
|<span data-ttu-id="eaa53-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eaa53-115">Application</span></span>|<span data-ttu-id="eaa53-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaa53-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eaa53-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eaa53-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleDefinitions/{roleDefinitionId}
GET /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/roleDefinition
```

## <a name="optional-query-parameters"></a><span data-ttu-id="eaa53-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="eaa53-118">Optional query parameters</span></span>
<span data-ttu-id="eaa53-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaa53-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="eaa53-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa53-120">Request headers</span></span>
|<span data-ttu-id="eaa53-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eaa53-121">Header</span></span>|<span data-ttu-id="eaa53-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eaa53-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eaa53-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="eaa53-123">Authorization</span></span>|<span data-ttu-id="eaa53-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eaa53-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eaa53-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eaa53-125">Accept</span></span>|<span data-ttu-id="eaa53-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eaa53-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eaa53-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa53-127">Request body</span></span>
<span data-ttu-id="eaa53-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="eaa53-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="eaa53-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaa53-129">Response</span></span>
<span data-ttu-id="eaa53-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de [roleDefinition](../resources/intune-rbac-roledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaa53-130">If successful, this method returns a `200 OK` response code and [roleDefinition](../resources/intune-rbac-roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eaa53-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eaa53-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="eaa53-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa53-132">Request</span></span>
<span data-ttu-id="eaa53-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaa53-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}
```

### <a name="response"></a><span data-ttu-id="eaa53-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaa53-134">Response</span></span>
<span data-ttu-id="eaa53-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eaa53-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 690

{
  "value": {
    "@odata.type": "#microsoft.graph.roleDefinition",
    "id": "70fdcd08-cd08-70fd-08cd-fd7008cdfd70",
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
}
```



