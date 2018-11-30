---
title: Crear windows10NetworkBoundaryConfiguration
description: Crear un nuevo objeto windows10NetworkBoundaryConfiguration.
ms.openlocfilehash: 23ecf0e8b223f0aa7ac36a1d8406ccd1f56d4bc9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090509"
---
# <a name="create-windows10networkboundaryconfiguration"></a><span data-ttu-id="8578e-103">Crear windows10NetworkBoundaryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8578e-103">Create windows10NetworkBoundaryConfiguration</span></span>

> <span data-ttu-id="8578e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8578e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8578e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8578e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8578e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8578e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8578e-107">Crear un nuevo objeto [windows10NetworkBoundaryConfiguration](../resources/intune-deviceconfig-windows10networkboundaryconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="8578e-107">Create a new [windows10NetworkBoundaryConfiguration](../resources/intune-deviceconfig-windows10networkboundaryconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8578e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8578e-108">Prerequisites</span></span>
<span data-ttu-id="8578e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8578e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8578e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8578e-111">Permission type</span></span>|<span data-ttu-id="8578e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8578e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8578e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8578e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8578e-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8578e-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8578e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8578e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8578e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8578e-116">Not supported.</span></span>|
|<span data-ttu-id="8578e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8578e-117">Application</span></span>|<span data-ttu-id="8578e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8578e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8578e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8578e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="8578e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8578e-120">Request headers</span></span>
|<span data-ttu-id="8578e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8578e-121">Header</span></span>|<span data-ttu-id="8578e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8578e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8578e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8578e-123">Authorization</span></span>|<span data-ttu-id="8578e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8578e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8578e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8578e-125">Accept</span></span>|<span data-ttu-id="8578e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8578e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8578e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8578e-127">Request body</span></span>
<span data-ttu-id="8578e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windows10NetworkBoundaryConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8578e-128">In the request body, supply a JSON representation for the windows10NetworkBoundaryConfiguration object.</span></span>

<span data-ttu-id="8578e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windows10NetworkBoundaryConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8578e-129">The following table shows the properties that are required when you create the windows10NetworkBoundaryConfiguration.</span></span>

|<span data-ttu-id="8578e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8578e-130">Property</span></span>|<span data-ttu-id="8578e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8578e-131">Type</span></span>|<span data-ttu-id="8578e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8578e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8578e-133">id</span><span class="sxs-lookup"><span data-stu-id="8578e-133">id</span></span>|<span data-ttu-id="8578e-134">String</span><span class="sxs-lookup"><span data-stu-id="8578e-134">String</span></span>|<span data-ttu-id="8578e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8578e-135">Key of the entity.</span></span> <span data-ttu-id="8578e-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8578e-137">lastModifiedDateTime</span></span>|<span data-ttu-id="8578e-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8578e-138">DateTimeOffset</span></span>|<span data-ttu-id="8578e-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8578e-139">DateTime the object was last modified.</span></span> <span data-ttu-id="8578e-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8578e-141">roleScopeTagIds</span></span>|<span data-ttu-id="8578e-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="8578e-142">String collection</span></span>|<span data-ttu-id="8578e-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8578e-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8578e-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="8578e-145">supportsScopeTags</span></span>|<span data-ttu-id="8578e-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="8578e-146">Boolean</span></span>|<span data-ttu-id="8578e-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8578e-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="8578e-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="8578e-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="8578e-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="8578e-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="8578e-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8578e-150">This property is read-only.</span></span> <span data-ttu-id="8578e-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8578e-152">createdDateTime</span></span>|<span data-ttu-id="8578e-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8578e-153">DateTimeOffset</span></span>|<span data-ttu-id="8578e-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8578e-154">DateTime the object was created.</span></span> <span data-ttu-id="8578e-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-156">descripción</span><span class="sxs-lookup"><span data-stu-id="8578e-156">description</span></span>|<span data-ttu-id="8578e-157">String</span><span class="sxs-lookup"><span data-stu-id="8578e-157">String</span></span>|<span data-ttu-id="8578e-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8578e-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8578e-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-160">displayName</span><span class="sxs-lookup"><span data-stu-id="8578e-160">displayName</span></span>|<span data-ttu-id="8578e-161">String</span><span class="sxs-lookup"><span data-stu-id="8578e-161">String</span></span>|<span data-ttu-id="8578e-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8578e-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8578e-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-164">version</span><span class="sxs-lookup"><span data-stu-id="8578e-164">version</span></span>|<span data-ttu-id="8578e-165">Int32</span><span class="sxs-lookup"><span data-stu-id="8578e-165">Int32</span></span>|<span data-ttu-id="8578e-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8578e-166">Version of the device configuration.</span></span> <span data-ttu-id="8578e-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8578e-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8578e-168">windowsNetworkIsolationPolicy</span><span class="sxs-lookup"><span data-stu-id="8578e-168">windowsNetworkIsolationPolicy</span></span>|[<span data-ttu-id="8578e-169">windowsNetworkIsolationPolicy</span><span class="sxs-lookup"><span data-stu-id="8578e-169">windowsNetworkIsolationPolicy</span></span>](../resources/intune-deviceconfig-windowsnetworkisolationpolicy.md)|<span data-ttu-id="8578e-170">Directiva de aislamiento de red de Windows</span><span class="sxs-lookup"><span data-stu-id="8578e-170">Windows Network Isolation Policy</span></span>|



## <a name="response"></a><span data-ttu-id="8578e-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8578e-171">Response</span></span>
<span data-ttu-id="8578e-172">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windows10NetworkBoundaryConfiguration](../resources/intune-deviceconfig-windows10networkboundaryconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8578e-172">If successful, this method returns a `201 Created` response code and a [windows10NetworkBoundaryConfiguration](../resources/intune-deviceconfig-windows10networkboundaryconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8578e-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8578e-173">Example</span></span>
### <a name="request"></a><span data-ttu-id="8578e-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8578e-174">Request</span></span>
<span data-ttu-id="8578e-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8578e-175">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1308

{
  "@odata.type": "#microsoft.graph.windows10NetworkBoundaryConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "windowsNetworkIsolationPolicy": {
    "@odata.type": "microsoft.graph.windowsNetworkIsolationPolicy",
    "enterpriseNetworkDomainNames": [
      "Enterprise Network Domain Names value"
    ],
    "enterpriseCloudResources": [
      {
        "@odata.type": "microsoft.graph.proxiedDomain",
        "ipAddressOrFQDN": "Ip Address Or FQDN value",
        "proxy": "Proxy value"
      }
    ],
    "enterpriseIPRanges": [
      {
        "@odata.type": "microsoft.graph.iPv6Range",
        "lowerAddress": "Lower Address value",
        "upperAddress": "Upper Address value"
      }
    ],
    "enterpriseInternalProxyServers": [
      "Enterprise Internal Proxy Servers value"
    ],
    "enterpriseIPRangesAreAuthoritative": true,
    "enterpriseProxyServers": [
      "Enterprise Proxy Servers value"
    ],
    "enterpriseProxyServersAreAuthoritative": true,
    "neutralDomainResources": [
      "Neutral Domain Resources value"
    ]
  }
}
```

### <a name="response"></a><span data-ttu-id="8578e-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8578e-176">Response</span></span>
<span data-ttu-id="8578e-p111">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8578e-p111">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1416

{
  "@odata.type": "#microsoft.graph.windows10NetworkBoundaryConfiguration",
  "id": "afbc9e01-9e01-afbc-019e-bcaf019ebcaf",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "windowsNetworkIsolationPolicy": {
    "@odata.type": "microsoft.graph.windowsNetworkIsolationPolicy",
    "enterpriseNetworkDomainNames": [
      "Enterprise Network Domain Names value"
    ],
    "enterpriseCloudResources": [
      {
        "@odata.type": "microsoft.graph.proxiedDomain",
        "ipAddressOrFQDN": "Ip Address Or FQDN value",
        "proxy": "Proxy value"
      }
    ],
    "enterpriseIPRanges": [
      {
        "@odata.type": "microsoft.graph.iPv6Range",
        "lowerAddress": "Lower Address value",
        "upperAddress": "Upper Address value"
      }
    ],
    "enterpriseInternalProxyServers": [
      "Enterprise Internal Proxy Servers value"
    ],
    "enterpriseIPRangesAreAuthoritative": true,
    "enterpriseProxyServers": [
      "Enterprise Proxy Servers value"
    ],
    "enterpriseProxyServersAreAuthoritative": true,
    "neutralDomainResources": [
      "Neutral Domain Resources value"
    ]
  }
}
```





