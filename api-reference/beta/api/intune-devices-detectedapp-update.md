---
title: Actualizar detectedApp
description: Actualice las propiedades de un objeto detectedApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 550bbcfd422f12bc3c11102e3438ffab0162680b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862954"
---
# <a name="update-detectedapp"></a><span data-ttu-id="49121-103">Actualizar detectedApp</span><span class="sxs-lookup"><span data-stu-id="49121-103">Update detectedApp</span></span>

> <span data-ttu-id="49121-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="49121-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="49121-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="49121-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="49121-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="49121-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="49121-107">Actualice las propiedades de un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="49121-107">Update the properties of a [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="49121-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="49121-108">Prerequisites</span></span>
<span data-ttu-id="49121-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="49121-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="49121-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="49121-111">Permission type</span></span>|<span data-ttu-id="49121-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="49121-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="49121-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="49121-113">Delegated (work or school account)</span></span>|<span data-ttu-id="49121-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="49121-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="49121-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="49121-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="49121-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49121-116">Not supported.</span></span>|
|<span data-ttu-id="49121-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="49121-117">Application</span></span>|<span data-ttu-id="49121-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="49121-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="49121-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49121-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/detectedApps/{detectedAppId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="49121-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49121-120">Request headers</span></span>
|<span data-ttu-id="49121-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49121-121">Header</span></span>|<span data-ttu-id="49121-122">Valor</span><span class="sxs-lookup"><span data-stu-id="49121-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="49121-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="49121-123">Authorization</span></span>|<span data-ttu-id="49121-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="49121-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="49121-125">Accept</span><span class="sxs-lookup"><span data-stu-id="49121-125">Accept</span></span>|<span data-ttu-id="49121-126">application/json</span><span class="sxs-lookup"><span data-stu-id="49121-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="49121-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49121-127">Request body</span></span>
<span data-ttu-id="49121-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="49121-128">In the request body, supply a JSON representation for the [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>

<span data-ttu-id="49121-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="49121-129">The following table shows the properties that are required when you create the [detectedApp](../resources/intune-devices-detectedapp.md).</span></span>

|<span data-ttu-id="49121-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="49121-130">Property</span></span>|<span data-ttu-id="49121-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="49121-131">Type</span></span>|<span data-ttu-id="49121-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="49121-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="49121-133">id</span><span class="sxs-lookup"><span data-stu-id="49121-133">id</span></span>|<span data-ttu-id="49121-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="49121-134">String</span></span>|<span data-ttu-id="49121-135">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="49121-135">The unique Identifier for the detected application.</span></span> <span data-ttu-id="49121-136">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="49121-136">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="49121-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="49121-137">Read-only.</span></span>|
|<span data-ttu-id="49121-138">displayName</span><span class="sxs-lookup"><span data-stu-id="49121-138">displayName</span></span>|<span data-ttu-id="49121-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="49121-139">String</span></span>|<span data-ttu-id="49121-140">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="49121-140">Name of the discovered application.</span></span> <span data-ttu-id="49121-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="49121-141">Read-only</span></span>|
|<span data-ttu-id="49121-142">version</span><span class="sxs-lookup"><span data-stu-id="49121-142">version</span></span>|<span data-ttu-id="49121-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="49121-143">String</span></span>|<span data-ttu-id="49121-144">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="49121-144">Version of the discovered application.</span></span> <span data-ttu-id="49121-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="49121-145">Read-only</span></span>|
|<span data-ttu-id="49121-146">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="49121-146">sizeInByte</span></span>|<span data-ttu-id="49121-147">Int64</span><span class="sxs-lookup"><span data-stu-id="49121-147">Int64</span></span>|<span data-ttu-id="49121-148">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="49121-148">Discovered application size in bytes.</span></span> <span data-ttu-id="49121-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="49121-149">Read-only</span></span>|
|<span data-ttu-id="49121-150">deviceCount</span><span class="sxs-lookup"><span data-stu-id="49121-150">deviceCount</span></span>|<span data-ttu-id="49121-151">Int32</span><span class="sxs-lookup"><span data-stu-id="49121-151">Int32</span></span>|<span data-ttu-id="49121-152">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="49121-152">The number of devices that have installed this application</span></span>|



## <a name="response"></a><span data-ttu-id="49121-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49121-153">Response</span></span>
<span data-ttu-id="49121-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [detectedApp](../resources/intune-devices-detectedapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49121-154">If successful, this method returns a `200 OK` response code and an updated [detectedApp](../resources/intune-devices-detectedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="49121-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49121-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="49121-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49121-156">Request</span></span>
<span data-ttu-id="49121-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49121-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/detectedApps/{detectedAppId}
Content-type: application/json
Content-length: 117

{
  "displayName": "Display Name value",
  "version": "Version value",
  "sizeInByte": 10,
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="49121-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49121-158">Response</span></span>
<span data-ttu-id="49121-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49121-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 216

{
  "@odata.type": "#microsoft.graph.detectedApp",
  "id": "caf60db6-0db6-caf6-b60d-f6cab60df6ca",
  "displayName": "Display Name value",
  "version": "Version value",
  "sizeInByte": 10,
  "deviceCount": 11
}
```





