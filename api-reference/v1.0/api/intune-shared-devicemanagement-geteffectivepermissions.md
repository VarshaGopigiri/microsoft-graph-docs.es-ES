---
title: Función getEffectivePermissions
description: Recupera los permisos efectivos del usuario autenticado actualmente
author: tfitzmac
ms.openlocfilehash: 3d4b277b0a5a3d5cc0584b602ad28c2e2e96e2b5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317006"
---
# <a name="geteffectivepermissions-function"></a><span data-ttu-id="fbec8-103">Función getEffectivePermissions</span><span class="sxs-lookup"><span data-stu-id="fbec8-103">getEffectivePermissions function</span></span>

> <span data-ttu-id="fbec8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fbec8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fbec8-105">Recupera los permisos efectivos del usuario autenticado actualmente</span><span class="sxs-lookup"><span data-stu-id="fbec8-105">Retrieves the effective permissions of the currently authenticated user</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fbec8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fbec8-106">Prerequisites</span></span>
<span data-ttu-id="fbec8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fbec8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fbec8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbec8-109">Permission type</span></span>|<span data-ttu-id="fbec8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbec8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fbec8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbec8-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="fbec8-112">&nbsp;&nbsp; Control de acceso basado en roles</span><span class="sxs-lookup"><span data-stu-id="fbec8-112">&nbsp; &nbsp; Role-based access control</span></span> | <span data-ttu-id="fbec8-113">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="fbec8-113">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="fbec8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbec8-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fbec8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbec8-115">Not supported.</span></span>|
|<span data-ttu-id="fbec8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbec8-116">Application</span></span>|<span data-ttu-id="fbec8-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbec8-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fbec8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbec8-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/getEffectivePermissions
```

## <a name="request-headers"></a><span data-ttu-id="fbec8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec8-119">Request headers</span></span>
|<span data-ttu-id="fbec8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbec8-120">Header</span></span>|<span data-ttu-id="fbec8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fbec8-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fbec8-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="fbec8-122">Authorization</span></span>|<span data-ttu-id="fbec8-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fbec8-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fbec8-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fbec8-124">Accept</span></span>|<span data-ttu-id="fbec8-125">application/json</span><span class="sxs-lookup"><span data-stu-id="fbec8-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fbec8-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec8-126">Request body</span></span>
<span data-ttu-id="fbec8-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="fbec8-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="fbec8-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="fbec8-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="fbec8-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fbec8-129">Property</span></span>|<span data-ttu-id="fbec8-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="fbec8-130">Type</span></span>|<span data-ttu-id="fbec8-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbec8-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fbec8-132">scope</span><span class="sxs-lookup"><span data-stu-id="fbec8-132">scope</span></span>|<span data-ttu-id="fbec8-133">String</span><span class="sxs-lookup"><span data-stu-id="fbec8-133">String</span></span>|<span data-ttu-id="fbec8-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="fbec8-134">Not yet documented</span></span>|


## <a name="response"></a><span data-ttu-id="fbec8-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbec8-135">Response</span></span>
<span data-ttu-id="fbec8-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [rolePermission](../resources/intune-rbac-rolepermission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbec8-136">If successful, this function returns a `200 OK` response code and a [rolePermission](../resources/intune-rbac-rolepermission.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fbec8-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbec8-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="fbec8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbec8-138">Request</span></span>
<span data-ttu-id="fbec8-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbec8-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/getEffectivePermissions(scope='parameterValue')
```

### <a name="response"></a><span data-ttu-id="fbec8-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbec8-140">Response</span></span>
<span data-ttu-id="fbec8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fbec8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 471

{
  "value": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "Actions value"
      ],
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
  ]
}
```



