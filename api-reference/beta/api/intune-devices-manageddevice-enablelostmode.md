---
title: acción enableLostMode
description: Habilitar el modo pierden
ms.openlocfilehash: de49cffccf3f87e91644a33128dfdfaa74b3f233
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087013"
---
# <a name="enablelostmode-action"></a><span data-ttu-id="c69ea-103">acción enableLostMode</span><span class="sxs-lookup"><span data-stu-id="c69ea-103">enableLostMode action</span></span>

> <span data-ttu-id="c69ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c69ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c69ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c69ea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c69ea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c69ea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c69ea-107">Habilitar el modo pierden</span><span class="sxs-lookup"><span data-stu-id="c69ea-107">Enable lost mode</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c69ea-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c69ea-108">Prerequisites</span></span>
<span data-ttu-id="c69ea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c69ea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c69ea-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c69ea-111">Permission type</span></span>|<span data-ttu-id="c69ea-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c69ea-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c69ea-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c69ea-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c69ea-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="c69ea-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="c69ea-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c69ea-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c69ea-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c69ea-116">Not supported.</span></span>|
|<span data-ttu-id="c69ea-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c69ea-117">Application</span></span>|<span data-ttu-id="c69ea-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c69ea-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c69ea-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c69ea-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/enableLostMode
POST /deviceManagement/managedDevices/{managedDeviceId}/enableLostMode
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/enableLostMode
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/enableLostMode
```

## <a name="request-headers"></a><span data-ttu-id="c69ea-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c69ea-120">Request headers</span></span>
|<span data-ttu-id="c69ea-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c69ea-121">Header</span></span>|<span data-ttu-id="c69ea-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c69ea-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c69ea-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c69ea-123">Authorization</span></span>|<span data-ttu-id="c69ea-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c69ea-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c69ea-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c69ea-125">Accept</span></span>|<span data-ttu-id="c69ea-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c69ea-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c69ea-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c69ea-127">Request body</span></span>
<span data-ttu-id="c69ea-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="c69ea-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="c69ea-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="c69ea-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="c69ea-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c69ea-130">Property</span></span>|<span data-ttu-id="c69ea-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c69ea-131">Type</span></span>|<span data-ttu-id="c69ea-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c69ea-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c69ea-133">message</span><span class="sxs-lookup"><span data-stu-id="c69ea-133">message</span></span>|<span data-ttu-id="c69ea-134">String</span><span class="sxs-lookup"><span data-stu-id="c69ea-134">String</span></span>|<span data-ttu-id="c69ea-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c69ea-135">Not yet documented</span></span>|
|<span data-ttu-id="c69ea-136">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="c69ea-136">phoneNumber</span></span>|<span data-ttu-id="c69ea-137">String</span><span class="sxs-lookup"><span data-stu-id="c69ea-137">String</span></span>|<span data-ttu-id="c69ea-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c69ea-138">Not yet documented</span></span>|
|<span data-ttu-id="c69ea-139">pie de página</span><span class="sxs-lookup"><span data-stu-id="c69ea-139">footer</span></span>|<span data-ttu-id="c69ea-140">String</span><span class="sxs-lookup"><span data-stu-id="c69ea-140">String</span></span>|<span data-ttu-id="c69ea-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="c69ea-141">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="c69ea-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c69ea-142">Response</span></span>
<span data-ttu-id="c69ea-143">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c69ea-143">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c69ea-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c69ea-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="c69ea-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c69ea-145">Request</span></span>
<span data-ttu-id="c69ea-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c69ea-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/enableLostMode

Content-type: application/json
Content-length: 103

{
  "message": "Message value",
  "phoneNumber": "Phone Number value",
  "footer": "Footer value"
}
```

### <a name="response"></a><span data-ttu-id="c69ea-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c69ea-147">Response</span></span>
<span data-ttu-id="c69ea-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c69ea-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





