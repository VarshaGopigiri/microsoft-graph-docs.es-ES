---
title: Actualizar macOSDeviceFeaturesConfiguration
description: Actualice las propiedades de un objeto macOSDeviceFeaturesConfiguration.
author: tfitzmac
ms.openlocfilehash: aecefa3e348613fa2aa0f9974f2aafbce56c8051
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348457"
---
# <a name="update-macosdevicefeaturesconfiguration"></a><span data-ttu-id="d2fd6-103">Actualizar macOSDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2fd6-103">Update macOSDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="d2fd6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2fd6-105">Actualice las propiedades de un objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d2fd6-105">Update the properties of a [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d2fd6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d2fd6-106">Prerequisites</span></span>
<span data-ttu-id="d2fd6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d2fd6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d2fd6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2fd6-109">Permission type</span></span>|<span data-ttu-id="d2fd6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d2fd6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="d2fd6-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d2fd6-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d2fd6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d2fd6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-114">Not supported.</span></span>|
|<span data-ttu-id="d2fd6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2fd6-115">Application</span></span>|<span data-ttu-id="d2fd6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d2fd6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2fd6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="d2fd6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2fd6-118">Request headers</span></span>
|<span data-ttu-id="d2fd6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2fd6-119">Header</span></span>|<span data-ttu-id="d2fd6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d2fd6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d2fd6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="d2fd6-121">Authorization</span></span>|<span data-ttu-id="d2fd6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d2fd6-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d2fd6-123">Accept</span></span>|<span data-ttu-id="d2fd6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="d2fd6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d2fd6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d2fd6-125">Request body</span></span>
<span data-ttu-id="d2fd6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d2fd6-126">In the request body, supply a JSON representation for the [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="d2fd6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d2fd6-127">The following table shows the properties that are required when you create the [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span></span>

|<span data-ttu-id="d2fd6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2fd6-128">Property</span></span>|<span data-ttu-id="d2fd6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2fd6-129">Type</span></span>|<span data-ttu-id="d2fd6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2fd6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2fd6-131">id</span><span class="sxs-lookup"><span data-stu-id="d2fd6-131">id</span></span>|<span data-ttu-id="d2fd6-132">String</span><span class="sxs-lookup"><span data-stu-id="d2fd6-132">String</span></span>|<span data-ttu-id="d2fd6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-133">Key of the entity.</span></span> <span data-ttu-id="d2fd6-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2fd6-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d2fd6-135">lastModifiedDateTime</span></span>|<span data-ttu-id="d2fd6-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2fd6-136">DateTimeOffset</span></span>|<span data-ttu-id="d2fd6-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-137">DateTime the object was last modified.</span></span> <span data-ttu-id="d2fd6-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2fd6-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d2fd6-139">createdDateTime</span></span>|<span data-ttu-id="d2fd6-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d2fd6-140">DateTimeOffset</span></span>|<span data-ttu-id="d2fd6-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-141">DateTime the object was created.</span></span> <span data-ttu-id="d2fd6-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2fd6-143">descripción</span><span class="sxs-lookup"><span data-stu-id="d2fd6-143">description</span></span>|<span data-ttu-id="d2fd6-144">String</span><span class="sxs-lookup"><span data-stu-id="d2fd6-144">String</span></span>|<span data-ttu-id="d2fd6-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d2fd6-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2fd6-147">displayName</span><span class="sxs-lookup"><span data-stu-id="d2fd6-147">displayName</span></span>|<span data-ttu-id="d2fd6-148">String</span><span class="sxs-lookup"><span data-stu-id="d2fd6-148">String</span></span>|<span data-ttu-id="d2fd6-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d2fd6-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d2fd6-151">version</span><span class="sxs-lookup"><span data-stu-id="d2fd6-151">version</span></span>|<span data-ttu-id="d2fd6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="d2fd6-152">Int32</span></span>|<span data-ttu-id="d2fd6-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-153">Version of the device configuration.</span></span> <span data-ttu-id="d2fd6-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d2fd6-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="d2fd6-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2fd6-155">Response</span></span>
<span data-ttu-id="d2fd6-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-156">If successful, this method returns a `200 OK` response code and an updated [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2fd6-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2fd6-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="d2fd6-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2fd6-158">Request</span></span>
<span data-ttu-id="d2fd6-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 170

{
  "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="d2fd6-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2fd6-160">Response</span></span>
<span data-ttu-id="d2fd6-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d2fd6-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 342

{
  "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
  "id": "49fa957d-957d-49fa-7d95-fa497d95fa49",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```



