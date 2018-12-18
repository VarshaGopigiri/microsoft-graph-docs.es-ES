---
title: Eliminar managedDevice
description: Elimina un managedDevice.
author: tfitzmac
ms.openlocfilehash: 24273ab5e6a930609b9a830ffc18b6ab0b456121
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323236"
---
# <a name="delete-manageddevice"></a><span data-ttu-id="af9d9-103">Eliminar managedDevice</span><span class="sxs-lookup"><span data-stu-id="af9d9-103">Delete managedDevice</span></span>

> <span data-ttu-id="af9d9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="af9d9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="af9d9-105">Elimina un [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="af9d9-105">Deletes a [managedDevice](../resources/intune-devices-manageddevice.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="af9d9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="af9d9-106">Prerequisites</span></span>
<span data-ttu-id="af9d9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="af9d9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="af9d9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="af9d9-109">Permission type</span></span>|<span data-ttu-id="af9d9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="af9d9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="af9d9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="af9d9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="af9d9-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="af9d9-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="af9d9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="af9d9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="af9d9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af9d9-114">Not supported.</span></span>|
|<span data-ttu-id="af9d9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="af9d9-115">Application</span></span>|<span data-ttu-id="af9d9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="af9d9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="af9d9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="af9d9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}/managedDevices/{managedDeviceId}
DELETE /deviceManagement/managedDevices/{managedDeviceId}
DELETE /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}
```

## <a name="request-headers"></a><span data-ttu-id="af9d9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="af9d9-118">Request headers</span></span>
|<span data-ttu-id="af9d9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af9d9-119">Header</span></span>|<span data-ttu-id="af9d9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="af9d9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="af9d9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="af9d9-121">Authorization</span></span>|<span data-ttu-id="af9d9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="af9d9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="af9d9-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="af9d9-123">Accept</span></span>|<span data-ttu-id="af9d9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="af9d9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="af9d9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="af9d9-125">Request body</span></span>
<span data-ttu-id="af9d9-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="af9d9-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="af9d9-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af9d9-127">Response</span></span>
<span data-ttu-id="af9d9-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="af9d9-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="af9d9-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="af9d9-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="af9d9-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="af9d9-130">Request</span></span>
<span data-ttu-id="af9d9-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="af9d9-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}
```

### <a name="response"></a><span data-ttu-id="af9d9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="af9d9-132">Response</span></span>
<span data-ttu-id="af9d9-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="af9d9-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



