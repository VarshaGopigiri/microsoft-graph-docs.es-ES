---
title: Crear iosDeviceFeaturesConfiguration
description: Cree un objeto iosDeviceFeaturesConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b721495e6299fbe59b18cea0818ae61d74e364e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931737"
---
# <a name="create-iosdevicefeaturesconfiguration"></a><span data-ttu-id="db9b7-103">Crear iosDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="db9b7-103">Create iosDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="db9b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="db9b7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="db9b7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="db9b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="db9b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="db9b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="db9b7-107">Cree un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="db9b7-107">Create a new [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="db9b7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="db9b7-108">Prerequisites</span></span>
<span data-ttu-id="db9b7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="db9b7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="db9b7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="db9b7-111">Permission type</span></span>|<span data-ttu-id="db9b7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="db9b7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="db9b7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="db9b7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="db9b7-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="db9b7-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="db9b7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="db9b7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="db9b7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db9b7-116">Not supported.</span></span>|
|<span data-ttu-id="db9b7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="db9b7-117">Application</span></span>|<span data-ttu-id="db9b7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="db9b7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="db9b7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="db9b7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="db9b7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="db9b7-120">Request headers</span></span>
|<span data-ttu-id="db9b7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="db9b7-121">Header</span></span>|<span data-ttu-id="db9b7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="db9b7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="db9b7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="db9b7-123">Authorization</span></span>|<span data-ttu-id="db9b7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="db9b7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="db9b7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="db9b7-125">Accept</span></span>|<span data-ttu-id="db9b7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="db9b7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="db9b7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="db9b7-127">Request body</span></span>
<span data-ttu-id="db9b7-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosDeviceFeaturesConfiguration.</span><span class="sxs-lookup"><span data-stu-id="db9b7-128">In the request body, supply a JSON representation for the iosDeviceFeaturesConfiguration object.</span></span>

<span data-ttu-id="db9b7-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosDeviceFeaturesConfiguration.</span><span class="sxs-lookup"><span data-stu-id="db9b7-129">The following table shows the properties that are required when you create the iosDeviceFeaturesConfiguration.</span></span>

|<span data-ttu-id="db9b7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="db9b7-130">Property</span></span>|<span data-ttu-id="db9b7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="db9b7-131">Type</span></span>|<span data-ttu-id="db9b7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="db9b7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="db9b7-133">id</span><span class="sxs-lookup"><span data-stu-id="db9b7-133">id</span></span>|<span data-ttu-id="db9b7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="db9b7-134">String</span></span>|<span data-ttu-id="db9b7-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="db9b7-135">Key of the entity.</span></span> <span data-ttu-id="db9b7-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="db9b7-137">lastModifiedDateTime</span></span>|<span data-ttu-id="db9b7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="db9b7-138">DateTimeOffset</span></span>|<span data-ttu-id="db9b7-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="db9b7-139">DateTime the object was last modified.</span></span> <span data-ttu-id="db9b7-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="db9b7-141">roleScopeTagIds</span></span>|<span data-ttu-id="db9b7-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="db9b7-142">String collection</span></span>|<span data-ttu-id="db9b7-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="db9b7-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="db9b7-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="db9b7-145">supportsScopeTags</span></span>|<span data-ttu-id="db9b7-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="db9b7-146">Boolean</span></span>|<span data-ttu-id="db9b7-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="db9b7-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="db9b7-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="db9b7-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="db9b7-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="db9b7-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="db9b7-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="db9b7-150">This property is read-only.</span></span> <span data-ttu-id="db9b7-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="db9b7-152">createdDateTime</span></span>|<span data-ttu-id="db9b7-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="db9b7-153">DateTimeOffset</span></span>|<span data-ttu-id="db9b7-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="db9b7-154">DateTime the object was created.</span></span> <span data-ttu-id="db9b7-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-156">descripción</span><span class="sxs-lookup"><span data-stu-id="db9b7-156">description</span></span>|<span data-ttu-id="db9b7-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="db9b7-157">String</span></span>|<span data-ttu-id="db9b7-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db9b7-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="db9b7-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-160">displayName</span><span class="sxs-lookup"><span data-stu-id="db9b7-160">displayName</span></span>|<span data-ttu-id="db9b7-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="db9b7-161">String</span></span>|<span data-ttu-id="db9b7-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db9b7-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="db9b7-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-164">version</span><span class="sxs-lookup"><span data-stu-id="db9b7-164">version</span></span>|<span data-ttu-id="db9b7-165">Int32</span><span class="sxs-lookup"><span data-stu-id="db9b7-165">Int32</span></span>|<span data-ttu-id="db9b7-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db9b7-166">Version of the device configuration.</span></span> <span data-ttu-id="db9b7-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="db9b7-168">airPrintDestinations</span><span class="sxs-lookup"><span data-stu-id="db9b7-168">airPrintDestinations</span></span>|<span data-ttu-id="db9b7-169">colección de [airPrintDestination](../resources/intune-deviceconfig-airprintdestination.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-169">[airPrintDestination](../resources/intune-deviceconfig-airprintdestination.md) collection</span></span>|<span data-ttu-id="db9b7-170">Una matriz de impresoras AirPrint que siempre se deben mostrar.</span><span class="sxs-lookup"><span data-stu-id="db9b7-170">An array of AirPrint printers that should always be shown.</span></span> <span data-ttu-id="db9b7-171">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="db9b7-171">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="db9b7-172">Se hereda de [appleDeviceFeaturesConfigurationBase](../resources/intune-deviceconfig-appledevicefeaturesconfigurationbase.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-172">Inherited from [appleDeviceFeaturesConfigurationBase](../resources/intune-deviceconfig-appledevicefeaturesconfigurationbase.md)</span></span>|
|<span data-ttu-id="db9b7-173">assetTagTemplate</span><span class="sxs-lookup"><span data-stu-id="db9b7-173">assetTagTemplate</span></span>|<span data-ttu-id="db9b7-174">Cadena</span><span class="sxs-lookup"><span data-stu-id="db9b7-174">String</span></span>|<span data-ttu-id="db9b7-175">Información de la etiqueta de activo del dispositivo, se muestra en la ventana de inicio de sesión y en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="db9b7-175">Asset tag information for the device, displayed on the login window and lock screen.</span></span>|
|<span data-ttu-id="db9b7-176">contentFilterSettings</span><span class="sxs-lookup"><span data-stu-id="db9b7-176">contentFilterSettings</span></span>|[<span data-ttu-id="db9b7-177">iosWebContentFilterBase</span><span class="sxs-lookup"><span data-stu-id="db9b7-177">iosWebContentFilterBase</span></span>](../resources/intune-deviceconfig-ioswebcontentfilterbase.md)|<span data-ttu-id="db9b7-178">Obtiene o establece iOS configuración del filtro de contenido Web, sólo en modo supervisado</span><span class="sxs-lookup"><span data-stu-id="db9b7-178">Gets or sets iOS Web Content Filter settings, supervised mode only</span></span>|
|<span data-ttu-id="db9b7-179">lockScreenFootnote</span><span class="sxs-lookup"><span data-stu-id="db9b7-179">lockScreenFootnote</span></span>|<span data-ttu-id="db9b7-180">Cadena</span><span class="sxs-lookup"><span data-stu-id="db9b7-180">String</span></span>|<span data-ttu-id="db9b7-181">Nota al pie que se muestra en la ventana de inicio de sesión y la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="db9b7-181">A footnote displayed on the login window and lock screen.</span></span> <span data-ttu-id="db9b7-182">Disponible en iOS 9.3.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="db9b7-182">Available in iOS 9.3.1 and later.</span></span>|
|<span data-ttu-id="db9b7-183">homeScreenDockIcons</span><span class="sxs-lookup"><span data-stu-id="db9b7-183">homeScreenDockIcons</span></span>|<span data-ttu-id="db9b7-184">Colección [iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-184">[iosHomeScreenItem](../resources/intune-deviceconfig-ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="db9b7-185">Lista de las aplicaciones y carpetas que aparecen en el Dock de la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="db9b7-185">A list of app and folders to appear on the Home Screen Dock.</span></span> <span data-ttu-id="db9b7-186">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="db9b7-186">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="db9b7-187">homeScreenPages</span><span class="sxs-lookup"><span data-stu-id="db9b7-187">homeScreenPages</span></span>|<span data-ttu-id="db9b7-188">Colección [iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-188">[iosHomeScreenPage](../resources/intune-deviceconfig-ioshomescreenpage.md) collection</span></span>|<span data-ttu-id="db9b7-189">Lista de páginas en la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="db9b7-189">A list of pages on the Home Screen.</span></span> <span data-ttu-id="db9b7-190">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="db9b7-190">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="db9b7-191">notificationSettings</span><span class="sxs-lookup"><span data-stu-id="db9b7-191">notificationSettings</span></span>|<span data-ttu-id="db9b7-192">Colección [iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md)</span><span class="sxs-lookup"><span data-stu-id="db9b7-192">[iosNotificationSettings](../resources/intune-deviceconfig-iosnotificationsettings.md) collection</span></span>|<span data-ttu-id="db9b7-193">Configuración de notificaciones de cada identificador de agrupación. Solo se aplica a los dispositivos en modo supervisado (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="db9b7-193">Notification settings for each bundle id. Applicable to devices in supervised mode only (iOS 9.3 and later).</span></span> <span data-ttu-id="db9b7-194">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="db9b7-194">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="db9b7-195">singleSignOnSettings</span><span class="sxs-lookup"><span data-stu-id="db9b7-195">singleSignOnSettings</span></span>|[<span data-ttu-id="db9b7-196">iosSingleSignOnSettings</span><span class="sxs-lookup"><span data-stu-id="db9b7-196">iosSingleSignOnSettings</span></span>](../resources/intune-deviceconfig-iossinglesignonsettings.md)|<span data-ttu-id="db9b7-197">La configuración de inicio de sesión de Kerberos que les permiten a las aplicaciones de recepción de dispositivos para autenticar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="db9b7-197">The Kerberos login settings that enable apps on receiving devices to authenticate smoothly.</span></span>|



## <a name="response"></a><span data-ttu-id="db9b7-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db9b7-198">Response</span></span>
<span data-ttu-id="db9b7-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="db9b7-199">If successful, this method returns a `201 Created` response code and a [iosDeviceFeaturesConfiguration](../resources/intune-deviceconfig-iosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="db9b7-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="db9b7-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="db9b7-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="db9b7-201">Request</span></span>
<span data-ttu-id="db9b7-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="db9b7-202">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 3543

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "airPrintDestinations": [
    {
      "@odata.type": "microsoft.graph.airPrintDestination",
      "ipAddress": "Ip Address value",
      "resourcePath": "Resource Path value",
      "port": 4,
      "forceTls": true
    }
  ],
  "assetTagTemplate": "Asset Tag Template value",
  "contentFilterSettings": {
    "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
    "specificWebsitesOnly": [
      {
        "@odata.type": "microsoft.graph.iosBookmark",
        "url": "Url value",
        "bookmarkFolder": "Bookmark Folder value",
        "displayName": "Display Name value"
      }
    ],
    "websiteList": [
      {
        "@odata.type": "microsoft.graph.iosBookmark",
        "url": "Url value",
        "bookmarkFolder": "Bookmark Folder value",
        "displayName": "Display Name value"
      }
    ]
  },
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
  ],
  "singleSignOnSettings": {
    "@odata.type": "microsoft.graph.iosSingleSignOnSettings",
    "allowedAppsList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "allowedUrls": [
      "Allowed Urls value"
    ],
    "displayName": "Display Name value",
    "kerberosPrincipalName": "Kerberos Principal Name value",
    "kerberosRealm": "Kerberos Realm value"
  }
}
```

### <a name="response"></a><span data-ttu-id="db9b7-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="db9b7-203">Response</span></span>
<span data-ttu-id="db9b7-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="db9b7-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 3651

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "airPrintDestinations": [
    {
      "@odata.type": "microsoft.graph.airPrintDestination",
      "ipAddress": "Ip Address value",
      "resourcePath": "Resource Path value",
      "port": 4,
      "forceTls": true
    }
  ],
  "assetTagTemplate": "Asset Tag Template value",
  "contentFilterSettings": {
    "@odata.type": "microsoft.graph.iosWebContentFilterSpecificWebsitesAccess",
    "specificWebsitesOnly": [
      {
        "@odata.type": "microsoft.graph.iosBookmark",
        "url": "Url value",
        "bookmarkFolder": "Bookmark Folder value",
        "displayName": "Display Name value"
      }
    ],
    "websiteList": [
      {
        "@odata.type": "microsoft.graph.iosBookmark",
        "url": "Url value",
        "bookmarkFolder": "Bookmark Folder value",
        "displayName": "Display Name value"
      }
    ]
  },
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
  ],
  "singleSignOnSettings": {
    "@odata.type": "microsoft.graph.iosSingleSignOnSettings",
    "allowedAppsList": [
      {
        "@odata.type": "microsoft.graph.appListItem",
        "name": "Name value",
        "publisher": "Publisher value",
        "appStoreUrl": "https://example.com/appStoreUrl/",
        "appId": "App Id value"
      }
    ],
    "allowedUrls": [
      "Allowed Urls value"
    ],
    "displayName": "Display Name value",
    "kerberosPrincipalName": "Kerberos Principal Name value",
    "kerberosRealm": "Kerberos Realm value"
  }
}
```





