---
title: Acción wipe
description: Eliminar los datos de un dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3da2d5619c57a083c7702d3b9accfa8d52f20568
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834422"
---
# <a name="wipe-action"></a><span data-ttu-id="b58ba-103">Acción wipe</span><span class="sxs-lookup"><span data-stu-id="b58ba-103">wipe action</span></span>

> <span data-ttu-id="b58ba-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b58ba-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b58ba-105">Eliminar los datos de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="b58ba-105">Wipe a device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b58ba-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b58ba-106">Prerequisites</span></span>
<span data-ttu-id="b58ba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b58ba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b58ba-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b58ba-109">Permission type</span></span>|<span data-ttu-id="b58ba-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b58ba-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b58ba-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b58ba-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b58ba-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="b58ba-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="b58ba-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b58ba-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b58ba-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b58ba-114">Not supported.</span></span>|
|<span data-ttu-id="b58ba-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b58ba-115">Application</span></span>|<span data-ttu-id="b58ba-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b58ba-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b58ba-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b58ba-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/managedDevices/{managedDeviceId}/wipe
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/wipe
```

## <a name="request-headers"></a><span data-ttu-id="b58ba-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b58ba-118">Request headers</span></span>
|<span data-ttu-id="b58ba-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b58ba-119">Header</span></span>|<span data-ttu-id="b58ba-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b58ba-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b58ba-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b58ba-121">Authorization</span></span>|<span data-ttu-id="b58ba-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b58ba-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b58ba-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b58ba-123">Accept</span></span>|<span data-ttu-id="b58ba-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b58ba-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b58ba-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b58ba-125">Request body</span></span>
<span data-ttu-id="b58ba-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="b58ba-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="b58ba-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="b58ba-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="b58ba-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b58ba-128">Property</span></span>|<span data-ttu-id="b58ba-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b58ba-129">Type</span></span>|<span data-ttu-id="b58ba-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b58ba-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b58ba-131">keepEnrollmentData</span><span class="sxs-lookup"><span data-stu-id="b58ba-131">keepEnrollmentData</span></span>|<span data-ttu-id="b58ba-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="b58ba-132">Boolean</span></span>|<span data-ttu-id="b58ba-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b58ba-133">Not yet documented</span></span>|
|<span data-ttu-id="b58ba-134">keepUserData</span><span class="sxs-lookup"><span data-stu-id="b58ba-134">keepUserData</span></span>|<span data-ttu-id="b58ba-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="b58ba-135">Boolean</span></span>|<span data-ttu-id="b58ba-136">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b58ba-136">Not yet documented</span></span>|
|<span data-ttu-id="b58ba-137">macOsUnlockCode</span><span class="sxs-lookup"><span data-stu-id="b58ba-137">macOsUnlockCode</span></span>|<span data-ttu-id="b58ba-138">String</span><span class="sxs-lookup"><span data-stu-id="b58ba-138">String</span></span>|<span data-ttu-id="b58ba-139">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b58ba-139">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="b58ba-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b58ba-140">Response</span></span>
<span data-ttu-id="b58ba-141">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b58ba-141">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b58ba-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b58ba-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="b58ba-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b58ba-143">Request</span></span>
<span data-ttu-id="b58ba-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b58ba-144">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/wipe

Content-type: application/json
Content-length: 109

{
  "keepEnrollmentData": true,
  "keepUserData": true,
  "macOsUnlockCode": "Mac Os Unlock Code value"
}
```

### <a name="response"></a><span data-ttu-id="b58ba-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b58ba-145">Response</span></span>
<span data-ttu-id="b58ba-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b58ba-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



