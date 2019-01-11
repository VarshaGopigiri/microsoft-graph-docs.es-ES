---
title: Acción rebootNow
description: Reiniciar dispositivo
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dbe6ef14c47e0a9b136a3fad3bfac8a148f4e838
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889568"
---
# <a name="rebootnow-action"></a><span data-ttu-id="e1afb-103">Acción rebootNow</span><span class="sxs-lookup"><span data-stu-id="e1afb-103">rebootNow action</span></span>

> <span data-ttu-id="e1afb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e1afb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e1afb-105">Reiniciar dispositivo</span><span class="sxs-lookup"><span data-stu-id="e1afb-105">Reboot device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e1afb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e1afb-106">Prerequisites</span></span>
<span data-ttu-id="e1afb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e1afb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e1afb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1afb-109">Permission type</span></span>|<span data-ttu-id="e1afb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1afb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e1afb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1afb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e1afb-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="e1afb-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="e1afb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1afb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e1afb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1afb-114">Not supported.</span></span>|
|<span data-ttu-id="e1afb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1afb-115">Application</span></span>|<span data-ttu-id="e1afb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1afb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e1afb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1afb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/rebootNow
POST /deviceManagement/managedDevices/{managedDeviceId}/rebootNow
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/rebootNow
```

## <a name="request-headers"></a><span data-ttu-id="e1afb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1afb-118">Request headers</span></span>
|<span data-ttu-id="e1afb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1afb-119">Header</span></span>|<span data-ttu-id="e1afb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e1afb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e1afb-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e1afb-121">Authorization</span></span>|<span data-ttu-id="e1afb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e1afb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e1afb-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e1afb-123">Accept</span></span>|<span data-ttu-id="e1afb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e1afb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e1afb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e1afb-125">Request body</span></span>
<span data-ttu-id="e1afb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e1afb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e1afb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1afb-127">Response</span></span>
<span data-ttu-id="e1afb-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="e1afb-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="e1afb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1afb-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e1afb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1afb-130">Request</span></span>
<span data-ttu-id="e1afb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1afb-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/rebootNow
```

### <a name="response"></a><span data-ttu-id="e1afb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1afb-132">Response</span></span>
<span data-ttu-id="e1afb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e1afb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



