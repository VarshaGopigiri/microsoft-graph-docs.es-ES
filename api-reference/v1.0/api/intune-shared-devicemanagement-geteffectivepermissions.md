---
title: Función getEffectivePermissions
description: Recupera los permisos efectivos del usuario autenticado actualmente
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: f40412a8d95fd6bde17843b0c13e81f00459dd12
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980079"
---
# <a name="geteffectivepermissions-function"></a><span data-ttu-id="b9e1b-103">Función getEffectivePermissions</span><span class="sxs-lookup"><span data-stu-id="b9e1b-103">getEffectivePermissions function</span></span>

> <span data-ttu-id="b9e1b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b9e1b-105">Recupera los permisos efectivos del usuario autenticado actualmente</span><span class="sxs-lookup"><span data-stu-id="b9e1b-105">Retrieves the effective permissions of the currently authenticated user</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9e1b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9e1b-106">Prerequisites</span></span>
<span data-ttu-id="b9e1b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b9e1b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b9e1b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b9e1b-109">Permission type</span></span>|<span data-ttu-id="b9e1b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b9e1b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b9e1b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b9e1b-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="b9e1b-112">&nbsp;&nbsp; Control de acceso basado en roles</span><span class="sxs-lookup"><span data-stu-id="b9e1b-112">&nbsp; &nbsp; Role-based access control</span></span> | <span data-ttu-id="b9e1b-113">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="b9e1b-113">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="b9e1b-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b9e1b-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b9e1b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-115">Not supported.</span></span>|
|<span data-ttu-id="b9e1b-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b9e1b-116">Application</span></span>|<span data-ttu-id="b9e1b-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b9e1b-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9e1b-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/getEffectivePermissions
```

## <a name="request-headers"></a><span data-ttu-id="b9e1b-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9e1b-119">Request headers</span></span>
|<span data-ttu-id="b9e1b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9e1b-120">Header</span></span>|<span data-ttu-id="b9e1b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b9e1b-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b9e1b-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="b9e1b-122">Authorization</span></span>|<span data-ttu-id="b9e1b-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b9e1b-124">Accept</span><span class="sxs-lookup"><span data-stu-id="b9e1b-124">Accept</span></span>|<span data-ttu-id="b9e1b-125">application/json</span><span class="sxs-lookup"><span data-stu-id="b9e1b-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b9e1b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9e1b-126">Request body</span></span>
<span data-ttu-id="b9e1b-127">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-127">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="b9e1b-128">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-128">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="b9e1b-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9e1b-129">Property</span></span>|<span data-ttu-id="b9e1b-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9e1b-130">Type</span></span>|<span data-ttu-id="b9e1b-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9e1b-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b9e1b-132">scope</span><span class="sxs-lookup"><span data-stu-id="b9e1b-132">scope</span></span>|<span data-ttu-id="b9e1b-133">String</span><span class="sxs-lookup"><span data-stu-id="b9e1b-133">String</span></span>|<span data-ttu-id="b9e1b-134">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b9e1b-134">Not yet documented</span></span>|


## <a name="response"></a><span data-ttu-id="b9e1b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9e1b-135">Response</span></span>
<span data-ttu-id="b9e1b-136">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [rolePermission](../resources/intune-rbac-rolepermission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-136">If successful, this function returns a `200 OK` response code and a [rolePermission](../resources/intune-rbac-rolepermission.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b9e1b-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9e1b-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="b9e1b-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9e1b-138">Request</span></span>
<span data-ttu-id="b9e1b-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-139">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/getEffectivePermissions(scope='parameterValue')
```

### <a name="response"></a><span data-ttu-id="b9e1b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9e1b-140">Response</span></span>
<span data-ttu-id="b9e1b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9e1b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



