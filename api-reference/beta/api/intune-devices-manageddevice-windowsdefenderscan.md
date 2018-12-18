---
title: Acción windowsDefenderScan
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: d64ce1e595717d99608547ff4622d35d22d18552
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305092"
---
# <a name="windowsdefenderscan-action"></a><span data-ttu-id="f4f45-103">Acción windowsDefenderScan</span><span class="sxs-lookup"><span data-stu-id="f4f45-103">windowsDefenderScan action</span></span>

> <span data-ttu-id="f4f45-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f4f45-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f4f45-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f4f45-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f4f45-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4f45-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4f45-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f4f45-107">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f4f45-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f4f45-108">Prerequisites</span></span>
<span data-ttu-id="f4f45-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f4f45-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f4f45-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4f45-111">Permission type</span></span>|<span data-ttu-id="f4f45-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4f45-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f4f45-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4f45-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f4f45-114">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="f4f45-114">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="f4f45-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4f45-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f4f45-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4f45-116">Not supported.</span></span>|
|<span data-ttu-id="f4f45-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4f45-117">Application</span></span>|<span data-ttu-id="f4f45-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4f45-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f4f45-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4f45-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/windowsDefenderScan
POST /deviceManagement/managedDevices/{managedDeviceId}/windowsDefenderScan
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/windowsDefenderScan
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/windowsDefenderScan
```

## <a name="request-headers"></a><span data-ttu-id="f4f45-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4f45-120">Request headers</span></span>
|<span data-ttu-id="f4f45-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4f45-121">Header</span></span>|<span data-ttu-id="f4f45-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f4f45-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f4f45-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f4f45-123">Authorization</span></span>|<span data-ttu-id="f4f45-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f4f45-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f4f45-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f4f45-125">Accept</span></span>|<span data-ttu-id="f4f45-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f4f45-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4f45-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4f45-127">Request body</span></span>
<span data-ttu-id="f4f45-128">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="f4f45-128">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="f4f45-129">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="f4f45-129">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="f4f45-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4f45-130">Property</span></span>|<span data-ttu-id="f4f45-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4f45-131">Type</span></span>|<span data-ttu-id="f4f45-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4f45-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4f45-133">quickScan</span><span class="sxs-lookup"><span data-stu-id="f4f45-133">quickScan</span></span>|<span data-ttu-id="f4f45-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="f4f45-134">Boolean</span></span>|<span data-ttu-id="f4f45-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f4f45-135">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="f4f45-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4f45-136">Response</span></span>
<span data-ttu-id="f4f45-137">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f4f45-137">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f4f45-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4f45-138">Example</span></span>
### <a name="request"></a><span data-ttu-id="f4f45-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4f45-139">Request</span></span>
<span data-ttu-id="f4f45-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4f45-140">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}/windowsDefenderScan

Content-type: application/json
Content-length: 25

{
  "quickScan": true
}
```

### <a name="response"></a><span data-ttu-id="f4f45-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4f45-141">Response</span></span>
<span data-ttu-id="f4f45-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4f45-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```





