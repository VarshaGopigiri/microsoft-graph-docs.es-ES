---
title: Actualizar detectedApp
description: Actualice las propiedades de un objeto detectedApp.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 86b8eb3bc1bac0902ce36bd763c633f06919d2fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821934"
---
# <a name="update-detectedapp"></a><span data-ttu-id="de4a9-103">Actualizar detectedApp</span><span class="sxs-lookup"><span data-stu-id="de4a9-103">Update detectedApp</span></span>

> <span data-ttu-id="de4a9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="de4a9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="de4a9-105">Actualice las propiedades de un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="de4a9-105">Update the properties of a [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="de4a9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="de4a9-106">Prerequisites</span></span>
<span data-ttu-id="de4a9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="de4a9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="de4a9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de4a9-109">Permission type</span></span>|<span data-ttu-id="de4a9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de4a9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="de4a9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de4a9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="de4a9-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="de4a9-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="de4a9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de4a9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="de4a9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de4a9-114">Not supported.</span></span>|
|<span data-ttu-id="de4a9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de4a9-115">Application</span></span>|<span data-ttu-id="de4a9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de4a9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="de4a9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de4a9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/detectedApps/{detectedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="de4a9-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de4a9-118">Request headers</span></span>
|<span data-ttu-id="de4a9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de4a9-119">Header</span></span>|<span data-ttu-id="de4a9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="de4a9-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="de4a9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="de4a9-121">Authorization</span></span>|<span data-ttu-id="de4a9-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="de4a9-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="de4a9-123">Accept</span><span class="sxs-lookup"><span data-stu-id="de4a9-123">Accept</span></span>|<span data-ttu-id="de4a9-124">application/json</span><span class="sxs-lookup"><span data-stu-id="de4a9-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="de4a9-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="de4a9-125">Request body</span></span>
<span data-ttu-id="de4a9-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="de4a9-126">In the request body, supply a JSON representation for the [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>

<span data-ttu-id="de4a9-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="de4a9-127">The following table shows the properties that are required when you create the [detectedApp](../resources/intune-devices-detectedapp.md).</span></span>

|<span data-ttu-id="de4a9-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="de4a9-128">Property</span></span>|<span data-ttu-id="de4a9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="de4a9-129">Type</span></span>|<span data-ttu-id="de4a9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="de4a9-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="de4a9-131">id</span><span class="sxs-lookup"><span data-stu-id="de4a9-131">id</span></span>|<span data-ttu-id="de4a9-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="de4a9-132">String</span></span>|<span data-ttu-id="de4a9-133">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="de4a9-133">The unique Identifier for the detected application.</span></span> <span data-ttu-id="de4a9-134">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="de4a9-134">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="de4a9-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de4a9-135">Read-only.</span></span>|
|<span data-ttu-id="de4a9-136">displayName</span><span class="sxs-lookup"><span data-stu-id="de4a9-136">displayName</span></span>|<span data-ttu-id="de4a9-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="de4a9-137">String</span></span>|<span data-ttu-id="de4a9-138">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="de4a9-138">Name of the discovered application.</span></span> <span data-ttu-id="de4a9-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de4a9-139">Read-only</span></span>|
|<span data-ttu-id="de4a9-140">version</span><span class="sxs-lookup"><span data-stu-id="de4a9-140">version</span></span>|<span data-ttu-id="de4a9-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="de4a9-141">String</span></span>|<span data-ttu-id="de4a9-142">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="de4a9-142">Version of the discovered application.</span></span> <span data-ttu-id="de4a9-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de4a9-143">Read-only</span></span>|
|<span data-ttu-id="de4a9-144">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="de4a9-144">sizeInByte</span></span>|<span data-ttu-id="de4a9-145">Int64</span><span class="sxs-lookup"><span data-stu-id="de4a9-145">Int64</span></span>|<span data-ttu-id="de4a9-146">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="de4a9-146">Discovered application size in bytes.</span></span> <span data-ttu-id="de4a9-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="de4a9-147">Read-only</span></span>|
|<span data-ttu-id="de4a9-148">deviceCount</span><span class="sxs-lookup"><span data-stu-id="de4a9-148">deviceCount</span></span>|<span data-ttu-id="de4a9-149">Int32</span><span class="sxs-lookup"><span data-stu-id="de4a9-149">Int32</span></span>|<span data-ttu-id="de4a9-150">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="de4a9-150">The number of devices that have installed this application</span></span>|



## <a name="response"></a><span data-ttu-id="de4a9-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de4a9-151">Response</span></span>
<span data-ttu-id="de4a9-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [detectedApp](../resources/intune-devices-detectedapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de4a9-152">If successful, this method returns a `200 OK` response code and an updated [detectedApp](../resources/intune-devices-detectedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="de4a9-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de4a9-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="de4a9-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de4a9-154">Request</span></span>
<span data-ttu-id="de4a9-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de4a9-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}
Content-type: application/json
Content-length: 167

{
  "@odata.type": "#microsoft.graph.detectedApp",
  "displayName": "Display Name value",
  "version": "Version value",
  "sizeInByte": 10,
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="de4a9-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de4a9-156">Response</span></span>
<span data-ttu-id="de4a9-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="de4a9-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



