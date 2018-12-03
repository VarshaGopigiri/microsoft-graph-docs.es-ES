---
title: Actualizar iosCustomConfiguration
description: Actualice las propiedades de un objeto iosCustomConfiguration.
ms.openlocfilehash: 6151c93e83bd35db70d6c5428d55bde92e8027de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030675"
---
# <a name="update-ioscustomconfiguration"></a><span data-ttu-id="b4c91-103">Actualizar iosCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4c91-103">Update iosCustomConfiguration</span></span>

> <span data-ttu-id="b4c91-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4c91-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4c91-105">Actualice las propiedades de un objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b4c91-105">Update the properties of a [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b4c91-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b4c91-106">Prerequisites</span></span>
<span data-ttu-id="b4c91-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4c91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4c91-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4c91-109">Permission type</span></span>|<span data-ttu-id="b4c91-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4c91-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b4c91-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4c91-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b4c91-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4c91-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b4c91-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4c91-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b4c91-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4c91-114">Not supported.</span></span>|
|<span data-ttu-id="b4c91-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4c91-115">Application</span></span>|<span data-ttu-id="b4c91-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4c91-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b4c91-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4c91-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="b4c91-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c91-118">Request headers</span></span>
|<span data-ttu-id="b4c91-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4c91-119">Header</span></span>|<span data-ttu-id="b4c91-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b4c91-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b4c91-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4c91-121">Authorization</span></span>|<span data-ttu-id="b4c91-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b4c91-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b4c91-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b4c91-123">Accept</span></span>|<span data-ttu-id="b4c91-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b4c91-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b4c91-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c91-125">Request body</span></span>
<span data-ttu-id="b4c91-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b4c91-126">In the request body, supply a JSON representation for the [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) object.</span></span>

<span data-ttu-id="b4c91-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b4c91-127">The following table shows the properties that are required when you create the [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md).</span></span>

|<span data-ttu-id="b4c91-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4c91-128">Property</span></span>|<span data-ttu-id="b4c91-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4c91-129">Type</span></span>|<span data-ttu-id="b4c91-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4c91-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4c91-131">id</span><span class="sxs-lookup"><span data-stu-id="b4c91-131">id</span></span>|<span data-ttu-id="b4c91-132">String</span><span class="sxs-lookup"><span data-stu-id="b4c91-132">String</span></span>|<span data-ttu-id="b4c91-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b4c91-133">Key of the entity.</span></span> <span data-ttu-id="b4c91-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b4c91-135">lastModifiedDateTime</span></span>|<span data-ttu-id="b4c91-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4c91-136">DateTimeOffset</span></span>|<span data-ttu-id="b4c91-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b4c91-137">DateTime the object was last modified.</span></span> <span data-ttu-id="b4c91-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b4c91-139">createdDateTime</span></span>|<span data-ttu-id="b4c91-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b4c91-140">DateTimeOffset</span></span>|<span data-ttu-id="b4c91-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b4c91-141">DateTime the object was created.</span></span> <span data-ttu-id="b4c91-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-143">descripción</span><span class="sxs-lookup"><span data-stu-id="b4c91-143">description</span></span>|<span data-ttu-id="b4c91-144">String</span><span class="sxs-lookup"><span data-stu-id="b4c91-144">String</span></span>|<span data-ttu-id="b4c91-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4c91-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b4c91-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-147">displayName</span><span class="sxs-lookup"><span data-stu-id="b4c91-147">displayName</span></span>|<span data-ttu-id="b4c91-148">String</span><span class="sxs-lookup"><span data-stu-id="b4c91-148">String</span></span>|<span data-ttu-id="b4c91-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4c91-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b4c91-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-151">version</span><span class="sxs-lookup"><span data-stu-id="b4c91-151">version</span></span>|<span data-ttu-id="b4c91-152">Int32</span><span class="sxs-lookup"><span data-stu-id="b4c91-152">Int32</span></span>|<span data-ttu-id="b4c91-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4c91-153">Version of the device configuration.</span></span> <span data-ttu-id="b4c91-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b4c91-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b4c91-155">payloadName</span><span class="sxs-lookup"><span data-stu-id="b4c91-155">payloadName</span></span>|<span data-ttu-id="b4c91-156">String</span><span class="sxs-lookup"><span data-stu-id="b4c91-156">String</span></span>|<span data-ttu-id="b4c91-157">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="b4c91-157">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="b4c91-158">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="b4c91-158">payloadFileName</span></span>|<span data-ttu-id="b4c91-159">String</span><span class="sxs-lookup"><span data-stu-id="b4c91-159">String</span></span>|<span data-ttu-id="b4c91-160">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="b4c91-160">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="b4c91-161">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="b4c91-161">\*.xml).</span></span>|
|<span data-ttu-id="b4c91-162">carga útil</span><span class="sxs-lookup"><span data-stu-id="b4c91-162">payload</span></span>|<span data-ttu-id="b4c91-163">Binario</span><span class="sxs-lookup"><span data-stu-id="b4c91-163">Binary</span></span>|<span data-ttu-id="b4c91-164">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="b4c91-164">Payload.</span></span> <span data-ttu-id="b4c91-165">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="b4c91-165">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="b4c91-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4c91-166">Response</span></span>
<span data-ttu-id="b4c91-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4c91-167">If successful, this method returns a `200 OK` response code and an updated [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4c91-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4c91-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="b4c91-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c91-169">Request</span></span>
<span data-ttu-id="b4c91-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4c91-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 279

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a><span data-ttu-id="b4c91-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4c91-171">Response</span></span>
<span data-ttu-id="b4c91-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4c91-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 451

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "id": "f34428e3-28e3-f344-e328-44f3e32844f3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```


