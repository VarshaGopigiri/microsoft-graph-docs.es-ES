---
title: Acción logoutSharedAppleDeviceActiveUser
description: Cerrar la sesión del usuario activo del dispositivo Apple compartido
author: tfitzmac
ms.openlocfilehash: 7f88f050e38d7d352b43722a7e0a71fca2fa4fb6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302068"
---
# <a name="logoutsharedappledeviceactiveuser-action"></a><span data-ttu-id="aca66-103">Acción logoutSharedAppleDeviceActiveUser</span><span class="sxs-lookup"><span data-stu-id="aca66-103">logoutSharedAppleDeviceActiveUser action</span></span>

> <span data-ttu-id="aca66-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aca66-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aca66-105">Cerrar la sesión del usuario activo del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="aca66-105">Logout shared Apple device active user</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aca66-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aca66-106">Prerequisites</span></span>
<span data-ttu-id="aca66-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="aca66-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="aca66-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aca66-109">Permission type</span></span>|<span data-ttu-id="aca66-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aca66-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aca66-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aca66-111">Delegated (work or school account)</span></span>|<span data-ttu-id="aca66-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="aca66-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="aca66-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aca66-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aca66-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aca66-114">Not supported.</span></span>|
|<span data-ttu-id="aca66-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aca66-115">Application</span></span>|<span data-ttu-id="aca66-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aca66-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aca66-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aca66-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
POST /deviceManagement/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
```

## <a name="request-headers"></a><span data-ttu-id="aca66-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aca66-118">Request headers</span></span>
|<span data-ttu-id="aca66-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aca66-119">Header</span></span>|<span data-ttu-id="aca66-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aca66-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aca66-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="aca66-121">Authorization</span></span>|<span data-ttu-id="aca66-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aca66-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aca66-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="aca66-123">Accept</span></span>|<span data-ttu-id="aca66-124">application/json</span><span class="sxs-lookup"><span data-stu-id="aca66-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aca66-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aca66-125">Request body</span></span>
<span data-ttu-id="aca66-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aca66-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aca66-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aca66-127">Response</span></span>
<span data-ttu-id="aca66-128">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="aca66-128">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="aca66-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aca66-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="aca66-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aca66-130">Request</span></span>
<span data-ttu-id="aca66-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aca66-131">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/logoutSharedAppleDeviceActiveUser
```

### <a name="response"></a><span data-ttu-id="aca66-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aca66-132">Response</span></span>
<span data-ttu-id="aca66-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aca66-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



