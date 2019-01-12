---
title: tipo de recurso windows10VpnConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar el dispositivo de Windows 10 (escritorio o móvil) para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 775a4dfbeb46c27264b5539c51c63b29b488565b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937772"
---
# <a name="windows10vpnconfiguration-resource-type"></a><span data-ttu-id="287a1-104">tipo de recurso windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-104">windows10VpnConfiguration resource type</span></span>

> <span data-ttu-id="287a1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="287a1-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="287a1-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="287a1-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="287a1-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="287a1-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="287a1-108">Proporcionando las configuraciones de este perfil puede indicar el dispositivo de Windows 10 (escritorio o móvil) para conectarse al extremo VPN que desee.</span><span class="sxs-lookup"><span data-stu-id="287a1-108">By providing the configurations in this profile you can instruct the Windows 10 device (desktop or mobile) to connect to desired VPN endpoint.</span></span> <span data-ttu-id="287a1-109">Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.</span><span class="sxs-lookup"><span data-stu-id="287a1-109">By specifying the authentication method and security types expected by VPN endpoint you can make the VPN connection seamless for end user.</span></span>

<span data-ttu-id="287a1-110">Hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-110">Inherits from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>

## <a name="methods"></a><span data-ttu-id="287a1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="287a1-111">Methods</span></span>
|<span data-ttu-id="287a1-112">Método</span><span class="sxs-lookup"><span data-stu-id="287a1-112">Method</span></span>|<span data-ttu-id="287a1-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="287a1-113">Return Type</span></span>|<span data-ttu-id="287a1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="287a1-114">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="287a1-115">Lista windows10VpnConfigurations</span><span class="sxs-lookup"><span data-stu-id="287a1-115">List windows10VpnConfigurations</span></span>](../api/intune-deviceconfig-windows10vpnconfiguration-list.md)|<span data-ttu-id="287a1-116">colección de [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-116">[windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) collection</span></span>|<span data-ttu-id="287a1-117">Propiedades de la lista y relaciones de los objetos [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="287a1-117">List properties and relationships of the [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="287a1-118">Obtener windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-118">Get windows10VpnConfiguration</span></span>](../api/intune-deviceconfig-windows10vpnconfiguration-get.md)|[<span data-ttu-id="287a1-119">windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-119">windows10VpnConfiguration</span></span>](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|<span data-ttu-id="287a1-120">Leer las propiedades y las relaciones del objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="287a1-120">Read properties and relationships of the [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>|
|[<span data-ttu-id="287a1-121">Crear windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-121">Create windows10VpnConfiguration</span></span>](../api/intune-deviceconfig-windows10vpnconfiguration-create.md)|[<span data-ttu-id="287a1-122">windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-122">windows10VpnConfiguration</span></span>](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|<span data-ttu-id="287a1-123">Crear un nuevo objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="287a1-123">Create a new [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>|
|[<span data-ttu-id="287a1-124">Eliminar windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-124">Delete windows10VpnConfiguration</span></span>](../api/intune-deviceconfig-windows10vpnconfiguration-delete.md)|<span data-ttu-id="287a1-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="287a1-125">None</span></span>|<span data-ttu-id="287a1-126">Elimina un [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="287a1-126">Deletes a [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md).</span></span>|
|[<span data-ttu-id="287a1-127">Actualizar windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-127">Update windows10VpnConfiguration</span></span>](../api/intune-deviceconfig-windows10vpnconfiguration-update.md)|[<span data-ttu-id="287a1-128">windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="287a1-128">windows10VpnConfiguration</span></span>](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|<span data-ttu-id="287a1-129">Actualizar las propiedades de un objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="287a1-129">Update the properties of a [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="287a1-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="287a1-130">Properties</span></span>
|<span data-ttu-id="287a1-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="287a1-131">Property</span></span>|<span data-ttu-id="287a1-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="287a1-132">Type</span></span>|<span data-ttu-id="287a1-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="287a1-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="287a1-134">id</span><span class="sxs-lookup"><span data-stu-id="287a1-134">id</span></span>|<span data-ttu-id="287a1-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-135">String</span></span>|<span data-ttu-id="287a1-136">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="287a1-136">Key of the entity.</span></span> <span data-ttu-id="287a1-137">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-137">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-138">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="287a1-138">lastModifiedDateTime</span></span>|<span data-ttu-id="287a1-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="287a1-139">DateTimeOffset</span></span>|<span data-ttu-id="287a1-140">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="287a1-140">DateTime the object was last modified.</span></span> <span data-ttu-id="287a1-141">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-141">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-142">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="287a1-142">roleScopeTagIds</span></span>|<span data-ttu-id="287a1-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="287a1-143">String collection</span></span>|<span data-ttu-id="287a1-144">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="287a1-144">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="287a1-145">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-145">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-146">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="287a1-146">supportsScopeTags</span></span>|<span data-ttu-id="287a1-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-147">Boolean</span></span>|<span data-ttu-id="287a1-148">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="287a1-148">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="287a1-149">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="287a1-149">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="287a1-150">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="287a1-150">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="287a1-151">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="287a1-151">This property is read-only.</span></span> <span data-ttu-id="287a1-152">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-152">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="287a1-153">createdDateTime</span></span>|<span data-ttu-id="287a1-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="287a1-154">DateTimeOffset</span></span>|<span data-ttu-id="287a1-155">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="287a1-155">DateTime the object was created.</span></span> <span data-ttu-id="287a1-156">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-156">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-157">descripción</span><span class="sxs-lookup"><span data-stu-id="287a1-157">description</span></span>|<span data-ttu-id="287a1-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-158">String</span></span>|<span data-ttu-id="287a1-159">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-159">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="287a1-160">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-160">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-161">displayName</span><span class="sxs-lookup"><span data-stu-id="287a1-161">displayName</span></span>|<span data-ttu-id="287a1-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-162">String</span></span>|<span data-ttu-id="287a1-163">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-163">Admin provided name of the device configuration.</span></span> <span data-ttu-id="287a1-164">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-164">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-165">version</span><span class="sxs-lookup"><span data-stu-id="287a1-165">version</span></span>|<span data-ttu-id="287a1-166">Int32</span><span class="sxs-lookup"><span data-stu-id="287a1-166">Int32</span></span>|<span data-ttu-id="287a1-167">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-167">Version of the device configuration.</span></span> <span data-ttu-id="287a1-168">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-168">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-169">connectionName</span><span class="sxs-lookup"><span data-stu-id="287a1-169">connectionName</span></span>|<span data-ttu-id="287a1-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-170">String</span></span>|<span data-ttu-id="287a1-171">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="287a1-171">Connection name displayed to the user.</span></span> <span data-ttu-id="287a1-172">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-172">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-173">servidores</span><span class="sxs-lookup"><span data-stu-id="287a1-173">servers</span></span>|<span data-ttu-id="287a1-174">colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-174">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="287a1-175">Lista de servidores VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="287a1-175">List of VPN Servers on the network.</span></span> <span data-ttu-id="287a1-176">Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="287a1-176">Make sure end users can access these network locations.</span></span> <span data-ttu-id="287a1-177">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="287a1-177">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="287a1-178">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-178">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-179">customXml</span><span class="sxs-lookup"><span data-stu-id="287a1-179">customXml</span></span>|<span data-ttu-id="287a1-180">Binario</span><span class="sxs-lookup"><span data-stu-id="287a1-180">Binary</span></span>|<span data-ttu-id="287a1-181">Comandos XML personalizados que configura la conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="287a1-181">Custom XML commands that configures the VPN connection.</span></span> <span data-ttu-id="287a1-182">(Matriz de bytes codificada UTF8) Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-182">(UTF8 encoded byte array) Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-183">profileTarget</span><span class="sxs-lookup"><span data-stu-id="287a1-183">profileTarget</span></span>|[<span data-ttu-id="287a1-184">windows10VpnProfileTarget</span><span class="sxs-lookup"><span data-stu-id="287a1-184">windows10VpnProfileTarget</span></span>](../resources/intune-deviceconfig-windows10vpnprofiletarget.md)|<span data-ttu-id="287a1-185">Tipo de perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="287a1-185">Profile target type.</span></span> <span data-ttu-id="287a1-186">Los valores posibles son: `user`, `device` y `autoPilotDevice`.</span><span class="sxs-lookup"><span data-stu-id="287a1-186">Possible values are: `user`, `device`, `autoPilotDevice`.</span></span>|
|<span data-ttu-id="287a1-187">connectionType</span><span class="sxs-lookup"><span data-stu-id="287a1-187">connectionType</span></span>|[<span data-ttu-id="287a1-188">windows10VpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="287a1-188">windows10VpnConnectionType</span></span>](../resources/intune-deviceconfig-windows10vpnconnectiontype.md)|<span data-ttu-id="287a1-189">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="287a1-189">Connection type.</span></span> <span data-ttu-id="287a1-190">Los valores posibles son: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `automatic`, `ikEv2`, `l2tp`, `pptp`, `citrix` y `paloAltoGlobalProtect`.</span><span class="sxs-lookup"><span data-stu-id="287a1-190">Possible values are: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `automatic`, `ikEv2`, `l2tp`, `pptp`, `citrix`, `paloAltoGlobalProtect`.</span></span>|
|<span data-ttu-id="287a1-191">enableSplitTunneling</span><span class="sxs-lookup"><span data-stu-id="287a1-191">enableSplitTunneling</span></span>|<span data-ttu-id="287a1-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-192">Boolean</span></span>|<span data-ttu-id="287a1-193">Habilitar túnel dividido.</span><span class="sxs-lookup"><span data-stu-id="287a1-193">Enable split tunneling.</span></span>|
|<span data-ttu-id="287a1-194">enableAlwaysOn</span><span class="sxs-lookup"><span data-stu-id="287a1-194">enableAlwaysOn</span></span>|<span data-ttu-id="287a1-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-195">Boolean</span></span>|<span data-ttu-id="287a1-196">Habilitar siempre en el modo.</span><span class="sxs-lookup"><span data-stu-id="287a1-196">Enable Always On mode.</span></span>|
|<span data-ttu-id="287a1-197">enableDeviceTunnel</span><span class="sxs-lookup"><span data-stu-id="287a1-197">enableDeviceTunnel</span></span>|<span data-ttu-id="287a1-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-198">Boolean</span></span>|<span data-ttu-id="287a1-199">Habilitar túnel de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-199">Enable device tunnel.</span></span>|
|<span data-ttu-id="287a1-200">enableDnsRegistration</span><span class="sxs-lookup"><span data-stu-id="287a1-200">enableDnsRegistration</span></span>|<span data-ttu-id="287a1-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-201">Boolean</span></span>|<span data-ttu-id="287a1-202">Habilitar el registro de dirección IP con DNS interno.</span><span class="sxs-lookup"><span data-stu-id="287a1-202">Enable IP address registration with internal DNS.</span></span>|
|<span data-ttu-id="287a1-203">dnsSuffixes</span><span class="sxs-lookup"><span data-stu-id="287a1-203">dnsSuffixes</span></span>|<span data-ttu-id="287a1-204">Colección String</span><span class="sxs-lookup"><span data-stu-id="287a1-204">String collection</span></span>|<span data-ttu-id="287a1-205">Especificar sufijos DNS para agregar a la lista de búsqueda DNS para enrutar correctamente los nombres cortos.</span><span class="sxs-lookup"><span data-stu-id="287a1-205">Specify DNS suffixes to add to the DNS search list to properly route short names.</span></span>|
|<span data-ttu-id="287a1-206">authenticationMethod</span><span class="sxs-lookup"><span data-stu-id="287a1-206">authenticationMethod</span></span>|[<span data-ttu-id="287a1-207">windows10VpnAuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="287a1-207">windows10VpnAuthenticationMethod</span></span>](../resources/intune-deviceconfig-windows10vpnauthenticationmethod.md)|<span data-ttu-id="287a1-208">Método de autenticación.</span><span class="sxs-lookup"><span data-stu-id="287a1-208">Authentication method.</span></span> <span data-ttu-id="287a1-209">Los valores posibles son: `certificate`, `usernameAndPassword` y `customEapXml`.</span><span class="sxs-lookup"><span data-stu-id="287a1-209">Possible values are: `certificate`, `usernameAndPassword`, `customEapXml`.</span></span>|
|<span data-ttu-id="287a1-210">rememberUserCredentials</span><span class="sxs-lookup"><span data-stu-id="287a1-210">rememberUserCredentials</span></span>|<span data-ttu-id="287a1-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-211">Boolean</span></span>|<span data-ttu-id="287a1-212">Recuerde que las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="287a1-212">Remember user credentials.</span></span>|
|<span data-ttu-id="287a1-213">enableConditionalAccess</span><span class="sxs-lookup"><span data-stu-id="287a1-213">enableConditionalAccess</span></span>|<span data-ttu-id="287a1-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-214">Boolean</span></span>|<span data-ttu-id="287a1-215">Habilite el acceso condicional.</span><span class="sxs-lookup"><span data-stu-id="287a1-215">Enable conditional access.</span></span>|
|<span data-ttu-id="287a1-216">enableSingleSignOnWithAlternateCertificate</span><span class="sxs-lookup"><span data-stu-id="287a1-216">enableSingleSignOnWithAlternateCertificate</span></span>|<span data-ttu-id="287a1-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-217">Boolean</span></span>|<span data-ttu-id="287a1-218">Habilitar sesión único (SSO) con certificado alternativa.</span><span class="sxs-lookup"><span data-stu-id="287a1-218">Enable single sign-on (SSO) with alternate certificate.</span></span>|
|<span data-ttu-id="287a1-219">singleSignOnEku</span><span class="sxs-lookup"><span data-stu-id="287a1-219">singleSignOnEku</span></span>|[<span data-ttu-id="287a1-220">ExtendeKeyUsage</span><span class="sxs-lookup"><span data-stu-id="287a1-220">extendedKeyUsage</span></span>](../resources/intune-deviceconfig-extendedkeyusage.md)|<span data-ttu-id="287a1-221">Single sign-on extendido clave (EKU).</span><span class="sxs-lookup"><span data-stu-id="287a1-221">Single sign-on Extended Key Usage (EKU).</span></span>|
|<span data-ttu-id="287a1-222">singleSignOnIssuerHash</span><span class="sxs-lookup"><span data-stu-id="287a1-222">singleSignOnIssuerHash</span></span>|<span data-ttu-id="287a1-223">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-223">String</span></span>|<span data-ttu-id="287a1-224">Hash de emisor de inicio de sesión único.</span><span class="sxs-lookup"><span data-stu-id="287a1-224">Single sign-on issuer hash.</span></span>|
|<span data-ttu-id="287a1-225">eapXml</span><span class="sxs-lookup"><span data-stu-id="287a1-225">eapXml</span></span>|<span data-ttu-id="287a1-226">Binario</span><span class="sxs-lookup"><span data-stu-id="287a1-226">Binary</span></span>|<span data-ttu-id="287a1-227">Protocolo de autenticación extensible (EAP) XML.</span><span class="sxs-lookup"><span data-stu-id="287a1-227">Extensible Authentication Protocol (EAP) XML.</span></span> <span data-ttu-id="287a1-228">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="287a1-228">(UTF8 encoded byte array)</span></span>|
|<span data-ttu-id="287a1-229">proxyServer</span><span class="sxs-lookup"><span data-stu-id="287a1-229">proxyServer</span></span>|[<span data-ttu-id="287a1-230">windows10VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="287a1-230">windows10VpnProxyServer</span></span>](../resources/intune-deviceconfig-windows10vpnproxyserver.md)|<span data-ttu-id="287a1-231">Servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="287a1-231">Proxy Server.</span></span>|
|<span data-ttu-id="287a1-232">associatedApps</span><span class="sxs-lookup"><span data-stu-id="287a1-232">associatedApps</span></span>|<span data-ttu-id="287a1-233">colección de [windows10AssociatedApps](../resources/intune-deviceconfig-windows10associatedapps.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-233">[windows10AssociatedApps](../resources/intune-deviceconfig-windows10associatedapps.md) collection</span></span>|<span data-ttu-id="287a1-234">Aplicaciones asociadas.</span><span class="sxs-lookup"><span data-stu-id="287a1-234">Associated Apps.</span></span> <span data-ttu-id="287a1-235">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="287a1-235">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="287a1-236">onlyAssociatedAppsCanUseConnection</span><span class="sxs-lookup"><span data-stu-id="287a1-236">onlyAssociatedAppsCanUseConnection</span></span>|<span data-ttu-id="287a1-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="287a1-237">Boolean</span></span>|<span data-ttu-id="287a1-238">Sólo las aplicaciones asociadas pueden utilizar conexión (VPN por aplicación).</span><span class="sxs-lookup"><span data-stu-id="287a1-238">Only associated Apps can use connection (per-app VPN).</span></span>|
|<span data-ttu-id="287a1-239">windowsInformationProtectionDomain</span><span class="sxs-lookup"><span data-stu-id="287a1-239">windowsInformationProtectionDomain</span></span>|<span data-ttu-id="287a1-240">Cadena</span><span class="sxs-lookup"><span data-stu-id="287a1-240">String</span></span>|<span data-ttu-id="287a1-241">Dominio de protección de información de Windows (curso) para asociar a esta conexión.</span><span class="sxs-lookup"><span data-stu-id="287a1-241">Windows Information Protection (WIP) domain to associate with this connection.</span></span>|
|<span data-ttu-id="287a1-242">trafficRules</span><span class="sxs-lookup"><span data-stu-id="287a1-242">trafficRules</span></span>|<span data-ttu-id="287a1-243">colección de [vpnTrafficRule](../resources/intune-deviceconfig-vpntrafficrule.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-243">[vpnTrafficRule](../resources/intune-deviceconfig-vpntrafficrule.md) collection</span></span>|<span data-ttu-id="287a1-244">Reglas de tráfico.</span><span class="sxs-lookup"><span data-stu-id="287a1-244">Traffic rules.</span></span> <span data-ttu-id="287a1-245">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="287a1-245">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="287a1-246">rutas</span><span class="sxs-lookup"><span data-stu-id="287a1-246">routes</span></span>|<span data-ttu-id="287a1-247">colección de [vpnRoute](../resources/intune-deviceconfig-vpnroute.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-247">[vpnRoute](../resources/intune-deviceconfig-vpnroute.md) collection</span></span>|<span data-ttu-id="287a1-248">Rutas (opcionales para los proveedores de terceros).</span><span class="sxs-lookup"><span data-stu-id="287a1-248">Routes (optional for third-party providers).</span></span> <span data-ttu-id="287a1-249">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="287a1-249">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="287a1-250">dnsRules</span><span class="sxs-lookup"><span data-stu-id="287a1-250">dnsRules</span></span>|<span data-ttu-id="287a1-251">colección de [vpnDnsRule](../resources/intune-deviceconfig-vpndnsrule.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-251">[vpnDnsRule](../resources/intune-deviceconfig-vpndnsrule.md) collection</span></span>|<span data-ttu-id="287a1-252">Reglas de DNS.</span><span class="sxs-lookup"><span data-stu-id="287a1-252">DNS rules.</span></span> <span data-ttu-id="287a1-253">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="287a1-253">This collection can contain a maximum of 1000 elements.</span></span>|

## <a name="relationships"></a><span data-ttu-id="287a1-254">Relaciones</span><span class="sxs-lookup"><span data-stu-id="287a1-254">Relationships</span></span>
|<span data-ttu-id="287a1-255">Relación</span><span class="sxs-lookup"><span data-stu-id="287a1-255">Relationship</span></span>|<span data-ttu-id="287a1-256">Tipo</span><span class="sxs-lookup"><span data-stu-id="287a1-256">Type</span></span>|<span data-ttu-id="287a1-257">Descripción</span><span class="sxs-lookup"><span data-stu-id="287a1-257">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="287a1-258">groupAssignments</span><span class="sxs-lookup"><span data-stu-id="287a1-258">groupAssignments</span></span>|<span data-ttu-id="287a1-259">colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-259">[deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) collection</span></span>|<span data-ttu-id="287a1-260">La lista de asignaciones de grupo para el perfil de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-260">The list of group assignments for the device configuration profile.</span></span> <span data-ttu-id="287a1-261">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-261">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-262">asignaciones</span><span class="sxs-lookup"><span data-stu-id="287a1-262">assignments</span></span>|<span data-ttu-id="287a1-263">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-263">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="287a1-264">La lista de tareas para el perfil de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-264">The list of assignments for the device configuration profile.</span></span> <span data-ttu-id="287a1-265">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-265">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-266">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="287a1-266">deviceStatuses</span></span>|<span data-ttu-id="287a1-267">Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-267">[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="287a1-268">Estado de instalación de configuración del dispositivo por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="287a1-268">Device configuration installation status by device.</span></span> <span data-ttu-id="287a1-269">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-269">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-270">userStatuses</span><span class="sxs-lookup"><span data-stu-id="287a1-270">userStatuses</span></span>|<span data-ttu-id="287a1-271">Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-271">[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="287a1-272">Estado de instalación de configuración de dispositivo por usuario.</span><span class="sxs-lookup"><span data-stu-id="287a1-272">Device configuration installation status by user.</span></span> <span data-ttu-id="287a1-273">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-273">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-274">deviceStatusOverview</span><span class="sxs-lookup"><span data-stu-id="287a1-274">deviceStatusOverview</span></span>|[<span data-ttu-id="287a1-275">deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="287a1-275">deviceConfigurationDeviceOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|<span data-ttu-id="287a1-276">Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-276">Device Configuration devices status overview Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-277">userStatusOverview</span><span class="sxs-lookup"><span data-stu-id="287a1-277">userStatusOverview</span></span>|[<span data-ttu-id="287a1-278">deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="287a1-278">deviceConfigurationUserOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|<span data-ttu-id="287a1-279">Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-279">Device Configuration users status overview Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-280">deviceSettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="287a1-280">deviceSettingStateSummaries</span></span>|<span data-ttu-id="287a1-281">Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-281">[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) collection</span></span>|<span data-ttu-id="287a1-282">Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="287a1-282">Device Configuration Setting State Device Summary Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="287a1-283">identityCertificate</span><span class="sxs-lookup"><span data-stu-id="287a1-283">identityCertificate</span></span>|[<span data-ttu-id="287a1-284">windowsCertificateProfileBase</span><span class="sxs-lookup"><span data-stu-id="287a1-284">windowsCertificateProfileBase</span></span>](../resources/intune-deviceconfig-windowscertificateprofilebase.md)|<span data-ttu-id="287a1-285">Certificado de identidad para la autenticación de cliente al método de autenticación es el certificado.</span><span class="sxs-lookup"><span data-stu-id="287a1-285">Identity certificate for client authentication when authentication method is certificate.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="287a1-286">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="287a1-286">JSON Representation</span></span>
<span data-ttu-id="287a1-287">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="287a1-287">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10VpnConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10VpnConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "connectionName": "String",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "String",
      "address": "String",
      "isDefaultServer": true
    }
  ],
  "customXml": "binary",
  "profileTarget": "String",
  "connectionType": "String",
  "enableSplitTunneling": true,
  "enableAlwaysOn": true,
  "enableDeviceTunnel": true,
  "enableDnsRegistration": true,
  "dnsSuffixes": [
    "String"
  ],
  "authenticationMethod": "String",
  "rememberUserCredentials": true,
  "enableConditionalAccess": true,
  "enableSingleSignOnWithAlternateCertificate": true,
  "singleSignOnEku": {
    "@odata.type": "microsoft.graph.extendedKeyUsage",
    "name": "String",
    "objectIdentifier": "String"
  },
  "singleSignOnIssuerHash": "String",
  "eapXml": "binary",
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows10VpnProxyServer",
    "automaticConfigurationScriptUrl": "String",
    "address": "String",
    "port": 1024,
    "bypassProxyServerForLocalAddress": true
  },
  "associatedApps": [
    {
      "@odata.type": "microsoft.graph.windows10AssociatedApps",
      "appType": "String",
      "identifier": "String"
    }
  ],
  "onlyAssociatedAppsCanUseConnection": true,
  "windowsInformationProtectionDomain": "String",
  "trafficRules": [
    {
      "@odata.type": "microsoft.graph.vpnTrafficRule",
      "name": "String",
      "protocols": 1024,
      "localPortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 1024,
          "upperNumber": 1024
        }
      ],
      "remotePortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 1024,
          "upperNumber": 1024
        }
      ],
      "localAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ],
      "remoteAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ],
      "appId": "String",
      "appType": "String",
      "routingPolicyType": "String",
      "claims": "String"
    }
  ],
  "routes": [
    {
      "@odata.type": "microsoft.graph.vpnRoute",
      "destinationPrefix": "String",
      "prefixSize": 1024
    }
  ],
  "dnsRules": [
    {
      "@odata.type": "microsoft.graph.vpnDnsRule",
      "name": "String",
      "servers": [
        "String"
      ],
      "proxyServerUri": "String"
    }
  ]
}
```





