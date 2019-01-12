---
title: acción updateDeviceProfileAssignment
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 92eadbdc08d89c01a86cdd0e6e030d92332c9b9e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975347"
---
# <a name="updatedeviceprofileassignment-action"></a><span data-ttu-id="06476-103">acción updateDeviceProfileAssignment</span><span class="sxs-lookup"><span data-stu-id="06476-103">updateDeviceProfileAssignment action</span></span>

> <span data-ttu-id="06476-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06476-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06476-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06476-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="06476-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06476-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06476-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="06476-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="06476-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="06476-108">Prerequisites</span></span>
<span data-ttu-id="06476-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06476-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06476-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06476-111">Permission type</span></span>|<span data-ttu-id="06476-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06476-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="06476-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06476-113">Delegated (work or school account)</span></span>|<span data-ttu-id="06476-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06476-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="06476-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06476-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06476-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06476-116">Not supported.</span></span>|
|<span data-ttu-id="06476-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06476-117">Application</span></span>|<span data-ttu-id="06476-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06476-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06476-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06476-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}/updateDeviceProfileAssignment
```

## <a name="request-headers"></a><span data-ttu-id="06476-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06476-120">Request headers</span></span>
|<span data-ttu-id="06476-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06476-121">Header</span></span>|<span data-ttu-id="06476-122">Valor</span><span class="sxs-lookup"><span data-stu-id="06476-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06476-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="06476-123">Authorization</span></span>|<span data-ttu-id="06476-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="06476-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06476-125">Accept</span><span class="sxs-lookup"><span data-stu-id="06476-125">Accept</span></span>|<span data-ttu-id="06476-126">application/json</span><span class="sxs-lookup"><span data-stu-id="06476-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06476-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06476-127">Request body</span></span>
<span data-ttu-id="06476-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="06476-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="06476-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="06476-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="06476-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06476-130">Property</span></span>|<span data-ttu-id="06476-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="06476-131">Type</span></span>|<span data-ttu-id="06476-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="06476-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="06476-133">DeviceID</span><span class="sxs-lookup"><span data-stu-id="06476-133">deviceIds</span></span>|<span data-ttu-id="06476-134">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="06476-134">String collection</span></span>|<span data-ttu-id="06476-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="06476-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="06476-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06476-136">Response</span></span>
<span data-ttu-id="06476-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="06476-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="06476-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06476-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="06476-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06476-139">Request</span></span>
<span data-ttu-id="06476-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06476-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles/{enrollmentProfileId}/updateDeviceProfileAssignment

Content-type: application/json
Content-length: 51

{
  "deviceIds": [
    "Device Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="06476-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06476-141">Response</span></span>
<span data-ttu-id="06476-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06476-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





