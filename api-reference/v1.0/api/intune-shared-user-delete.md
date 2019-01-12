---
title: Eliminar usuario
description: Elimina un user.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3bb78ef11b67ba2a4d0c5f8ab9b15c65ad2ec26f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961529"
---
# <a name="delete-user"></a><span data-ttu-id="f13ac-103">Eliminar usuario</span><span class="sxs-lookup"><span data-stu-id="f13ac-103">Delete user</span></span>

> <span data-ttu-id="f13ac-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f13ac-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f13ac-105">Elimina un [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="f13ac-105">Deletes a [user](../resources/intune-shared-user.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f13ac-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f13ac-106">Prerequisites</span></span>
<span data-ttu-id="f13ac-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f13ac-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f13ac-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f13ac-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="f13ac-109">Los permisos específicos necesarios depende de contexto.</span><span class="sxs-lookup"><span data-stu-id="f13ac-109">The specific permission required depends on context.</span></span>

|<span data-ttu-id="f13ac-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f13ac-110">Permission type</span></span>|<span data-ttu-id="f13ac-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f13ac-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f13ac-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f13ac-112">Delegated (work or school account)</span></span>| <span data-ttu-id="f13ac-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="f13ac-113">_varies by context_</span></span>|
| <span data-ttu-id="f13ac-114">&nbsp;&nbsp; Dispositivos</span><span class="sxs-lookup"><span data-stu-id="f13ac-114">&nbsp; &nbsp; Devices</span></span> | <span data-ttu-id="f13ac-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f13ac-115">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="f13ac-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="f13ac-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="f13ac-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f13ac-117">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="f13ac-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="f13ac-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="f13ac-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f13ac-119">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="f13ac-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="f13ac-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="f13ac-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f13ac-121">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="f13ac-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f13ac-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f13ac-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f13ac-123">Not supported.</span></span>|
|<span data-ttu-id="f13ac-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f13ac-124">Application</span></span>|<span data-ttu-id="f13ac-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f13ac-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f13ac-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f13ac-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="f13ac-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f13ac-127">Request headers</span></span>
|<span data-ttu-id="f13ac-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f13ac-128">Header</span></span>|<span data-ttu-id="f13ac-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f13ac-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f13ac-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="f13ac-130">Authorization</span></span>|<span data-ttu-id="f13ac-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f13ac-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f13ac-132">Accept</span><span class="sxs-lookup"><span data-stu-id="f13ac-132">Accept</span></span>|<span data-ttu-id="f13ac-133">application/json</span><span class="sxs-lookup"><span data-stu-id="f13ac-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f13ac-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f13ac-134">Request body</span></span>
<span data-ttu-id="f13ac-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f13ac-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f13ac-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f13ac-136">Response</span></span>
<span data-ttu-id="f13ac-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="f13ac-137">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="f13ac-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f13ac-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="f13ac-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f13ac-139">Request</span></span>
<span data-ttu-id="f13ac-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f13ac-140">Here is an example of the request.</span></span>

``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="f13ac-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f13ac-141">Response</span></span>
<span data-ttu-id="f13ac-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f13ac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



