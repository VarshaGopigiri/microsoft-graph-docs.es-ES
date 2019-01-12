---
title: asignar acción
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 33bb8030df7118aed4f4f112bed1f31bc320b3f5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940375"
---
# <a name="assign-action"></a><span data-ttu-id="4699f-103">asignar acción</span><span class="sxs-lookup"><span data-stu-id="4699f-103">assign action</span></span>

> <span data-ttu-id="4699f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4699f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4699f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4699f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4699f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4699f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4699f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4699f-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4699f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4699f-108">Prerequisites</span></span>
<span data-ttu-id="4699f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4699f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4699f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4699f-111">Permission type</span></span>|<span data-ttu-id="4699f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4699f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4699f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4699f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4699f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4699f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4699f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4699f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4699f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4699f-116">Not supported.</span></span>|
|<span data-ttu-id="4699f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4699f-117">Application</span></span>|<span data-ttu-id="4699f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4699f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4699f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4699f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="4699f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4699f-120">Request headers</span></span>
|<span data-ttu-id="4699f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4699f-121">Header</span></span>|<span data-ttu-id="4699f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4699f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4699f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4699f-123">Authorization</span></span>|<span data-ttu-id="4699f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4699f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4699f-125">Accept</span><span class="sxs-lookup"><span data-stu-id="4699f-125">Accept</span></span>|<span data-ttu-id="4699f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4699f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4699f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4699f-127">Request body</span></span>
<span data-ttu-id="4699f-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="4699f-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="4699f-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="4699f-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="4699f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4699f-130">Property</span></span>|<span data-ttu-id="4699f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4699f-131">Type</span></span>|<span data-ttu-id="4699f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4699f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4699f-133">asignaciones</span><span class="sxs-lookup"><span data-stu-id="4699f-133">assignments</span></span>|<span data-ttu-id="4699f-134">colección de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)</span><span class="sxs-lookup"><span data-stu-id="4699f-134">[embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) collection</span></span>|<span data-ttu-id="4699f-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4699f-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="4699f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4699f-136">Response</span></span>
<span data-ttu-id="4699f-137">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y una colección de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4699f-137">If successful, this action returns a `200 OK` response code and a [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) collection in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4699f-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4699f-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="4699f-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4699f-139">Request</span></span>
<span data-ttu-id="4699f-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4699f-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/embeddedSIMActivationCodePools/{embeddedSIMActivationCodePoolId}/assign

Content-type: application/json
Content-length: 287

{
  "assignments": [
    {
      "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
      "id": "e7304dcc-4dcc-e730-cc4d-30e7cc4d30e7",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="4699f-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4699f-141">Response</span></span>
<span data-ttu-id="4699f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4699f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 281

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
      "id": "e7304dcc-4dcc-e730-cc4d-30e7cc4d30e7",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      }
    }
  ]
}
```





