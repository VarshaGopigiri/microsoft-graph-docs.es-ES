---
title: Crear deviceCategory
description: Cree un objeto deviceCategory.
ms.openlocfilehash: 43a731716150a7cc9515a6497840cc47271e88c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031083"
---
# <a name="create-devicecategory"></a><span data-ttu-id="203dc-103">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="203dc-103">Create deviceCategory</span></span>

> <span data-ttu-id="203dc-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="203dc-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="203dc-105">Cree un objeto [deviceCategory](../resources/intune-shared-devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="203dc-105">Create a new [deviceCategory](../resources/intune-shared-devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="203dc-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="203dc-106">Prerequisites</span></span>
<span data-ttu-id="203dc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="203dc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="203dc-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="203dc-109">Permission type</span></span>|<span data-ttu-id="203dc-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="203dc-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="203dc-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="203dc-111">Delegated (work or school account)</span></span>||
| <span data-ttu-id="203dc-112">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="203dc-112">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="203dc-113">DeviceManagementManaged Devices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="203dc-113">DeviceManagementManaged Devices.ReadWrite.All</span></span>|
|<span data-ttu-id="203dc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="203dc-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="203dc-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="203dc-115">Not supported.</span></span>|
|<span data-ttu-id="203dc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="203dc-116">Application</span></span>|<span data-ttu-id="203dc-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="203dc-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="203dc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="203dc-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="203dc-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="203dc-119">Request headers</span></span>
|<span data-ttu-id="203dc-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="203dc-120">Header</span></span>|<span data-ttu-id="203dc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="203dc-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="203dc-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="203dc-122">Authorization</span></span>|<span data-ttu-id="203dc-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="203dc-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="203dc-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="203dc-124">Accept</span></span>|<span data-ttu-id="203dc-125">application/json</span><span class="sxs-lookup"><span data-stu-id="203dc-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="203dc-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="203dc-126">Request body</span></span>
<span data-ttu-id="203dc-127">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="203dc-127">In the request body, supply a JSON representation for the deviceCategory object.</span></span>

<span data-ttu-id="203dc-128">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="203dc-128">The following table shows the properties that are required when you create the deviceCategory.</span></span>

|<span data-ttu-id="203dc-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="203dc-129">Property</span></span>|<span data-ttu-id="203dc-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="203dc-130">Type</span></span>|<span data-ttu-id="203dc-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="203dc-131">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="203dc-132">id</span><span class="sxs-lookup"><span data-stu-id="203dc-132">id</span></span>|<span data-ttu-id="203dc-133">String</span><span class="sxs-lookup"><span data-stu-id="203dc-133">String</span></span>|<span data-ttu-id="203dc-134">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="203dc-134">Unique identifier for the device category.</span></span> <span data-ttu-id="203dc-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="203dc-135">Read-only.</span></span>|
|<span data-ttu-id="203dc-136">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="203dc-136">**Onboarding**</span></span>|
|<span data-ttu-id="203dc-137">displayName</span><span class="sxs-lookup"><span data-stu-id="203dc-137">displayName</span></span>|<span data-ttu-id="203dc-138">String</span><span class="sxs-lookup"><span data-stu-id="203dc-138">String</span></span>|<span data-ttu-id="203dc-139">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="203dc-139">Display name for the device category.</span></span>|
|<span data-ttu-id="203dc-140">descripción</span><span class="sxs-lookup"><span data-stu-id="203dc-140">description</span></span>|<span data-ttu-id="203dc-141">String</span><span class="sxs-lookup"><span data-stu-id="203dc-141">String</span></span>|<span data-ttu-id="203dc-142">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="203dc-142">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="203dc-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="203dc-143">Response</span></span>
<span data-ttu-id="203dc-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCategory](../resources/intune-shared-devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="203dc-144">If successful, this method returns a `201 Created` response code and a [deviceCategory](../resources/intune-shared-devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="203dc-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="203dc-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="203dc-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="203dc-146">Request</span></span>
<span data-ttu-id="203dc-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="203dc-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories
Content-type: application/json
Content-length: 135

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="203dc-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="203dc-148">Response</span></span>
<span data-ttu-id="203dc-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="203dc-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 184

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8",
  "displayName": "Display Name value",
  "description": "Description value"
}
```



