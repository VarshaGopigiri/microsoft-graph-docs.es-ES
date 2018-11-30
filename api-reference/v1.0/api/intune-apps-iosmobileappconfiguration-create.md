---
title: Crear iosMobileAppConfiguration
description: Crear un nuevo objeto iosMobileAppConfiguration.
ms.openlocfilehash: 24bd4b7a606ce95a146d0ce5273ba268766bb6c2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029529"
---
# <a name="create-iosmobileappconfiguration"></a><span data-ttu-id="97d1e-103">Crear iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="97d1e-103">Create iosMobileAppConfiguration</span></span>

> <span data-ttu-id="97d1e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="97d1e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="97d1e-105">Crear un nuevo objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="97d1e-105">Create a new [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="97d1e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97d1e-106">Prerequisites</span></span>
<span data-ttu-id="97d1e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="97d1e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="97d1e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="97d1e-109">Permission type</span></span>|<span data-ttu-id="97d1e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="97d1e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="97d1e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="97d1e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="97d1e-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="97d1e-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="97d1e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="97d1e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="97d1e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97d1e-114">Not supported.</span></span>|
|<span data-ttu-id="97d1e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="97d1e-115">Application</span></span>|<span data-ttu-id="97d1e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="97d1e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="97d1e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="97d1e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="97d1e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="97d1e-118">Request headers</span></span>
|<span data-ttu-id="97d1e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97d1e-119">Header</span></span>|<span data-ttu-id="97d1e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="97d1e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="97d1e-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="97d1e-121">Authorization</span></span>|<span data-ttu-id="97d1e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="97d1e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="97d1e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="97d1e-123">Accept</span></span>|<span data-ttu-id="97d1e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="97d1e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="97d1e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="97d1e-125">Request body</span></span>
<span data-ttu-id="97d1e-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="97d1e-126">In the request body, supply a JSON representation for the iosMobileAppConfiguration object.</span></span>

<span data-ttu-id="97d1e-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="97d1e-127">The following table shows the properties that are required when you create the iosMobileAppConfiguration.</span></span>

|<span data-ttu-id="97d1e-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="97d1e-128">Property</span></span>|<span data-ttu-id="97d1e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="97d1e-129">Type</span></span>|<span data-ttu-id="97d1e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="97d1e-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="97d1e-131">id</span><span class="sxs-lookup"><span data-stu-id="97d1e-131">id</span></span>|<span data-ttu-id="97d1e-132">String</span><span class="sxs-lookup"><span data-stu-id="97d1e-132">String</span></span>|<span data-ttu-id="97d1e-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="97d1e-133">Key of the entity.</span></span> <span data-ttu-id="97d1e-134">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-134">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-135">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="97d1e-135">targetedMobileApps</span></span>|<span data-ttu-id="97d1e-136">Colección string</span><span class="sxs-lookup"><span data-stu-id="97d1e-136">String collection</span></span>|<span data-ttu-id="97d1e-137">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="97d1e-137">the associated app.</span></span> <span data-ttu-id="97d1e-138">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-138">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="97d1e-139">createdDateTime</span></span>|<span data-ttu-id="97d1e-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97d1e-140">DateTimeOffset</span></span>|<span data-ttu-id="97d1e-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="97d1e-141">DateTime the object was created.</span></span> <span data-ttu-id="97d1e-142">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-142">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-143">descripción</span><span class="sxs-lookup"><span data-stu-id="97d1e-143">description</span></span>|<span data-ttu-id="97d1e-144">String</span><span class="sxs-lookup"><span data-stu-id="97d1e-144">String</span></span>|<span data-ttu-id="97d1e-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97d1e-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="97d1e-146">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-146">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-147">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="97d1e-147">lastModifiedDateTime</span></span>|<span data-ttu-id="97d1e-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="97d1e-148">DateTimeOffset</span></span>|<span data-ttu-id="97d1e-149">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="97d1e-149">DateTime the object was last modified.</span></span> <span data-ttu-id="97d1e-150">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-150">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-151">displayName</span><span class="sxs-lookup"><span data-stu-id="97d1e-151">displayName</span></span>|<span data-ttu-id="97d1e-152">String</span><span class="sxs-lookup"><span data-stu-id="97d1e-152">String</span></span>|<span data-ttu-id="97d1e-153">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97d1e-153">Admin provided name of the device configuration.</span></span> <span data-ttu-id="97d1e-154">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-154">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-155">versión</span><span class="sxs-lookup"><span data-stu-id="97d1e-155">version</span></span>|<span data-ttu-id="97d1e-156">Int32</span><span class="sxs-lookup"><span data-stu-id="97d1e-156">Int32</span></span>|<span data-ttu-id="97d1e-157">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97d1e-157">Version of the device configuration.</span></span> <span data-ttu-id="97d1e-158">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-158">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="97d1e-159">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="97d1e-159">encodedSettingXml</span></span>|<span data-ttu-id="97d1e-160">Binario</span><span class="sxs-lookup"><span data-stu-id="97d1e-160">Binary</span></span>|<span data-ttu-id="97d1e-161">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="97d1e-161">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="97d1e-162">configuración</span><span class="sxs-lookup"><span data-stu-id="97d1e-162">settings</span></span>|<span data-ttu-id="97d1e-163">Colección [appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="97d1e-163">[appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="97d1e-164">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="97d1e-164">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="97d1e-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97d1e-165">Response</span></span>
<span data-ttu-id="97d1e-166">Si se ejecuta correctamente, este método devuelve un `201 Created` código de respuesta y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="97d1e-166">If successful, this method returns a `201 Created` response code and a [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="97d1e-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97d1e-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="97d1e-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="97d1e-168">Request</span></span>
<span data-ttu-id="97d1e-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97d1e-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations
Content-type: application/json
Content-length: 534

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "encodedSettingXml": "ZW5jb2RlZFNldHRpbmdYbWw=",
  "settings": [
    {
      "@odata.type": "microsoft.graph.appConfigurationSettingItem",
      "appConfigKey": "App Config Key value",
      "appConfigKeyType": "integerType",
      "appConfigKeyValue": "App Config Key Value value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="97d1e-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="97d1e-170">Response</span></span>
<span data-ttu-id="97d1e-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="97d1e-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 706

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "id": "b2c33191-3191-b2c3-9131-c3b29131c3b2",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "encodedSettingXml": "ZW5jb2RlZFNldHRpbmdYbWw=",
  "settings": [
    {
      "@odata.type": "microsoft.graph.appConfigurationSettingItem",
      "appConfigKey": "App Config Key value",
      "appConfigKeyType": "integerType",
      "appConfigKeyValue": "App Config Key Value value"
    }
  ]
}
```


