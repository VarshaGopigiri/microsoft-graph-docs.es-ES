---
title: Crear windows81VpnConfiguration
description: Crear un nuevo objeto windows81VpnConfiguration.
ms.openlocfilehash: 7bf50bacf245a020ba72084ead62a545d59a93c6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088979"
---
# <a name="create-windows81vpnconfiguration"></a><span data-ttu-id="4634c-103">Crear windows81VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="4634c-103">Create windows81VpnConfiguration</span></span>

> <span data-ttu-id="4634c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4634c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4634c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4634c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4634c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4634c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4634c-107">Crear un nuevo objeto [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="4634c-107">Create a new [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4634c-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4634c-108">Prerequisites</span></span>
<span data-ttu-id="4634c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4634c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4634c-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4634c-111">Permission type</span></span>|<span data-ttu-id="4634c-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4634c-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4634c-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4634c-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4634c-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4634c-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4634c-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4634c-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4634c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4634c-116">Not supported.</span></span>|
|<span data-ttu-id="4634c-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4634c-117">Application</span></span>|<span data-ttu-id="4634c-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4634c-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4634c-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4634c-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="4634c-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4634c-120">Request headers</span></span>
|<span data-ttu-id="4634c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4634c-121">Header</span></span>|<span data-ttu-id="4634c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4634c-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4634c-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="4634c-123">Authorization</span></span>|<span data-ttu-id="4634c-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4634c-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4634c-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4634c-125">Accept</span></span>|<span data-ttu-id="4634c-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4634c-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4634c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4634c-127">Request body</span></span>
<span data-ttu-id="4634c-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows81VpnConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4634c-128">In the request body, supply a JSON representation for the windows81VpnConfiguration object.</span></span>

<span data-ttu-id="4634c-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows81VpnConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4634c-129">The following table shows the properties that are required when you create the windows81VpnConfiguration.</span></span>

|<span data-ttu-id="4634c-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4634c-130">Property</span></span>|<span data-ttu-id="4634c-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4634c-131">Type</span></span>|<span data-ttu-id="4634c-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4634c-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4634c-133">id</span><span class="sxs-lookup"><span data-stu-id="4634c-133">id</span></span>|<span data-ttu-id="4634c-134">String</span><span class="sxs-lookup"><span data-stu-id="4634c-134">String</span></span>|<span data-ttu-id="4634c-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4634c-135">Key of the entity.</span></span> <span data-ttu-id="4634c-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4634c-137">lastModifiedDateTime</span></span>|<span data-ttu-id="4634c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4634c-138">DateTimeOffset</span></span>|<span data-ttu-id="4634c-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="4634c-139">DateTime the object was last modified.</span></span> <span data-ttu-id="4634c-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="4634c-141">roleScopeTagIds</span></span>|<span data-ttu-id="4634c-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="4634c-142">String collection</span></span>|<span data-ttu-id="4634c-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="4634c-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="4634c-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="4634c-145">supportsScopeTags</span></span>|<span data-ttu-id="4634c-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="4634c-146">Boolean</span></span>|<span data-ttu-id="4634c-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4634c-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="4634c-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="4634c-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="4634c-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="4634c-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="4634c-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="4634c-150">This property is read-only.</span></span> <span data-ttu-id="4634c-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4634c-152">createdDateTime</span></span>|<span data-ttu-id="4634c-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4634c-153">DateTimeOffset</span></span>|<span data-ttu-id="4634c-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="4634c-154">DateTime the object was created.</span></span> <span data-ttu-id="4634c-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-156">descripción</span><span class="sxs-lookup"><span data-stu-id="4634c-156">description</span></span>|<span data-ttu-id="4634c-157">String</span><span class="sxs-lookup"><span data-stu-id="4634c-157">String</span></span>|<span data-ttu-id="4634c-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4634c-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="4634c-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-160">displayName</span><span class="sxs-lookup"><span data-stu-id="4634c-160">displayName</span></span>|<span data-ttu-id="4634c-161">String</span><span class="sxs-lookup"><span data-stu-id="4634c-161">String</span></span>|<span data-ttu-id="4634c-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4634c-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="4634c-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-164">version</span><span class="sxs-lookup"><span data-stu-id="4634c-164">version</span></span>|<span data-ttu-id="4634c-165">Int32</span><span class="sxs-lookup"><span data-stu-id="4634c-165">Int32</span></span>|<span data-ttu-id="4634c-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4634c-166">Version of the device configuration.</span></span> <span data-ttu-id="4634c-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-168">connectionName</span><span class="sxs-lookup"><span data-stu-id="4634c-168">connectionName</span></span>|<span data-ttu-id="4634c-169">String</span><span class="sxs-lookup"><span data-stu-id="4634c-169">String</span></span>|<span data-ttu-id="4634c-170">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="4634c-170">Connection name displayed to the user.</span></span> <span data-ttu-id="4634c-171">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-171">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-172">servidores</span><span class="sxs-lookup"><span data-stu-id="4634c-172">servers</span></span>|<span data-ttu-id="4634c-173">colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-173">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="4634c-174">Lista de servidores VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="4634c-174">List of VPN Servers on the network.</span></span> <span data-ttu-id="4634c-175">Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="4634c-175">Make sure end users can access these network locations.</span></span> <span data-ttu-id="4634c-176">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="4634c-176">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="4634c-177">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-177">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-178">customXml</span><span class="sxs-lookup"><span data-stu-id="4634c-178">customXml</span></span>|<span data-ttu-id="4634c-179">Binario</span><span class="sxs-lookup"><span data-stu-id="4634c-179">Binary</span></span>|<span data-ttu-id="4634c-180">Comandos XML personalizados que configura la conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="4634c-180">Custom XML commands that configures the VPN connection.</span></span> <span data-ttu-id="4634c-181">(Matriz de bytes codificada UTF8) Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4634c-181">(UTF8 encoded byte array) Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="4634c-182">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="4634c-182">applyOnlyToWindows81</span></span>|<span data-ttu-id="4634c-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="4634c-183">Boolean</span></span>|<span data-ttu-id="4634c-184">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4634c-184">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="4634c-185">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4634c-185">This property is read-only.</span></span>|
|<span data-ttu-id="4634c-186">connectionType</span><span class="sxs-lookup"><span data-stu-id="4634c-186">connectionType</span></span>|[<span data-ttu-id="4634c-187">windowsVpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="4634c-187">windowsVpnConnectionType</span></span>](../resources/intune-deviceconfig-windowsvpnconnectiontype.md)|<span data-ttu-id="4634c-188">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="4634c-188">Connection type.</span></span> <span data-ttu-id="4634c-189">Los valores posibles son: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect` y `checkPointCapsuleVpn`.</span><span class="sxs-lookup"><span data-stu-id="4634c-189">Possible values are: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`.</span></span>|
|<span data-ttu-id="4634c-190">loginGroupOrDomain</span><span class="sxs-lookup"><span data-stu-id="4634c-190">loginGroupOrDomain</span></span>|<span data-ttu-id="4634c-191">String</span><span class="sxs-lookup"><span data-stu-id="4634c-191">String</span></span>|<span data-ttu-id="4634c-192">Grupo de inicio de sesión o dominio cuando se establece el tipo de conexión a Dell SonicWALL Mobile conexión.</span><span class="sxs-lookup"><span data-stu-id="4634c-192">Login group or domain when connection type is set to Dell SonicWALL Mobile Connection.</span></span>|
|<span data-ttu-id="4634c-193">enableSplitTunneling</span><span class="sxs-lookup"><span data-stu-id="4634c-193">enableSplitTunneling</span></span>|<span data-ttu-id="4634c-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="4634c-194">Boolean</span></span>|<span data-ttu-id="4634c-195">Habilitar túnel dividido para la VPN.</span><span class="sxs-lookup"><span data-stu-id="4634c-195">Enable split tunneling for the VPN.</span></span>|
|<span data-ttu-id="4634c-196">proxyServer</span><span class="sxs-lookup"><span data-stu-id="4634c-196">proxyServer</span></span>|[<span data-ttu-id="4634c-197">windows81VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="4634c-197">windows81VpnProxyServer</span></span>](../resources/intune-deviceconfig-windows81vpnproxyserver.md)|<span data-ttu-id="4634c-198">Servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="4634c-198">Proxy Server.</span></span>|



## <a name="response"></a><span data-ttu-id="4634c-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4634c-199">Response</span></span>
<span data-ttu-id="4634c-200">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4634c-200">If successful, this method returns a `201 Created` response code and a [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4634c-201">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4634c-201">Example</span></span>
### <a name="request"></a><span data-ttu-id="4634c-202">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4634c-202">Request</span></span>
<span data-ttu-id="4634c-203">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4634c-203">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1079

{
  "@odata.type": "#microsoft.graph.windows81VpnConfiguration",
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
  "applyOnlyToWindows81": true,
  "connectionType": "f5EdgeClient",
  "loginGroupOrDomain": "Login Group Or Domain value",
  "enableSplitTunneling": true,
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows81VpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4,
    "automaticallyDetectProxySettings": true,
    "bypassProxyServerForLocalAddress": true
  }
}
```

### <a name="response"></a><span data-ttu-id="4634c-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4634c-204">Response</span></span>
<span data-ttu-id="4634c-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4634c-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1187

{
  "@odata.type": "#microsoft.graph.windows81VpnConfiguration",
  "id": "6aa07da3-7da3-6aa0-a37d-a06aa37da06a",
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
  "applyOnlyToWindows81": true,
  "connectionType": "f5EdgeClient",
  "loginGroupOrDomain": "Login Group Or Domain value",
  "enableSplitTunneling": true,
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows81VpnProxyServer",
    "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
    "address": "Address value",
    "port": 4,
    "automaticallyDetectProxySettings": true,
    "bypassProxyServerForLocalAddress": true
  }
}
```




