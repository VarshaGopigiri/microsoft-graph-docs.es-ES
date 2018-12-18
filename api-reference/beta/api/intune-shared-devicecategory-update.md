---
title: Actualizar deviceCategory
description: Actualice las propiedades de un objeto deviceCategory.
author: tfitzmac
ms.openlocfilehash: 8676067ff4ce34358bcfd8400d28e1d73bd11f68
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27321521"
---
# <a name="update-devicecategory"></a><span data-ttu-id="01513-103">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="01513-103">Update deviceCategory</span></span>

> <span data-ttu-id="01513-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01513-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01513-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01513-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="01513-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01513-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01513-107">Actualice las propiedades de un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="01513-107">Update the properties of a [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01513-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="01513-108">Prerequisites</span></span>

<span data-ttu-id="01513-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01513-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01513-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01513-111">Permission type</span></span>|<span data-ttu-id="01513-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01513-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="01513-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01513-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="01513-114">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="01513-114">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="01513-115">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01513-115">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
| <span data-ttu-id="01513-116">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="01513-116">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="01513-117">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01513-117">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="01513-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01513-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="01513-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01513-119">Not supported.</span></span>|
|<span data-ttu-id="01513-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01513-120">Application</span></span>|<span data-ttu-id="01513-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01513-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="01513-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01513-122">HTTP Request</span></span>

<span data-ttu-id="01513-123">**Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="01513-123">**Device management**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

<span data-ttu-id="01513-124">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="01513-124">**On-boarding**</span></span>

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="request-headers"></a><span data-ttu-id="01513-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01513-125">Request headers</span></span>

|<span data-ttu-id="01513-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01513-126">Header</span></span>|<span data-ttu-id="01513-127">Valor</span><span class="sxs-lookup"><span data-stu-id="01513-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="01513-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="01513-128">Authorization</span></span>|<span data-ttu-id="01513-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="01513-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="01513-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="01513-130">Accept</span></span>|<span data-ttu-id="01513-131">application/json</span><span class="sxs-lookup"><span data-stu-id="01513-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="01513-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01513-132">Request body</span></span>

<span data-ttu-id="01513-133">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="01513-133">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>

<span data-ttu-id="01513-134">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="01513-134">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune-shared-devicecategory.md).</span></span>

|<span data-ttu-id="01513-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01513-135">Property</span></span>|<span data-ttu-id="01513-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="01513-136">Type</span></span>|<span data-ttu-id="01513-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="01513-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01513-138">id</span><span class="sxs-lookup"><span data-stu-id="01513-138">id</span></span>|<span data-ttu-id="01513-139">String</span><span class="sxs-lookup"><span data-stu-id="01513-139">String</span></span>|<span data-ttu-id="01513-140">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01513-140">Unique identifier for the device category.</span></span> <span data-ttu-id="01513-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01513-141">Read-only.</span></span>|
|<span data-ttu-id="01513-142">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="01513-142">**Onboarding**</span></span>|
|<span data-ttu-id="01513-143">descripción</span><span class="sxs-lookup"><span data-stu-id="01513-143">description</span></span>|<span data-ttu-id="01513-144">String</span><span class="sxs-lookup"><span data-stu-id="01513-144">String</span></span>|<span data-ttu-id="01513-145">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01513-145">Optional description for the device category.</span></span>|
|<span data-ttu-id="01513-146">displayName</span><span class="sxs-lookup"><span data-stu-id="01513-146">displayName</span></span>|<span data-ttu-id="01513-147">String</span><span class="sxs-lookup"><span data-stu-id="01513-147">String</span></span>|<span data-ttu-id="01513-148">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01513-148">Display name for the device category.</span></span>|

## <a name="response"></a><span data-ttu-id="01513-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01513-149">Response</span></span>

<span data-ttu-id="01513-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01513-150">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01513-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01513-151">Example</span></span>

### <a name="request"></a><span data-ttu-id="01513-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01513-152">Request</span></span>

<span data-ttu-id="01513-153">Estos son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01513-153">Here are examples of the request.</span></span>

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

### <a name="response"></a><span data-ttu-id="01513-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01513-154">Response</span></span>

<span data-ttu-id="01513-155">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01513-155">Here is an example of the response.</span></span> <span data-ttu-id="01513-156">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="01513-156">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="01513-157">Propiedades de la respuesta variará según el contexto.</span><span class="sxs-lookup"><span data-stu-id="01513-157">Response properties will vary according to context.</span></span>

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



