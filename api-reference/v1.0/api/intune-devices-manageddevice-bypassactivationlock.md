---
title: Acción bypassActivationLock
description: Omitir bloqueo de activación
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 026f4fa6380a5dd49d1d6baf2f1bd84d9e8bec89
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810538"
---
# <a name="bypassactivationlock-action"></a><span data-ttu-id="97b72-103">Acción bypassActivationLock</span><span class="sxs-lookup"><span data-stu-id="97b72-103">bypassActivationLock action</span></span>

> <span data-ttu-id="97b72-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97b72-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97b72-105">Omitir bloqueo de activación</span><span class="sxs-lookup"><span data-stu-id="97b72-105">Bypass activation lock</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97b72-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97b72-106">Prerequisites</span></span>
<span data-ttu-id="97b72-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97b72-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97b72-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97b72-109">Permission type</span></span>|<span data-ttu-id="97b72-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97b72-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97b72-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97b72-111">Delegated (work or school account)</span></span>|<span data-ttu-id="97b72-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="97b72-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="97b72-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97b72-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97b72-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97b72-114">Not supported.</span></span>|
|<span data-ttu-id="97b72-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97b72-115">Application</span></span>|<span data-ttu-id="97b72-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97b72-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97b72-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97b72-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/bypassActivationLock
POST /deviceManagement/managedDevices/{managedDeviceId}/bypassActivationLock
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/bypassActivationLock
```

## <a name="request-headers"></a><span data-ttu-id="97b72-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97b72-118">Request headers</span></span>
|<span data-ttu-id="97b72-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97b72-119">Header</span></span>|<span data-ttu-id="97b72-120">Valor</span><span class="sxs-lookup"><span data-stu-id="97b72-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97b72-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="97b72-121">Authorization</span></span>|<span data-ttu-id="97b72-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97b72-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97b72-123">Accept</span><span class="sxs-lookup"><span data-stu-id="97b72-123">Accept</span></span>|<span data-ttu-id="97b72-124">application/json</span><span class="sxs-lookup"><span data-stu-id="97b72-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97b72-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97b72-125">Request body</span></span>
<span data-ttu-id="97b72-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="97b72-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="97b72-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97b72-127">Response</span></span>
<span data-ttu-id="97b72-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="97b72-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="97b72-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97b72-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="97b72-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97b72-130">Request</span></span>
<span data-ttu-id="97b72-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97b72-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/bypassActivationLock
```

### <a name="response"></a><span data-ttu-id="97b72-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97b72-132">Response</span></span>
<span data-ttu-id="97b72-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97b72-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



