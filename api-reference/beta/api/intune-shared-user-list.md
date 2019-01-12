---
title: Enumerar usuarios
description: Enumere las propiedades y las relaciones de los objetos user.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 16fe6273ec71c37f0ef6408e3671f42fadcc6123
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959716"
---
# <a name="list-users"></a><span data-ttu-id="52fa9-103">Enumerar usuarios</span><span class="sxs-lookup"><span data-stu-id="52fa9-103">List users</span></span>

> <span data-ttu-id="52fa9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52fa9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52fa9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52fa9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="52fa9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52fa9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52fa9-107">Enumere las propiedades y las relaciones de los objetos [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="52fa9-107">List properties and relationships of the [user](../resources/intune-shared-user.md) objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52fa9-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52fa9-108">Prerequisites</span></span>

<span data-ttu-id="52fa9-109">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="52fa9-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="52fa9-110">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="52fa9-110">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="52fa9-111">El permiso específico depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="52fa9-111">The specific permission depends on the context.</span></span>

|<span data-ttu-id="52fa9-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52fa9-112">Permission type</span></span>|<span data-ttu-id="52fa9-113">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52fa9-113">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="52fa9-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52fa9-114">Delegated (work or school account)</span></span>||
| <span data-ttu-id="52fa9-115">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="52fa9-115">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="52fa9-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="52fa9-116">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
| <span data-ttu-id="52fa9-117">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="52fa9-117">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="52fa9-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="52fa9-118">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
| <span data-ttu-id="52fa9-119">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="52fa9-119">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="52fa9-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="52fa9-120">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span> |
| <span data-ttu-id="52fa9-121">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="52fa9-121">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="52fa9-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="52fa9-122">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span> |
|<span data-ttu-id="52fa9-123">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52fa9-123">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="52fa9-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52fa9-124">Not supported.</span></span>|
|<span data-ttu-id="52fa9-125">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52fa9-125">Application</span></span>|<span data-ttu-id="52fa9-126">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52fa9-126">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="52fa9-127">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52fa9-127">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users
```

## <a name="request-headers"></a><span data-ttu-id="52fa9-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52fa9-128">Request headers</span></span>

|<span data-ttu-id="52fa9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52fa9-129">Header</span></span>|<span data-ttu-id="52fa9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="52fa9-130">Value</span></span>|
|:---|:---|
|<span data-ttu-id="52fa9-131">Autorización</span><span class="sxs-lookup"><span data-stu-id="52fa9-131">Authorization</span></span>|<span data-ttu-id="52fa9-132">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="52fa9-132">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="52fa9-133">Accept</span><span class="sxs-lookup"><span data-stu-id="52fa9-133">Accept</span></span>|<span data-ttu-id="52fa9-134">application/json</span><span class="sxs-lookup"><span data-stu-id="52fa9-134">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="52fa9-135">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52fa9-135">Request body</span></span>

<span data-ttu-id="52fa9-136">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52fa9-136">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="52fa9-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52fa9-137">Response</span></span>

<span data-ttu-id="52fa9-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52fa9-138">If successful, this method returns a `200 OK` response code and a collection of [user](../resources/intune-shared-user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52fa9-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52fa9-139">Example</span></span>

### <a name="request"></a><span data-ttu-id="52fa9-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52fa9-140">Request</span></span>

<span data-ttu-id="52fa9-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52fa9-141">Here is an example of the request.</span></span>

``` http
GET https://graph.microsoft.com/beta/users
```

### <a name="response"></a><span data-ttu-id="52fa9-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52fa9-142">Response</span></span>

<span data-ttu-id="52fa9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52fa9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

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



