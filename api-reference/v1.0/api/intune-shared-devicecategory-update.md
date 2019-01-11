---
title: Actualizar deviceCategory
description: Actualice las propiedades de un objeto deviceCategory.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 38377c7b92983f10ad42284b7790782cde2264fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27832980"
---
# <a name="update-devicecategory"></a><span data-ttu-id="ec316-103">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="ec316-103">Update deviceCategory</span></span>

> <span data-ttu-id="ec316-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec316-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec316-105">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="ec316-105">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ec316-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ec316-106">Prerequisites</span></span>
<span data-ttu-id="ec316-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec316-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ec316-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec316-109">Permission type</span></span>|<span data-ttu-id="ec316-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec316-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ec316-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec316-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="ec316-112">&nbsp;&nbsp; **Incorporación** y</span><span class="sxs-lookup"><span data-stu-id="ec316-112">&nbsp; &nbsp; **Onboarding** and</span></span> <br> <span data-ttu-id="ec316-113">&nbsp;&nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ec316-113">&nbsp; &nbsp; **Device Management**</span></span>| <span data-ttu-id="ec316-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ec316-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="ec316-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec316-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ec316-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec316-116">Not supported.</span></span>|
|<span data-ttu-id="ec316-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec316-117">Application</span></span>|<span data-ttu-id="ec316-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec316-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ec316-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec316-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
```

## <a name="request-headers"></a><span data-ttu-id="ec316-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec316-120">Request headers</span></span>
|<span data-ttu-id="ec316-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec316-121">Header</span></span>|<span data-ttu-id="ec316-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ec316-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ec316-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ec316-123">Authorization</span></span>|<span data-ttu-id="ec316-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ec316-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ec316-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ec316-125">Accept</span></span>|<span data-ttu-id="ec316-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ec316-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ec316-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec316-127">Request body</span></span>
<span data-ttu-id="ec316-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="ec316-128">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

<span data-ttu-id="ec316-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="ec316-129">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>

|<span data-ttu-id="ec316-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec316-130">Property</span></span>|<span data-ttu-id="ec316-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec316-131">Type</span></span>|<span data-ttu-id="ec316-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec316-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec316-133">id</span><span class="sxs-lookup"><span data-stu-id="ec316-133">id</span></span>|<span data-ttu-id="ec316-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec316-134">String</span></span>|<span data-ttu-id="ec316-135">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec316-135">Unique identifier for the device category.</span></span> <span data-ttu-id="ec316-136">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ec316-136">Read-only.</span></span>|
|<span data-ttu-id="ec316-137">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="ec316-137">**Onboarding**</span></span>|
|<span data-ttu-id="ec316-138">displayName</span><span class="sxs-lookup"><span data-stu-id="ec316-138">displayName</span></span>|<span data-ttu-id="ec316-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec316-139">String</span></span>|<span data-ttu-id="ec316-140">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec316-140">Display name for the device category.</span></span>|
|<span data-ttu-id="ec316-141">descripción</span><span class="sxs-lookup"><span data-stu-id="ec316-141">description</span></span>|<span data-ttu-id="ec316-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec316-142">String</span></span>|<span data-ttu-id="ec316-143">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec316-143">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="ec316-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec316-144">Response</span></span>
<span data-ttu-id="ec316-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec316-145">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec316-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec316-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="ec316-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec316-147">Request</span></span>
<span data-ttu-id="ec316-148">Estos son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec316-148">Here are examples of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ec316-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec316-149">Response</span></span>
<span data-ttu-id="ec316-150">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec316-150">Here is an example of the response.</span></span> <span data-ttu-id="ec316-151">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="ec316-151">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="ec316-152">Propiedades de la respuesta variará según el contexto.</span><span class="sxs-lookup"><span data-stu-id="ec316-152">Response properties will vary according to context.</span></span>
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



