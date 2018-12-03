---
title: Actualizar deviceCategory
description: Actualice las propiedades de un objeto deviceCategory.
ms.openlocfilehash: bd01264d6e7e07a71c683c948fe6b01fd3822f5b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091180"
---
# <a name="update-devicecategory"></a><span data-ttu-id="3048b-103">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="3048b-103">Update deviceCategory</span></span>

> <span data-ttu-id="3048b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3048b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3048b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3048b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="3048b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3048b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3048b-107">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="3048b-107">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3048b-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3048b-108">Prerequisites</span></span>

<span data-ttu-id="3048b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3048b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3048b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3048b-111">Permission type</span></span>|<span data-ttu-id="3048b-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3048b-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3048b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3048b-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="3048b-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="3048b-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="3048b-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3048b-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="3048b-116">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="3048b-116">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="3048b-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3048b-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="3048b-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3048b-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3048b-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3048b-119">Not supported.</span></span>|
|<span data-ttu-id="3048b-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3048b-120">Application</span></span>|<span data-ttu-id="3048b-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3048b-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3048b-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3048b-122">HTTP Request</span></span>

<span data-ttu-id="3048b-123">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="3048b-123">**Device management**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

<span data-ttu-id="3048b-124">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="3048b-124">**On-boarding**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="3048b-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3048b-125">Request headers</span></span>

|<span data-ttu-id="3048b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3048b-126">Header</span></span>|<span data-ttu-id="3048b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3048b-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3048b-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="3048b-128">Authorization</span></span>|<span data-ttu-id="3048b-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3048b-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3048b-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3048b-130">Accept</span></span>|<span data-ttu-id="3048b-131">application/json</span><span class="sxs-lookup"><span data-stu-id="3048b-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3048b-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3048b-132">Request body</span></span>

<span data-ttu-id="3048b-133">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="3048b-133">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

<span data-ttu-id="3048b-134">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="3048b-134">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>

|<span data-ttu-id="3048b-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3048b-135">Property</span></span>|<span data-ttu-id="3048b-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="3048b-136">Type</span></span>|<span data-ttu-id="3048b-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="3048b-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3048b-138">id</span><span class="sxs-lookup"><span data-stu-id="3048b-138">id</span></span>|<span data-ttu-id="3048b-139">String</span><span class="sxs-lookup"><span data-stu-id="3048b-139">String</span></span>|<span data-ttu-id="3048b-140">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3048b-140">Unique identifier for the device category.</span></span> <span data-ttu-id="3048b-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3048b-141">Read-only.</span></span>|
|<span data-ttu-id="3048b-142">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="3048b-142">**Onboarding**</span></span>|
|<span data-ttu-id="3048b-143">descripción</span><span class="sxs-lookup"><span data-stu-id="3048b-143">description</span></span>|<span data-ttu-id="3048b-144">String</span><span class="sxs-lookup"><span data-stu-id="3048b-144">String</span></span>|<span data-ttu-id="3048b-145">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3048b-145">Optional description for the device category.</span></span>|
|<span data-ttu-id="3048b-146">displayName</span><span class="sxs-lookup"><span data-stu-id="3048b-146">displayName</span></span>|<span data-ttu-id="3048b-147">String</span><span class="sxs-lookup"><span data-stu-id="3048b-147">String</span></span>|<span data-ttu-id="3048b-148">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3048b-148">Display name for the device category.</span></span>|

## <a name="response"></a><span data-ttu-id="3048b-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3048b-149">Response</span></span>

<span data-ttu-id="3048b-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3048b-150">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3048b-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3048b-151">Example</span></span>

### <a name="request"></a><span data-ttu-id="3048b-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3048b-152">Request</span></span>

<span data-ttu-id="3048b-153">Estos son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3048b-153">Here are examples of the request.</span></span>

``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCategories/{deviceCategoryId}
Content-type: application/json
Content-length: 82

{
  "displayName": "Display Name value",
  "description": "Description value"
}

PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

### <a name="response"></a><span data-ttu-id="3048b-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3048b-154">Response</span></span>

<span data-ttu-id="3048b-155">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3048b-155">Here is an example of the response.</span></span> <span data-ttu-id="3048b-156">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="3048b-156">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="3048b-157">Propiedades de la respuesta variará según el contexto.</span><span class="sxs-lookup"><span data-stu-id="3048b-157">Response properties will vary according to context.</span></span>

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



