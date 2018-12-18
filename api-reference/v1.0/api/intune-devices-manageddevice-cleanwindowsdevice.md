---
title: Acción cleanWindowsDevice
description: Limpiar dispositivo Windows
author: tfitzmac
ms.openlocfilehash: 9d19b71f200381c10b7501eadf9007162ff9fff3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301767"
---
# <a name="cleanwindowsdevice-action"></a><span data-ttu-id="43245-103">Acción cleanWindowsDevice</span><span class="sxs-lookup"><span data-stu-id="43245-103">cleanWindowsDevice action</span></span>

> <span data-ttu-id="43245-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43245-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43245-105">Limpiar dispositivo Windows</span><span class="sxs-lookup"><span data-stu-id="43245-105">Clean Windows device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="43245-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="43245-106">Prerequisites</span></span>
<span data-ttu-id="43245-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="43245-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="43245-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43245-109">Permission type</span></span>|<span data-ttu-id="43245-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43245-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="43245-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43245-111">Delegated (work or school account)</span></span>|<span data-ttu-id="43245-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="43245-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="43245-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43245-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="43245-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43245-114">Not supported.</span></span>|
|<span data-ttu-id="43245-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43245-115">Application</span></span>|<span data-ttu-id="43245-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="43245-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="43245-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43245-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/cleanWindowsDevice
POST /deviceManagement/managedDevices/{managedDeviceId}/cleanWindowsDevice
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/cleanWindowsDevice
```

## <a name="request-headers"></a><span data-ttu-id="43245-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43245-118">Request headers</span></span>
|<span data-ttu-id="43245-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43245-119">Header</span></span>|<span data-ttu-id="43245-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43245-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="43245-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="43245-121">Authorization</span></span>|<span data-ttu-id="43245-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="43245-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="43245-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="43245-123">Accept</span></span>|<span data-ttu-id="43245-124">application/json</span><span class="sxs-lookup"><span data-stu-id="43245-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="43245-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43245-125">Request body</span></span>
<span data-ttu-id="43245-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="43245-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="43245-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="43245-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="43245-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43245-128">Property</span></span>|<span data-ttu-id="43245-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="43245-129">Type</span></span>|<span data-ttu-id="43245-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="43245-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="43245-131">keepUserData</span><span class="sxs-lookup"><span data-stu-id="43245-131">keepUserData</span></span>|<span data-ttu-id="43245-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="43245-132">Boolean</span></span>|<span data-ttu-id="43245-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="43245-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="43245-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43245-134">Response</span></span>
<span data-ttu-id="43245-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="43245-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="43245-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43245-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="43245-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43245-137">Request</span></span>
<span data-ttu-id="43245-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43245-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/cleanWindowsDevice

Content-type: application/json
Content-length: 28

{
  "keepUserData": true
}
```

### <a name="response"></a><span data-ttu-id="43245-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43245-139">Response</span></span>
<span data-ttu-id="43245-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43245-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



