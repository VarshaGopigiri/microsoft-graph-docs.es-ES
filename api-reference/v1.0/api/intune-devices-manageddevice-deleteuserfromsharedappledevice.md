---
title: Acción deleteUserFromSharedAppleDevice
description: Eliminar usuario del dispositivo Apple compartido
author: tfitzmac
ms.openlocfilehash: e2b2eb30f54c3e1efe53c3b99049cfccb3e3aa98
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329886"
---
# <a name="deleteuserfromsharedappledevice-action"></a><span data-ttu-id="ba611-103">Acción deleteUserFromSharedAppleDevice</span><span class="sxs-lookup"><span data-stu-id="ba611-103">deleteUserFromSharedAppleDevice action</span></span>

> <span data-ttu-id="ba611-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ba611-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ba611-105">Eliminar usuario del dispositivo Apple compartido</span><span class="sxs-lookup"><span data-stu-id="ba611-105">Delete user from shared Apple device</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ba611-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ba611-106">Prerequisites</span></span>
<span data-ttu-id="ba611-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ba611-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ba611-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ba611-109">Permission type</span></span>|<span data-ttu-id="ba611-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ba611-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ba611-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ba611-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ba611-112">DeviceManagementManagedDevices.PriviligedOperation.All</span><span class="sxs-lookup"><span data-stu-id="ba611-112">DeviceManagementManagedDevices.PriviligedOperation.All</span></span>|
|<span data-ttu-id="ba611-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ba611-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ba611-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba611-114">Not supported.</span></span>|
|<span data-ttu-id="ba611-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ba611-115">Application</span></span>|<span data-ttu-id="ba611-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ba611-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ba611-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ba611-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices/{managedDeviceId}/deleteUserFromSharedAppleDevice
POST /deviceManagement/managedDevices/{managedDeviceId}/deleteUserFromSharedAppleDevice
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deleteUserFromSharedAppleDevice
```

## <a name="request-headers"></a><span data-ttu-id="ba611-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ba611-118">Request headers</span></span>
|<span data-ttu-id="ba611-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba611-119">Header</span></span>|<span data-ttu-id="ba611-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ba611-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ba611-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ba611-121">Authorization</span></span>|<span data-ttu-id="ba611-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ba611-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ba611-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ba611-123">Accept</span></span>|<span data-ttu-id="ba611-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ba611-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ba611-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ba611-125">Request body</span></span>
<span data-ttu-id="ba611-126">En el cuerpo de la solicitud, proporcione una representación JSON de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="ba611-126">In the request body, supply JSON representation of the parameters.</span></span>

<span data-ttu-id="ba611-127">La siguiente tabla muestra los parámetros que se pueden usar con esta acción.</span><span class="sxs-lookup"><span data-stu-id="ba611-127">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="ba611-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ba611-128">Property</span></span>|<span data-ttu-id="ba611-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba611-129">Type</span></span>|<span data-ttu-id="ba611-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba611-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ba611-131">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ba611-131">userPrincipalName</span></span>|<span data-ttu-id="ba611-132">String</span><span class="sxs-lookup"><span data-stu-id="ba611-132">String</span></span>|<span data-ttu-id="ba611-133">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ba611-133">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="ba611-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba611-134">Response</span></span>
<span data-ttu-id="ba611-135">Si se ejecuta correctamente, esta acción devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="ba611-135">If successful, this action returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="ba611-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ba611-136">Example</span></span>
### <a name="request"></a><span data-ttu-id="ba611-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ba611-137">Request</span></span>
<span data-ttu-id="ba611-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ba611-138">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}/deleteUserFromSharedAppleDevice

Content-type: application/json
Content-length: 56

{
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="ba611-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ba611-139">Response</span></span>
<span data-ttu-id="ba611-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ba611-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



