---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
ms.openlocfilehash: cfb8a7d46d8383cdaae4f012cff4ed0a0ad93594
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031077"
---
# <a name="update-user"></a><span data-ttu-id="68eb0-103">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="68eb0-103">Update user</span></span>

> <span data-ttu-id="68eb0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68eb0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68eb0-105">Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="68eb0-105">Update the properties of a [user](../resources/intune-shared-user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="68eb0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68eb0-106">Prerequisites</span></span>
<span data-ttu-id="68eb0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="68eb0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="68eb0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68eb0-109">Permission type</span></span>|<span data-ttu-id="68eb0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68eb0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="68eb0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68eb0-111">Delegated (work or school account)</span></span>| <span data-ttu-id="68eb0-112">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="68eb0-112">_varies by context_</span></span>|
| <span data-ttu-id="68eb0-113">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="68eb0-113">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="68eb0-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68eb0-114">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="68eb0-115">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="68eb0-115">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="68eb0-116">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68eb0-116">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="68eb0-117">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="68eb0-117">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="68eb0-118">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68eb0-118">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="68eb0-119">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="68eb0-119">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="68eb0-120">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68eb0-120">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="68eb0-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68eb0-121">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="68eb0-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68eb0-122">Not supported.</span></span>|
|<span data-ttu-id="68eb0-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68eb0-123">Application</span></span>|<span data-ttu-id="68eb0-124">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68eb0-124">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="68eb0-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68eb0-125">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="68eb0-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68eb0-126">Request headers</span></span>
|<span data-ttu-id="68eb0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68eb0-127">Header</span></span>|<span data-ttu-id="68eb0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="68eb0-128">Value</span></span>|
|:---|:---|
|<span data-ttu-id="68eb0-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="68eb0-129">Authorization</span></span>|<span data-ttu-id="68eb0-130">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="68eb0-130">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="68eb0-131">Aceptar</span><span class="sxs-lookup"><span data-stu-id="68eb0-131">Accept</span></span>|<span data-ttu-id="68eb0-132">application/json</span><span class="sxs-lookup"><span data-stu-id="68eb0-132">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="68eb0-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68eb0-133">Request body</span></span>
<span data-ttu-id="68eb0-134">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="68eb0-134">In the request body, supply a JSON representation for the [user](../resources/intune-shared-user.md) object.</span></span>

<span data-ttu-id="68eb0-135">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="68eb0-135">The following table shows the properties that are required when you create the [user](../resources/intune-shared-user.md).</span></span>

|<span data-ttu-id="68eb0-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68eb0-136">Property</span></span>|<span data-ttu-id="68eb0-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="68eb0-137">Type</span></span>|<span data-ttu-id="68eb0-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="68eb0-138">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="68eb0-139">id</span><span class="sxs-lookup"><span data-stu-id="68eb0-139">id</span></span>|<span data-ttu-id="68eb0-140">String</span><span class="sxs-lookup"><span data-stu-id="68eb0-140">String</span></span>|<span data-ttu-id="68eb0-141">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="68eb0-141">Unique identifier of the user.</span></span>|
|<span data-ttu-id="68eb0-142">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="68eb0-142">**Onboarding**</span></span>|
|<span data-ttu-id="68eb0-143">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="68eb0-143">deviceEnrollmentLimit</span></span>|<span data-ttu-id="68eb0-144">Int32</span><span class="sxs-lookup"><span data-stu-id="68eb0-144">Int32</span></span>|<span data-ttu-id="68eb0-145">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="68eb0-145">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="68eb0-146">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="68eb0-146">Allowed values are 5 or 1000.</span></span>|

## <a name="response"></a><span data-ttu-id="68eb0-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68eb0-147">Response</span></span>
<span data-ttu-id="68eb0-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune-shared-user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68eb0-148">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68eb0-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68eb0-149">Example</span></span>

### <a name="request"></a><span data-ttu-id="68eb0-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68eb0-150">Request</span></span>
<span data-ttu-id="68eb0-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68eb0-151">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="68eb0-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68eb0-152">Response</span></span>
<span data-ttu-id="68eb0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68eb0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



