---
title: Crear iosDeviceFeaturesConfiguration
description: Cree un objeto iosDeviceFeaturesConfiguration.
author: tfitzmac
ms.openlocfilehash: 9467e42e16d88e0d1bfa02ea0996a8930d5d6cdd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307423"
---
# <a name="create-iosdevicefeaturesconfiguration"></a><span data-ttu-id="9f489-103">Crear iosDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f489-103">Create iosDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="9f489-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f489-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f489-105">Cree un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9f489-105">Create a new [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f489-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f489-106">Prerequisites</span></span>
<span data-ttu-id="9f489-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f489-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9f489-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f489-109">Permission type</span></span>|<span data-ttu-id="9f489-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f489-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f489-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f489-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9f489-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f489-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9f489-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f489-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f489-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f489-114">Not supported.</span></span>|
|<span data-ttu-id="9f489-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f489-115">Application</span></span>|<span data-ttu-id="9f489-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f489-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f489-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f489-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="9f489-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f489-118">Request headers</span></span>
|<span data-ttu-id="9f489-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f489-119">Header</span></span>|<span data-ttu-id="9f489-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9f489-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f489-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f489-121">Authorization</span></span>|<span data-ttu-id="9f489-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f489-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9f489-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9f489-123">Accept</span></span>|<span data-ttu-id="9f489-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9f489-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f489-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f489-125">Request body</span></span>
<span data-ttu-id="9f489-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosDeviceFeaturesConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9f489-126">In the request body, supply a JSON representation for the iosDeviceFeaturesConfiguration object.</span></span>

<span data-ttu-id="9f489-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosDeviceFeaturesConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9f489-127">The following table shows the properties that are required when you create the iosDeviceFeaturesConfiguration.</span></span>

|<span data-ttu-id="9f489-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f489-128">Property</span></span>|<span data-ttu-id="9f489-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f489-129">Type</span></span>|<span data-ttu-id="9f489-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f489-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f489-131">id</span><span class="sxs-lookup"><span data-stu-id="9f489-131">id</span></span>|<span data-ttu-id="9f489-132">String</span><span class="sxs-lookup"><span data-stu-id="9f489-132">String</span></span>|<span data-ttu-id="9f489-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9f489-133">Key of the entity.</span></span> <span data-ttu-id="9f489-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9f489-135">lastModifiedDateTime</span></span>|<span data-ttu-id="9f489-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f489-136">DateTimeOffset</span></span>|<span data-ttu-id="9f489-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9f489-137">DateTime the object was last modified.</span></span> <span data-ttu-id="9f489-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9f489-139">createdDateTime</span></span>|<span data-ttu-id="9f489-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9f489-140">DateTimeOffset</span></span>|<span data-ttu-id="9f489-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="9f489-141">DateTime the object was created.</span></span> <span data-ttu-id="9f489-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-143">descripción</span><span class="sxs-lookup"><span data-stu-id="9f489-143">description</span></span>|<span data-ttu-id="9f489-144">String</span><span class="sxs-lookup"><span data-stu-id="9f489-144">String</span></span>|<span data-ttu-id="9f489-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f489-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="9f489-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-147">displayName</span><span class="sxs-lookup"><span data-stu-id="9f489-147">displayName</span></span>|<span data-ttu-id="9f489-148">String</span><span class="sxs-lookup"><span data-stu-id="9f489-148">String</span></span>|<span data-ttu-id="9f489-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f489-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="9f489-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-151">version</span><span class="sxs-lookup"><span data-stu-id="9f489-151">version</span></span>|<span data-ttu-id="9f489-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9f489-152">Int32</span></span>|<span data-ttu-id="9f489-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f489-153">Version of the device configuration.</span></span> <span data-ttu-id="9f489-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9f489-155">assetTagTemplate</span><span class="sxs-lookup"><span data-stu-id="9f489-155">assetTagTemplate</span></span>|<span data-ttu-id="9f489-156">String</span><span class="sxs-lookup"><span data-stu-id="9f489-156">String</span></span>|<span data-ttu-id="9f489-157">Información de la etiqueta de activo del dispositivo, se muestra en la ventana de inicio de sesión y en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="9f489-157">Asset tag information for the device, displayed on the login window and lock screen.</span></span>|
|<span data-ttu-id="9f489-158">lockScreenFootnote</span><span class="sxs-lookup"><span data-stu-id="9f489-158">lockScreenFootnote</span></span>|<span data-ttu-id="9f489-159">String</span><span class="sxs-lookup"><span data-stu-id="9f489-159">String</span></span>|<span data-ttu-id="9f489-160">Nota al pie que se muestra en la ventana de inicio de sesión y la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="9f489-160">A footnote displayed on the login window and lock screen.</span></span> <span data-ttu-id="9f489-161">Disponible en iOS 9.3.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9f489-161">Available in iOS 9.3.1 and later.</span></span>|
|<span data-ttu-id="9f489-162">homeScreenDockIcons</span><span class="sxs-lookup"><span data-stu-id="9f489-162">homeScreenDockIcons</span></span>|<span data-ttu-id="9f489-163">Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-163">[iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="9f489-164">Lista de las aplicaciones y carpetas que aparecen en el Dock de la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="9f489-164">A list of app and folders to appear on the Home Screen Dock.</span></span> <span data-ttu-id="9f489-165">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="9f489-165">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="9f489-166">homeScreenPages</span><span class="sxs-lookup"><span data-stu-id="9f489-166">homeScreenPages</span></span>|<span data-ttu-id="9f489-167">Colección [iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-167">[iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md) collection</span></span>|<span data-ttu-id="9f489-168">Lista de páginas en la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="9f489-168">A list of pages on the Home Screen.</span></span> <span data-ttu-id="9f489-169">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="9f489-169">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="9f489-170">notificationSettings</span><span class="sxs-lookup"><span data-stu-id="9f489-170">notificationSettings</span></span>|<span data-ttu-id="9f489-171">Colección [iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md)</span><span class="sxs-lookup"><span data-stu-id="9f489-171">[iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md) collection</span></span>|<span data-ttu-id="9f489-172">Configuración de notificaciones de cada identificador de agrupación. Solo se aplica a los dispositivos en modo supervisado (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="9f489-172">Notification settings for each bundle id. Applicable to devices in supervised mode only (iOS 9.3 and later).</span></span> <span data-ttu-id="9f489-173">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="9f489-173">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="9f489-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f489-174">Response</span></span>
<span data-ttu-id="9f489-175">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f489-175">If successful, this method returns a `201 Created` response code and a [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f489-176">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f489-176">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f489-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f489-177">Request</span></span>
<span data-ttu-id="9f489-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f489-178">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="9f489-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f489-179">Response</span></span>
<span data-ttu-id="9f489-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f489-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



