---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 455a3e0c68fadc9768c434f5893dbc950a371bab
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922525"
---
# <a name="update-user"></a><span data-ttu-id="d0931-103">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="d0931-103">Update user</span></span>

> <span data-ttu-id="d0931-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0931-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0931-105">Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="d0931-105">Update the properties of a [user](../resources/intune-shared-user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0931-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0931-106">Prerequisites</span></span>
<span data-ttu-id="d0931-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0931-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d0931-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0931-109">Permission type</span></span>|<span data-ttu-id="d0931-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0931-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0931-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0931-111">Delegated (work or school account)</span></span>| <span data-ttu-id="d0931-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="d0931-112">_varies by context_</span></span>|
| <span data-ttu-id="d0931-113">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d0931-113">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="d0931-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0931-114">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="d0931-115">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="d0931-115">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="d0931-116">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0931-116">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="d0931-117">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="d0931-117">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="d0931-118">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0931-118">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="d0931-119">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="d0931-119">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="d0931-120">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0931-120">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="d0931-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0931-121">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0931-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0931-122">Not supported.</span></span>|
|<span data-ttu-id="d0931-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0931-123">Application</span></span>|<span data-ttu-id="d0931-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0931-124">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0931-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0931-125">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="d0931-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0931-126">Request headers</span></span>
|<span data-ttu-id="d0931-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0931-127">Header</span></span>|<span data-ttu-id="d0931-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d0931-128">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0931-129">Autorización</span><span class="sxs-lookup"><span data-stu-id="d0931-129">Authorization</span></span>|<span data-ttu-id="d0931-130">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0931-130">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d0931-131">Accept</span><span class="sxs-lookup"><span data-stu-id="d0931-131">Accept</span></span>|<span data-ttu-id="d0931-132">application/json</span><span class="sxs-lookup"><span data-stu-id="d0931-132">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0931-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0931-133">Request body</span></span>
<span data-ttu-id="d0931-134">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="d0931-134">In the request body, supply a JSON representation for the [user](../resources/intune-shared-user.md) object.</span></span>

<span data-ttu-id="d0931-135">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="d0931-135">The following table shows the properties that are required when you create the [user](../resources/intune-shared-user.md).</span></span>

|<span data-ttu-id="d0931-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0931-136">Property</span></span>|<span data-ttu-id="d0931-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0931-137">Type</span></span>|<span data-ttu-id="d0931-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0931-138">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0931-139">id</span><span class="sxs-lookup"><span data-stu-id="d0931-139">id</span></span>|<span data-ttu-id="d0931-140">String</span><span class="sxs-lookup"><span data-stu-id="d0931-140">String</span></span>|<span data-ttu-id="d0931-141">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="d0931-141">Unique identifier of the user.</span></span>|
|<span data-ttu-id="d0931-142">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="d0931-142">**Onboarding**</span></span>|
|<span data-ttu-id="d0931-143">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="d0931-143">deviceEnrollmentLimit</span></span>|<span data-ttu-id="d0931-144">Int32</span><span class="sxs-lookup"><span data-stu-id="d0931-144">Int32</span></span>|<span data-ttu-id="d0931-145">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="d0931-145">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="d0931-146">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="d0931-146">Allowed values are 5 or 1000.</span></span>|

## <a name="response"></a><span data-ttu-id="d0931-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0931-147">Response</span></span>
<span data-ttu-id="d0931-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune-shared-user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0931-148">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0931-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0931-149">Example</span></span>

### <a name="request"></a><span data-ttu-id="d0931-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0931-150">Request</span></span>
<span data-ttu-id="d0931-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0931-151">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="d0931-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0931-152">Response</span></span>
<span data-ttu-id="d0931-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0931-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



