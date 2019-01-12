---
title: Función getEffectivePermissions
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 978b615293e09d0f8b3f3c23fd17d3018fe17609
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973674"
---
# <a name="geteffectivepermissions-function"></a><span data-ttu-id="d72ea-103">Función getEffectivePermissions</span><span class="sxs-lookup"><span data-stu-id="d72ea-103">getEffectivePermissions function</span></span>

> <span data-ttu-id="d72ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d72ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d72ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d72ea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d72ea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d72ea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d72ea-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d72ea-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d72ea-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d72ea-108">Prerequisites</span></span>
<span data-ttu-id="d72ea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d72ea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d72ea-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d72ea-111">Permission type</span></span>|<span data-ttu-id="d72ea-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d72ea-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d72ea-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d72ea-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="d72ea-114">&nbsp;&nbsp; **Control de acceso basado en roles (RBAC)**</span><span class="sxs-lookup"><span data-stu-id="d72ea-114">&nbsp; &nbsp; **Role-based access control (RBAC)**</span></span> | <span data-ttu-id="d72ea-115">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="d72ea-115">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="d72ea-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d72ea-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d72ea-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d72ea-117">Not supported.</span></span>|
|<span data-ttu-id="d72ea-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d72ea-118">Application</span></span>|<span data-ttu-id="d72ea-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d72ea-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d72ea-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d72ea-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/getEffectivePermissions
```

## <a name="request-headers"></a><span data-ttu-id="d72ea-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d72ea-121">Request headers</span></span>
|<span data-ttu-id="d72ea-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d72ea-122">Header</span></span>|<span data-ttu-id="d72ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d72ea-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d72ea-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="d72ea-124">Authorization</span></span>|<span data-ttu-id="d72ea-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d72ea-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d72ea-126">Accept</span><span class="sxs-lookup"><span data-stu-id="d72ea-126">Accept</span></span>|<span data-ttu-id="d72ea-127">application/json</span><span class="sxs-lookup"><span data-stu-id="d72ea-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d72ea-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d72ea-128">Request body</span></span>
<span data-ttu-id="d72ea-129">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="d72ea-129">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="d72ea-130">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="d72ea-130">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="d72ea-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d72ea-131">Property</span></span>|<span data-ttu-id="d72ea-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="d72ea-132">Type</span></span>|<span data-ttu-id="d72ea-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="d72ea-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d72ea-134">scope</span><span class="sxs-lookup"><span data-stu-id="d72ea-134">scope</span></span>|<span data-ttu-id="d72ea-135">String</span><span class="sxs-lookup"><span data-stu-id="d72ea-135">String</span></span>|<span data-ttu-id="d72ea-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="d72ea-136">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="d72ea-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d72ea-137">Response</span></span>
<span data-ttu-id="d72ea-138">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [rolePermission](../resources/intune-rbac-rolepermission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d72ea-138">If successful, this function returns a `200 OK` response code and a [rolePermission](../resources/intune-rbac-rolepermission.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d72ea-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d72ea-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="d72ea-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d72ea-140">Request</span></span>
<span data-ttu-id="d72ea-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d72ea-141">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/getEffectivePermissions(scope='parameterValue')
```

### <a name="response"></a><span data-ttu-id="d72ea-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d72ea-142">Response</span></span>
<span data-ttu-id="d72ea-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d72ea-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



