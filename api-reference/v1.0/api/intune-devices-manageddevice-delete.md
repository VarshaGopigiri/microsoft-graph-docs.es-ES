---
title: Eliminar managedDevice
description: Elimina un managedDevice.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f66debc301af301674145c6bf9a50c8f3e4f0bf0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865152"
---
# <a name="delete-manageddevice"></a><span data-ttu-id="e8679-103">Eliminar managedDevice</span><span class="sxs-lookup"><span data-stu-id="e8679-103">Delete managedDevice</span></span>

> <span data-ttu-id="e8679-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e8679-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e8679-105">Elimina un [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="e8679-105">Deletes a [managedDevice](../resources/intune-devices-manageddevice.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e8679-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e8679-106">Prerequisites</span></span>
<span data-ttu-id="e8679-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e8679-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e8679-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8679-109">Permission type</span></span>|<span data-ttu-id="e8679-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8679-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e8679-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8679-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e8679-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e8679-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="e8679-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8679-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e8679-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8679-114">Not supported.</span></span>|
|<span data-ttu-id="e8679-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8679-115">Application</span></span>|<span data-ttu-id="e8679-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8679-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e8679-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8679-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}/managedDevices/{managedDeviceId}
DELETE /deviceManagement/managedDevices/{managedDeviceId}
DELETE /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}
```

## <a name="request-headers"></a><span data-ttu-id="e8679-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8679-118">Request headers</span></span>
|<span data-ttu-id="e8679-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8679-119">Header</span></span>|<span data-ttu-id="e8679-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e8679-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e8679-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e8679-121">Authorization</span></span>|<span data-ttu-id="e8679-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e8679-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e8679-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e8679-123">Accept</span></span>|<span data-ttu-id="e8679-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e8679-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e8679-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8679-125">Request body</span></span>
<span data-ttu-id="e8679-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e8679-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e8679-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8679-127">Response</span></span>
<span data-ttu-id="e8679-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e8679-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e8679-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8679-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e8679-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8679-130">Request</span></span>
<span data-ttu-id="e8679-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8679-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}
```

### <a name="response"></a><span data-ttu-id="e8679-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8679-132">Response</span></span>
<span data-ttu-id="e8679-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e8679-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



