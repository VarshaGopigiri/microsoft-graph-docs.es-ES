---
title: Enumerar usuarios
description: Enumere las propiedades y las relaciones de los objetos user.
author: tfitzmac
ms.openlocfilehash: 9d68b6855a80262daf359950967517a4ec8faa8c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357144"
---
# <a name="list-users"></a><span data-ttu-id="d6dcf-103">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="d6dcf-103">List users</span></span>

> <span data-ttu-id="d6dcf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d6dcf-105">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="d6dcf-105">List properties and relationships of the [user](../resources/intune-shared-user.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d6dcf-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d6dcf-106">Prerequisites</span></span>
<span data-ttu-id="d6dcf-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d6dcf-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d6dcf-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="d6dcf-109">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-109">The specific permission depends on the context.</span></span>

|<span data-ttu-id="d6dcf-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d6dcf-110">Permission type</span></span>|<span data-ttu-id="d6dcf-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d6dcf-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d6dcf-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d6dcf-112">Delegated (work or school account)</span></span>| <span data-ttu-id="d6dcf-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="d6dcf-113">_varies by context_</span></span>|
| <span data-ttu-id="d6dcf-114">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d6dcf-114">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="d6dcf-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6dcf-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="d6dcf-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="d6dcf-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="d6dcf-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6dcf-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="d6dcf-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="d6dcf-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="d6dcf-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6dcf-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="d6dcf-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="d6dcf-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="d6dcf-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="d6dcf-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="d6dcf-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d6dcf-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d6dcf-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-123">Not supported.</span></span>|
|<span data-ttu-id="d6dcf-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d6dcf-124">Application</span></span>|<span data-ttu-id="d6dcf-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d6dcf-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6dcf-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users
```

## <a name="request-headers"></a><span data-ttu-id="d6dcf-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6dcf-127">Request headers</span></span>
|<span data-ttu-id="d6dcf-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6dcf-128">Header</span></span>|<span data-ttu-id="d6dcf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dcf-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d6dcf-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="d6dcf-130">Authorization</span></span>|<span data-ttu-id="d6dcf-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d6dcf-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d6dcf-132">Accept</span></span>|<span data-ttu-id="d6dcf-133">application/json</span><span class="sxs-lookup"><span data-stu-id="d6dcf-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d6dcf-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6dcf-134">Request body</span></span>
<span data-ttu-id="d6dcf-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d6dcf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6dcf-136">Response</span></span>
<span data-ttu-id="d6dcf-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-137">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/intune-shared-user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6dcf-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6dcf-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="d6dcf-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6dcf-139">Request</span></span>
<span data-ttu-id="d6dcf-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-140">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users
```

### <a name="response"></a><span data-ttu-id="d6dcf-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6dcf-141">Response</span></span>
<span data-ttu-id="d6dcf-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6dcf-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 136

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.user",
      "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
    }
  ]
}
```



