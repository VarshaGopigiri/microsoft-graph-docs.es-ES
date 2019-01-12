---
title: Crear iosVpnConfiguration
description: Crear un nuevo objeto iosVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cdacab0555999b454c031d985abcf8e64f4ed375
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953063"
---
# <a name="create-iosvpnconfiguration"></a><span data-ttu-id="50b3c-103">Crear iosVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="50b3c-103">Create iosVpnConfiguration</span></span>

> <span data-ttu-id="50b3c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50b3c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50b3c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50b3c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="50b3c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="50b3c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="50b3c-107">Crear un nuevo objeto [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="50b3c-107">Create a new [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="50b3c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="50b3c-108">Prerequisites</span></span>
<span data-ttu-id="50b3c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="50b3c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="50b3c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="50b3c-111">Permission type</span></span>|<span data-ttu-id="50b3c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="50b3c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="50b3c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="50b3c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="50b3c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="50b3c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="50b3c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="50b3c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="50b3c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50b3c-116">Not supported.</span></span>|
|<span data-ttu-id="50b3c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="50b3c-117">Application</span></span>|<span data-ttu-id="50b3c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="50b3c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="50b3c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="50b3c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="50b3c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="50b3c-120">Request headers</span></span>
|<span data-ttu-id="50b3c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50b3c-121">Header</span></span>|<span data-ttu-id="50b3c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="50b3c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="50b3c-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="50b3c-123">Authorization</span></span>|<span data-ttu-id="50b3c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="50b3c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="50b3c-125">Accept</span><span class="sxs-lookup"><span data-stu-id="50b3c-125">Accept</span></span>|<span data-ttu-id="50b3c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="50b3c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="50b3c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="50b3c-127">Request body</span></span>
<span data-ttu-id="50b3c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto iosVpnConfiguration.</span><span class="sxs-lookup"><span data-stu-id="50b3c-128">In the request body, supply a JSON representation for the iosVpnConfiguration object.</span></span>

<span data-ttu-id="50b3c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el iosVpnConfiguration.</span><span class="sxs-lookup"><span data-stu-id="50b3c-129">The following table shows the properties that are required when you create the iosVpnConfiguration.</span></span>

|<span data-ttu-id="50b3c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50b3c-130">Property</span></span>|<span data-ttu-id="50b3c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="50b3c-131">Type</span></span>|<span data-ttu-id="50b3c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="50b3c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="50b3c-133">id</span><span class="sxs-lookup"><span data-stu-id="50b3c-133">id</span></span>|<span data-ttu-id="50b3c-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-134">String</span></span>|<span data-ttu-id="50b3c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="50b3c-135">Key of the entity.</span></span> <span data-ttu-id="50b3c-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="50b3c-137">lastModifiedDateTime</span></span>|<span data-ttu-id="50b3c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50b3c-138">DateTimeOffset</span></span>|<span data-ttu-id="50b3c-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="50b3c-139">DateTime the object was last modified.</span></span> <span data-ttu-id="50b3c-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="50b3c-141">roleScopeTagIds</span></span>|<span data-ttu-id="50b3c-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="50b3c-142">String collection</span></span>|<span data-ttu-id="50b3c-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="50b3c-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="50b3c-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="50b3c-145">supportsScopeTags</span></span>|<span data-ttu-id="50b3c-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="50b3c-146">Boolean</span></span>|<span data-ttu-id="50b3c-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="50b3c-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="50b3c-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="50b3c-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="50b3c-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="50b3c-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="50b3c-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="50b3c-150">This property is read-only.</span></span> <span data-ttu-id="50b3c-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="50b3c-152">createdDateTime</span></span>|<span data-ttu-id="50b3c-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="50b3c-153">DateTimeOffset</span></span>|<span data-ttu-id="50b3c-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="50b3c-154">DateTime the object was created.</span></span> <span data-ttu-id="50b3c-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-156">descripción</span><span class="sxs-lookup"><span data-stu-id="50b3c-156">description</span></span>|<span data-ttu-id="50b3c-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-157">String</span></span>|<span data-ttu-id="50b3c-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50b3c-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="50b3c-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-160">displayName</span><span class="sxs-lookup"><span data-stu-id="50b3c-160">displayName</span></span>|<span data-ttu-id="50b3c-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-161">String</span></span>|<span data-ttu-id="50b3c-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50b3c-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="50b3c-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-164">version</span><span class="sxs-lookup"><span data-stu-id="50b3c-164">version</span></span>|<span data-ttu-id="50b3c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="50b3c-165">Int32</span></span>|<span data-ttu-id="50b3c-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50b3c-166">Version of the device configuration.</span></span> <span data-ttu-id="50b3c-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-168">connectionName</span><span class="sxs-lookup"><span data-stu-id="50b3c-168">connectionName</span></span>|<span data-ttu-id="50b3c-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-169">String</span></span>|<span data-ttu-id="50b3c-170">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="50b3c-170">Connection name displayed to the user.</span></span> <span data-ttu-id="50b3c-171">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-171">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-172">connectionType</span><span class="sxs-lookup"><span data-stu-id="50b3c-172">connectionType</span></span>|[<span data-ttu-id="50b3c-173">appleVpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="50b3c-173">appleVpnConnectionType</span></span>](../resources/intune-deviceconfig-applevpnconnectiontype.md)|<span data-ttu-id="50b3c-174">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="50b3c-174">Connection type.</span></span> <span data-ttu-id="50b3c-175">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="50b3c-175">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md).</span></span> <span data-ttu-id="50b3c-176">Los valores posibles son: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `customVpn`, `ciscoIPSec`, `citrix`, `ciscoAnyConnectV2`, `paloAltoGlobalProtect`, `zscalerPrivateAccess`, `f5Access2018`, `citrixSso`, `paloAltoGlobalProtectV2`.</span><span class="sxs-lookup"><span data-stu-id="50b3c-176">Possible values are: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `customVpn`, `ciscoIPSec`, `citrix`, `ciscoAnyConnectV2`, `paloAltoGlobalProtect`, `zscalerPrivateAccess`, `f5Access2018`, `citrixSso`, `paloAltoGlobalProtectV2`.</span></span>|
|<span data-ttu-id="50b3c-177">loginGroupOrDomain</span><span class="sxs-lookup"><span data-stu-id="50b3c-177">loginGroupOrDomain</span></span>|<span data-ttu-id="50b3c-178">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-178">String</span></span>|<span data-ttu-id="50b3c-179">Grupo de inicio de sesión o dominio cuando se establece el tipo de conexión a Dell SonicWALL Mobile conexión.</span><span class="sxs-lookup"><span data-stu-id="50b3c-179">Login group or domain when connection type is set to Dell SonicWALL Mobile Connection.</span></span> <span data-ttu-id="50b3c-180">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-180">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-181">role</span><span class="sxs-lookup"><span data-stu-id="50b3c-181">role</span></span>|<span data-ttu-id="50b3c-182">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-182">String</span></span>|<span data-ttu-id="50b3c-183">Función de tipo de conexión se establece en impulsos seguro.</span><span class="sxs-lookup"><span data-stu-id="50b3c-183">Role when connection type is set to Pulse Secure.</span></span> <span data-ttu-id="50b3c-184">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-184">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-185">dominio kerberos</span><span class="sxs-lookup"><span data-stu-id="50b3c-185">realm</span></span>|<span data-ttu-id="50b3c-186">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-186">String</span></span>|<span data-ttu-id="50b3c-187">Dominio Kerberos cuando se establece el tipo de conexión a impulsos seguro.</span><span class="sxs-lookup"><span data-stu-id="50b3c-187">Realm when connection type is set to Pulse Secure.</span></span> <span data-ttu-id="50b3c-188">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-188">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-189">servidor</span><span class="sxs-lookup"><span data-stu-id="50b3c-189">server</span></span>|[<span data-ttu-id="50b3c-190">servidor de VPN</span><span class="sxs-lookup"><span data-stu-id="50b3c-190">vpnServer</span></span>](../resources/intune-deviceconfig-vpnserver.md)|<span data-ttu-id="50b3c-191">Servidor de VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="50b3c-191">VPN Server on the network.</span></span> <span data-ttu-id="50b3c-192">Asegúrese de que los usuarios finales pueden tener acceso a esta ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="50b3c-192">Make sure end users can access this network location.</span></span> <span data-ttu-id="50b3c-193">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-193">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-194">identificador</span><span class="sxs-lookup"><span data-stu-id="50b3c-194">identifier</span></span>|<span data-ttu-id="50b3c-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-195">String</span></span>|<span data-ttu-id="50b3c-196">Identificador proporcionado por el proveedor de VPN cuando se establece el tipo de conexión a VPN personalizado.</span><span class="sxs-lookup"><span data-stu-id="50b3c-196">Identifier provided by VPN vendor when connection type is set to Custom VPN.</span></span> <span data-ttu-id="50b3c-197">Por ejemplo: AnyConnect de Cisco usa un identificador de la com.cisco.anyconnect.applevpn.plugin de formulario Inherited desde [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-197">For example: Cisco AnyConnect uses an identifier of the form com.cisco.anyconnect.applevpn.plugin Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-198">customData</span><span class="sxs-lookup"><span data-stu-id="50b3c-198">customData</span></span>|<span data-ttu-id="50b3c-199">colección [keyValue](../resources/intune-deviceconfig-keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-199">[keyValue](../resources/intune-deviceconfig-keyvalue.md) collection</span></span>|<span data-ttu-id="50b3c-200">Datos personalizados cuando se establece el tipo de conexión a VPN personalizado.</span><span class="sxs-lookup"><span data-stu-id="50b3c-200">Custom data when connection type is set to Custom VPN.</span></span> <span data-ttu-id="50b3c-201">Use este campo para habilitar la funcionalidad no admitida por Intune, pero disponible en la solución de VPN.</span><span class="sxs-lookup"><span data-stu-id="50b3c-201">Use this field to enable functionality not supported by Intune, but available in your VPN solution.</span></span> <span data-ttu-id="50b3c-202">Póngase en contacto con su proveedor de VPN para obtener información sobre cómo agregar estos pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="50b3c-202">Contact your VPN vendor to learn how to add these key/value pairs.</span></span> <span data-ttu-id="50b3c-203">Esta colección puede contener un máximo de 25 elementos.</span><span class="sxs-lookup"><span data-stu-id="50b3c-203">This collection can contain a maximum of 25 elements.</span></span> <span data-ttu-id="50b3c-204">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-204">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-205">customKeyValueData</span><span class="sxs-lookup"><span data-stu-id="50b3c-205">customKeyValueData</span></span>|<span data-ttu-id="50b3c-206">Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-206">[keyValuePair](../resources/intune-shared-keyvaluepair.md) collection</span></span>|<span data-ttu-id="50b3c-207">Datos personalizados cuando se establece el tipo de conexión a VPN personalizado.</span><span class="sxs-lookup"><span data-stu-id="50b3c-207">Custom data when connection type is set to Custom VPN.</span></span> <span data-ttu-id="50b3c-208">Use este campo para habilitar la funcionalidad no admitida por Intune, pero disponible en la solución de VPN.</span><span class="sxs-lookup"><span data-stu-id="50b3c-208">Use this field to enable functionality not supported by Intune, but available in your VPN solution.</span></span> <span data-ttu-id="50b3c-209">Póngase en contacto con su proveedor de VPN para obtener información sobre cómo agregar estos pares de clave y valor.</span><span class="sxs-lookup"><span data-stu-id="50b3c-209">Contact your VPN vendor to learn how to add these key/value pairs.</span></span> <span data-ttu-id="50b3c-210">Esta colección puede contener un máximo de 25 elementos.</span><span class="sxs-lookup"><span data-stu-id="50b3c-210">This collection can contain a maximum of 25 elements.</span></span> <span data-ttu-id="50b3c-211">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-211">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-212">enableSplitTunneling</span><span class="sxs-lookup"><span data-stu-id="50b3c-212">enableSplitTunneling</span></span>|<span data-ttu-id="50b3c-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="50b3c-213">Boolean</span></span>|<span data-ttu-id="50b3c-214">Enviar todo el tráfico de red a través de VPN.</span><span class="sxs-lookup"><span data-stu-id="50b3c-214">Send all network traffic through VPN.</span></span> <span data-ttu-id="50b3c-215">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-215">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-216">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="50b3c-216">authenticationMethod</span></span>|[<span data-ttu-id="50b3c-217">vpnAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="50b3c-217">vpnAuthenticationMethod</span></span>](../resources/intune-deviceconfig-vpnauthenticationmethod.md)|<span data-ttu-id="50b3c-218">Método de autenticación para esta conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="50b3c-218">Authentication method for this VPN connection.</span></span> <span data-ttu-id="50b3c-219">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="50b3c-219">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md).</span></span> <span data-ttu-id="50b3c-220">Los valores posibles son: `certificate` y `usernameAndPassword`.</span><span class="sxs-lookup"><span data-stu-id="50b3c-220">Possible values are: `certificate`, `usernameAndPassword`.</span></span>|
|<span data-ttu-id="50b3c-221">enablePerApp</span><span class="sxs-lookup"><span data-stu-id="50b3c-221">enablePerApp</span></span>|<span data-ttu-id="50b3c-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="50b3c-222">Boolean</span></span>|<span data-ttu-id="50b3c-223">Si se establece en true, crea de carga por aplicación VPN que más adelante se puede asociar con las aplicaciones que pueden desencadenar este conexiones VPN en dispositivo de iOS del usuario final.</span><span class="sxs-lookup"><span data-stu-id="50b3c-223">Setting this to true creates Per-App VPN payload which can later be associated with Apps that can trigger this VPN conneciton on the end user's iOS device.</span></span> <span data-ttu-id="50b3c-224">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-224">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-225">safariDomains</span><span class="sxs-lookup"><span data-stu-id="50b3c-225">safariDomains</span></span>|<span data-ttu-id="50b3c-226">Colección String</span><span class="sxs-lookup"><span data-stu-id="50b3c-226">String collection</span></span>|<span data-ttu-id="50b3c-227">Dominios de Safari cuando está habilitada esta VPN por la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b3c-227">Safari domains when this VPN per App setting is enabled.</span></span> <span data-ttu-id="50b3c-228">Además de las aplicaciones asociadas con esta VPN, dominios de Safari especifiquen aquí también podrá desencadenar esta conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="50b3c-228">In addition to the apps associated with this VPN, Safari domains specified here will also be able to trigger this VPN connection.</span></span> <span data-ttu-id="50b3c-229">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-229">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-230">onDemandRules</span><span class="sxs-lookup"><span data-stu-id="50b3c-230">onDemandRules</span></span>|<span data-ttu-id="50b3c-231">colección de [vpnOnDemandRule](../resources/intune-deviceconfig-vpnondemandrule.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-231">[vpnOnDemandRule](../resources/intune-deviceconfig-vpnondemandrule.md) collection</span></span>|<span data-ttu-id="50b3c-232">Reglas de On Demand.</span><span class="sxs-lookup"><span data-stu-id="50b3c-232">On-Demand Rules.</span></span> <span data-ttu-id="50b3c-233">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="50b3c-233">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="50b3c-234">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-234">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-235">proxyServer</span><span class="sxs-lookup"><span data-stu-id="50b3c-235">proxyServer</span></span>|[<span data-ttu-id="50b3c-236">vpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="50b3c-236">vpnProxyServer</span></span>](../resources/intune-deviceconfig-vpnproxyserver.md)|<span data-ttu-id="50b3c-237">Servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="50b3c-237">Proxy Server.</span></span> <span data-ttu-id="50b3c-238">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-238">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-239">optInToDeviceIdSharing</span><span class="sxs-lookup"><span data-stu-id="50b3c-239">optInToDeviceIdSharing</span></span>|<span data-ttu-id="50b3c-240">Booleano</span><span class="sxs-lookup"><span data-stu-id="50b3c-240">Boolean</span></span>|<span data-ttu-id="50b3c-241">Participar en uso compartido de identificador del dispositivo a los clientes de vpn de terceros para su uso durante la validación de control de acceso de red.</span><span class="sxs-lookup"><span data-stu-id="50b3c-241">Opt-In to sharing the device's Id to third-party vpn clients for use during network access control validation.</span></span> <span data-ttu-id="50b3c-242">Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="50b3c-242">Inherited from [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)</span></span>|
|<span data-ttu-id="50b3c-243">tipo de proveedor</span><span class="sxs-lookup"><span data-stu-id="50b3c-243">providerType</span></span>|[<span data-ttu-id="50b3c-244">vpnProviderType</span><span class="sxs-lookup"><span data-stu-id="50b3c-244">vpnProviderType</span></span>](../resources/intune-deviceconfig-vpnprovidertype.md)|<span data-ttu-id="50b3c-245">Tipo de proveedor de VPN por cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="50b3c-245">Provider type for per-app VPN.</span></span> <span data-ttu-id="50b3c-246">Los valores posibles son: `notConfigured`, `appProxy` y `packetTunnel`.</span><span class="sxs-lookup"><span data-stu-id="50b3c-246">Possible values are: `notConfigured`, `appProxy`, `packetTunnel`.</span></span>|
|<span data-ttu-id="50b3c-247">userDomain</span><span class="sxs-lookup"><span data-stu-id="50b3c-247">userDomain</span></span>|<span data-ttu-id="50b3c-248">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-248">String</span></span>|<span data-ttu-id="50b3c-249">Sólo Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-249">Zscaler only.</span></span> <span data-ttu-id="50b3c-250">Escriba un dominio estático para rellenar previamente el campo de inicio de sesión con en la aplicación Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-250">Enter a static domain to pre-populate the login field with in the Zscaler app.</span></span> <span data-ttu-id="50b3c-251">Si se deja vacía, se utilizará el dominio del usuario Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50b3c-251">If this is left empty, the user's Azure Active Directory domain will be used instead.</span></span>|
|<span data-ttu-id="50b3c-252">strictEnforcement</span><span class="sxs-lookup"><span data-stu-id="50b3c-252">strictEnforcement</span></span>|<span data-ttu-id="50b3c-253">Booleano</span><span class="sxs-lookup"><span data-stu-id="50b3c-253">Boolean</span></span>|<span data-ttu-id="50b3c-254">Sólo Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-254">Zscaler only.</span></span> <span data-ttu-id="50b3c-255">Bloques de tráfico de red hasta que el usuario cierre sesión en la aplicación Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-255">Blocks network traffic until the user signs into Zscaler app.</span></span> <span data-ttu-id="50b3c-256">"True" significa que el tráfico se bloquea.</span><span class="sxs-lookup"><span data-stu-id="50b3c-256">"True" means traffic is blocked.</span></span>|
|<span data-ttu-id="50b3c-257">cloudName</span><span class="sxs-lookup"><span data-stu-id="50b3c-257">cloudName</span></span>|<span data-ttu-id="50b3c-258">Cadena</span><span class="sxs-lookup"><span data-stu-id="50b3c-258">String</span></span>|<span data-ttu-id="50b3c-259">Sólo Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-259">Zscaler only.</span></span> <span data-ttu-id="50b3c-260">Nube de Zscaler que está asignado el usuario.</span><span class="sxs-lookup"><span data-stu-id="50b3c-260">Zscaler cloud which the user is assigned to.</span></span>|
|<span data-ttu-id="50b3c-261">excludeList</span><span class="sxs-lookup"><span data-stu-id="50b3c-261">excludeList</span></span>|<span data-ttu-id="50b3c-262">Colección String</span><span class="sxs-lookup"><span data-stu-id="50b3c-262">String collection</span></span>|<span data-ttu-id="50b3c-263">Sólo Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-263">Zscaler only.</span></span> <span data-ttu-id="50b3c-264">Lista de direcciones de red que no se envían a través de la nube de Zscaler.</span><span class="sxs-lookup"><span data-stu-id="50b3c-264">List of network addresses which are not sent through the Zscaler cloud.</span></span>|



## <a name="response"></a><span data-ttu-id="50b3c-265">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50b3c-265">Response</span></span>
<span data-ttu-id="50b3c-266">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="50b3c-266">If successful, this method returns a `201 Created` response code and a [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="50b3c-267">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="50b3c-267">Example</span></span>
### <a name="request"></a><span data-ttu-id="50b3c-268">Solicitud</span><span class="sxs-lookup"><span data-stu-id="50b3c-268">Request</span></span>
<span data-ttu-id="50b3c-269">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="50b3c-269">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 2106

{
  "@odata.type": "#microsoft.graph.iosVpnConfiguration",
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
  "loginGroupOrDomain": "Login Group Or Domain value",
  "role": "Role value",
  "realm": "Realm value",
  "server": {
    "@odata.type": "microsoft.graph.vpnServer",
    "description": "Description value",
    "address": "Address value",
    "isDefaultServer": true
  },
  "identifier": "Identifier value",
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
  "enableSplitTunneling": true,
  "authenticationMethod": "usernameAndPassword",
  "enablePerApp": true,
  "safariDomains": [
    "Safari Domains value"
  ],
  "onDemandRules": [
    {
      "@odata.type": "microsoft.graph.vpnOnDemandRule",
      "ssids": [
        "Ssids value"
      ],
      "dnsSearchDomains": [
        "Dns Search Domains value"
      ],
      "probeUrl": "https://example.com/probeUrl/",
      "action": "evaluateConnection",
      "domainAction": "neverConnect",
      "domains": [
        "Domains value"
      ],
      "probeRequiredUrl": "https://example.com/probeRequiredUrl/"
    }
  ],
  "proxyServer": {
    "@odata.type": "microsoft.graph.vpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4
  },
  "optInToDeviceIdSharing": true,
  "providerType": "appProxy",
  "userDomain": "User Domain value",
  "strictEnforcement": true,
  "cloudName": "Cloud Name value",
  "excludeList": [
    "Exclude List value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="50b3c-270">Respuesta</span><span class="sxs-lookup"><span data-stu-id="50b3c-270">Response</span></span>
<span data-ttu-id="50b3c-p132">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="50b3c-p132">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 2214

{
  "@odata.type": "#microsoft.graph.iosVpnConfiguration",
  "id": "bd12424c-424c-bd12-4c42-12bd4c4212bd",
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
  "loginGroupOrDomain": "Login Group Or Domain value",
  "role": "Role value",
  "realm": "Realm value",
  "server": {
    "@odata.type": "microsoft.graph.vpnServer",
    "description": "Description value",
    "address": "Address value",
    "isDefaultServer": true
  },
  "identifier": "Identifier value",
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
  "enableSplitTunneling": true,
  "authenticationMethod": "usernameAndPassword",
  "enablePerApp": true,
  "safariDomains": [
    "Safari Domains value"
  ],
  "onDemandRules": [
    {
      "@odata.type": "microsoft.graph.vpnOnDemandRule",
      "ssids": [
        "Ssids value"
      ],
      "dnsSearchDomains": [
        "Dns Search Domains value"
      ],
      "probeUrl": "https://example.com/probeUrl/",
      "action": "evaluateConnection",
      "domainAction": "neverConnect",
      "domains": [
        "Domains value"
      ],
      "probeRequiredUrl": "https://example.com/probeRequiredUrl/"
    }
  ],
  "proxyServer": {
    "@odata.type": "microsoft.graph.vpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4
  },
  "optInToDeviceIdSharing": true,
  "providerType": "appProxy",
  "userDomain": "User Domain value",
  "strictEnforcement": true,
  "cloudName": "Cloud Name value",
  "excludeList": [
    "Exclude List value"
  ]
}
```





