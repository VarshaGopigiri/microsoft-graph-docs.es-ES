---
title: Crear iosMobileAppConfiguration
description: Crear un nuevo objeto iosMobileAppConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: dd5c5aabb8e23e4e9d4adf781c59847f5edc10eb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27854365"
---
# <a name="create-iosmobileappconfiguration"></a><span data-ttu-id="a03e0-103">Crear iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="a03e0-103">Create iosMobileAppConfiguration</span></span>

> <span data-ttu-id="a03e0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a03e0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a03e0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a03e0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a03e0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a03e0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a03e0-107">Crear un nuevo objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="a03e0-107">Create a new [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a03e0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a03e0-108">Prerequisites</span></span>
<span data-ttu-id="a03e0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a03e0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a03e0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a03e0-111">Permission type</span></span>|<span data-ttu-id="a03e0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a03e0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a03e0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a03e0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a03e0-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a03e0-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a03e0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a03e0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a03e0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a03e0-116">Not supported.</span></span>|
|<span data-ttu-id="a03e0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a03e0-117">Application</span></span>|<span data-ttu-id="a03e0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a03e0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a03e0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a03e0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="a03e0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a03e0-120">Request headers</span></span>
|<span data-ttu-id="a03e0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a03e0-121">Header</span></span>|<span data-ttu-id="a03e0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a03e0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a03e0-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a03e0-123">Authorization</span></span>|<span data-ttu-id="a03e0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a03e0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a03e0-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a03e0-125">Accept</span></span>|<span data-ttu-id="a03e0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a03e0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a03e0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a03e0-127">Request body</span></span>
<span data-ttu-id="a03e0-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a03e0-128">In the request body, supply a JSON representation for the iosMobileAppConfiguration object.</span></span>

<span data-ttu-id="a03e0-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a03e0-129">The following table shows the properties that are required when you create the iosMobileAppConfiguration.</span></span>

|<span data-ttu-id="a03e0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a03e0-130">Property</span></span>|<span data-ttu-id="a03e0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a03e0-131">Type</span></span>|<span data-ttu-id="a03e0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a03e0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a03e0-133">id</span><span class="sxs-lookup"><span data-stu-id="a03e0-133">id</span></span>|<span data-ttu-id="a03e0-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a03e0-134">String</span></span>|<span data-ttu-id="a03e0-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a03e0-135">Key of the entity.</span></span> <span data-ttu-id="a03e0-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-137">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="a03e0-137">targetedMobileApps</span></span>|<span data-ttu-id="a03e0-138">Colección string</span><span class="sxs-lookup"><span data-stu-id="a03e0-138">String collection</span></span>|<span data-ttu-id="a03e0-139">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="a03e0-139">the associated app.</span></span> <span data-ttu-id="a03e0-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="a03e0-141">roleScopeTagIds</span></span>|<span data-ttu-id="a03e0-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="a03e0-142">String collection</span></span>|<span data-ttu-id="a03e0-143">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a03e0-143">List of Scope Tags for this App configuration entity.</span></span> <span data-ttu-id="a03e0-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a03e0-145">createdDateTime</span></span>|<span data-ttu-id="a03e0-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a03e0-146">DateTimeOffset</span></span>|<span data-ttu-id="a03e0-147">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="a03e0-147">DateTime the object was created.</span></span> <span data-ttu-id="a03e0-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-149">descripción</span><span class="sxs-lookup"><span data-stu-id="a03e0-149">description</span></span>|<span data-ttu-id="a03e0-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="a03e0-150">String</span></span>|<span data-ttu-id="a03e0-151">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a03e0-151">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="a03e0-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a03e0-153">lastModifiedDateTime</span></span>|<span data-ttu-id="a03e0-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a03e0-154">DateTimeOffset</span></span>|<span data-ttu-id="a03e0-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="a03e0-155">DateTime the object was last modified.</span></span> <span data-ttu-id="a03e0-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-157">displayName</span><span class="sxs-lookup"><span data-stu-id="a03e0-157">displayName</span></span>|<span data-ttu-id="a03e0-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="a03e0-158">String</span></span>|<span data-ttu-id="a03e0-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a03e0-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="a03e0-160">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-160">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-161">versión</span><span class="sxs-lookup"><span data-stu-id="a03e0-161">version</span></span>|<span data-ttu-id="a03e0-162">Int32</span><span class="sxs-lookup"><span data-stu-id="a03e0-162">Int32</span></span>|<span data-ttu-id="a03e0-163">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a03e0-163">Version of the device configuration.</span></span> <span data-ttu-id="a03e0-164">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-164">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="a03e0-165">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="a03e0-165">encodedSettingXml</span></span>|<span data-ttu-id="a03e0-166">Binario</span><span class="sxs-lookup"><span data-stu-id="a03e0-166">Binary</span></span>|<span data-ttu-id="a03e0-167">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="a03e0-167">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="a03e0-168">configuración</span><span class="sxs-lookup"><span data-stu-id="a03e0-168">settings</span></span>|<span data-ttu-id="a03e0-169">Colección [appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="a03e0-169">[appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="a03e0-170">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a03e0-170">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="a03e0-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a03e0-171">Response</span></span>
<span data-ttu-id="a03e0-172">Si se ejecuta correctamente, este método devuelve un `201 Created` código de respuesta y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a03e0-172">If successful, this method returns a `201 Created` response code and a [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a03e0-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a03e0-173">Example</span></span>
### <a name="request"></a><span data-ttu-id="a03e0-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a03e0-174">Request</span></span>
<span data-ttu-id="a03e0-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a03e0-175">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations
Content-type: application/json
Content-length: 660

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
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

### <a name="response"></a><span data-ttu-id="a03e0-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a03e0-176">Response</span></span>
<span data-ttu-id="a03e0-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a03e0-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 768

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "id": "b2c33191-3191-b2c3-9131-c3b29131c3b2",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
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





