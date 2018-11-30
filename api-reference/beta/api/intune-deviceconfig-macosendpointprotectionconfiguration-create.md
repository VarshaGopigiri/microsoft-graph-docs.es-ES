---
title: Crear macOSEndpointProtectionConfiguration
description: Crear un nuevo objeto macOSEndpointProtectionConfiguration.
ms.openlocfilehash: 9f34936359cb3bee08a3427669bc1bc0c2fb7ac2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087765"
---
# <a name="create-macosendpointprotectionconfiguration"></a><span data-ttu-id="5f435-103">Crear macOSEndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f435-103">Create macOSEndpointProtectionConfiguration</span></span>

> <span data-ttu-id="5f435-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f435-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f435-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f435-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5f435-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5f435-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f435-107">Crear un nuevo objeto [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="5f435-107">Create a new [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f435-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5f435-108">Prerequisites</span></span>
<span data-ttu-id="5f435-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f435-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5f435-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f435-111">Permission type</span></span>|<span data-ttu-id="5f435-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f435-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f435-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f435-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5f435-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f435-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5f435-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f435-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f435-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f435-116">Not supported.</span></span>|
|<span data-ttu-id="5f435-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f435-117">Application</span></span>|<span data-ttu-id="5f435-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f435-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f435-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f435-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="5f435-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f435-120">Request headers</span></span>
|<span data-ttu-id="5f435-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f435-121">Header</span></span>|<span data-ttu-id="5f435-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5f435-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f435-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f435-123">Authorization</span></span>|<span data-ttu-id="5f435-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5f435-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5f435-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5f435-125">Accept</span></span>|<span data-ttu-id="5f435-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5f435-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f435-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5f435-127">Request body</span></span>
<span data-ttu-id="5f435-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto macOSEndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f435-128">In the request body, supply a JSON representation for the macOSEndpointProtectionConfiguration object.</span></span>

<span data-ttu-id="5f435-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el macOSEndpointProtectionConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f435-129">The following table shows the properties that are required when you create the macOSEndpointProtectionConfiguration.</span></span>

|<span data-ttu-id="5f435-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f435-130">Property</span></span>|<span data-ttu-id="5f435-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f435-131">Type</span></span>|<span data-ttu-id="5f435-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f435-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f435-133">id</span><span class="sxs-lookup"><span data-stu-id="5f435-133">id</span></span>|<span data-ttu-id="5f435-134">String</span><span class="sxs-lookup"><span data-stu-id="5f435-134">String</span></span>|<span data-ttu-id="5f435-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5f435-135">Key of the entity.</span></span> <span data-ttu-id="5f435-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5f435-137">lastModifiedDateTime</span></span>|<span data-ttu-id="5f435-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f435-138">DateTimeOffset</span></span>|<span data-ttu-id="5f435-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="5f435-139">DateTime the object was last modified.</span></span> <span data-ttu-id="5f435-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="5f435-141">roleScopeTagIds</span></span>|<span data-ttu-id="5f435-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="5f435-142">String collection</span></span>|<span data-ttu-id="5f435-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="5f435-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="5f435-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="5f435-145">supportsScopeTags</span></span>|<span data-ttu-id="5f435-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f435-146">Boolean</span></span>|<span data-ttu-id="5f435-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5f435-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="5f435-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="5f435-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="5f435-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="5f435-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="5f435-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f435-150">This property is read-only.</span></span> <span data-ttu-id="5f435-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5f435-152">createdDateTime</span></span>|<span data-ttu-id="5f435-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f435-153">DateTimeOffset</span></span>|<span data-ttu-id="5f435-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="5f435-154">DateTime the object was created.</span></span> <span data-ttu-id="5f435-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-156">descripción</span><span class="sxs-lookup"><span data-stu-id="5f435-156">description</span></span>|<span data-ttu-id="5f435-157">String</span><span class="sxs-lookup"><span data-stu-id="5f435-157">String</span></span>|<span data-ttu-id="5f435-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f435-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="5f435-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-160">displayName</span><span class="sxs-lookup"><span data-stu-id="5f435-160">displayName</span></span>|<span data-ttu-id="5f435-161">String</span><span class="sxs-lookup"><span data-stu-id="5f435-161">String</span></span>|<span data-ttu-id="5f435-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f435-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="5f435-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-164">version</span><span class="sxs-lookup"><span data-stu-id="5f435-164">version</span></span>|<span data-ttu-id="5f435-165">Int32</span><span class="sxs-lookup"><span data-stu-id="5f435-165">Int32</span></span>|<span data-ttu-id="5f435-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f435-166">Version of the device configuration.</span></span> <span data-ttu-id="5f435-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="5f435-168">gatekeeperAllowedAppSource</span><span class="sxs-lookup"><span data-stu-id="5f435-168">gatekeeperAllowedAppSource</span></span>|[<span data-ttu-id="5f435-169">macOSGatekeeperAppSources</span><span class="sxs-lookup"><span data-stu-id="5f435-169">macOSGatekeeperAppSources</span></span>](../resources/intune-deviceconfig-macosgatekeeperappsources.md)|<span data-ttu-id="5f435-170">Del sistema y la configuración de privacidad que determina qué aplicaciones de ubicaciones de descarga se pueden ejecutar desde un dispositivo de Mac OS.</span><span class="sxs-lookup"><span data-stu-id="5f435-170">System and Privacy setting that determines which download locations apps can be run from on a macOS device.</span></span> <span data-ttu-id="5f435-171">Los valores posibles son: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers` y `anywhere`.</span><span class="sxs-lookup"><span data-stu-id="5f435-171">Possible values are: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers`, `anywhere`.</span></span>|
|<span data-ttu-id="5f435-172">gatekeeperBlockOverride</span><span class="sxs-lookup"><span data-stu-id="5f435-172">gatekeeperBlockOverride</span></span>|<span data-ttu-id="5f435-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f435-173">Boolean</span></span>|<span data-ttu-id="5f435-174">Si se establece en true, el usuario anular para se deshabilitará el equipo selector.</span><span class="sxs-lookup"><span data-stu-id="5f435-174">If set to true, the user override for Gatekeeper will be disabled.</span></span>|
|<span data-ttu-id="5f435-175">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="5f435-175">firewallEnabled</span></span>|<span data-ttu-id="5f435-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f435-176">Boolean</span></span>|<span data-ttu-id="5f435-177">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="5f435-177">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="5f435-178">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="5f435-178">firewallBlockAllIncoming</span></span>|<span data-ttu-id="5f435-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f435-179">Boolean</span></span>|<span data-ttu-id="5f435-180">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="5f435-180">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="5f435-181">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="5f435-181">firewallEnableStealthMode</span></span>|<span data-ttu-id="5f435-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="5f435-182">Boolean</span></span>|<span data-ttu-id="5f435-183">Corresponde a "Habilitar modo silencioso".</span><span class="sxs-lookup"><span data-stu-id="5f435-183">Corresponds to “Enable stealth mode.”</span></span>|
|<span data-ttu-id="5f435-184">firewallApplications</span><span class="sxs-lookup"><span data-stu-id="5f435-184">firewallApplications</span></span>|<span data-ttu-id="5f435-185">colección de [macOSFirewallApplication](../resources/intune-deviceconfig-macosfirewallapplication.md)</span><span class="sxs-lookup"><span data-stu-id="5f435-185">[macOSFirewallApplication](../resources/intune-deviceconfig-macosfirewallapplication.md) collection</span></span>|<span data-ttu-id="5f435-186">Lista de aplicaciones con la configuración de firewall.</span><span class="sxs-lookup"><span data-stu-id="5f435-186">List of applications with firewall settings.</span></span> <span data-ttu-id="5f435-187">Configuración de Firewall para aplicaciones en esta lista no se determina por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5f435-187">Firewall settings for applications not on this list are determined by the user.</span></span> <span data-ttu-id="5f435-188">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="5f435-188">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="5f435-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f435-189">Response</span></span>
<span data-ttu-id="5f435-190">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f435-190">If successful, this method returns a `201 Created` response code and a [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f435-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f435-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f435-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f435-192">Request</span></span>
<span data-ttu-id="5f435-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f435-193">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 711

{
  "@odata.type": "#microsoft.graph.macOSEndpointProtectionConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "gatekeeperAllowedAppSource": "macAppStore",
  "gatekeeperBlockOverride": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true,
  "firewallApplications": [
    {
      "@odata.type": "microsoft.graph.macOSFirewallApplication",
      "bundleId": "Bundle Id value",
      "allowsIncomingConnections": true
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="5f435-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f435-194">Response</span></span>
<span data-ttu-id="5f435-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5f435-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 819

{
  "@odata.type": "#microsoft.graph.macOSEndpointProtectionConfiguration",
  "id": "7bf7f3ca-f3ca-7bf7-caf3-f77bcaf3f77b",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "gatekeeperAllowedAppSource": "macAppStore",
  "gatekeeperBlockOverride": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true,
  "firewallApplications": [
    {
      "@odata.type": "microsoft.graph.macOSFirewallApplication",
      "bundleId": "Bundle Id value",
      "allowsIncomingConnections": true
    }
  ]
}
```




