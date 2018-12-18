---
title: Actualizar windows10VpnConfiguration
description: Actualizar las propiedades de un objeto windows10VpnConfiguration.
author: tfitzmac
ms.openlocfilehash: 24112120dd414bc7929d9223094b528b32ad818a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27305071"
---
# <a name="update-windows10vpnconfiguration"></a><span data-ttu-id="d92a8-103">Actualizar windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="d92a8-103">Update windows10VpnConfiguration</span></span>

> <span data-ttu-id="d92a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d92a8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d92a8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d92a8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d92a8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d92a8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d92a8-107">Actualizar las propiedades de un objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d92a8-107">Update the properties of a [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d92a8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d92a8-108">Prerequisites</span></span>
<span data-ttu-id="d92a8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d92a8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d92a8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d92a8-111">Permission type</span></span>|<span data-ttu-id="d92a8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d92a8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d92a8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d92a8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d92a8-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d92a8-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="d92a8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d92a8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d92a8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d92a8-116">Not supported.</span></span>|
|<span data-ttu-id="d92a8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d92a8-117">Application</span></span>|<span data-ttu-id="d92a8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d92a8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d92a8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d92a8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="d92a8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d92a8-120">Request headers</span></span>
|<span data-ttu-id="d92a8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d92a8-121">Header</span></span>|<span data-ttu-id="d92a8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d92a8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d92a8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d92a8-123">Authorization</span></span>|<span data-ttu-id="d92a8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d92a8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d92a8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d92a8-125">Accept</span></span>|<span data-ttu-id="d92a8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d92a8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d92a8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d92a8-127">Request body</span></span>
<span data-ttu-id="d92a8-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="d92a8-128">In the request body, supply a JSON representation for the [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>

<span data-ttu-id="d92a8-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="d92a8-129">The following table shows the properties that are required when you create the [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md).</span></span>

|<span data-ttu-id="d92a8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d92a8-130">Property</span></span>|<span data-ttu-id="d92a8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d92a8-131">Type</span></span>|<span data-ttu-id="d92a8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d92a8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d92a8-133">id</span><span class="sxs-lookup"><span data-stu-id="d92a8-133">id</span></span>|<span data-ttu-id="d92a8-134">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-134">String</span></span>|<span data-ttu-id="d92a8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="d92a8-135">Key of the entity.</span></span> <span data-ttu-id="d92a8-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d92a8-137">lastModifiedDateTime</span></span>|<span data-ttu-id="d92a8-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d92a8-138">DateTimeOffset</span></span>|<span data-ttu-id="d92a8-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="d92a8-139">DateTime the object was last modified.</span></span> <span data-ttu-id="d92a8-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d92a8-141">roleScopeTagIds</span></span>|<span data-ttu-id="d92a8-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="d92a8-142">String collection</span></span>|<span data-ttu-id="d92a8-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="d92a8-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="d92a8-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="d92a8-145">supportsScopeTags</span></span>|<span data-ttu-id="d92a8-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-146">Boolean</span></span>|<span data-ttu-id="d92a8-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d92a8-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="d92a8-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="d92a8-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="d92a8-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="d92a8-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="d92a8-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="d92a8-150">This property is read-only.</span></span> <span data-ttu-id="d92a8-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d92a8-152">createdDateTime</span></span>|<span data-ttu-id="d92a8-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d92a8-153">DateTimeOffset</span></span>|<span data-ttu-id="d92a8-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="d92a8-154">DateTime the object was created.</span></span> <span data-ttu-id="d92a8-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-156">descripción</span><span class="sxs-lookup"><span data-stu-id="d92a8-156">description</span></span>|<span data-ttu-id="d92a8-157">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-157">String</span></span>|<span data-ttu-id="d92a8-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d92a8-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="d92a8-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-160">displayName</span><span class="sxs-lookup"><span data-stu-id="d92a8-160">displayName</span></span>|<span data-ttu-id="d92a8-161">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-161">String</span></span>|<span data-ttu-id="d92a8-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d92a8-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="d92a8-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-164">version</span><span class="sxs-lookup"><span data-stu-id="d92a8-164">version</span></span>|<span data-ttu-id="d92a8-165">Int32</span><span class="sxs-lookup"><span data-stu-id="d92a8-165">Int32</span></span>|<span data-ttu-id="d92a8-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d92a8-166">Version of the device configuration.</span></span> <span data-ttu-id="d92a8-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-168">connectionName</span><span class="sxs-lookup"><span data-stu-id="d92a8-168">connectionName</span></span>|<span data-ttu-id="d92a8-169">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-169">String</span></span>|<span data-ttu-id="d92a8-170">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="d92a8-170">Connection name displayed to the user.</span></span> <span data-ttu-id="d92a8-171">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-171">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-172">servidores</span><span class="sxs-lookup"><span data-stu-id="d92a8-172">servers</span></span>|<span data-ttu-id="d92a8-173">colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-173">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="d92a8-174">Lista de servidores VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="d92a8-174">List of VPN Servers on the network.</span></span> <span data-ttu-id="d92a8-175">Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="d92a8-175">Make sure end users can access these network locations.</span></span> <span data-ttu-id="d92a8-176">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-176">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="d92a8-177">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-177">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-178">customXml</span><span class="sxs-lookup"><span data-stu-id="d92a8-178">customXml</span></span>|<span data-ttu-id="d92a8-179">Binario</span><span class="sxs-lookup"><span data-stu-id="d92a8-179">Binary</span></span>|<span data-ttu-id="d92a8-180">Comandos XML personalizados que configura la conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="d92a8-180">Custom XML commands that configures the VPN connection.</span></span> <span data-ttu-id="d92a8-181">(Matriz de bytes codificada UTF8) Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-181">(UTF8 encoded byte array) Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="d92a8-182">profileTarget</span><span class="sxs-lookup"><span data-stu-id="d92a8-182">profileTarget</span></span>|[<span data-ttu-id="d92a8-183">windows10VpnProfileTarget</span><span class="sxs-lookup"><span data-stu-id="d92a8-183">windows10VpnProfileTarget</span></span>](../resources/intune-deviceconfig-windows10vpnprofiletarget.md)|<span data-ttu-id="d92a8-184">Tipo de perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="d92a8-184">Profile target type.</span></span> <span data-ttu-id="d92a8-185">Los valores posibles son: `user`, `device` y `autoPilotDevice`.</span><span class="sxs-lookup"><span data-stu-id="d92a8-185">Possible values are: `user`, `device`, `autoPilotDevice`.</span></span>|
|<span data-ttu-id="d92a8-186">connectionType</span><span class="sxs-lookup"><span data-stu-id="d92a8-186">connectionType</span></span>|[<span data-ttu-id="d92a8-187">windows10VpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="d92a8-187">windows10VpnConnectionType</span></span>](../resources/intune-deviceconfig-windows10vpnconnectiontype.md)|<span data-ttu-id="d92a8-188">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="d92a8-188">Connection type.</span></span> <span data-ttu-id="d92a8-189">Los valores posibles son: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `automatic`, `ikEv2`, `l2tp`, `pptp`, `citrix` y `paloAltoGlobalProtect`.</span><span class="sxs-lookup"><span data-stu-id="d92a8-189">Possible values are: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `automatic`, `ikEv2`, `l2tp`, `pptp`, `citrix`, `paloAltoGlobalProtect`.</span></span>|
|<span data-ttu-id="d92a8-190">enableSplitTunneling</span><span class="sxs-lookup"><span data-stu-id="d92a8-190">enableSplitTunneling</span></span>|<span data-ttu-id="d92a8-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-191">Boolean</span></span>|<span data-ttu-id="d92a8-192">Habilitar túnel dividido.</span><span class="sxs-lookup"><span data-stu-id="d92a8-192">Enable split tunneling.</span></span>|
|<span data-ttu-id="d92a8-193">enableAlwaysOn</span><span class="sxs-lookup"><span data-stu-id="d92a8-193">enableAlwaysOn</span></span>|<span data-ttu-id="d92a8-194">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-194">Boolean</span></span>|<span data-ttu-id="d92a8-195">Habilitar siempre en el modo.</span><span class="sxs-lookup"><span data-stu-id="d92a8-195">Enable Always On mode.</span></span>|
|<span data-ttu-id="d92a8-196">enableDeviceTunnel</span><span class="sxs-lookup"><span data-stu-id="d92a8-196">enableDeviceTunnel</span></span>|<span data-ttu-id="d92a8-197">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-197">Boolean</span></span>|<span data-ttu-id="d92a8-198">Habilitar túnel de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d92a8-198">Enable device tunnel.</span></span>|
|<span data-ttu-id="d92a8-199">enableDnsRegistration</span><span class="sxs-lookup"><span data-stu-id="d92a8-199">enableDnsRegistration</span></span>|<span data-ttu-id="d92a8-200">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-200">Boolean</span></span>|<span data-ttu-id="d92a8-201">Habilitar el registro de dirección IP con DNS interno.</span><span class="sxs-lookup"><span data-stu-id="d92a8-201">Enable IP address registration with internal DNS.</span></span>|
|<span data-ttu-id="d92a8-202">dnsSuffixes</span><span class="sxs-lookup"><span data-stu-id="d92a8-202">dnsSuffixes</span></span>|<span data-ttu-id="d92a8-203">Colección String</span><span class="sxs-lookup"><span data-stu-id="d92a8-203">String collection</span></span>|<span data-ttu-id="d92a8-204">Especificar sufijos DNS para agregar a la lista de búsqueda DNS para enrutar correctamente los nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-204">Specify DNS suffixes to add to the DNS search list to properly route short names.</span></span>|
|<span data-ttu-id="d92a8-205">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d92a8-205">authenticationMethod</span></span>|[<span data-ttu-id="d92a8-206">windows10VpnAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="d92a8-206">windows10VpnAuthenticationMethod</span></span>](../resources/intune-deviceconfig-windows10vpnauthenticationmethod.md)|<span data-ttu-id="d92a8-207">Método de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d92a8-207">Authentication method.</span></span> <span data-ttu-id="d92a8-208">Los valores posibles son: `certificate`, `usernameAndPassword` y `customEapXml`.</span><span class="sxs-lookup"><span data-stu-id="d92a8-208">Possible values are: `certificate`, `usernameAndPassword`, `customEapXml`.</span></span>|
|<span data-ttu-id="d92a8-209">rememberUserCredentials</span><span class="sxs-lookup"><span data-stu-id="d92a8-209">rememberUserCredentials</span></span>|<span data-ttu-id="d92a8-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-210">Boolean</span></span>|<span data-ttu-id="d92a8-211">Recuerde que las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="d92a8-211">Remember user credentials.</span></span>|
|<span data-ttu-id="d92a8-212">enableConditionalAccess</span><span class="sxs-lookup"><span data-stu-id="d92a8-212">enableConditionalAccess</span></span>|<span data-ttu-id="d92a8-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-213">Boolean</span></span>|<span data-ttu-id="d92a8-214">Habilite el acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="d92a8-214">Enable conditional access.</span></span>|
|<span data-ttu-id="d92a8-215">enableSingleSignOnWithAlternateCertificate</span><span class="sxs-lookup"><span data-stu-id="d92a8-215">enableSingleSignOnWithAlternateCertificate</span></span>|<span data-ttu-id="d92a8-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-216">Boolean</span></span>|<span data-ttu-id="d92a8-217">Habilitar sesión único (SSO) con certificado alternativa.</span><span class="sxs-lookup"><span data-stu-id="d92a8-217">Enable single sign-on (SSO) with alternate certificate.</span></span>|
|<span data-ttu-id="d92a8-218">singleSignOnEku</span><span class="sxs-lookup"><span data-stu-id="d92a8-218">singleSignOnEku</span></span>|[<span data-ttu-id="d92a8-219">ExtendeKeyUsage</span><span class="sxs-lookup"><span data-stu-id="d92a8-219">extendedKeyUsage</span></span>](../resources/intune-deviceconfig-extendedkeyusage.md)|<span data-ttu-id="d92a8-220">Single sign-on extendido clave (EKU).</span><span class="sxs-lookup"><span data-stu-id="d92a8-220">Single sign-on Extended Key Usage (EKU).</span></span>|
|<span data-ttu-id="d92a8-221">singleSignOnIssuerHash</span><span class="sxs-lookup"><span data-stu-id="d92a8-221">singleSignOnIssuerHash</span></span>|<span data-ttu-id="d92a8-222">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-222">String</span></span>|<span data-ttu-id="d92a8-223">Hash de emisor de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="d92a8-223">Single sign-on issuer hash.</span></span>|
|<span data-ttu-id="d92a8-224">eapXml</span><span class="sxs-lookup"><span data-stu-id="d92a8-224">eapXml</span></span>|<span data-ttu-id="d92a8-225">Binario</span><span class="sxs-lookup"><span data-stu-id="d92a8-225">Binary</span></span>|<span data-ttu-id="d92a8-226">Protocolo de autenticación extensible (EAP) XML.</span><span class="sxs-lookup"><span data-stu-id="d92a8-226">Extensible Authentication Protocol (EAP) XML.</span></span> <span data-ttu-id="d92a8-227">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="d92a8-227">(UTF8 encoded byte array)</span></span>|
|<span data-ttu-id="d92a8-228">proxyServer</span><span class="sxs-lookup"><span data-stu-id="d92a8-228">proxyServer</span></span>|[<span data-ttu-id="d92a8-229">windows10VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="d92a8-229">windows10VpnProxyServer</span></span>](../resources/intune-deviceconfig-windows10vpnproxyserver.md)|<span data-ttu-id="d92a8-230">Servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="d92a8-230">Proxy Server.</span></span>|
|<span data-ttu-id="d92a8-231">associatedApps</span><span class="sxs-lookup"><span data-stu-id="d92a8-231">associatedApps</span></span>|<span data-ttu-id="d92a8-232">colección de [windows10AssociatedApps](../resources/intune-deviceconfig-windows10associatedapps.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-232">[windows10AssociatedApps](../resources/intune-deviceconfig-windows10associatedapps.md) collection</span></span>|<span data-ttu-id="d92a8-233">Aplicaciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="d92a8-233">Associated Apps.</span></span> <span data-ttu-id="d92a8-234">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-234">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="d92a8-235">onlyAssociatedAppsCanUseConnection</span><span class="sxs-lookup"><span data-stu-id="d92a8-235">onlyAssociatedAppsCanUseConnection</span></span>|<span data-ttu-id="d92a8-236">Boolean</span><span class="sxs-lookup"><span data-stu-id="d92a8-236">Boolean</span></span>|<span data-ttu-id="d92a8-237">Sólo las aplicaciones asociadas pueden utilizar conexión (VPN por aplicación).</span><span class="sxs-lookup"><span data-stu-id="d92a8-237">Only associated Apps can use connection (per-app VPN).</span></span>|
|<span data-ttu-id="d92a8-238">windowsInformationProtectionDomain</span><span class="sxs-lookup"><span data-stu-id="d92a8-238">windowsInformationProtectionDomain</span></span>|<span data-ttu-id="d92a8-239">String</span><span class="sxs-lookup"><span data-stu-id="d92a8-239">String</span></span>|<span data-ttu-id="d92a8-240">Dominio de protección de información de Windows (curso) para asociar a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="d92a8-240">Windows Information Protection (WIP) domain to associate with this connection.</span></span>|
|<span data-ttu-id="d92a8-241">trafficRules</span><span class="sxs-lookup"><span data-stu-id="d92a8-241">trafficRules</span></span>|<span data-ttu-id="d92a8-242">colección de [vpnTrafficRule](../resources/intune-deviceconfig-vpntrafficrule.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-242">[vpnTrafficRule](../resources/intune-deviceconfig-vpntrafficrule.md) collection</span></span>|<span data-ttu-id="d92a8-243">Reglas de tráfico.</span><span class="sxs-lookup"><span data-stu-id="d92a8-243">Traffic rules.</span></span> <span data-ttu-id="d92a8-244">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-244">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="d92a8-245">rutas</span><span class="sxs-lookup"><span data-stu-id="d92a8-245">routes</span></span>|<span data-ttu-id="d92a8-246">colección de [vpnRoute](../resources/intune-deviceconfig-vpnroute.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-246">[vpnRoute](../resources/intune-deviceconfig-vpnroute.md) collection</span></span>|<span data-ttu-id="d92a8-247">Rutas (opcionales para los proveedores de terceros).</span><span class="sxs-lookup"><span data-stu-id="d92a8-247">Routes (optional for third-party providers).</span></span> <span data-ttu-id="d92a8-248">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-248">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="d92a8-249">dnsRules</span><span class="sxs-lookup"><span data-stu-id="d92a8-249">dnsRules</span></span>|<span data-ttu-id="d92a8-250">colección de [vpnDnsRule](../resources/intune-deviceconfig-vpndnsrule.md)</span><span class="sxs-lookup"><span data-stu-id="d92a8-250">[vpnDnsRule](../resources/intune-deviceconfig-vpndnsrule.md) collection</span></span>|<span data-ttu-id="d92a8-251">Reglas de DNS.</span><span class="sxs-lookup"><span data-stu-id="d92a8-251">DNS rules.</span></span> <span data-ttu-id="d92a8-252">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="d92a8-252">This collection can contain a maximum of 1000 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="d92a8-253">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d92a8-253">Response</span></span>
<span data-ttu-id="d92a8-254">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d92a8-254">If successful, this method returns a `200 OK` response code and an updated [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d92a8-255">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d92a8-255">Example</span></span>
### <a name="request"></a><span data-ttu-id="d92a8-256">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d92a8-256">Request</span></span>
<span data-ttu-id="d92a8-257">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d92a8-257">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 3259

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
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "customXml": "Y3VzdG9tWG1s",
  "profileTarget": "device",
  "connectionType": "f5EdgeClient",
  "enableSplitTunneling": true,
  "enableAlwaysOn": true,
  "enableDeviceTunnel": true,
  "enableDnsRegistration": true,
  "dnsSuffixes": [
    "Dns Suffixes value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "rememberUserCredentials": true,
  "enableConditionalAccess": true,
  "enableSingleSignOnWithAlternateCertificate": true,
  "singleSignOnEku": {
    "@odata.type": "microsoft.graph.extendedKeyUsage",
    "name": "Name value",
    "objectIdentifier": "Object Identifier value"
  },
  "singleSignOnIssuerHash": "Single Sign On Issuer Hash value",
  "eapXml": "ZWFwWG1s",
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows10VpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4,
    "bypassProxyServerForLocalAddress": true
  },
  "associatedApps": [
    {
      "@odata.type": "microsoft.graph.windows10AssociatedApps",
      "appType": "universal",
      "identifier": "Identifier value"
    }
  ],
  "onlyAssociatedAppsCanUseConnection": true,
  "windowsInformationProtectionDomain": "Windows Information Protection Domain value",
  "trafficRules": [
    {
      "@odata.type": "microsoft.graph.vpnTrafficRule",
      "name": "Name value",
      "protocols": 9,
      "localPortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 11,
          "upperNumber": 11
        }
      ],
      "remotePortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 11,
          "upperNumber": 11
        }
      ],
      "localAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ],
      "remoteAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ],
      "appId": "App Id value",
      "appType": "desktop",
      "routingPolicyType": "splitTunnel",
      "claims": "Claims value"
    }
  ],
  "routes": [
    {
      "@odata.type": "microsoft.graph.vpnRoute",
      "destinationPrefix": "Destination Prefix value",
      "prefixSize": 10
    }
  ],
  "dnsRules": [
    {
      "@odata.type": "microsoft.graph.vpnDnsRule",
      "name": "Name value",
      "servers": [
        "Servers value"
      ],
      "proxyServerUri": "Proxy Server Uri value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="d92a8-258">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d92a8-258">Response</span></span>
<span data-ttu-id="d92a8-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d92a8-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 3431

{
  "@odata.type": "#microsoft.graph.windows10VpnConfiguration",
  "id": "c23c9727-9727-c23c-2797-3cc227973cc2",
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
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "Description value",
      "address": "Address value",
      "isDefaultServer": true
    }
  ],
  "customXml": "Y3VzdG9tWG1s",
  "profileTarget": "device",
  "connectionType": "f5EdgeClient",
  "enableSplitTunneling": true,
  "enableAlwaysOn": true,
  "enableDeviceTunnel": true,
  "enableDnsRegistration": true,
  "dnsSuffixes": [
    "Dns Suffixes value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "rememberUserCredentials": true,
  "enableConditionalAccess": true,
  "enableSingleSignOnWithAlternateCertificate": true,
  "singleSignOnEku": {
    "@odata.type": "microsoft.graph.extendedKeyUsage",
    "name": "Name value",
    "objectIdentifier": "Object Identifier value"
  },
  "singleSignOnIssuerHash": "Single Sign On Issuer Hash value",
  "eapXml": "ZWFwWG1s",
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows10VpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4,
    "bypassProxyServerForLocalAddress": true
  },
  "associatedApps": [
    {
      "@odata.type": "microsoft.graph.windows10AssociatedApps",
      "appType": "universal",
      "identifier": "Identifier value"
    }
  ],
  "onlyAssociatedAppsCanUseConnection": true,
  "windowsInformationProtectionDomain": "Windows Information Protection Domain value",
  "trafficRules": [
    {
      "@odata.type": "microsoft.graph.vpnTrafficRule",
      "name": "Name value",
      "protocols": 9,
      "localPortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 11,
          "upperNumber": 11
        }
      ],
      "remotePortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 11,
          "upperNumber": 11
        }
      ],
      "localAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ],
      "remoteAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ],
      "appId": "App Id value",
      "appType": "desktop",
      "routingPolicyType": "splitTunnel",
      "claims": "Claims value"
    }
  ],
  "routes": [
    {
      "@odata.type": "microsoft.graph.vpnRoute",
      "destinationPrefix": "Destination Prefix value",
      "prefixSize": 10
    }
  ],
  "dnsRules": [
    {
      "@odata.type": "microsoft.graph.vpnDnsRule",
      "name": "Name value",
      "servers": [
        "Servers value"
      ],
      "proxyServerUri": "Proxy Server Uri value"
    }
  ]
}
```





