---
title: Actualizar macOSDeviceFeaturesConfiguration
description: Actualice las propiedades de un objeto macOSDeviceFeaturesConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0539e19de3cf7189e4bc35fea78f85bd52eaa80e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870248"
---
# <a name="update-macosdevicefeaturesconfiguration"></a><span data-ttu-id="efdf0-103">Actualizar macOSDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="efdf0-103">Update macOSDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="efdf0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="efdf0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="efdf0-105">Actualice las propiedades de un objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="efdf0-105">Update the properties of a [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="efdf0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="efdf0-106">Prerequisites</span></span>
<span data-ttu-id="efdf0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="efdf0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="efdf0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="efdf0-109">Permission type</span></span>|<span data-ttu-id="efdf0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="efdf0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="efdf0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="efdf0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="efdf0-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="efdf0-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="efdf0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="efdf0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="efdf0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="efdf0-114">Not supported.</span></span>|
|<span data-ttu-id="efdf0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="efdf0-115">Application</span></span>|<span data-ttu-id="efdf0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="efdf0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="efdf0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="efdf0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="efdf0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="efdf0-118">Request headers</span></span>
|<span data-ttu-id="efdf0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efdf0-119">Header</span></span>|<span data-ttu-id="efdf0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="efdf0-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="efdf0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="efdf0-121">Authorization</span></span>|<span data-ttu-id="efdf0-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="efdf0-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="efdf0-123">Accept</span><span class="sxs-lookup"><span data-stu-id="efdf0-123">Accept</span></span>|<span data-ttu-id="efdf0-124">application/json</span><span class="sxs-lookup"><span data-stu-id="efdf0-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="efdf0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="efdf0-125">Request body</span></span>
<span data-ttu-id="efdf0-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="efdf0-126">In the request body, supply a JSON representation for the [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="efdf0-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="efdf0-127">The following table shows the properties that are required when you create the [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md).</span></span>

|<span data-ttu-id="efdf0-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="efdf0-128">Property</span></span>|<span data-ttu-id="efdf0-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="efdf0-129">Type</span></span>|<span data-ttu-id="efdf0-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="efdf0-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="efdf0-131">id</span><span class="sxs-lookup"><span data-stu-id="efdf0-131">id</span></span>|<span data-ttu-id="efdf0-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="efdf0-132">String</span></span>|<span data-ttu-id="efdf0-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="efdf0-133">Key of the entity.</span></span> <span data-ttu-id="efdf0-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="efdf0-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="efdf0-135">lastModifiedDateTime</span></span>|<span data-ttu-id="efdf0-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="efdf0-136">DateTimeOffset</span></span>|<span data-ttu-id="efdf0-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="efdf0-137">DateTime the object was last modified.</span></span> <span data-ttu-id="efdf0-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="efdf0-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="efdf0-139">createdDateTime</span></span>|<span data-ttu-id="efdf0-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="efdf0-140">DateTimeOffset</span></span>|<span data-ttu-id="efdf0-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="efdf0-141">DateTime the object was created.</span></span> <span data-ttu-id="efdf0-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="efdf0-143">descripción</span><span class="sxs-lookup"><span data-stu-id="efdf0-143">description</span></span>|<span data-ttu-id="efdf0-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="efdf0-144">String</span></span>|<span data-ttu-id="efdf0-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efdf0-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="efdf0-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="efdf0-147">displayName</span><span class="sxs-lookup"><span data-stu-id="efdf0-147">displayName</span></span>|<span data-ttu-id="efdf0-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="efdf0-148">String</span></span>|<span data-ttu-id="efdf0-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efdf0-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="efdf0-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="efdf0-151">version</span><span class="sxs-lookup"><span data-stu-id="efdf0-151">version</span></span>|<span data-ttu-id="efdf0-152">Int32</span><span class="sxs-lookup"><span data-stu-id="efdf0-152">Int32</span></span>|<span data-ttu-id="efdf0-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="efdf0-153">Version of the device configuration.</span></span> <span data-ttu-id="efdf0-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="efdf0-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="efdf0-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="efdf0-155">Response</span></span>
<span data-ttu-id="efdf0-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="efdf0-156">If successful, this method returns a `200 OK` response code and an updated [macOSDeviceFeaturesConfiguration](../resources/intune-deviceconfig-macosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="efdf0-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efdf0-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="efdf0-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="efdf0-158">Request</span></span>
<span data-ttu-id="efdf0-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="efdf0-159">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="efdf0-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="efdf0-160">Response</span></span>
<span data-ttu-id="efdf0-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="efdf0-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



