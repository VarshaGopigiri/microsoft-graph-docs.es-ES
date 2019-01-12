---
title: Función getEffectivePermissions
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e8e91e35212d938426b875041f3226a2073a75be
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974654"
---
# <a name="geteffectivepermissions-function"></a><span data-ttu-id="37131-103">Función getEffectivePermissions</span><span class="sxs-lookup"><span data-stu-id="37131-103">getEffectivePermissions function</span></span>

> <span data-ttu-id="37131-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37131-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37131-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37131-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37131-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37131-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37131-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="37131-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="37131-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37131-108">Prerequisites</span></span>
<span data-ttu-id="37131-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37131-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37131-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37131-111">Permission type</span></span>|<span data-ttu-id="37131-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37131-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37131-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37131-113">Delegated (work or school account)</span></span>|<span data-ttu-id="37131-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="37131-114">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="37131-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37131-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37131-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37131-116">Not supported.</span></span>|
|<span data-ttu-id="37131-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37131-117">Application</span></span>|<span data-ttu-id="37131-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37131-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37131-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37131-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/getEffectivePermissions
```

## <a name="request-headers"></a><span data-ttu-id="37131-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37131-120">Request headers</span></span>
|<span data-ttu-id="37131-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37131-121">Header</span></span>|<span data-ttu-id="37131-122">Valor</span><span class="sxs-lookup"><span data-stu-id="37131-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37131-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="37131-123">Authorization</span></span>|<span data-ttu-id="37131-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37131-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37131-125">Accept</span><span class="sxs-lookup"><span data-stu-id="37131-125">Accept</span></span>|<span data-ttu-id="37131-126">application/json</span><span class="sxs-lookup"><span data-stu-id="37131-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37131-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37131-127">Request body</span></span>
<span data-ttu-id="37131-128">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="37131-128">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="37131-129">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="37131-129">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="37131-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37131-130">Property</span></span>|<span data-ttu-id="37131-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="37131-131">Type</span></span>|<span data-ttu-id="37131-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="37131-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37131-133">scope</span><span class="sxs-lookup"><span data-stu-id="37131-133">scope</span></span>|<span data-ttu-id="37131-134">String</span><span class="sxs-lookup"><span data-stu-id="37131-134">String</span></span>|<span data-ttu-id="37131-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="37131-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="37131-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37131-136">Response</span></span>
<span data-ttu-id="37131-137">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección [rolePermission](../resources/intune-rbac-rolepermission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37131-137">If successful, this function returns a `200 OK` response code and a [rolePermission](../resources/intune-rbac-rolepermission.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37131-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37131-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="37131-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37131-139">Request</span></span>
<span data-ttu-id="37131-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37131-140">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/getEffectivePermissions(scope='parameterValue')
```

### <a name="response"></a><span data-ttu-id="37131-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37131-141">Response</span></span>
<span data-ttu-id="37131-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37131-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





