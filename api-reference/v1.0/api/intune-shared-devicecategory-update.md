---
title: Actualizar deviceCategory
description: Actualice las propiedades de un objeto deviceCategory.
author: tfitzmac
ms.openlocfilehash: 73980aa4c178ff610ce44dc3b832c8c931d72740
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344306"
---
# <a name="update-devicecategory"></a><span data-ttu-id="91f1b-103">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="91f1b-103">Update deviceCategory</span></span>

> <span data-ttu-id="91f1b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="91f1b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="91f1b-105">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="91f1b-105">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="91f1b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="91f1b-106">Prerequisites</span></span>
<span data-ttu-id="91f1b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="91f1b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="91f1b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="91f1b-109">Permission type</span></span>|<span data-ttu-id="91f1b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="91f1b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="91f1b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="91f1b-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="91f1b-112">&nbsp;&nbsp; **Incorporación** y</span><span class="sxs-lookup"><span data-stu-id="91f1b-112">&nbsp; &nbsp; **Onboarding** and</span></span> <br> <span data-ttu-id="91f1b-113">&nbsp;&nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="91f1b-113">&nbsp; &nbsp; **Device Management**</span></span>| <span data-ttu-id="91f1b-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="91f1b-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="91f1b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="91f1b-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="91f1b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91f1b-116">Not supported.</span></span>|
|<span data-ttu-id="91f1b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="91f1b-117">Application</span></span>|<span data-ttu-id="91f1b-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="91f1b-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="91f1b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="91f1b-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
```

## <a name="request-headers"></a><span data-ttu-id="91f1b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="91f1b-120">Request headers</span></span>
|<span data-ttu-id="91f1b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91f1b-121">Header</span></span>|<span data-ttu-id="91f1b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="91f1b-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="91f1b-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="91f1b-123">Authorization</span></span>|<span data-ttu-id="91f1b-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="91f1b-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="91f1b-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="91f1b-125">Accept</span></span>|<span data-ttu-id="91f1b-126">application/json</span><span class="sxs-lookup"><span data-stu-id="91f1b-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="91f1b-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="91f1b-127">Request body</span></span>
<span data-ttu-id="91f1b-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="91f1b-128">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

<span data-ttu-id="91f1b-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="91f1b-129">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>

|<span data-ttu-id="91f1b-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91f1b-130">Property</span></span>|<span data-ttu-id="91f1b-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="91f1b-131">Type</span></span>|<span data-ttu-id="91f1b-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="91f1b-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="91f1b-133">id</span><span class="sxs-lookup"><span data-stu-id="91f1b-133">id</span></span>|<span data-ttu-id="91f1b-134">String</span><span class="sxs-lookup"><span data-stu-id="91f1b-134">String</span></span>|<span data-ttu-id="91f1b-135">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91f1b-135">Unique identifier for the device category.</span></span> <span data-ttu-id="91f1b-136">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="91f1b-136">Read-only.</span></span>|
|<span data-ttu-id="91f1b-137">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="91f1b-137">**Onboarding**</span></span>|
|<span data-ttu-id="91f1b-138">displayName</span><span class="sxs-lookup"><span data-stu-id="91f1b-138">displayName</span></span>|<span data-ttu-id="91f1b-139">String</span><span class="sxs-lookup"><span data-stu-id="91f1b-139">String</span></span>|<span data-ttu-id="91f1b-140">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91f1b-140">Display name for the device category.</span></span>|
|<span data-ttu-id="91f1b-141">descripción</span><span class="sxs-lookup"><span data-stu-id="91f1b-141">description</span></span>|<span data-ttu-id="91f1b-142">String</span><span class="sxs-lookup"><span data-stu-id="91f1b-142">String</span></span>|<span data-ttu-id="91f1b-143">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91f1b-143">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="91f1b-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91f1b-144">Response</span></span>
<span data-ttu-id="91f1b-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91f1b-145">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="91f1b-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="91f1b-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="91f1b-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="91f1b-147">Request</span></span>
<span data-ttu-id="91f1b-148">Estos son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="91f1b-148">Here are examples of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}
Content-type: application/json
Content-length: 82

{
  "displayName": "Display Name value",
  "description": "Description value"
}

PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

### <a name="response"></a><span data-ttu-id="91f1b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="91f1b-149">Response</span></span>
<span data-ttu-id="91f1b-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="91f1b-150">Here is an example of the response.</span></span> <span data-ttu-id="91f1b-151">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="91f1b-151">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="91f1b-152">Propiedades de la respuesta variará según el contexto.</span><span class="sxs-lookup"><span data-stu-id="91f1b-152">Response properties will vary according to context.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 184

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8",
  "displayName": "Display Name value",
  "description": "Description value"
}
```



