---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
ms.openlocfilehash: e1909d25e9cfd8281801ba0a398a3fc6901693bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083775"
---
# <a name="update-user"></a><span data-ttu-id="ed70f-103">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="ed70f-103">Update user</span></span>

> <span data-ttu-id="ed70f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed70f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed70f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed70f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ed70f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed70f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed70f-107">Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="ed70f-107">Update the properties of a [user](../resources/intune-shared-user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ed70f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ed70f-108">Prerequisites</span></span>

<span data-ttu-id="ed70f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ed70f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ed70f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ed70f-111">Permission type</span></span>|<span data-ttu-id="ed70f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ed70f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ed70f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ed70f-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="ed70f-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ed70f-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="ed70f-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed70f-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="ed70f-116">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="ed70f-116">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="ed70f-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed70f-117">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="ed70f-118">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="ed70f-118">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="ed70f-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed70f-119">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="ed70f-120">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="ed70f-120">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="ed70f-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ed70f-121">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="ed70f-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ed70f-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ed70f-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed70f-123">Not supported.</span></span>|
|<span data-ttu-id="ed70f-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ed70f-124">Application</span></span>|<span data-ttu-id="ed70f-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ed70f-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ed70f-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ed70f-126">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="ed70f-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ed70f-127">Request headers</span></span>

|<span data-ttu-id="ed70f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed70f-128">Header</span></span>|<span data-ttu-id="ed70f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ed70f-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ed70f-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="ed70f-130">Authorization</span></span>|<span data-ttu-id="ed70f-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ed70f-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ed70f-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ed70f-132">Accept</span></span>|<span data-ttu-id="ed70f-133">application/json</span><span class="sxs-lookup"><span data-stu-id="ed70f-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ed70f-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ed70f-134">Request body</span></span>

<span data-ttu-id="ed70f-135">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="ed70f-135">In the request body, supply a JSON representation for the [user](../resources/intune-shared-user.md) object.</span></span>

<span data-ttu-id="ed70f-136">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="ed70f-136">The following table shows the properties that are required when you create the [user](../resources/intune-shared-user.md).</span></span>

|<span data-ttu-id="ed70f-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed70f-137">Property</span></span>|<span data-ttu-id="ed70f-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed70f-138">Type</span></span>|<span data-ttu-id="ed70f-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed70f-139">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed70f-140">id</span><span class="sxs-lookup"><span data-stu-id="ed70f-140">id</span></span>|<span data-ttu-id="ed70f-141">String</span><span class="sxs-lookup"><span data-stu-id="ed70f-141">String</span></span>|<span data-ttu-id="ed70f-142">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="ed70f-142">Unique identifier of the user.</span></span>|
|<span data-ttu-id="ed70f-143">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="ed70f-143">**Onboarding**</span></span>|
|<span data-ttu-id="ed70f-144">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="ed70f-144">deviceEnrollmentLimit</span></span>|<span data-ttu-id="ed70f-145">Int32</span><span class="sxs-lookup"><span data-stu-id="ed70f-145">Int32</span></span>|<span data-ttu-id="ed70f-146">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="ed70f-146">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="ed70f-147">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="ed70f-147">Allowed values are 5 or 1000.</span></span>|

## <a name="response"></a><span data-ttu-id="ed70f-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed70f-148">Response</span></span>

<span data-ttu-id="ed70f-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune-shared-user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ed70f-149">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ed70f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ed70f-150">Example</span></span>

### <a name="request"></a><span data-ttu-id="ed70f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ed70f-151">Request</span></span>

<span data-ttu-id="ed70f-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ed70f-152">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="ed70f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ed70f-153">Response</span></span>

<span data-ttu-id="ed70f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ed70f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



