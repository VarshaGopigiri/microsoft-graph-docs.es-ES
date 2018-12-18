---
title: Crear windowsKioskConfiguration
description: Crear un nuevo objeto windowsKioskConfiguration.
author: tfitzmac
ms.openlocfilehash: 35630494206a234e248935a75483afa2da969ed4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327541"
---
# <a name="create-windowskioskconfiguration"></a><span data-ttu-id="39bca-103">Crear windowsKioskConfiguration</span><span class="sxs-lookup"><span data-stu-id="39bca-103">Create windowsKioskConfiguration</span></span>

> <span data-ttu-id="39bca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39bca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39bca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39bca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="39bca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="39bca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="39bca-107">Crear un nuevo objeto [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="39bca-107">Create a new [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="39bca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="39bca-108">Prerequisites</span></span>
<span data-ttu-id="39bca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="39bca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="39bca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="39bca-111">Permission type</span></span>|<span data-ttu-id="39bca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="39bca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="39bca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="39bca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="39bca-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="39bca-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="39bca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="39bca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="39bca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39bca-116">Not supported.</span></span>|
|<span data-ttu-id="39bca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="39bca-117">Application</span></span>|<span data-ttu-id="39bca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="39bca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="39bca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="39bca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="39bca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="39bca-120">Request headers</span></span>
|<span data-ttu-id="39bca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39bca-121">Header</span></span>|<span data-ttu-id="39bca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="39bca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="39bca-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="39bca-123">Authorization</span></span>|<span data-ttu-id="39bca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="39bca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="39bca-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="39bca-125">Accept</span></span>|<span data-ttu-id="39bca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="39bca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="39bca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="39bca-127">Request body</span></span>
<span data-ttu-id="39bca-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsKioskConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39bca-128">In the request body, supply a JSON representation for the windowsKioskConfiguration object.</span></span>

<span data-ttu-id="39bca-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsKioskConfiguration.</span><span class="sxs-lookup"><span data-stu-id="39bca-129">The following table shows the properties that are required when you create the windowsKioskConfiguration.</span></span>

|<span data-ttu-id="39bca-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39bca-130">Property</span></span>|<span data-ttu-id="39bca-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="39bca-131">Type</span></span>|<span data-ttu-id="39bca-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="39bca-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="39bca-133">id</span><span class="sxs-lookup"><span data-stu-id="39bca-133">id</span></span>|<span data-ttu-id="39bca-134">String</span><span class="sxs-lookup"><span data-stu-id="39bca-134">String</span></span>|<span data-ttu-id="39bca-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="39bca-135">Key of the entity.</span></span> <span data-ttu-id="39bca-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="39bca-137">lastModifiedDateTime</span></span>|<span data-ttu-id="39bca-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39bca-138">DateTimeOffset</span></span>|<span data-ttu-id="39bca-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="39bca-139">DateTime the object was last modified.</span></span> <span data-ttu-id="39bca-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="39bca-141">roleScopeTagIds</span></span>|<span data-ttu-id="39bca-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="39bca-142">String collection</span></span>|<span data-ttu-id="39bca-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="39bca-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="39bca-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="39bca-145">supportsScopeTags</span></span>|<span data-ttu-id="39bca-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="39bca-146">Boolean</span></span>|<span data-ttu-id="39bca-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="39bca-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="39bca-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="39bca-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="39bca-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="39bca-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="39bca-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="39bca-150">This property is read-only.</span></span> <span data-ttu-id="39bca-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="39bca-152">createdDateTime</span></span>|<span data-ttu-id="39bca-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="39bca-153">DateTimeOffset</span></span>|<span data-ttu-id="39bca-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="39bca-154">DateTime the object was created.</span></span> <span data-ttu-id="39bca-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-156">descripción</span><span class="sxs-lookup"><span data-stu-id="39bca-156">description</span></span>|<span data-ttu-id="39bca-157">String</span><span class="sxs-lookup"><span data-stu-id="39bca-157">String</span></span>|<span data-ttu-id="39bca-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39bca-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="39bca-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-160">displayName</span><span class="sxs-lookup"><span data-stu-id="39bca-160">displayName</span></span>|<span data-ttu-id="39bca-161">String</span><span class="sxs-lookup"><span data-stu-id="39bca-161">String</span></span>|<span data-ttu-id="39bca-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39bca-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="39bca-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-164">version</span><span class="sxs-lookup"><span data-stu-id="39bca-164">version</span></span>|<span data-ttu-id="39bca-165">Int32</span><span class="sxs-lookup"><span data-stu-id="39bca-165">Int32</span></span>|<span data-ttu-id="39bca-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="39bca-166">Version of the device configuration.</span></span> <span data-ttu-id="39bca-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="39bca-168">kioskProfiles</span><span class="sxs-lookup"><span data-stu-id="39bca-168">kioskProfiles</span></span>|<span data-ttu-id="39bca-169">colección de [windowsKioskProfile](../resources/intune-deviceconfig-windowskioskprofile.md)</span><span class="sxs-lookup"><span data-stu-id="39bca-169">[windowsKioskProfile](../resources/intune-deviceconfig-windowskioskprofile.md) collection</span></span>|<span data-ttu-id="39bca-170">Esta configuración de directiva permite que para definir una lista de perfiles de quiosco para una configuración de quiosco.</span><span class="sxs-lookup"><span data-stu-id="39bca-170">This policy setting allows to define a list of Kiosk profiles for a Kiosk configuration.</span></span> <span data-ttu-id="39bca-171">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="39bca-171">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="39bca-172">kioskBrowserDefaultUrl</span><span class="sxs-lookup"><span data-stu-id="39bca-172">kioskBrowserDefaultUrl</span></span>|<span data-ttu-id="39bca-173">String</span><span class="sxs-lookup"><span data-stu-id="39bca-173">String</span></span>|<span data-ttu-id="39bca-174">Especifique la dirección URL predeterminada debería ir el explorador en Inicio.</span><span class="sxs-lookup"><span data-stu-id="39bca-174">Specify the default URL the browser should navigate to on launch.</span></span>|
|<span data-ttu-id="39bca-175">kioskBrowserEnableHomeButton</span><span class="sxs-lookup"><span data-stu-id="39bca-175">kioskBrowserEnableHomeButton</span></span>|<span data-ttu-id="39bca-176">Boolean</span><span class="sxs-lookup"><span data-stu-id="39bca-176">Boolean</span></span>|<span data-ttu-id="39bca-177">Habilitar el botón página principal del explorador de quiosco.</span><span class="sxs-lookup"><span data-stu-id="39bca-177">Enable the kiosk browser's home button.</span></span> <span data-ttu-id="39bca-178">De forma predeterminada, el botón página principal está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="39bca-178">By default, the home button is disabled.</span></span>|
|<span data-ttu-id="39bca-179">kioskBrowserEnableNavigationButtons</span><span class="sxs-lookup"><span data-stu-id="39bca-179">kioskBrowserEnableNavigationButtons</span></span>|<span data-ttu-id="39bca-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="39bca-180">Boolean</span></span>|<span data-ttu-id="39bca-181">Habilitar buttons(forward/back) de navegación del explorador de quiosco.</span><span class="sxs-lookup"><span data-stu-id="39bca-181">Enable the kiosk browser's navigation buttons(forward/back).</span></span> <span data-ttu-id="39bca-182">De forma predeterminada, se deshabilitan los botones de navegación.</span><span class="sxs-lookup"><span data-stu-id="39bca-182">By default, the navigation buttons are disabled.</span></span>|
|<span data-ttu-id="39bca-183">kioskBrowserEnableEndSessionButton</span><span class="sxs-lookup"><span data-stu-id="39bca-183">kioskBrowserEnableEndSessionButton</span></span>|<span data-ttu-id="39bca-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="39bca-184">Boolean</span></span>|<span data-ttu-id="39bca-185">Habilitar botón de sesión del explorador de quiosco final.</span><span class="sxs-lookup"><span data-stu-id="39bca-185">Enable the kiosk browser's end session button.</span></span> <span data-ttu-id="39bca-186">De forma predeterminada, el botón de la sesión de end está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="39bca-186">By default, the end session button is disabled.</span></span>|
|<span data-ttu-id="39bca-187">kioskBrowserRestartOnIdleTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="39bca-187">kioskBrowserRestartOnIdleTimeInMinutes</span></span>|<span data-ttu-id="39bca-188">Int32</span><span class="sxs-lookup"><span data-stu-id="39bca-188">Int32</span></span>|<span data-ttu-id="39bca-189">Especifique el número de minutos que la sesión está inactiva hasta que se reinicie el Explorador de quiosco en un estado actualizado.</span><span class="sxs-lookup"><span data-stu-id="39bca-189">Specify the number of minutes the session is idle until the kiosk browser restarts in a fresh state.</span></span>  <span data-ttu-id="39bca-190">Los valores válidos son 1 1440.</span><span class="sxs-lookup"><span data-stu-id="39bca-190">Valid values are 1-1440.</span></span> <span data-ttu-id="39bca-191">Valores válidos 1 y 1440.</span><span class="sxs-lookup"><span data-stu-id="39bca-191">Valid values 1 to 1440</span></span>|
|<span data-ttu-id="39bca-192">kioskBrowserBlockedURLs</span><span class="sxs-lookup"><span data-stu-id="39bca-192">kioskBrowserBlockedURLs</span></span>|<span data-ttu-id="39bca-193">Colección String</span><span class="sxs-lookup"><span data-stu-id="39bca-193">String collection</span></span>|<span data-ttu-id="39bca-194">Especificar las direcciones URL que los exploradores de Quiosco no deberían ir a</span><span class="sxs-lookup"><span data-stu-id="39bca-194">Specify URLs that the kiosk browsers should not navigate to</span></span>|
|<span data-ttu-id="39bca-195">kioskBrowserBlockedUrlExceptions</span><span class="sxs-lookup"><span data-stu-id="39bca-195">kioskBrowserBlockedUrlExceptions</span></span>|<span data-ttu-id="39bca-196">Colección String</span><span class="sxs-lookup"><span data-stu-id="39bca-196">String collection</span></span>|<span data-ttu-id="39bca-197">Especificar las direcciones URL que se permite el Explorador de quiosco para navegar a</span><span class="sxs-lookup"><span data-stu-id="39bca-197">Specify URLs that the kiosk browser is allowed to navigate to</span></span>|



## <a name="response"></a><span data-ttu-id="39bca-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39bca-198">Response</span></span>
<span data-ttu-id="39bca-199">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="39bca-199">If successful, this method returns a `201 Created` response code and a [windowsKioskConfiguration](../resources/intune-deviceconfig-windowskioskconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="39bca-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="39bca-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="39bca-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="39bca-201">Request</span></span>
<span data-ttu-id="39bca-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="39bca-202">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1662

{
  "@odata.type": "#microsoft.graph.windowsKioskConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "kioskProfiles": [
    {
      "@odata.type": "microsoft.graph.windowsKioskProfile",
      "profileId": "Profile Id value",
      "profileName": "Profile Name value",
      "appConfiguration": {
        "@odata.type": "microsoft.graph.windowsKioskMultipleApps",
        "apps": [
          {
            "@odata.type": "microsoft.graph.windowsKioskUWPApp",
            "startLayoutTileSize": "small",
            "name": "Name value",
            "appUserModelId": "App User Model Id value",
            "appId": "App Id value",
            "containedAppId": "Contained App Id value"
          }
        ],
        "showTaskBar": true,
        "disallowDesktopApps": true,
        "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
      },
      "userAccountsConfiguration": [
        {
          "@odata.type": "microsoft.graph.windowsKioskVisitor"
        }
      ]
    }
  ],
  "kioskBrowserDefaultUrl": "https://example.com/kioskBrowserDefaultUrl/",
  "kioskBrowserEnableHomeButton": true,
  "kioskBrowserEnableNavigationButtons": true,
  "kioskBrowserEnableEndSessionButton": true,
  "kioskBrowserRestartOnIdleTimeInMinutes": 6,
  "kioskBrowserBlockedURLs": [
    "Kiosk Browser Blocked URLs value"
  ],
  "kioskBrowserBlockedUrlExceptions": [
    "Kiosk Browser Blocked Url Exceptions value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="39bca-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="39bca-203">Response</span></span>
<span data-ttu-id="39bca-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="39bca-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1770

{
  "@odata.type": "#microsoft.graph.windowsKioskConfiguration",
  "id": "146a990b-990b-146a-0b99-6a140b996a14",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "kioskProfiles": [
    {
      "@odata.type": "microsoft.graph.windowsKioskProfile",
      "profileId": "Profile Id value",
      "profileName": "Profile Name value",
      "appConfiguration": {
        "@odata.type": "microsoft.graph.windowsKioskMultipleApps",
        "apps": [
          {
            "@odata.type": "microsoft.graph.windowsKioskUWPApp",
            "startLayoutTileSize": "small",
            "name": "Name value",
            "appUserModelId": "App User Model Id value",
            "appId": "App Id value",
            "containedAppId": "Contained App Id value"
          }
        ],
        "showTaskBar": true,
        "disallowDesktopApps": true,
        "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s"
      },
      "userAccountsConfiguration": [
        {
          "@odata.type": "microsoft.graph.windowsKioskVisitor"
        }
      ]
    }
  ],
  "kioskBrowserDefaultUrl": "https://example.com/kioskBrowserDefaultUrl/",
  "kioskBrowserEnableHomeButton": true,
  "kioskBrowserEnableNavigationButtons": true,
  "kioskBrowserEnableEndSessionButton": true,
  "kioskBrowserRestartOnIdleTimeInMinutes": 6,
  "kioskBrowserBlockedURLs": [
    "Kiosk Browser Blocked URLs value"
  ],
  "kioskBrowserBlockedUrlExceptions": [
    "Kiosk Browser Blocked Url Exceptions value"
  ]
}
```





