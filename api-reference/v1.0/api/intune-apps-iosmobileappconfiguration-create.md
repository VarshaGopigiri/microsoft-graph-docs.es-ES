---
title: Crear iosMobileAppConfiguration
description: Crear un nuevo objeto iosMobileAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: d85a55e8ea645b451f2248ab8d82836238b6c8e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822326"
---
# <a name="create-iosmobileappconfiguration"></a><span data-ttu-id="fc7e5-103">Crear iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc7e5-103">Create iosMobileAppConfiguration</span></span>

> <span data-ttu-id="fc7e5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc7e5-105">Crear un nuevo objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="fc7e5-105">Create a new [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fc7e5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fc7e5-106">Prerequisites</span></span>
<span data-ttu-id="fc7e5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fc7e5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fc7e5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc7e5-109">Permission type</span></span>|<span data-ttu-id="fc7e5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fc7e5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="fc7e5-112">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc7e5-112">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="fc7e5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fc7e5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-114">Not supported.</span></span>|
|<span data-ttu-id="fc7e5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc7e5-115">Application</span></span>|<span data-ttu-id="fc7e5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc7e5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc7e5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="fc7e5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc7e5-118">Request headers</span></span>
|<span data-ttu-id="fc7e5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc7e5-119">Header</span></span>|<span data-ttu-id="fc7e5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fc7e5-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fc7e5-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="fc7e5-121">Authorization</span></span>|<span data-ttu-id="fc7e5-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fc7e5-123">Accept</span><span class="sxs-lookup"><span data-stu-id="fc7e5-123">Accept</span></span>|<span data-ttu-id="fc7e5-124">application/json</span><span class="sxs-lookup"><span data-stu-id="fc7e5-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc7e5-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc7e5-125">Request body</span></span>
<span data-ttu-id="fc7e5-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-126">In the request body, supply a JSON representation for the iosMobileAppConfiguration object.</span></span>

<span data-ttu-id="fc7e5-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-127">The following table shows the properties that are required when you create the iosMobileAppConfiguration.</span></span>

|<span data-ttu-id="fc7e5-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc7e5-128">Property</span></span>|<span data-ttu-id="fc7e5-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc7e5-129">Type</span></span>|<span data-ttu-id="fc7e5-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc7e5-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc7e5-131">id</span><span class="sxs-lookup"><span data-stu-id="fc7e5-131">id</span></span>|<span data-ttu-id="fc7e5-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc7e5-132">String</span></span>|<span data-ttu-id="fc7e5-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-133">Key of the entity.</span></span> <span data-ttu-id="fc7e5-134">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-134">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-135">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="fc7e5-135">targetedMobileApps</span></span>|<span data-ttu-id="fc7e5-136">Colección string</span><span class="sxs-lookup"><span data-stu-id="fc7e5-136">String collection</span></span>|<span data-ttu-id="fc7e5-137">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-137">the associated app.</span></span> <span data-ttu-id="fc7e5-138">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-138">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="fc7e5-139">createdDateTime</span></span>|<span data-ttu-id="fc7e5-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc7e5-140">DateTimeOffset</span></span>|<span data-ttu-id="fc7e5-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-141">DateTime the object was created.</span></span> <span data-ttu-id="fc7e5-142">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-142">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-143">descripción</span><span class="sxs-lookup"><span data-stu-id="fc7e5-143">description</span></span>|<span data-ttu-id="fc7e5-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc7e5-144">String</span></span>|<span data-ttu-id="fc7e5-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="fc7e5-146">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-146">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-147">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="fc7e5-147">lastModifiedDateTime</span></span>|<span data-ttu-id="fc7e5-148">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc7e5-148">DateTimeOffset</span></span>|<span data-ttu-id="fc7e5-149">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-149">DateTime the object was last modified.</span></span> <span data-ttu-id="fc7e5-150">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-150">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-151">displayName</span><span class="sxs-lookup"><span data-stu-id="fc7e5-151">displayName</span></span>|<span data-ttu-id="fc7e5-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="fc7e5-152">String</span></span>|<span data-ttu-id="fc7e5-153">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-153">Admin provided name of the device configuration.</span></span> <span data-ttu-id="fc7e5-154">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-154">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-155">versión</span><span class="sxs-lookup"><span data-stu-id="fc7e5-155">version</span></span>|<span data-ttu-id="fc7e5-156">Int32</span><span class="sxs-lookup"><span data-stu-id="fc7e5-156">Int32</span></span>|<span data-ttu-id="fc7e5-157">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-157">Version of the device configuration.</span></span> <span data-ttu-id="fc7e5-158">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-158">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="fc7e5-159">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="fc7e5-159">encodedSettingXml</span></span>|<span data-ttu-id="fc7e5-160">Binario</span><span class="sxs-lookup"><span data-stu-id="fc7e5-160">Binary</span></span>|<span data-ttu-id="fc7e5-161">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-161">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="fc7e5-162">configuración</span><span class="sxs-lookup"><span data-stu-id="fc7e5-162">settings</span></span>|<span data-ttu-id="fc7e5-163">Colección [appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="fc7e5-163">[appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="fc7e5-164">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-164">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="fc7e5-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc7e5-165">Response</span></span>
<span data-ttu-id="fc7e5-166">Si se ejecuta correctamente, este método devuelve un `201 Created` código de respuesta y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-166">If successful, this method returns a `201 Created` response code and a [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc7e5-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc7e5-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="fc7e5-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc7e5-168">Request</span></span>
<span data-ttu-id="fc7e5-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-169">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="fc7e5-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc7e5-170">Response</span></span>
<span data-ttu-id="fc7e5-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc7e5-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



