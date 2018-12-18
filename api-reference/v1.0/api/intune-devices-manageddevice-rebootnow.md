---
title: Acción rebootNow
description: Reiniciar dispositivo
author: tfitzmac
ms.openlocfilehash: 54b058a5dc8c425c70667c2d04f6a12fe1a81685
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323327"
---
# <a name="rebootnow-action"></a><span data-ttu-id="f26d4-103">Acción rebootNow</span><span class="sxs-lookup"><span data-stu-id="f26d4-103">rebootNow action</span></span>

> <span data-ttu-id="f26d4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f26d4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f26d4-105">Reiniciar dispositivo</span><span class="sxs-lookup"><span data-stu-id="f26d4-105">Reboot device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f26d4-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f26d4-106">Prerequisites</span></span>
<span data-ttu-id="f26d4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f26d4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f26d4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f26d4-109">Permission type</span></span>|<span data-ttu-id="f26d4-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f26d4-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f26d4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f26d4-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f26d4-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="f26d4-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="f26d4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f26d4-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f26d4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f26d4-114">Not supported.</span></span>|
|<span data-ttu-id="f26d4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f26d4-115">Application</span></span>|<span data-ttu-id="f26d4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f26d4-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f26d4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f26d4-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/rebootNow
POST /deviceManagement/managedDevices/{managedDeviceId}/rebootNow
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/rebootNow
```

## <a name="request-headers"></a><span data-ttu-id="f26d4-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f26d4-118">Request headers</span></span>
|<span data-ttu-id="f26d4-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f26d4-119">Header</span></span>|<span data-ttu-id="f26d4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f26d4-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f26d4-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f26d4-121">Authorization</span></span>|<span data-ttu-id="f26d4-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f26d4-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f26d4-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f26d4-123">Accept</span></span>|<span data-ttu-id="f26d4-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f26d4-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f26d4-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f26d4-125">Request body</span></span>
<span data-ttu-id="f26d4-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f26d4-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f26d4-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f26d4-127">Response</span></span>
<span data-ttu-id="f26d4-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f26d4-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f26d4-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f26d4-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f26d4-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f26d4-130">Request</span></span>
<span data-ttu-id="f26d4-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f26d4-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/rebootNow
```

### <a name="response"></a><span data-ttu-id="f26d4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f26d4-132">Response</span></span>
<span data-ttu-id="f26d4-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f26d4-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



