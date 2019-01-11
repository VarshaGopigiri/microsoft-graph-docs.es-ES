---
title: Acción wipe
description: Eliminar los datos de un dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 91b04311692609687792ce22c5cc81074239ba23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842843"
---
# <a name="wipe-action"></a><span data-ttu-id="a0d6e-103">Acción wipe</span><span class="sxs-lookup"><span data-stu-id="a0d6e-103">wipe action</span></span>

> <span data-ttu-id="a0d6e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a0d6e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a0d6e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0d6e-107">Eliminar los datos de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="a0d6e-107">Wipe a device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a0d6e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a0d6e-108">Prerequisites</span></span>
<span data-ttu-id="a0d6e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a0d6e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a0d6e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0d6e-111">Permission type</span></span>|<span data-ttu-id="a0d6e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0d6e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a0d6e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0d6e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a0d6e-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="a0d6e-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="a0d6e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0d6e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a0d6e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-116">Not supported.</span></span>|
|<span data-ttu-id="a0d6e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0d6e-117">Application</span></span>|<span data-ttu-id="a0d6e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a0d6e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0d6e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/wipe
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/wipe
```

## <a name="request-headers"></a><span data-ttu-id="a0d6e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d6e-120">Request headers</span></span>
|<span data-ttu-id="a0d6e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0d6e-121">Header</span></span>|<span data-ttu-id="a0d6e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a0d6e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a0d6e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0d6e-123">Authorization</span></span>|<span data-ttu-id="a0d6e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a0d6e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a0d6e-125">Accept</span></span>|<span data-ttu-id="a0d6e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a0d6e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a0d6e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d6e-127">Request body</span></span>
<span data-ttu-id="a0d6e-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="a0d6e-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="a0d6e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0d6e-130">Property</span></span>|<span data-ttu-id="a0d6e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0d6e-131">Type</span></span>|<span data-ttu-id="a0d6e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0d6e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a0d6e-133">keepEnrollmentData</span><span class="sxs-lookup"><span data-stu-id="a0d6e-133">keepEnrollmentData</span></span>|<span data-ttu-id="a0d6e-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="a0d6e-134">Boolean</span></span>|<span data-ttu-id="a0d6e-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a0d6e-135">Not yet documented</span></span>|
|<span data-ttu-id="a0d6e-136">keepUserData</span><span class="sxs-lookup"><span data-stu-id="a0d6e-136">keepUserData</span></span>|<span data-ttu-id="a0d6e-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="a0d6e-137">Boolean</span></span>|<span data-ttu-id="a0d6e-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a0d6e-138">Not yet documented</span></span>|
|<span data-ttu-id="a0d6e-139">macOsUnlockCode</span><span class="sxs-lookup"><span data-stu-id="a0d6e-139">macOsUnlockCode</span></span>|<span data-ttu-id="a0d6e-140">String</span><span class="sxs-lookup"><span data-stu-id="a0d6e-140">String</span></span>|<span data-ttu-id="a0d6e-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a0d6e-141">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a0d6e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0d6e-142">Response</span></span>
<span data-ttu-id="a0d6e-143">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-143">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a0d6e-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0d6e-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="a0d6e-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0d6e-145">Request</span></span>
<span data-ttu-id="a0d6e-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-146">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/wipe

Content-type: application/json
Content-length: 109

{
  "keepEnrollmentData": true,
  "keepUserData": true,
  "macOsUnlockCode": "Mac Os Unlock Code value"
}
```

### <a name="response"></a><span data-ttu-id="a0d6e-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0d6e-147">Response</span></span>
<span data-ttu-id="a0d6e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0d6e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





