---
title: Actualizar usuario
description: Actualiza las propiedades de un objeto de usuario.
author: tfitzmac
ms.openlocfilehash: c4fb2bde10d913b6bd9c30a34b6e1b9e8169a9e6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317391"
---
# <a name="update-user"></a><span data-ttu-id="466c4-103">Actualizar usuario</span><span class="sxs-lookup"><span data-stu-id="466c4-103">Update user</span></span>

> <span data-ttu-id="466c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="466c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="466c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="466c4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="466c4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="466c4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="466c4-107">Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="466c4-107">Update the properties of a [user](../resources/intune-shared-user.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="466c4-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="466c4-108">Prerequisites</span></span>

<span data-ttu-id="466c4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="466c4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="466c4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="466c4-111">Permission type</span></span>|<span data-ttu-id="466c4-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="466c4-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="466c4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="466c4-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="466c4-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="466c4-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="466c4-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="466c4-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="466c4-116">&nbsp;&nbsp; **MAM**</span><span class="sxs-lookup"><span data-stu-id="466c4-116">&nbsp; &nbsp; **MAM**</span></span> | <span data-ttu-id="466c4-117">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="466c4-117">DeviceManagementApps.ReadWrite.All</span></span>|
| <span data-ttu-id="466c4-118">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="466c4-118">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="466c4-119">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="466c4-119">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
| <span data-ttu-id="466c4-120">&nbsp; &nbsp; **Solución de problemas**</span><span class="sxs-lookup"><span data-stu-id="466c4-120">&nbsp; &nbsp; **Troubleshooting**</span></span> | <span data-ttu-id="466c4-121">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="466c4-121">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="466c4-122">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="466c4-122">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="466c4-123">No admitida.</span><span class="sxs-lookup"><span data-stu-id="466c4-123">Not supported.</span></span>|
|<span data-ttu-id="466c4-124">Aplicación</span><span class="sxs-lookup"><span data-stu-id="466c4-124">Application</span></span>|<span data-ttu-id="466c4-125">No admitida.</span><span class="sxs-lookup"><span data-stu-id="466c4-125">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="466c4-126">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="466c4-126">HTTP Request</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="466c4-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="466c4-127">Request headers</span></span>

|<span data-ttu-id="466c4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="466c4-128">Header</span></span>|<span data-ttu-id="466c4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="466c4-129">Value</span></span>|
|:---|:---|
|<span data-ttu-id="466c4-130">Autorización</span><span class="sxs-lookup"><span data-stu-id="466c4-130">Authorization</span></span>|<span data-ttu-id="466c4-131">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="466c4-131">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="466c4-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="466c4-132">Accept</span></span>|<span data-ttu-id="466c4-133">application/json</span><span class="sxs-lookup"><span data-stu-id="466c4-133">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="466c4-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="466c4-134">Request body</span></span>

<span data-ttu-id="466c4-135">En el cuerpo de la solicitud, especifique una representación JSON del objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="466c4-135">In the request body, supply a JSON representation for the [user](../resources/intune-shared-user.md) object.</span></span>

<span data-ttu-id="466c4-136">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [user](../resources/intune-shared-user.md).</span><span class="sxs-lookup"><span data-stu-id="466c4-136">The following table shows the properties that are required when you create the [user](../resources/intune-shared-user.md).</span></span>

|<span data-ttu-id="466c4-137">Propiedad</span><span class="sxs-lookup"><span data-stu-id="466c4-137">Property</span></span>|<span data-ttu-id="466c4-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="466c4-138">Type</span></span>|<span data-ttu-id="466c4-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="466c4-139">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="466c4-140">id</span><span class="sxs-lookup"><span data-stu-id="466c4-140">id</span></span>|<span data-ttu-id="466c4-141">String</span><span class="sxs-lookup"><span data-stu-id="466c4-141">String</span></span>|<span data-ttu-id="466c4-142">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="466c4-142">Unique identifier of the user.</span></span>|
|<span data-ttu-id="466c4-143">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="466c4-143">**Onboarding**</span></span>|
|<span data-ttu-id="466c4-144">deviceEnrollmentLimit</span><span class="sxs-lookup"><span data-stu-id="466c4-144">deviceEnrollmentLimit</span></span>|<span data-ttu-id="466c4-145">Int32</span><span class="sxs-lookup"><span data-stu-id="466c4-145">Int32</span></span>|<span data-ttu-id="466c4-146">El límite del número máximo de dispositivos que el usuario puede inscribir.</span><span class="sxs-lookup"><span data-stu-id="466c4-146">The limit on the maximum number of devices that the user is permitted to enroll.</span></span> <span data-ttu-id="466c4-147">Los valores permitidos son 5 o 1000.</span><span class="sxs-lookup"><span data-stu-id="466c4-147">Allowed values are 5 or 1000.</span></span>|

## <a name="response"></a><span data-ttu-id="466c4-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="466c4-148">Response</span></span>

<span data-ttu-id="466c4-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/intune-shared-user.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="466c4-149">If successful, this method returns a `200 OK` response code and an updated [user](../resources/intune-shared-user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="466c4-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="466c4-150">Example</span></span>

### <a name="request"></a><span data-ttu-id="466c4-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="466c4-151">Request</span></span>

<span data-ttu-id="466c4-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="466c4-152">Here is an example of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="466c4-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="466c4-153">Response</span></span>

<span data-ttu-id="466c4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="466c4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```



