---
title: Actualizar iosDeviceFeaturesConfiguration
description: Actualice las propiedades de un objeto iosDeviceFeaturesConfiguration.
ms.openlocfilehash: 473e28586e51d858320605957e446d730023c8f9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030971"
---
# <a name="update-iosdevicefeaturesconfiguration"></a><span data-ttu-id="618f2-103">Actualizar iosDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="618f2-103">Update iosDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="618f2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="618f2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="618f2-105">Actualice las propiedades de un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="618f2-105">Update the properties of a [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="618f2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="618f2-106">Prerequisites</span></span>
<span data-ttu-id="618f2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="618f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="618f2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="618f2-109">Permission type</span></span>|<span data-ttu-id="618f2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="618f2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="618f2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="618f2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="618f2-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="618f2-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="618f2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="618f2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="618f2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="618f2-114">Not supported.</span></span>|
|<span data-ttu-id="618f2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="618f2-115">Application</span></span>|<span data-ttu-id="618f2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="618f2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="618f2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="618f2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="618f2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="618f2-118">Request headers</span></span>
|<span data-ttu-id="618f2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="618f2-119">Header</span></span>|<span data-ttu-id="618f2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="618f2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="618f2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="618f2-121">Authorization</span></span>|<span data-ttu-id="618f2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="618f2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="618f2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="618f2-123">Accept</span></span>|<span data-ttu-id="618f2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="618f2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="618f2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="618f2-125">Request body</span></span>
<span data-ttu-id="618f2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="618f2-126">In the request body, supply a JSON representation for the [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="618f2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="618f2-127">The following table shows the properties that are required when you create the [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span></span>

|<span data-ttu-id="618f2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="618f2-128">Property</span></span>|<span data-ttu-id="618f2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="618f2-129">Type</span></span>|<span data-ttu-id="618f2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="618f2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="618f2-131">id</span><span class="sxs-lookup"><span data-stu-id="618f2-131">id</span></span>|<span data-ttu-id="618f2-132">String</span><span class="sxs-lookup"><span data-stu-id="618f2-132">String</span></span>|<span data-ttu-id="618f2-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="618f2-133">Key of the entity.</span></span> <span data-ttu-id="618f2-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="618f2-135">lastModifiedDateTime</span></span>|<span data-ttu-id="618f2-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="618f2-136">DateTimeOffset</span></span>|<span data-ttu-id="618f2-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="618f2-137">DateTime the object was last modified.</span></span> <span data-ttu-id="618f2-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="618f2-139">createdDateTime</span></span>|<span data-ttu-id="618f2-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="618f2-140">DateTimeOffset</span></span>|<span data-ttu-id="618f2-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="618f2-141">DateTime the object was created.</span></span> <span data-ttu-id="618f2-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-143">descripción</span><span class="sxs-lookup"><span data-stu-id="618f2-143">description</span></span>|<span data-ttu-id="618f2-144">String</span><span class="sxs-lookup"><span data-stu-id="618f2-144">String</span></span>|<span data-ttu-id="618f2-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="618f2-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="618f2-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-147">displayName</span><span class="sxs-lookup"><span data-stu-id="618f2-147">displayName</span></span>|<span data-ttu-id="618f2-148">String</span><span class="sxs-lookup"><span data-stu-id="618f2-148">String</span></span>|<span data-ttu-id="618f2-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="618f2-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="618f2-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-151">version</span><span class="sxs-lookup"><span data-stu-id="618f2-151">version</span></span>|<span data-ttu-id="618f2-152">Int32</span><span class="sxs-lookup"><span data-stu-id="618f2-152">Int32</span></span>|<span data-ttu-id="618f2-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="618f2-153">Version of the device configuration.</span></span> <span data-ttu-id="618f2-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="618f2-155">assetTagTemplate</span><span class="sxs-lookup"><span data-stu-id="618f2-155">assetTagTemplate</span></span>|<span data-ttu-id="618f2-156">String</span><span class="sxs-lookup"><span data-stu-id="618f2-156">String</span></span>|<span data-ttu-id="618f2-157">Información de la etiqueta de activo del dispositivo, se muestra en la ventana de inicio de sesión y en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="618f2-157">Asset tag information for the device, displayed on the login window and lock screen.</span></span>|
|<span data-ttu-id="618f2-158">lockScreenFootnote</span><span class="sxs-lookup"><span data-stu-id="618f2-158">lockScreenFootnote</span></span>|<span data-ttu-id="618f2-159">String</span><span class="sxs-lookup"><span data-stu-id="618f2-159">String</span></span>|<span data-ttu-id="618f2-160">Nota al pie que se muestra en la ventana de inicio de sesión y la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="618f2-160">A footnote displayed on the login window and lock screen.</span></span> <span data-ttu-id="618f2-161">Disponible en iOS 9.3.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="618f2-161">Available in iOS 9.3.1 and later.</span></span>|
|<span data-ttu-id="618f2-162">homeScreenDockIcons</span><span class="sxs-lookup"><span data-stu-id="618f2-162">homeScreenDockIcons</span></span>|<span data-ttu-id="618f2-163">Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-163">[iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="618f2-164">Lista de las aplicaciones y carpetas que aparecen en el Dock de la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="618f2-164">A list of app and folders to appear on the Home Screen Dock.</span></span> <span data-ttu-id="618f2-165">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="618f2-165">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="618f2-166">homeScreenPages</span><span class="sxs-lookup"><span data-stu-id="618f2-166">homeScreenPages</span></span>|<span data-ttu-id="618f2-167">Colección [iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-167">[iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md) collection</span></span>|<span data-ttu-id="618f2-168">Lista de páginas en la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="618f2-168">A list of pages on the Home Screen.</span></span> <span data-ttu-id="618f2-169">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="618f2-169">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="618f2-170">notificationSettings</span><span class="sxs-lookup"><span data-stu-id="618f2-170">notificationSettings</span></span>|<span data-ttu-id="618f2-171">Colección [iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md)</span><span class="sxs-lookup"><span data-stu-id="618f2-171">[iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md) collection</span></span>|<span data-ttu-id="618f2-172">Configuración de notificaciones de cada identificador de agrupación. Solo se aplica a los dispositivos en modo supervisado (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="618f2-172">Notification settings for each bundle id. Applicable to devices in supervised mode only (iOS 9.3 and later).</span></span> <span data-ttu-id="618f2-173">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="618f2-173">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="618f2-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="618f2-174">Response</span></span>
<span data-ttu-id="618f2-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="618f2-175">If successful, this method returns a `200 OK` response code and an updated [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="618f2-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="618f2-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="618f2-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="618f2-177">Request</span></span>
<span data-ttu-id="618f2-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="618f2-178">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1988

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="618f2-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="618f2-179">Response</span></span>
<span data-ttu-id="618f2-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="618f2-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2160

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```


