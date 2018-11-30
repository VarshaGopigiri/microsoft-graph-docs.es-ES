---
title: acción executeAction
description: Todavía no documentado
ms.openlocfilehash: 1358b95bbb61aaef71df44c87ab6aeb0bc210761
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090320"
---
# <a name="executeaction-action"></a><span data-ttu-id="bc8a0-103">acción executeAction</span><span class="sxs-lookup"><span data-stu-id="bc8a0-103">executeAction action</span></span>

> <span data-ttu-id="bc8a0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bc8a0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bc8a0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bc8a0-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bc8a0-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bc8a0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc8a0-108">Prerequisites</span></span>
<span data-ttu-id="bc8a0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc8a0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bc8a0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc8a0-111">Permission type</span></span>|<span data-ttu-id="bc8a0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc8a0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bc8a0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc8a0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="bc8a0-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="bc8a0-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="bc8a0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc8a0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bc8a0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-116">Not supported.</span></span>|
|<span data-ttu-id="bc8a0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc8a0-117">Application</span></span>|<span data-ttu-id="bc8a0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bc8a0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc8a0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/executeAction
POST /deviceManagement/managedDevices/executeAction
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/executeAction
```

## <a name="request-headers"></a><span data-ttu-id="bc8a0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc8a0-120">Request headers</span></span>
|<span data-ttu-id="bc8a0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc8a0-121">Header</span></span>|<span data-ttu-id="bc8a0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bc8a0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bc8a0-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc8a0-123">Authorization</span></span>|<span data-ttu-id="bc8a0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bc8a0-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bc8a0-125">Accept</span></span>|<span data-ttu-id="bc8a0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="bc8a0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bc8a0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc8a0-127">Request body</span></span>
<span data-ttu-id="bc8a0-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="bc8a0-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="bc8a0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bc8a0-130">Property</span></span>|<span data-ttu-id="bc8a0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc8a0-131">Type</span></span>|<span data-ttu-id="bc8a0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc8a0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bc8a0-133">actionName</span><span class="sxs-lookup"><span data-stu-id="bc8a0-133">actionName</span></span>|[<span data-ttu-id="bc8a0-134">managedDeviceRemoteAction</span><span class="sxs-lookup"><span data-stu-id="bc8a0-134">managedDeviceRemoteAction</span></span>](../resources/intune-devices-manageddeviceremoteaction.md)|<span data-ttu-id="bc8a0-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bc8a0-135">Not yet documented</span></span>|
|<span data-ttu-id="bc8a0-136">DeviceID</span><span class="sxs-lookup"><span data-stu-id="bc8a0-136">deviceIds</span></span>|<span data-ttu-id="bc8a0-137">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="bc8a0-137">String collection</span></span>|<span data-ttu-id="bc8a0-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="bc8a0-138">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="bc8a0-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc8a0-139">Response</span></span>
<span data-ttu-id="bc8a0-140">Si tiene éxito, esta acción devuelve un `200 OK` código de respuesta y un [bulkManagedDeviceActionResult](../resources/intune-devices-bulkmanageddeviceactionresult.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-140">If successful, this action returns a `200 OK` response code and a [bulkManagedDeviceActionResult](../resources/intune-devices-bulkmanageddeviceactionresult.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc8a0-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc8a0-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="bc8a0-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc8a0-142">Request</span></span>
<span data-ttu-id="bc8a0-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/executeAction

Content-type: application/json
Content-length: 78

{
  "actionName": "delete",
  "deviceIds": [
    "Device Ids value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="bc8a0-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc8a0-144">Response</span></span>
<span data-ttu-id="bc8a0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bc8a0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 385

{
  "value": {
    "@odata.type": "microsoft.graph.bulkManagedDeviceActionResult",
    "successfulDeviceIds": [
      "Successful Device Ids value"
    ],
    "failedDeviceIds": [
      "Failed Device Ids value"
    ],
    "notFoundDeviceIds": [
      "Not Found Device Ids value"
    ],
    "notSupportedDeviceIds": [
      "Not Supported Device Ids value"
    ]
  }
}
```





