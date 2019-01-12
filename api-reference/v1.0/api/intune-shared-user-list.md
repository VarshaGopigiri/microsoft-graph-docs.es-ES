---
title: Enumerar usuarios
description: Enumere las propiedades y las relaciones de los objetos user.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 76e1d8cf21ed2c7757255b67d5646187827f9d59
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27970692"
---
# <a name="list-users"></a><span data-ttu-id="17262-103">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="17262-103">List users</span></span>

> <span data-ttu-id="17262-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="17262-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="17262-105">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="17262-105">List properties and relationships of the [user](../resources/intune-shared-user.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="17262-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="17262-106">Prerequisites</span></span>
<span data-ttu-id="17262-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="17262-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="17262-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17262-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="17262-109">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="17262-109">The specific permission depends on the context.</span></span>

|<span data-ttu-id="17262-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17262-110">Permission type</span></span>|<span data-ttu-id="17262-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17262-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="17262-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17262-112">Delegated (work or school account)</span></span>| <span data-ttu-id="17262-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="17262-113">_varies by context_</span></span>|
| <span data-ttu-id="17262-114">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="17262-114">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="17262-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="17262-115">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="17262-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="17262-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="17262-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="17262-117">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="17262-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="17262-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="17262-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="17262-119">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="17262-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="17262-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="17262-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="17262-121">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="17262-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17262-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="17262-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17262-123">Not supported.</span></span>|
|<span data-ttu-id="17262-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17262-124">Application</span></span>|<span data-ttu-id="17262-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17262-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="17262-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17262-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users
```

## <a name="request-headers"></a><span data-ttu-id="17262-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17262-127">Request headers</span></span>
|<span data-ttu-id="17262-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17262-128">Header</span></span>|<span data-ttu-id="17262-129">Valor</span><span class="sxs-lookup"><span data-stu-id="17262-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="17262-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="17262-130">Authorization</span></span>|<span data-ttu-id="17262-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="17262-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="17262-132">Accept</span><span class="sxs-lookup"><span data-stu-id="17262-132">Accept</span></span>|<span data-ttu-id="17262-133">application/json</span><span class="sxs-lookup"><span data-stu-id="17262-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="17262-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17262-134">Request body</span></span>
<span data-ttu-id="17262-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="17262-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="17262-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17262-136">Response</span></span>
<span data-ttu-id="17262-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17262-137">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/intune-shared-user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="17262-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17262-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="17262-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17262-139">Request</span></span>
<span data-ttu-id="17262-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17262-140">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/v1.0/users
```

### <a name="response"></a><span data-ttu-id="17262-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17262-141">Response</span></span>
<span data-ttu-id="17262-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17262-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



