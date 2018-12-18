---
title: Crear detectedApp
description: Cree un objeto detectedApp.
author: tfitzmac
ms.openlocfilehash: 60c47746e49429e37a5a40a5c86714d209ff6c3d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355485"
---
# <a name="create-detectedapp"></a><span data-ttu-id="3647c-103">Crear detectedApp</span><span class="sxs-lookup"><span data-stu-id="3647c-103">Create detectedApp</span></span>

> <span data-ttu-id="3647c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3647c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3647c-105">Cree un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="3647c-105">Create a new [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3647c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3647c-106">Prerequisites</span></span>
<span data-ttu-id="3647c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3647c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3647c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3647c-109">Permission type</span></span>|<span data-ttu-id="3647c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3647c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3647c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3647c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="3647c-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3647c-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="3647c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3647c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3647c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3647c-114">Not supported.</span></span>|
|<span data-ttu-id="3647c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3647c-115">Application</span></span>|<span data-ttu-id="3647c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3647c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3647c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3647c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/detectedApps
```

## <a name="request-headers"></a><span data-ttu-id="3647c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3647c-118">Request headers</span></span>
|<span data-ttu-id="3647c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3647c-119">Header</span></span>|<span data-ttu-id="3647c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3647c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3647c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="3647c-121">Authorization</span></span>|<span data-ttu-id="3647c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3647c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3647c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="3647c-123">Accept</span></span>|<span data-ttu-id="3647c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3647c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3647c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3647c-125">Request body</span></span>
<span data-ttu-id="3647c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto detectedApp.</span><span class="sxs-lookup"><span data-stu-id="3647c-126">In the request body, supply a JSON representation for the detectedApp object.</span></span>

<span data-ttu-id="3647c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto detectedApp.</span><span class="sxs-lookup"><span data-stu-id="3647c-127">The following table shows the properties that are required when you create the detectedApp.</span></span>

|<span data-ttu-id="3647c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3647c-128">Property</span></span>|<span data-ttu-id="3647c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="3647c-129">Type</span></span>|<span data-ttu-id="3647c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="3647c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3647c-131">id</span><span class="sxs-lookup"><span data-stu-id="3647c-131">id</span></span>|<span data-ttu-id="3647c-132">String</span><span class="sxs-lookup"><span data-stu-id="3647c-132">String</span></span>|<span data-ttu-id="3647c-133">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="3647c-133">The unique Identifier for the detected application.</span></span> <span data-ttu-id="3647c-134">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3647c-134">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="3647c-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3647c-135">Read-only.</span></span>|
|<span data-ttu-id="3647c-136">displayName</span><span class="sxs-lookup"><span data-stu-id="3647c-136">displayName</span></span>|<span data-ttu-id="3647c-137">String</span><span class="sxs-lookup"><span data-stu-id="3647c-137">String</span></span>|<span data-ttu-id="3647c-138">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="3647c-138">Name of the discovered application.</span></span> <span data-ttu-id="3647c-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3647c-139">Read-only</span></span>|
|<span data-ttu-id="3647c-140">version</span><span class="sxs-lookup"><span data-stu-id="3647c-140">version</span></span>|<span data-ttu-id="3647c-141">String</span><span class="sxs-lookup"><span data-stu-id="3647c-141">String</span></span>|<span data-ttu-id="3647c-142">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="3647c-142">Version of the discovered application.</span></span> <span data-ttu-id="3647c-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3647c-143">Read-only</span></span>|
|<span data-ttu-id="3647c-144">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="3647c-144">sizeInByte</span></span>|<span data-ttu-id="3647c-145">Int64</span><span class="sxs-lookup"><span data-stu-id="3647c-145">Int64</span></span>|<span data-ttu-id="3647c-146">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="3647c-146">Discovered application size in bytes.</span></span> <span data-ttu-id="3647c-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="3647c-147">Read-only</span></span>|
|<span data-ttu-id="3647c-148">deviceCount</span><span class="sxs-lookup"><span data-stu-id="3647c-148">deviceCount</span></span>|<span data-ttu-id="3647c-149">Int32</span><span class="sxs-lookup"><span data-stu-id="3647c-149">Int32</span></span>|<span data-ttu-id="3647c-150">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="3647c-150">The number of devices that have installed this application</span></span>|



## <a name="response"></a><span data-ttu-id="3647c-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3647c-151">Response</span></span>
<span data-ttu-id="3647c-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [detectedApp](../resources/intune-devices-detectedapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3647c-152">If successful, this method returns a `201 Created` response code and a [detectedApp](../resources/intune-devices-detectedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3647c-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3647c-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="3647c-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3647c-154">Request</span></span>
<span data-ttu-id="3647c-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3647c-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/detectedApps
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

### <a name="response"></a><span data-ttu-id="3647c-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3647c-156">Response</span></span>
<span data-ttu-id="3647c-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3647c-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



