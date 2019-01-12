---
title: Actualizar iosMobileAppConfiguration
description: Actualiza las propiedades de un objeto iosMobileAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 298ca5b76b82f43daee84f7d2a36cbb0e12b058d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942125"
---
# <a name="update-iosmobileappconfiguration"></a><span data-ttu-id="ea254-103">Actualizar iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea254-103">Update iosMobileAppConfiguration</span></span>

> <span data-ttu-id="ea254-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea254-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea254-105">Actualiza las propiedades de un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea254-105">Update the properties of a [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea254-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea254-106">Prerequisites</span></span>
<span data-ttu-id="ea254-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ea254-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ea254-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea254-109">Permission type</span></span>|<span data-ttu-id="ea254-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea254-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea254-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea254-111">Delegated (work or school account)</span></span>|<span data-ttu-id="ea254-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea254-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="ea254-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea254-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea254-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea254-114">Not supported.</span></span>|
|<span data-ttu-id="ea254-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea254-115">Application</span></span>|<span data-ttu-id="ea254-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea254-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea254-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea254-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ea254-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea254-118">Request headers</span></span>
|<span data-ttu-id="ea254-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea254-119">Header</span></span>|<span data-ttu-id="ea254-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ea254-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea254-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="ea254-121">Authorization</span></span>|<span data-ttu-id="ea254-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea254-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea254-123">Accept</span><span class="sxs-lookup"><span data-stu-id="ea254-123">Accept</span></span>|<span data-ttu-id="ea254-124">application/json</span><span class="sxs-lookup"><span data-stu-id="ea254-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea254-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea254-125">Request body</span></span>
<span data-ttu-id="ea254-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea254-126">In the request body, supply a JSON representation for the [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>

<span data-ttu-id="ea254-127">En la tabla siguiente se muestran las propiedades necesarias para crear [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea254-127">The following table shows the properties that are required when you create the [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span></span>

|<span data-ttu-id="ea254-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea254-128">Property</span></span>|<span data-ttu-id="ea254-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea254-129">Type</span></span>|<span data-ttu-id="ea254-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea254-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea254-131">id</span><span class="sxs-lookup"><span data-stu-id="ea254-131">id</span></span>|<span data-ttu-id="ea254-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea254-132">String</span></span>|<span data-ttu-id="ea254-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea254-133">Key of the entity.</span></span> <span data-ttu-id="ea254-134">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-134">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-135">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="ea254-135">targetedMobileApps</span></span>|<span data-ttu-id="ea254-136">Colección string</span><span class="sxs-lookup"><span data-stu-id="ea254-136">String collection</span></span>|<span data-ttu-id="ea254-137">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="ea254-137">the associated app.</span></span> <span data-ttu-id="ea254-138">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-138">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ea254-139">createdDateTime</span></span>|<span data-ttu-id="ea254-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea254-140">DateTimeOffset</span></span>|<span data-ttu-id="ea254-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ea254-141">DateTime the object was created.</span></span> <span data-ttu-id="ea254-142">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-142">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-143">descripción</span><span class="sxs-lookup"><span data-stu-id="ea254-143">description</span></span>|<span data-ttu-id="ea254-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea254-144">String</span></span>|<span data-ttu-id="ea254-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea254-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ea254-146">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-146">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-147">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea254-147">lastModifiedDateTime</span></span>|<span data-ttu-id="ea254-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea254-148">DateTimeOffset</span></span>|<span data-ttu-id="ea254-149">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ea254-149">DateTime the object was last modified.</span></span> <span data-ttu-id="ea254-150">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-150">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-151">displayName</span><span class="sxs-lookup"><span data-stu-id="ea254-151">displayName</span></span>|<span data-ttu-id="ea254-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea254-152">String</span></span>|<span data-ttu-id="ea254-153">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea254-153">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ea254-154">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-154">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-155">versión</span><span class="sxs-lookup"><span data-stu-id="ea254-155">version</span></span>|<span data-ttu-id="ea254-156">Int32</span><span class="sxs-lookup"><span data-stu-id="ea254-156">Int32</span></span>|<span data-ttu-id="ea254-157">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea254-157">Version of the device configuration.</span></span> <span data-ttu-id="ea254-158">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-158">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="ea254-159">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="ea254-159">encodedSettingXml</span></span>|<span data-ttu-id="ea254-160">Binario</span><span class="sxs-lookup"><span data-stu-id="ea254-160">Binary</span></span>|<span data-ttu-id="ea254-161">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="ea254-161">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="ea254-162">configuración</span><span class="sxs-lookup"><span data-stu-id="ea254-162">settings</span></span>|<span data-ttu-id="ea254-163">Colección [appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="ea254-163">[appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="ea254-164">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ea254-164">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="ea254-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea254-165">Response</span></span>
<span data-ttu-id="ea254-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea254-166">If successful, this method returns a `200 OK` response code and an updated [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea254-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea254-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea254-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea254-168">Request</span></span>
<span data-ttu-id="ea254-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea254-169">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
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

### <a name="response"></a><span data-ttu-id="ea254-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea254-170">Response</span></span>
<span data-ttu-id="ea254-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea254-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



