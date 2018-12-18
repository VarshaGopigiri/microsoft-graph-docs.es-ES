---
title: Actualizar windows81VpnConfiguration
description: Actualizar las propiedades de un objeto windows81VpnConfiguration.
author: tfitzmac
ms.openlocfilehash: cabc382272c1943dce8361dd35c29c5b0f397826
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355345"
---
# <a name="update-windows81vpnconfiguration"></a><span data-ttu-id="2a74f-103">Actualizar windows81VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a74f-103">Update windows81VpnConfiguration</span></span>

> <span data-ttu-id="2a74f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2a74f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2a74f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2a74f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2a74f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2a74f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2a74f-107">Actualizar las propiedades de un objeto [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2a74f-107">Update the properties of a [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2a74f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2a74f-108">Prerequisites</span></span>
<span data-ttu-id="2a74f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2a74f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2a74f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2a74f-111">Permission type</span></span>|<span data-ttu-id="2a74f-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2a74f-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2a74f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2a74f-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2a74f-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2a74f-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2a74f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2a74f-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2a74f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a74f-116">Not supported.</span></span>|
|<span data-ttu-id="2a74f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2a74f-117">Application</span></span>|<span data-ttu-id="2a74f-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2a74f-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2a74f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a74f-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="2a74f-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a74f-120">Request headers</span></span>
|<span data-ttu-id="2a74f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a74f-121">Header</span></span>|<span data-ttu-id="2a74f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2a74f-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2a74f-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2a74f-123">Authorization</span></span>|<span data-ttu-id="2a74f-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2a74f-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2a74f-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2a74f-125">Accept</span></span>|<span data-ttu-id="2a74f-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2a74f-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2a74f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a74f-127">Request body</span></span>
<span data-ttu-id="2a74f-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2a74f-128">In the request body, supply a JSON representation for the [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) object.</span></span>

<span data-ttu-id="2a74f-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="2a74f-129">The following table shows the properties that are required when you create the [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md).</span></span>

|<span data-ttu-id="2a74f-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a74f-130">Property</span></span>|<span data-ttu-id="2a74f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a74f-131">Type</span></span>|<span data-ttu-id="2a74f-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a74f-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2a74f-133">id</span><span class="sxs-lookup"><span data-stu-id="2a74f-133">id</span></span>|<span data-ttu-id="2a74f-134">String</span><span class="sxs-lookup"><span data-stu-id="2a74f-134">String</span></span>|<span data-ttu-id="2a74f-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2a74f-135">Key of the entity.</span></span> <span data-ttu-id="2a74f-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2a74f-137">lastModifiedDateTime</span></span>|<span data-ttu-id="2a74f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2a74f-138">DateTimeOffset</span></span>|<span data-ttu-id="2a74f-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="2a74f-139">DateTime the object was last modified.</span></span> <span data-ttu-id="2a74f-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="2a74f-141">roleScopeTagIds</span></span>|<span data-ttu-id="2a74f-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="2a74f-142">String collection</span></span>|<span data-ttu-id="2a74f-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="2a74f-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="2a74f-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="2a74f-145">supportsScopeTags</span></span>|<span data-ttu-id="2a74f-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="2a74f-146">Boolean</span></span>|<span data-ttu-id="2a74f-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2a74f-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="2a74f-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="2a74f-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="2a74f-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="2a74f-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="2a74f-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="2a74f-150">This property is read-only.</span></span> <span data-ttu-id="2a74f-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2a74f-152">createdDateTime</span></span>|<span data-ttu-id="2a74f-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2a74f-153">DateTimeOffset</span></span>|<span data-ttu-id="2a74f-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="2a74f-154">DateTime the object was created.</span></span> <span data-ttu-id="2a74f-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-156">descripción</span><span class="sxs-lookup"><span data-stu-id="2a74f-156">description</span></span>|<span data-ttu-id="2a74f-157">String</span><span class="sxs-lookup"><span data-stu-id="2a74f-157">String</span></span>|<span data-ttu-id="2a74f-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a74f-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="2a74f-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-160">displayName</span><span class="sxs-lookup"><span data-stu-id="2a74f-160">displayName</span></span>|<span data-ttu-id="2a74f-161">String</span><span class="sxs-lookup"><span data-stu-id="2a74f-161">String</span></span>|<span data-ttu-id="2a74f-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a74f-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="2a74f-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-164">version</span><span class="sxs-lookup"><span data-stu-id="2a74f-164">version</span></span>|<span data-ttu-id="2a74f-165">Int32</span><span class="sxs-lookup"><span data-stu-id="2a74f-165">Int32</span></span>|<span data-ttu-id="2a74f-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a74f-166">Version of the device configuration.</span></span> <span data-ttu-id="2a74f-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-168">connectionName</span><span class="sxs-lookup"><span data-stu-id="2a74f-168">connectionName</span></span>|<span data-ttu-id="2a74f-169">String</span><span class="sxs-lookup"><span data-stu-id="2a74f-169">String</span></span>|<span data-ttu-id="2a74f-170">Nombre de la conexión que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="2a74f-170">Connection name displayed to the user.</span></span> <span data-ttu-id="2a74f-171">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-171">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-172">servidores</span><span class="sxs-lookup"><span data-stu-id="2a74f-172">servers</span></span>|<span data-ttu-id="2a74f-173">colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-173">[vpnServer](../resources/intune-deviceconfig-vpnserver.md) collection</span></span>|<span data-ttu-id="2a74f-174">Lista de servidores VPN en la red.</span><span class="sxs-lookup"><span data-stu-id="2a74f-174">List of VPN Servers on the network.</span></span> <span data-ttu-id="2a74f-175">Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="2a74f-175">Make sure end users can access these network locations.</span></span> <span data-ttu-id="2a74f-176">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="2a74f-176">This collection can contain a maximum of 500 elements.</span></span> <span data-ttu-id="2a74f-177">Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-177">Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-178">customXml</span><span class="sxs-lookup"><span data-stu-id="2a74f-178">customXml</span></span>|<span data-ttu-id="2a74f-179">Binario</span><span class="sxs-lookup"><span data-stu-id="2a74f-179">Binary</span></span>|<span data-ttu-id="2a74f-180">Comandos XML personalizados que configura la conexión VPN.</span><span class="sxs-lookup"><span data-stu-id="2a74f-180">Custom XML commands that configures the VPN connection.</span></span> <span data-ttu-id="2a74f-181">(Matriz de bytes codificada UTF8) Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="2a74f-181">(UTF8 encoded byte array) Inherited from [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)</span></span>|
|<span data-ttu-id="2a74f-182">applyOnlyToWindows81</span><span class="sxs-lookup"><span data-stu-id="2a74f-182">applyOnlyToWindows81</span></span>|<span data-ttu-id="2a74f-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="2a74f-183">Boolean</span></span>|<span data-ttu-id="2a74f-184">Valor que indica si esta directiva se aplica solo a Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="2a74f-184">Value indicating whether this policy only applies to Windows 8.1.</span></span> <span data-ttu-id="2a74f-185">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2a74f-185">This property is read-only.</span></span>|
|<span data-ttu-id="2a74f-186">connectionType</span><span class="sxs-lookup"><span data-stu-id="2a74f-186">connectionType</span></span>|[<span data-ttu-id="2a74f-187">windowsVpnConnectionType</span><span class="sxs-lookup"><span data-stu-id="2a74f-187">windowsVpnConnectionType</span></span>](../resources/intune-deviceconfig-windowsvpnconnectiontype.md)|<span data-ttu-id="2a74f-188">Tipo de conexión.</span><span class="sxs-lookup"><span data-stu-id="2a74f-188">Connection type.</span></span> <span data-ttu-id="2a74f-189">Los valores posibles son: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect` y `checkPointCapsuleVpn`.</span><span class="sxs-lookup"><span data-stu-id="2a74f-189">Possible values are: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`.</span></span>|
|<span data-ttu-id="2a74f-190">loginGroupOrDomain</span><span class="sxs-lookup"><span data-stu-id="2a74f-190">loginGroupOrDomain</span></span>|<span data-ttu-id="2a74f-191">String</span><span class="sxs-lookup"><span data-stu-id="2a74f-191">String</span></span>|<span data-ttu-id="2a74f-192">Grupo de inicio de sesión o dominio cuando se establece el tipo de conexión a Dell SonicWALL Mobile conexión.</span><span class="sxs-lookup"><span data-stu-id="2a74f-192">Login group or domain when connection type is set to Dell SonicWALL Mobile Connection.</span></span>|
|<span data-ttu-id="2a74f-193">enableSplitTunneling</span><span class="sxs-lookup"><span data-stu-id="2a74f-193">enableSplitTunneling</span></span>|<span data-ttu-id="2a74f-194">Boolean</span><span class="sxs-lookup"><span data-stu-id="2a74f-194">Boolean</span></span>|<span data-ttu-id="2a74f-195">Habilitar túnel dividido para la VPN.</span><span class="sxs-lookup"><span data-stu-id="2a74f-195">Enable split tunneling for the VPN.</span></span>|
|<span data-ttu-id="2a74f-196">proxyServer</span><span class="sxs-lookup"><span data-stu-id="2a74f-196">proxyServer</span></span>|[<span data-ttu-id="2a74f-197">windows81VpnProxyServer</span><span class="sxs-lookup"><span data-stu-id="2a74f-197">windows81VpnProxyServer</span></span>](../resources/intune-deviceconfig-windows81vpnproxyserver.md)|<span data-ttu-id="2a74f-198">Servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="2a74f-198">Proxy Server.</span></span>|



## <a name="response"></a><span data-ttu-id="2a74f-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a74f-199">Response</span></span>
<span data-ttu-id="2a74f-200">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a74f-200">If successful, this method returns a `200 OK` response code and an updated [windows81VpnConfiguration](../resources/intune-deviceconfig-windows81vpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2a74f-201">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a74f-201">Example</span></span>
### <a name="request"></a><span data-ttu-id="2a74f-202">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a74f-202">Request</span></span>
<span data-ttu-id="2a74f-203">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a74f-203">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1015

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

### <a name="response"></a><span data-ttu-id="2a74f-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a74f-204">Response</span></span>
<span data-ttu-id="2a74f-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a74f-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





