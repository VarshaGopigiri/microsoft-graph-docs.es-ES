---
title: Acción updateWindowsDeviceAccount
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5ede62413a25aa3dc5af3ad08b8912a126598ff5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965603"
---
# <a name="updatewindowsdeviceaccount-action"></a><span data-ttu-id="a730a-103">Acción updateWindowsDeviceAccount</span><span class="sxs-lookup"><span data-stu-id="a730a-103">updateWindowsDeviceAccount action</span></span>

> <span data-ttu-id="a730a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a730a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a730a-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a730a-105">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a730a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a730a-106">Prerequisites</span></span>
<span data-ttu-id="a730a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a730a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a730a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a730a-109">Permission type</span></span>|<span data-ttu-id="a730a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a730a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a730a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a730a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a730a-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="a730a-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="a730a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a730a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a730a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a730a-114">Not supported.</span></span>|
|<span data-ttu-id="a730a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a730a-115">Application</span></span>|<span data-ttu-id="a730a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a730a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a730a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a730a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/updateWindowsDeviceAccount
POST /deviceManagement/managedDevices/{managedDeviceId}/updateWindowsDeviceAccount
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/updateWindowsDeviceAccount
```

## <a name="request-headers"></a><span data-ttu-id="a730a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a730a-118">Request headers</span></span>
|<span data-ttu-id="a730a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a730a-119">Header</span></span>|<span data-ttu-id="a730a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a730a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a730a-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a730a-121">Authorization</span></span>|<span data-ttu-id="a730a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a730a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a730a-123">Accept</span><span class="sxs-lookup"><span data-stu-id="a730a-123">Accept</span></span>|<span data-ttu-id="a730a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a730a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a730a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a730a-125">Request body</span></span>
<span data-ttu-id="a730a-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="a730a-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="a730a-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="a730a-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="a730a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a730a-128">Property</span></span>|<span data-ttu-id="a730a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a730a-129">Type</span></span>|<span data-ttu-id="a730a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a730a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a730a-131">updateWindowsDeviceAccountActionParameter</span><span class="sxs-lookup"><span data-stu-id="a730a-131">updateWindowsDeviceAccountActionParameter</span></span>|[<span data-ttu-id="a730a-132">updateWindowsDeviceAccountActionParameter</span><span class="sxs-lookup"><span data-stu-id="a730a-132">updateWindowsDeviceAccountActionParameter</span></span>](../resources/intune-devices-updatewindowsdeviceaccountactionparameter.md)|<span data-ttu-id="a730a-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a730a-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="a730a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a730a-134">Response</span></span>
<span data-ttu-id="a730a-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="a730a-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="a730a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a730a-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="a730a-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a730a-137">Request</span></span>
<span data-ttu-id="a730a-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a730a-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/updateWindowsDeviceAccount

Content-type: application/json
Content-length: 532

{
  "updateWindowsDeviceAccountActionParameter": {
    "@odata.type": "microsoft.graph.updateWindowsDeviceAccountActionParameter",
    "deviceAccount": {
      "@odata.type": "microsoft.graph.windowsDeviceAccount",
      "password": "Password value"
    },
    "passwordRotationEnabled": true,
    "calendarSyncEnabled": true,
    "deviceAccountEmail": "Device Account Email value",
    "exchangeServer": "Exchange Server value",
    "sessionInitiationProtocalAddress": "Session Initiation Protocal Address value"
  }
}
```

### <a name="response"></a><span data-ttu-id="a730a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a730a-139">Response</span></span>
<span data-ttu-id="a730a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a730a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



