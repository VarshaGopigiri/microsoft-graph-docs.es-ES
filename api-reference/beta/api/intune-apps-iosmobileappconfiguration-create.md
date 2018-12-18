---
title: Crear iosMobileAppConfiguration
description: Crear un nuevo objeto iosMobileAppConfiguration.
author: tfitzmac
ms.openlocfilehash: e61a90540e0541fd9b14f4cad33e8ea9f95a803a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315788"
---
# <a name="create-iosmobileappconfiguration"></a><span data-ttu-id="89e8f-103">Crear iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="89e8f-103">Create iosMobileAppConfiguration</span></span>

> <span data-ttu-id="89e8f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="89e8f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="89e8f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="89e8f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="89e8f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89e8f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89e8f-107">Crear un nuevo objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="89e8f-107">Create a new [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="89e8f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="89e8f-108">Prerequisites</span></span>
<span data-ttu-id="89e8f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="89e8f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="89e8f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89e8f-111">Permission type</span></span>|<span data-ttu-id="89e8f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89e8f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="89e8f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89e8f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="89e8f-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="89e8f-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="89e8f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89e8f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="89e8f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89e8f-116">Not supported.</span></span>|
|<span data-ttu-id="89e8f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89e8f-117">Application</span></span>|<span data-ttu-id="89e8f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89e8f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="89e8f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89e8f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="89e8f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89e8f-120">Request headers</span></span>
|<span data-ttu-id="89e8f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89e8f-121">Header</span></span>|<span data-ttu-id="89e8f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="89e8f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="89e8f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="89e8f-123">Authorization</span></span>|<span data-ttu-id="89e8f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="89e8f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="89e8f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="89e8f-125">Accept</span></span>|<span data-ttu-id="89e8f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="89e8f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="89e8f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89e8f-127">Request body</span></span>
<span data-ttu-id="89e8f-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="89e8f-128">In the request body, supply a JSON representation for the iosMobileAppConfiguration object.</span></span>

<span data-ttu-id="89e8f-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="89e8f-129">The following table shows the properties that are required when you create the iosMobileAppConfiguration.</span></span>

|<span data-ttu-id="89e8f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89e8f-130">Property</span></span>|<span data-ttu-id="89e8f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="89e8f-131">Type</span></span>|<span data-ttu-id="89e8f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="89e8f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="89e8f-133">id</span><span class="sxs-lookup"><span data-stu-id="89e8f-133">id</span></span>|<span data-ttu-id="89e8f-134">String</span><span class="sxs-lookup"><span data-stu-id="89e8f-134">String</span></span>|<span data-ttu-id="89e8f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="89e8f-135">Key of the entity.</span></span> <span data-ttu-id="89e8f-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-137">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="89e8f-137">targetedMobileApps</span></span>|<span data-ttu-id="89e8f-138">Colección string</span><span class="sxs-lookup"><span data-stu-id="89e8f-138">String collection</span></span>|<span data-ttu-id="89e8f-139">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="89e8f-139">the associated app.</span></span> <span data-ttu-id="89e8f-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="89e8f-141">roleScopeTagIds</span></span>|<span data-ttu-id="89e8f-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="89e8f-142">String collection</span></span>|<span data-ttu-id="89e8f-143">Lista de etiquetas de ámbito para esta entidad de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e8f-143">List of Scope Tags for this App configuration entity.</span></span> <span data-ttu-id="89e8f-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-145">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="89e8f-145">createdDateTime</span></span>|<span data-ttu-id="89e8f-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="89e8f-146">DateTimeOffset</span></span>|<span data-ttu-id="89e8f-147">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="89e8f-147">DateTime the object was created.</span></span> <span data-ttu-id="89e8f-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-149">descripción</span><span class="sxs-lookup"><span data-stu-id="89e8f-149">description</span></span>|<span data-ttu-id="89e8f-150">String</span><span class="sxs-lookup"><span data-stu-id="89e8f-150">String</span></span>|<span data-ttu-id="89e8f-151">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89e8f-151">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="89e8f-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="89e8f-153">lastModifiedDateTime</span></span>|<span data-ttu-id="89e8f-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="89e8f-154">DateTimeOffset</span></span>|<span data-ttu-id="89e8f-155">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="89e8f-155">DateTime the object was last modified.</span></span> <span data-ttu-id="89e8f-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-157">displayName</span><span class="sxs-lookup"><span data-stu-id="89e8f-157">displayName</span></span>|<span data-ttu-id="89e8f-158">String</span><span class="sxs-lookup"><span data-stu-id="89e8f-158">String</span></span>|<span data-ttu-id="89e8f-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89e8f-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="89e8f-160">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-160">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-161">versión</span><span class="sxs-lookup"><span data-stu-id="89e8f-161">version</span></span>|<span data-ttu-id="89e8f-162">Int32</span><span class="sxs-lookup"><span data-stu-id="89e8f-162">Int32</span></span>|<span data-ttu-id="89e8f-163">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89e8f-163">Version of the device configuration.</span></span> <span data-ttu-id="89e8f-164">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-164">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="89e8f-165">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="89e8f-165">encodedSettingXml</span></span>|<span data-ttu-id="89e8f-166">Binario</span><span class="sxs-lookup"><span data-stu-id="89e8f-166">Binary</span></span>|<span data-ttu-id="89e8f-167">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="89e8f-167">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="89e8f-168">configuración</span><span class="sxs-lookup"><span data-stu-id="89e8f-168">settings</span></span>|<span data-ttu-id="89e8f-169">Colección [appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="89e8f-169">[appConfigurationSettingItem](../resources/intune-apps-appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="89e8f-170">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="89e8f-170">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="89e8f-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89e8f-171">Response</span></span>
<span data-ttu-id="89e8f-172">Si se ejecuta correctamente, este método devuelve un `201 Created` código de respuesta y un objeto [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89e8f-172">If successful, this method returns a `201 Created` response code and a [iosMobileAppConfiguration](../resources/intune-apps-iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89e8f-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89e8f-173">Example</span></span>
### <a name="request"></a><span data-ttu-id="89e8f-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89e8f-174">Request</span></span>
<span data-ttu-id="89e8f-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89e8f-175">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="89e8f-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89e8f-176">Response</span></span>
<span data-ttu-id="89e8f-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="89e8f-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





