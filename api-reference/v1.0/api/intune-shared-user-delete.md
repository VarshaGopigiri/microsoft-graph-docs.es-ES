---
title: Eliminar usuario
description: Elimina un user.
author: tfitzmac
ms.openlocfilehash: 8ed00b2967fa04fd23351c7dbc369b25d97cba39
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337320"
---
# <a name="delete-user"></a><span data-ttu-id="99be6-103">Eliminar usuario</span><span class="sxs-lookup"><span data-stu-id="99be6-103">Delete user</span></span>

> <span data-ttu-id="99be6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="99be6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="99be6-105">Elimina un [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="99be6-105">Deletes a [user](../resources/intune-shared-user.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="99be6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="99be6-106">Prerequisites</span></span>
<span data-ttu-id="99be6-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="99be6-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="99be6-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99be6-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="99be6-109">Los permisos específicos necesarios depende de contexto.</span><span class="sxs-lookup"><span data-stu-id="99be6-109">The specific permission required depends on context.</span></span>

|<span data-ttu-id="99be6-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99be6-110">Permission type</span></span>|<span data-ttu-id="99be6-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99be6-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="99be6-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99be6-112">Delegated (work or school account)</span></span>| <span data-ttu-id="99be6-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="99be6-113">_varies by context_</span></span>|
| <span data-ttu-id="99be6-114">&nbsp;&nbsp; Dispositivos</span><span class="sxs-lookup"><span data-stu-id="99be6-114">&nbsp; &nbsp; Devices</span></span> | <span data-ttu-id="99be6-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99be6-115">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="99be6-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="99be6-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="99be6-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99be6-117">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="99be6-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="99be6-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="99be6-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99be6-119">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="99be6-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="99be6-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="99be6-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="99be6-121">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="99be6-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99be6-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="99be6-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99be6-123">Not supported.</span></span>|
|<span data-ttu-id="99be6-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99be6-124">Application</span></span>|<span data-ttu-id="99be6-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99be6-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="99be6-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99be6-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="99be6-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99be6-127">Request headers</span></span>
|<span data-ttu-id="99be6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99be6-128">Header</span></span>|<span data-ttu-id="99be6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="99be6-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="99be6-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="99be6-130">Authorization</span></span>|<span data-ttu-id="99be6-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="99be6-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="99be6-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="99be6-132">Accept</span></span>|<span data-ttu-id="99be6-133">application/json</span><span class="sxs-lookup"><span data-stu-id="99be6-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="99be6-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99be6-134">Request body</span></span>
<span data-ttu-id="99be6-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="99be6-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="99be6-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99be6-136">Response</span></span>
<span data-ttu-id="99be6-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="99be6-137">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="99be6-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99be6-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="99be6-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99be6-139">Request</span></span>
<span data-ttu-id="99be6-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99be6-140">Here is an example of the request.</span></span>

``` http
DELETE https://graph.microsoft.com/v1.0/users/{usersId}
```

### <a name="response"></a><span data-ttu-id="99be6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99be6-141">Response</span></span>
<span data-ttu-id="99be6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99be6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 204 No Content
```



