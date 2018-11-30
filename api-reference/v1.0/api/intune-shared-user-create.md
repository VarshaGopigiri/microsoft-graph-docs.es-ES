---
title: Crear usuario
description: Crea un objeto de usuario nuevo.
ms.openlocfilehash: e79fc06543b2f5d6c827b4f0900c4ba972bf6e74
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031612"
---
# <a name="create-user"></a><span data-ttu-id="f61de-103">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="f61de-103">Create user</span></span>

> <span data-ttu-id="f61de-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f61de-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f61de-105">Cree un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="f61de-105">Create a new [user](../resources/intune-shared-user.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f61de-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f61de-106">Prerequisites</span></span>
<span data-ttu-id="f61de-107">Uno de los siguientes permisos se requiere para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f61de-107">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="f61de-108">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f61de-108">To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>  <span data-ttu-id="f61de-109">Los permisos específicos necesarios depende del contexto.</span><span class="sxs-lookup"><span data-stu-id="f61de-109">The specific permission required depends on the context.</span></span>

|<span data-ttu-id="f61de-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f61de-110">Permission type</span></span>|<span data-ttu-id="f61de-111">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f61de-111">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f61de-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f61de-112">Delegated (work or school account)</span></span>| <span data-ttu-id="f61de-113">_varía según el contexto_</span><span class="sxs-lookup"><span data-stu-id="f61de-113">_varies by context_</span></span> |
| <span data-ttu-id="f61de-114">&nbsp;&nbsp; Administración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f61de-114">&nbsp; &nbsp; Device management</span></span> | <span data-ttu-id="f61de-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f61de-115">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
| <span data-ttu-id="f61de-116">&nbsp;&nbsp; MAM</span><span class="sxs-lookup"><span data-stu-id="f61de-116">&nbsp; &nbsp; MAM</span></span> | <span data-ttu-id="f61de-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f61de-117">DeviceManagementApps.ReadWrite.All</span></span> |
| <span data-ttu-id="f61de-118">&nbsp;&nbsp; Incorporación</span><span class="sxs-lookup"><span data-stu-id="f61de-118">&nbsp; &nbsp; Onboarding</span></span> | <span data-ttu-id="f61de-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f61de-119">DeviceManagementServiceConfig.ReadWrite.All</span></span> |
| <span data-ttu-id="f61de-120">&nbsp;&nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="f61de-120">&nbsp; &nbsp; Troubleshooting</span></span> | <span data-ttu-id="f61de-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f61de-121">DeviceManagementManagedDevices.ReadWrite.All</span></span> |
|<span data-ttu-id="f61de-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f61de-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f61de-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f61de-123">Not supported.</span></span>|
|<span data-ttu-id="f61de-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f61de-124">Application</span></span>|<span data-ttu-id="f61de-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f61de-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f61de-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f61de-126">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users
```

## <a name="request-headers"></a><span data-ttu-id="f61de-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f61de-127">Request headers</span></span>
|<span data-ttu-id="f61de-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f61de-128">Header</span></span>|<span data-ttu-id="f61de-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f61de-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f61de-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="f61de-130">Authorization</span></span>|<span data-ttu-id="f61de-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f61de-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f61de-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f61de-132">Accept</span></span>|<span data-ttu-id="f61de-133">application/json</span><span class="sxs-lookup"><span data-stu-id="f61de-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f61de-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f61de-134">Request body</span></span>
<span data-ttu-id="f61de-135">En el cuerpo de la solicitud, especifique una representación JSON del objeto user.</span><span class="sxs-lookup"><span data-stu-id="f61de-135">In the request body, supply a JSON representation for the user object.</span></span>

<span data-ttu-id="f61de-136">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto user.</span><span class="sxs-lookup"><span data-stu-id="f61de-136">The following table shows the properties that are required when you create the user.</span></span>

|<span data-ttu-id="f61de-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f61de-137">Property</span></span>|<span data-ttu-id="f61de-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="f61de-138">Type</span></span>|<span data-ttu-id="f61de-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="f61de-139">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f61de-140">id</span><span class="sxs-lookup"><span data-stu-id="f61de-140">id</span></span>|<span data-ttu-id="f61de-141">String</span><span class="sxs-lookup"><span data-stu-id="f61de-141">String</span></span>|<span data-ttu-id="f61de-142">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="f61de-142">Unique identifier of the user.</span></span>|
|<span data-ttu-id="f61de-143">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="f61de-143">**Onboarding**</span></span>|
|<span data-ttu-id="f61de-144">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="f61de-144">deviceEnrollmentLimit</span></span>|<span data-ttu-id="f61de-145">Int32</span><span class="sxs-lookup"><span data-stu-id="f61de-145">Int32</span></span>|<span data-ttu-id="f61de-146">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="f61de-146">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="f61de-147">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="f61de-147">Allowed values are 5 or 1000.</span></span>|

<span data-ttu-id="f61de-148">Compatibilidad con propiedades de cuerpo de solicitud varía según el contexto.</span><span class="sxs-lookup"><span data-stu-id="f61de-148">Request body property support varies according to context.</span></span>

## <a name="response"></a><span data-ttu-id="f61de-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f61de-149">Response</span></span>
<span data-ttu-id="f61de-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [user](../resources/intune-shared-user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f61de-150">If successful, this method returns a `201 Created` response code and a [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f61de-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f61de-151">Example</span></span>

### <a name="request"></a><span data-ttu-id="f61de-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f61de-152">Request</span></span>
<span data-ttu-id="f61de-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f61de-153">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json
Content-length: 46

{
  "@odata.type": "#microsoft.graph.user"
}
```

### <a name="response"></a><span data-ttu-id="f61de-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f61de-154">Response</span></span>
<span data-ttu-id="f61de-155">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f61de-155">Here is an example of the response.</span></span> <span data-ttu-id="f61de-156">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="f61de-156">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="f61de-157">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="f61de-157">Properties returned from an actual call vary according to context.</span></span>

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



