---
title: Crear detectedApp
description: Cree un objeto detectedApp.
ms.openlocfilehash: 1ff48803609ce03aed1ff6f979cfe6d7a804d68b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090326"
---
# <a name="create-detectedapp"></a><span data-ttu-id="eb9e7-103">Crear detectedApp</span><span class="sxs-lookup"><span data-stu-id="eb9e7-103">Create detectedApp</span></span>

> <span data-ttu-id="eb9e7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb9e7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="eb9e7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="eb9e7-107">Cree un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="eb9e7-107">Create a new [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eb9e7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eb9e7-108">Prerequisites</span></span>
<span data-ttu-id="eb9e7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="eb9e7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="eb9e7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eb9e7-111">Permission type</span></span>|<span data-ttu-id="eb9e7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eb9e7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="eb9e7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eb9e7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="eb9e7-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="eb9e7-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="eb9e7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eb9e7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="eb9e7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-116">Not supported.</span></span>|
|<span data-ttu-id="eb9e7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eb9e7-117">Application</span></span>|<span data-ttu-id="eb9e7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="eb9e7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eb9e7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/detectedApps
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps
```

## <a name="request-headers"></a><span data-ttu-id="eb9e7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9e7-120">Request headers</span></span>
|<span data-ttu-id="eb9e7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb9e7-121">Header</span></span>|<span data-ttu-id="eb9e7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="eb9e7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="eb9e7-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="eb9e7-123">Authorization</span></span>|<span data-ttu-id="eb9e7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="eb9e7-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="eb9e7-125">Accept</span></span>|<span data-ttu-id="eb9e7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="eb9e7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="eb9e7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9e7-127">Request body</span></span>
<span data-ttu-id="eb9e7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto detectedApp.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-128">In the request body, supply a JSON representation for the detectedApp object.</span></span>

<span data-ttu-id="eb9e7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto detectedApp.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-129">The following table shows the properties that are required when you create the detectedApp.</span></span>

|<span data-ttu-id="eb9e7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb9e7-130">Property</span></span>|<span data-ttu-id="eb9e7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb9e7-131">Type</span></span>|<span data-ttu-id="eb9e7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb9e7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="eb9e7-133">id</span><span class="sxs-lookup"><span data-stu-id="eb9e7-133">id</span></span>|<span data-ttu-id="eb9e7-134">String</span><span class="sxs-lookup"><span data-stu-id="eb9e7-134">String</span></span>|<span data-ttu-id="eb9e7-135">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-135">The unique Identifier for the detected application.</span></span> <span data-ttu-id="eb9e7-136">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-136">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="eb9e7-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-137">Read-only.</span></span>|
|<span data-ttu-id="eb9e7-138">displayName</span><span class="sxs-lookup"><span data-stu-id="eb9e7-138">displayName</span></span>|<span data-ttu-id="eb9e7-139">String</span><span class="sxs-lookup"><span data-stu-id="eb9e7-139">String</span></span>|<span data-ttu-id="eb9e7-140">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-140">Name of the discovered application.</span></span> <span data-ttu-id="eb9e7-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9e7-141">Read-only</span></span>|
|<span data-ttu-id="eb9e7-142">version</span><span class="sxs-lookup"><span data-stu-id="eb9e7-142">version</span></span>|<span data-ttu-id="eb9e7-143">String</span><span class="sxs-lookup"><span data-stu-id="eb9e7-143">String</span></span>|<span data-ttu-id="eb9e7-144">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-144">Version of the discovered application.</span></span> <span data-ttu-id="eb9e7-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9e7-145">Read-only</span></span>|
|<span data-ttu-id="eb9e7-146">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="eb9e7-146">sizeInByte</span></span>|<span data-ttu-id="eb9e7-147">Int64</span><span class="sxs-lookup"><span data-stu-id="eb9e7-147">Int64</span></span>|<span data-ttu-id="eb9e7-148">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-148">Discovered application size in bytes.</span></span> <span data-ttu-id="eb9e7-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="eb9e7-149">Read-only</span></span>|
|<span data-ttu-id="eb9e7-150">deviceCount</span><span class="sxs-lookup"><span data-stu-id="eb9e7-150">deviceCount</span></span>|<span data-ttu-id="eb9e7-151">Int32</span><span class="sxs-lookup"><span data-stu-id="eb9e7-151">Int32</span></span>|<span data-ttu-id="eb9e7-152">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-152">The number of devices that have installed this application</span></span>|



## <a name="response"></a><span data-ttu-id="eb9e7-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb9e7-153">Response</span></span>
<span data-ttu-id="eb9e7-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [detectedApp](../resources/intune-devices-detectedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-154">If successful, this method returns a `201 Created` response code and a [detectedApp](../resources/intune-devices-detectedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eb9e7-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb9e7-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="eb9e7-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eb9e7-156">Request</span></span>
<span data-ttu-id="eb9e7-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-157">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/detectedApps
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

### <a name="response"></a><span data-ttu-id="eb9e7-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eb9e7-158">Response</span></span>
<span data-ttu-id="eb9e7-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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




