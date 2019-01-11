---
title: Actualizar androidVpnConfiguration
description: Actualizar las propiedades de un objeto androidVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 6ad88fff142a6c4b3827135a31a80171687a3940
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812631"
---
# <a name="update-androidvpnconfiguration"></a><span data-ttu-id="d1b94-103">Actualizar androidVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1b94-103">Update androidVpnConfiguration</span></span>

> <span data-ttu-id="d1b94-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1b94-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1b94-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1b94-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d1b94-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d1b94-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d1b94-107">Actualizar las propiedades de un objeto [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b94-107">Update the properties of a [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d1b94-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d1b94-108">Prerequisites</span></span>
<span data-ttu-id="d1b94-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d1b94-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d1b94-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d1b94-111">Permission type</span></span>|<span data-ttu-id="d1b94-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d1b94-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d1b94-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d1b94-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d1b94-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d1b94-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d1b94-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d1b94-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d1b94-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1b94-116">Not supported.</span></span>|
|<span data-ttu-id="d1b94-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d1b94-117">Application</span></span>|<span data-ttu-id="d1b94-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d1b94-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d1b94-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d1b94-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="d1b94-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b94-120">Request headers</span></span>
|<span data-ttu-id="d1b94-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1b94-121">Header</span></span>|<span data-ttu-id="d1b94-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d1b94-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d1b94-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d1b94-123">Authorization</span></span>|<span data-ttu-id="d1b94-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d1b94-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d1b94-125">Accept</span><span class="sxs-lookup"><span data-stu-id="d1b94-125">Accept</span></span>|<span data-ttu-id="d1b94-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d1b94-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d1b94-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b94-127">Request body</span></span>
<span data-ttu-id="d1b94-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b94-128">In the request body, supply a JSON representation for the [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) object.</span></span>

<span data-ttu-id="d1b94-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d1b94-129">The following table shows the properties that are required when you create the [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md).</span></span>

|<span data-ttu-id="d1b94-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1b94-130">Property</span></span>|<span data-ttu-id="d1b94-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1b94-131">Type</span></span>|<span data-ttu-id="d1b94-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1b94-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d1b94-133">id</span><span class="sxs-lookup"><span data-stu-id="d1b94-133">id</span></span>|<span data-ttu-id="d1b94-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-134">String</span></span>|<span data-ttu-id="d1b94-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d1b94-135">Key of the entity.</span></span> <span data-ttu-id="d1b94-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d1b94-137">lastModifiedDateTime</span></span>|<span data-ttu-id="d1b94-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d1b94-138">DateTimeOffset</span></span>|<span data-ttu-id="d1b94-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d1b94-139">DateTime the object was last modified.</span></span> <span data-ttu-id="d1b94-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d1b94-141">roleScopeTagIds</span></span>|<span data-ttu-id="d1b94-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="d1b94-142">String collection</span></span>|<span data-ttu-id="d1b94-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="d1b94-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="d1b94-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="d1b94-145">supportsScopeTags</span></span>|<span data-ttu-id="d1b94-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="d1b94-146">Boolean</span></span>|<span data-ttu-id="d1b94-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d1b94-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="d1b94-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="d1b94-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="d1b94-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b94-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="d1b94-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1b94-150">This property is read-only.</span></span> <span data-ttu-id="d1b94-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d1b94-152">createdDateTime</span></span>|<span data-ttu-id="d1b94-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d1b94-153">DateTimeOffset</span></span>|<span data-ttu-id="d1b94-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d1b94-154">DateTime the object was created.</span></span> <span data-ttu-id="d1b94-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-156">descripción</span><span class="sxs-lookup"><span data-stu-id="d1b94-156">description</span></span>|<span data-ttu-id="d1b94-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-157">String</span></span>|<span data-ttu-id="d1b94-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1b94-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d1b94-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-160">displayName</span><span class="sxs-lookup"><span data-stu-id="d1b94-160">displayName</span></span>|<span data-ttu-id="d1b94-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-161">String</span></span>|<span data-ttu-id="d1b94-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1b94-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d1b94-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-164">version</span><span class="sxs-lookup"><span data-stu-id="d1b94-164">version</span></span>|<span data-ttu-id="d1b94-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d1b94-165">Int32</span></span>|<span data-ttu-id="d1b94-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1b94-166">Version of the device configuration.</span></span> <span data-ttu-id="d1b94-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d1b94-168">connectionName</span><span class="sxs-lookup"><span data-stu-id="d1b94-168">connectionName</span></span>|<span data-ttu-id="d1b94-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-169">String</span></span>|<span data-ttu-id="d1b94-170">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="d1b94-170">Connection name displayed to the user.</span></span>|
|<span data-ttu-id="d1b94-171">connectionType</span><span class="sxs-lookup"><span data-stu-id="d1b94-171">connectionType</span></span>|[<span data-ttu-id="d1b94-172">androidVpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="d1b94-172">androidVpnConnectionType</span></span>](../resources/intune-deviceconfig-androidvpnconnectiontype.md)|<span data-ttu-id="d1b94-173">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="d1b94-173">Connection type.</span></span> <span data-ttu-id="d1b94-174">Los valores posibles son: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `citrix`.</span><span class="sxs-lookup"><span data-stu-id="d1b94-174">Possible values are: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `citrix`.</span></span>|
|<span data-ttu-id="d1b94-175">role</span><span class="sxs-lookup"><span data-stu-id="d1b94-175">role</span></span>|<span data-ttu-id="d1b94-176">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-176">String</span></span>|<span data-ttu-id="d1b94-177">Función de tipo de conexión se establece en impulsos seguro.</span><span class="sxs-lookup"><span data-stu-id="d1b94-177">Role when connection type is set to Pulse Secure.</span></span>|
|<span data-ttu-id="d1b94-178">dominio kerberos</span><span class="sxs-lookup"><span data-stu-id="d1b94-178">realm</span></span>|<span data-ttu-id="d1b94-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-179">String</span></span>|<span data-ttu-id="d1b94-180">Dominio Kerberos cuando se establece el tipo de conexión a impulsos seguro.</span><span class="sxs-lookup"><span data-stu-id="d1b94-180">Realm when connection type is set to Pulse Secure.</span></span>|
|<span data-ttu-id="d1b94-181">servidores</span><span class="sxs-lookup"><span data-stu-id="d1b94-181">servers</span></span>|<span data-ttu-id="d1b94-182">colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-182">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="d1b94-183">Lista de servidores VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="d1b94-183">List of VPN Servers on the network.</span></span> <span data-ttu-id="d1b94-184">Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="d1b94-184">Make sure end users can access these network locations.</span></span> <span data-ttu-id="d1b94-185">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="d1b94-185">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="d1b94-186">huella digital</span><span class="sxs-lookup"><span data-stu-id="d1b94-186">fingerprint</span></span>|<span data-ttu-id="d1b94-187">Cadena</span><span class="sxs-lookup"><span data-stu-id="d1b94-187">String</span></span>|<span data-ttu-id="d1b94-188">Huella es una cadena que se usará para comprobar el servidor VPN puede ser de confianza, que sólo es aplicable al tipo de conexión es VPN Check Point con cápsula.</span><span class="sxs-lookup"><span data-stu-id="d1b94-188">Fingerprint is a string that will be used to verify the VPN server can be trusted, which is only applicable when connection type is Check Point Capsule VPN.</span></span>|
|<span data-ttu-id="d1b94-189">customData</span><span class="sxs-lookup"><span data-stu-id="d1b94-189">customData</span></span>|<span data-ttu-id="d1b94-190">colección [keyValue](../resources/intune-deviceconfig-keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-190">[keyValue](../resources/intune-deviceconfig-keyvalue.md) collection</span></span>|<span data-ttu-id="d1b94-191">Datos personalizados al tipo de conexión se establece en Citrix.</span><span class="sxs-lookup"><span data-stu-id="d1b94-191">Custom data when connection type is set to Citrix.</span></span> <span data-ttu-id="d1b94-192">Esta colección puede contener un máximo de 25 elementos.</span><span class="sxs-lookup"><span data-stu-id="d1b94-192">This collection can contain a maximum of 25 elements.</span></span>|
|<span data-ttu-id="d1b94-193">customKeyValueData</span><span class="sxs-lookup"><span data-stu-id="d1b94-193">customKeyValueData</span></span>|<span data-ttu-id="d1b94-194">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="d1b94-194">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="d1b94-195">Datos personalizados al tipo de conexión se establece en Citrix.</span><span class="sxs-lookup"><span data-stu-id="d1b94-195">Custom data when connection type is set to Citrix.</span></span> <span data-ttu-id="d1b94-196">Esta colección puede contener un máximo de 25 elementos.</span><span class="sxs-lookup"><span data-stu-id="d1b94-196">This collection can contain a maximum of 25 elements.</span></span>|
|<span data-ttu-id="d1b94-197">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d1b94-197">authenticationMethod</span></span>|[<span data-ttu-id="d1b94-198">vpnAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d1b94-198">vpnAuthenticationMethod</span></span>](../resources/intune-deviceconfig-vpnauthenticationmethod.md)|<span data-ttu-id="d1b94-199">Método de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d1b94-199">Authentication method.</span></span> <span data-ttu-id="d1b94-200">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="d1b94-200">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|



## <a name="response"></a><span data-ttu-id="d1b94-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1b94-201">Response</span></span>
<span data-ttu-id="d1b94-202">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d1b94-202">If successful, this method returns a `200 OK` response code and an updated [androidVpnConfiguration](../resources/intune-deviceconfig-androidvpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d1b94-203">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1b94-203">Example</span></span>
### <a name="request"></a><span data-ttu-id="d1b94-204">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d1b94-204">Request</span></span>
<span data-ttu-id="d1b94-205">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d1b94-205">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 980

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "connectionName": "Connection Name value",
  "connectionType": "pulseSecure",
  "role": "Role value",
  "realm": "Realm value",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "fingerprint": "Fingerprint value",
  "customData": [
    {
      "@odata.type": "microsoft.graph.keyValue",
      "key": "Key value",
      "value": "Value value"
    }
  ],
  "customKeyValueData": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "authenticationMethod": "usernameAndPassword"
}
```

### <a name="response"></a><span data-ttu-id="d1b94-206">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d1b94-206">Response</span></span>
<span data-ttu-id="d1b94-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d1b94-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1150

{
  "@odata.type": "#microsoft.graph.androidVpnConfiguration",
  "id": "d4c48852-8852-d4c4-5288-c4d45288c4d4",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "connectionName": "Connection Name value",
  "connectionType": "pulseSecure",
  "role": "Role value",
  "realm": "Realm value",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "fingerprint": "Fingerprint value",
  "customData": [
    {
      "@odata.type": "microsoft.graph.keyValue",
      "key": "Key value",
      "value": "Value value"
    }
  ],
  "customKeyValueData": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "Name value",
      "value": "Value value"
    }
  ],
  "authenticationMethod": "usernameAndPassword"
}
```





