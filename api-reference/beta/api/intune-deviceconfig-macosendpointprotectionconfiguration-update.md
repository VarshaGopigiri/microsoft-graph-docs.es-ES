---
title: Actualizar macOSEndpointProtectionConfiguration
description: Actualizar las propiedades de un objeto macOSEndpointProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6a9f2c5a1523b934258734befb7e5bea5955e4bc
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967913"
---
# <a name="update-macosendpointprotectionconfiguration"></a><span data-ttu-id="46d82-103">Actualizar macOSEndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="46d82-103">Update macOSEndpointProtectionConfiguration</span></span>

> <span data-ttu-id="46d82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="46d82-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46d82-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="46d82-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="46d82-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="46d82-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46d82-107">Actualizar las propiedades de un objeto [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="46d82-107">Update the properties of a [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46d82-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="46d82-108">Prerequisites</span></span>
<span data-ttu-id="46d82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="46d82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="46d82-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="46d82-111">Permission type</span></span>|<span data-ttu-id="46d82-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="46d82-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46d82-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="46d82-113">Delegated (work or school account)</span></span>|<span data-ttu-id="46d82-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46d82-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="46d82-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="46d82-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46d82-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46d82-116">Not supported.</span></span>|
|<span data-ttu-id="46d82-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="46d82-117">Application</span></span>|<span data-ttu-id="46d82-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="46d82-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46d82-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="46d82-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="46d82-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="46d82-120">Request headers</span></span>
|<span data-ttu-id="46d82-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46d82-121">Header</span></span>|<span data-ttu-id="46d82-122">Valor</span><span class="sxs-lookup"><span data-stu-id="46d82-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46d82-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="46d82-123">Authorization</span></span>|<span data-ttu-id="46d82-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="46d82-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="46d82-125">Accept</span><span class="sxs-lookup"><span data-stu-id="46d82-125">Accept</span></span>|<span data-ttu-id="46d82-126">application/json</span><span class="sxs-lookup"><span data-stu-id="46d82-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46d82-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="46d82-127">Request body</span></span>
<span data-ttu-id="46d82-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="46d82-128">In the request body, supply a JSON representation for the [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) object.</span></span>

<span data-ttu-id="46d82-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="46d82-129">The following table shows the properties that are required when you create the [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md).</span></span>

|<span data-ttu-id="46d82-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46d82-130">Property</span></span>|<span data-ttu-id="46d82-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="46d82-131">Type</span></span>|<span data-ttu-id="46d82-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="46d82-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46d82-133">id</span><span class="sxs-lookup"><span data-stu-id="46d82-133">id</span></span>|<span data-ttu-id="46d82-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="46d82-134">String</span></span>|<span data-ttu-id="46d82-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="46d82-135">Key of the entity.</span></span> <span data-ttu-id="46d82-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="46d82-137">lastModifiedDateTime</span></span>|<span data-ttu-id="46d82-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46d82-138">DateTimeOffset</span></span>|<span data-ttu-id="46d82-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="46d82-139">DateTime the object was last modified.</span></span> <span data-ttu-id="46d82-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="46d82-141">roleScopeTagIds</span></span>|<span data-ttu-id="46d82-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="46d82-142">String collection</span></span>|<span data-ttu-id="46d82-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="46d82-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="46d82-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="46d82-145">supportsScopeTags</span></span>|<span data-ttu-id="46d82-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="46d82-146">Boolean</span></span>|<span data-ttu-id="46d82-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d82-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="46d82-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="46d82-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="46d82-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="46d82-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="46d82-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="46d82-150">This property is read-only.</span></span> <span data-ttu-id="46d82-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46d82-152">createdDateTime</span></span>|<span data-ttu-id="46d82-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46d82-153">DateTimeOffset</span></span>|<span data-ttu-id="46d82-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="46d82-154">DateTime the object was created.</span></span> <span data-ttu-id="46d82-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-156">descripción</span><span class="sxs-lookup"><span data-stu-id="46d82-156">description</span></span>|<span data-ttu-id="46d82-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="46d82-157">String</span></span>|<span data-ttu-id="46d82-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46d82-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="46d82-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-160">displayName</span><span class="sxs-lookup"><span data-stu-id="46d82-160">displayName</span></span>|<span data-ttu-id="46d82-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="46d82-161">String</span></span>|<span data-ttu-id="46d82-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46d82-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="46d82-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-164">version</span><span class="sxs-lookup"><span data-stu-id="46d82-164">version</span></span>|<span data-ttu-id="46d82-165">Int32</span><span class="sxs-lookup"><span data-stu-id="46d82-165">Int32</span></span>|<span data-ttu-id="46d82-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46d82-166">Version of the device configuration.</span></span> <span data-ttu-id="46d82-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46d82-168">gatekeeperAllowedAppSource</span><span class="sxs-lookup"><span data-stu-id="46d82-168">gatekeeperAllowedAppSource</span></span>|[<span data-ttu-id="46d82-169">macOSGatekeeperAppSources</span><span class="sxs-lookup"><span data-stu-id="46d82-169">macOSGatekeeperAppSources</span></span>](../resources/intune-deviceconfig-macosgatekeeperappsources.md)|<span data-ttu-id="46d82-170">Del sistema y la configuración de privacidad que determina qué aplicaciones de ubicaciones de descarga se pueden ejecutar desde un dispositivo de Mac OS.</span><span class="sxs-lookup"><span data-stu-id="46d82-170">System and Privacy setting that determines which download locations apps can be run from on a macOS device.</span></span> <span data-ttu-id="46d82-171">Los valores posibles son: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers` y `anywhere`.</span><span class="sxs-lookup"><span data-stu-id="46d82-171">Possible values are: `notConfigured`, `macAppStore`, `macAppStoreAndIdentifiedDevelopers`, `anywhere`.</span></span>|
|<span data-ttu-id="46d82-172">gatekeeperBlockOverride</span><span class="sxs-lookup"><span data-stu-id="46d82-172">gatekeeperBlockOverride</span></span>|<span data-ttu-id="46d82-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="46d82-173">Boolean</span></span>|<span data-ttu-id="46d82-174">Si se establece en true, el usuario anular para se deshabilitará el equipo selector.</span><span class="sxs-lookup"><span data-stu-id="46d82-174">If set to true, the user override for Gatekeeper will be disabled.</span></span>|
|<span data-ttu-id="46d82-175">firewallEnabled</span><span class="sxs-lookup"><span data-stu-id="46d82-175">firewallEnabled</span></span>|<span data-ttu-id="46d82-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="46d82-176">Boolean</span></span>|<span data-ttu-id="46d82-177">Si el firewall se debe habilitar o no.</span><span class="sxs-lookup"><span data-stu-id="46d82-177">Whether the firewall should be enabled or not.</span></span>|
|<span data-ttu-id="46d82-178">firewallBlockAllIncoming</span><span class="sxs-lookup"><span data-stu-id="46d82-178">firewallBlockAllIncoming</span></span>|<span data-ttu-id="46d82-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="46d82-179">Boolean</span></span>|<span data-ttu-id="46d82-180">Corresponde a la opción "Bloquear todas las conexiones entrantes".</span><span class="sxs-lookup"><span data-stu-id="46d82-180">Corresponds to the “Block all incoming connections” option.</span></span>|
|<span data-ttu-id="46d82-181">firewallEnableStealthMode</span><span class="sxs-lookup"><span data-stu-id="46d82-181">firewallEnableStealthMode</span></span>|<span data-ttu-id="46d82-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="46d82-182">Boolean</span></span>|<span data-ttu-id="46d82-183">Corresponde a "Habilitar modo silencioso".</span><span class="sxs-lookup"><span data-stu-id="46d82-183">Corresponds to “Enable stealth mode.”</span></span>|
|<span data-ttu-id="46d82-184">firewallApplications</span><span class="sxs-lookup"><span data-stu-id="46d82-184">firewallApplications</span></span>|<span data-ttu-id="46d82-185">colección de [macOSFirewallApplication](../resources/intune-deviceconfig-macosfirewallapplication.md)</span><span class="sxs-lookup"><span data-stu-id="46d82-185">[macOSFirewallApplication](../resources/intune-deviceconfig-macosfirewallapplication.md) collection</span></span>|<span data-ttu-id="46d82-186">Lista de aplicaciones con la configuración de firewall.</span><span class="sxs-lookup"><span data-stu-id="46d82-186">List of applications with firewall settings.</span></span> <span data-ttu-id="46d82-187">Configuración de Firewall para aplicaciones en esta lista no se determina por el usuario.</span><span class="sxs-lookup"><span data-stu-id="46d82-187">Firewall settings for applications not on this list are determined by the user.</span></span> <span data-ttu-id="46d82-188">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="46d82-188">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="46d82-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46d82-189">Response</span></span>
<span data-ttu-id="46d82-190">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="46d82-190">If successful, this method returns a `200 OK` response code and an updated [macOSEndpointProtectionConfiguration](../resources/intune-deviceconfig-macosendpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46d82-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="46d82-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="46d82-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="46d82-192">Request</span></span>
<span data-ttu-id="46d82-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46d82-193">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 636

{
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

### <a name="response"></a><span data-ttu-id="46d82-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="46d82-194">Response</span></span>
<span data-ttu-id="46d82-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="46d82-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





