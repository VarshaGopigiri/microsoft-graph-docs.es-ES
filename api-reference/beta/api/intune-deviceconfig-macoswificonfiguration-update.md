---
title: Actualizar macOSWiFiConfiguration
description: Actualizar las propiedades de un objeto macOSWiFiConfiguration.
ms.openlocfilehash: 908e569f4ab4703a387fe5f8df6d66380a8ae5c0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084842"
---
# <a name="update-macoswificonfiguration"></a><span data-ttu-id="b02bd-103">Actualizar macOSWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="b02bd-103">Update macOSWiFiConfiguration</span></span>

> <span data-ttu-id="b02bd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b02bd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b02bd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b02bd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b02bd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b02bd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b02bd-107">Actualizar las propiedades de un objeto [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b02bd-107">Update the properties of a [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b02bd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b02bd-108">Prerequisites</span></span>
<span data-ttu-id="b02bd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b02bd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b02bd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b02bd-111">Permission type</span></span>|<span data-ttu-id="b02bd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b02bd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b02bd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b02bd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b02bd-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b02bd-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b02bd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b02bd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b02bd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b02bd-116">Not supported.</span></span>|
|<span data-ttu-id="b02bd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b02bd-117">Application</span></span>|<span data-ttu-id="b02bd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b02bd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b02bd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b02bd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="b02bd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b02bd-120">Request headers</span></span>
|<span data-ttu-id="b02bd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b02bd-121">Header</span></span>|<span data-ttu-id="b02bd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b02bd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b02bd-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="b02bd-123">Authorization</span></span>|<span data-ttu-id="b02bd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b02bd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b02bd-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b02bd-125">Accept</span></span>|<span data-ttu-id="b02bd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b02bd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b02bd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b02bd-127">Request body</span></span>
<span data-ttu-id="b02bd-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b02bd-128">In the request body, supply a JSON representation for the [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) object.</span></span>

<span data-ttu-id="b02bd-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b02bd-129">The following table shows the properties that are required when you create the [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md).</span></span>

|<span data-ttu-id="b02bd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b02bd-130">Property</span></span>|<span data-ttu-id="b02bd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b02bd-131">Type</span></span>|<span data-ttu-id="b02bd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b02bd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b02bd-133">id</span><span class="sxs-lookup"><span data-stu-id="b02bd-133">id</span></span>|<span data-ttu-id="b02bd-134">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-134">String</span></span>|<span data-ttu-id="b02bd-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b02bd-135">Key of the entity.</span></span> <span data-ttu-id="b02bd-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b02bd-137">lastModifiedDateTime</span></span>|<span data-ttu-id="b02bd-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b02bd-138">DateTimeOffset</span></span>|<span data-ttu-id="b02bd-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="b02bd-139">DateTime the object was last modified.</span></span> <span data-ttu-id="b02bd-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="b02bd-141">roleScopeTagIds</span></span>|<span data-ttu-id="b02bd-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="b02bd-142">String collection</span></span>|<span data-ttu-id="b02bd-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="b02bd-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="b02bd-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="b02bd-145">supportsScopeTags</span></span>|<span data-ttu-id="b02bd-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="b02bd-146">Boolean</span></span>|<span data-ttu-id="b02bd-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="b02bd-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="b02bd-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="b02bd-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="b02bd-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="b02bd-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="b02bd-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="b02bd-150">This property is read-only.</span></span> <span data-ttu-id="b02bd-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b02bd-152">createdDateTime</span></span>|<span data-ttu-id="b02bd-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b02bd-153">DateTimeOffset</span></span>|<span data-ttu-id="b02bd-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="b02bd-154">DateTime the object was created.</span></span> <span data-ttu-id="b02bd-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-156">descripción</span><span class="sxs-lookup"><span data-stu-id="b02bd-156">description</span></span>|<span data-ttu-id="b02bd-157">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-157">String</span></span>|<span data-ttu-id="b02bd-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b02bd-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b02bd-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-160">displayName</span><span class="sxs-lookup"><span data-stu-id="b02bd-160">displayName</span></span>|<span data-ttu-id="b02bd-161">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-161">String</span></span>|<span data-ttu-id="b02bd-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b02bd-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b02bd-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-164">version</span><span class="sxs-lookup"><span data-stu-id="b02bd-164">version</span></span>|<span data-ttu-id="b02bd-165">Int32</span><span class="sxs-lookup"><span data-stu-id="b02bd-165">Int32</span></span>|<span data-ttu-id="b02bd-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b02bd-166">Version of the device configuration.</span></span> <span data-ttu-id="b02bd-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b02bd-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b02bd-168">networkName</span><span class="sxs-lookup"><span data-stu-id="b02bd-168">networkName</span></span>|<span data-ttu-id="b02bd-169">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-169">String</span></span>|<span data-ttu-id="b02bd-170">Nombre de red</span><span class="sxs-lookup"><span data-stu-id="b02bd-170">Network Name</span></span>|
|<span data-ttu-id="b02bd-171">SSID</span><span class="sxs-lookup"><span data-stu-id="b02bd-171">ssid</span></span>|<span data-ttu-id="b02bd-172">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-172">String</span></span>|<span data-ttu-id="b02bd-173">Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b02bd-173">This is the name of the Wi-Fi network that is broadcast to all devices.</span></span>|
|<span data-ttu-id="b02bd-174">connectAutomatically</span><span class="sxs-lookup"><span data-stu-id="b02bd-174">connectAutomatically</span></span>|<span data-ttu-id="b02bd-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="b02bd-175">Boolean</span></span>|<span data-ttu-id="b02bd-176">Conectar automáticamente cuando esta red esté en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="b02bd-176">Connect automatically when this network is in range.</span></span> <span data-ttu-id="b02bd-177">Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="b02bd-177">Setting this to true will skip the user prompt and automatically connect the device to Wi-Fi network.</span></span>|
|<span data-ttu-id="b02bd-178">connectWhenNetworkNameIsHidden</span><span class="sxs-lookup"><span data-stu-id="b02bd-178">connectWhenNetworkNameIsHidden</span></span>|<span data-ttu-id="b02bd-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="b02bd-179">Boolean</span></span>|<span data-ttu-id="b02bd-180">Conectar cuando la red no sea de difusión su nombre (SSID).</span><span class="sxs-lookup"><span data-stu-id="b02bd-180">Connect when the network is not broadcasting its name (SSID).</span></span> <span data-ttu-id="b02bd-181">Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b02bd-181">When set to true, this profile forces the device to connect to a network that doesn't broadcast its SSID to all devices.</span></span>|
|<span data-ttu-id="b02bd-182">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="b02bd-182">wiFiSecurityType</span></span>|[<span data-ttu-id="b02bd-183">wiFiSecurityType</span><span class="sxs-lookup"><span data-stu-id="b02bd-183">wiFiSecurityType</span></span>](../resources/intune-deviceconfig-wifisecuritytype.md)|<span data-ttu-id="b02bd-184">Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b02bd-184">Indicates whether Wi-Fi endpoint uses an EAP based security type.</span></span> <span data-ttu-id="b02bd-185">Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span><span class="sxs-lookup"><span data-stu-id="b02bd-185">Possible values are: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.</span></span>|
|<span data-ttu-id="b02bd-186">proxySettings</span><span class="sxs-lookup"><span data-stu-id="b02bd-186">proxySettings</span></span>|[<span data-ttu-id="b02bd-187">wiFiProxySetting</span><span class="sxs-lookup"><span data-stu-id="b02bd-187">wiFiProxySetting</span></span>](../resources/intune-deviceconfig-wifiproxysetting.md)|<span data-ttu-id="b02bd-188">Tipo de proxy para esta conexión Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="b02bd-188">Proxy Type for this Wi-Fi connection.</span></span> <span data-ttu-id="b02bd-189">Los valores posibles son: `none`, `manual` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="b02bd-189">Possible values are: `none`, `manual`, `automatic`.</span></span>|
|<span data-ttu-id="b02bd-190">proxyManualAddress</span><span class="sxs-lookup"><span data-stu-id="b02bd-190">proxyManualAddress</span></span>|<span data-ttu-id="b02bd-191">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-191">String</span></span>|<span data-ttu-id="b02bd-192">Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="b02bd-192">IP Address or DNS hostname of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="b02bd-193">proxyManualPort</span><span class="sxs-lookup"><span data-stu-id="b02bd-193">proxyManualPort</span></span>|<span data-ttu-id="b02bd-194">Int32</span><span class="sxs-lookup"><span data-stu-id="b02bd-194">Int32</span></span>|<span data-ttu-id="b02bd-195">Puerto del servidor proxy cuando se selecciona la configuración manual.</span><span class="sxs-lookup"><span data-stu-id="b02bd-195">Port of the proxy server when manual configuration is selected.</span></span>|
|<span data-ttu-id="b02bd-196">proxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="b02bd-196">proxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="b02bd-197">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-197">String</span></span>|<span data-ttu-id="b02bd-198">URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="b02bd-198">URL of the proxy server automatic configuration script when automatic configuration is selected.</span></span> <span data-ttu-id="b02bd-199">Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="b02bd-199">This URL is typically the location of PAC (Proxy Auto Configuration) file.</span></span>|
|<span data-ttu-id="b02bd-200">preSharedKey</span><span class="sxs-lookup"><span data-stu-id="b02bd-200">preSharedKey</span></span>|<span data-ttu-id="b02bd-201">String</span><span class="sxs-lookup"><span data-stu-id="b02bd-201">String</span></span>|<span data-ttu-id="b02bd-202">Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.</span><span class="sxs-lookup"><span data-stu-id="b02bd-202">This is the pre-shared key for WPA Personal Wi-Fi network.</span></span>|



## <a name="response"></a><span data-ttu-id="b02bd-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b02bd-203">Response</span></span>
<span data-ttu-id="b02bd-204">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b02bd-204">If successful, this method returns a `200 OK` response code and an updated [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b02bd-205">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b02bd-205">Example</span></span>
### <a name="request"></a><span data-ttu-id="b02bd-206">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b02bd-206">Request</span></span>
<span data-ttu-id="b02bd-207">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b02bd-207">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 680

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value"
}
```

### <a name="response"></a><span data-ttu-id="b02bd-208">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b02bd-208">Response</span></span>
<span data-ttu-id="b02bd-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b02bd-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 849

{
  "@odata.type": "#microsoft.graph.macOSWiFiConfiguration",
  "id": "471203fb-03fb-4712-fb03-1247fb031247",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value"
}
```





