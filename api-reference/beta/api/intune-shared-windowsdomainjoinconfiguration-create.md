---
title: Crear windowsDomainJoinConfiguration
description: Crear un nuevo objeto windowsDomainJoinConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1622bbcf755837115431e77a9b319d1ca749af28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811637"
---
# <a name="create-windowsdomainjoinconfiguration"></a><span data-ttu-id="be2ff-103">Crear windowsDomainJoinConfiguration</span><span class="sxs-lookup"><span data-stu-id="be2ff-103">Create windowsDomainJoinConfiguration</span></span>

> <span data-ttu-id="be2ff-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be2ff-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be2ff-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be2ff-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="be2ff-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be2ff-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="be2ff-107">Crear un nuevo objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="be2ff-107">Create a new [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="be2ff-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="be2ff-108">Prerequisites</span></span>
<span data-ttu-id="be2ff-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="be2ff-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="be2ff-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="be2ff-111">Permission type</span></span>|<span data-ttu-id="be2ff-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="be2ff-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="be2ff-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="be2ff-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="be2ff-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="be2ff-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="be2ff-115">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="be2ff-115">DeviceManagementConfiguration.ReadWrite.All</span></span> |
|<span data-ttu-id="be2ff-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="be2ff-116">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="be2ff-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be2ff-117">Not supported.</span></span>|
|<span data-ttu-id="be2ff-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="be2ff-118">Application</span></span>|<span data-ttu-id="be2ff-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="be2ff-119">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="be2ff-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="be2ff-120">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="be2ff-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="be2ff-121">Request headers</span></span>

|<span data-ttu-id="be2ff-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be2ff-122">Header</span></span>|<span data-ttu-id="be2ff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="be2ff-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="be2ff-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="be2ff-124">Authorization</span></span>|<span data-ttu-id="be2ff-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="be2ff-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="be2ff-126">Accept</span><span class="sxs-lookup"><span data-stu-id="be2ff-126">Accept</span></span>|<span data-ttu-id="be2ff-127">application/json</span><span class="sxs-lookup"><span data-stu-id="be2ff-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="be2ff-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="be2ff-128">Request body</span></span>

<span data-ttu-id="be2ff-129">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsDomainJoinConfiguration.</span><span class="sxs-lookup"><span data-stu-id="be2ff-129">In the request body, supply a JSON representation for the windowsDomainJoinConfiguration object.</span></span>

<span data-ttu-id="be2ff-130">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsDomainJoinConfiguration.</span><span class="sxs-lookup"><span data-stu-id="be2ff-130">The following table shows the properties that are required when you create the windowsDomainJoinConfiguration.</span></span>

|<span data-ttu-id="be2ff-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be2ff-131">Property</span></span>|<span data-ttu-id="be2ff-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="be2ff-132">Type</span></span>|<span data-ttu-id="be2ff-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="be2ff-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="be2ff-134">id</span><span class="sxs-lookup"><span data-stu-id="be2ff-134">id</span></span>|<span data-ttu-id="be2ff-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-135">String</span></span>|<span data-ttu-id="be2ff-136">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="be2ff-136">Key of the entity.</span></span> <span data-ttu-id="be2ff-137">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-137">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-138">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="be2ff-138">**Device configuration**</span></span>|
|<span data-ttu-id="be2ff-139">activeDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="be2ff-139">activeDirectoryDomainName</span></span>|<span data-ttu-id="be2ff-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-140">String</span></span>|<span data-ttu-id="be2ff-141">Nombre de dominio de Active Directory para unirse a.</span><span class="sxs-lookup"><span data-stu-id="be2ff-141">Active Directory domain name to join.</span></span>|
|<span data-ttu-id="be2ff-142">computerNameStaticPrefix</span><span class="sxs-lookup"><span data-stu-id="be2ff-142">computerNameStaticPrefix</span></span>|<span data-ttu-id="be2ff-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-143">String</span></span>|<span data-ttu-id="be2ff-144">Prefijo fijo que se usará para el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-144">Fixed prefix to be used for computer name.</span></span>|
|<span data-ttu-id="be2ff-145">computerNameSuffixRandomCharCount</span><span class="sxs-lookup"><span data-stu-id="be2ff-145">computerNameSuffixRandomCharCount</span></span>|<span data-ttu-id="be2ff-146">Int32</span><span class="sxs-lookup"><span data-stu-id="be2ff-146">Int32</span></span>|<span data-ttu-id="be2ff-147">Genera de forma dinámica los caracteres que se utilizan como sufijo de nombre de equipo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-147">Dynamically generated characters used as suffix for computer name.</span></span> <span data-ttu-id="be2ff-148">Valores válidos 3 a 14</span><span class="sxs-lookup"><span data-stu-id="be2ff-148">Valid values 3 to 14</span></span>|
|<span data-ttu-id="be2ff-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="be2ff-149">createdDateTime</span></span>|<span data-ttu-id="be2ff-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be2ff-150">DateTimeOffset</span></span>|<span data-ttu-id="be2ff-151">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="be2ff-151">DateTime the object was created.</span></span> <span data-ttu-id="be2ff-152">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-152">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-153">descripción</span><span class="sxs-lookup"><span data-stu-id="be2ff-153">description</span></span>|<span data-ttu-id="be2ff-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-154">String</span></span>|<span data-ttu-id="be2ff-155">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-155">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="be2ff-156">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-156">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-157">displayName</span><span class="sxs-lookup"><span data-stu-id="be2ff-157">displayName</span></span>|<span data-ttu-id="be2ff-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-158">String</span></span>|<span data-ttu-id="be2ff-159">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-159">Admin provided name of the device configuration.</span></span> <span data-ttu-id="be2ff-160">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-160">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-161">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="be2ff-161">lastModifiedDateTime</span></span>|<span data-ttu-id="be2ff-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be2ff-162">DateTimeOffset</span></span>|<span data-ttu-id="be2ff-163">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="be2ff-163">DateTime the object was last modified.</span></span> <span data-ttu-id="be2ff-164">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-164">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-165">organizationalUnit</span><span class="sxs-lookup"><span data-stu-id="be2ff-165">organizationalUnit</span></span>|<span data-ttu-id="be2ff-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="be2ff-166">String</span></span>|<span data-ttu-id="be2ff-167">Unidad organizativa (OU) donde se creará la cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-167">Organizational unit (OU) where the computer account will be created.</span></span> <span data-ttu-id="be2ff-168">Si este parámetro es NULL, se usará el contenedor de objetos de equipo conocido como publicado en el dominio.</span><span class="sxs-lookup"><span data-stu-id="be2ff-168">If this parameter is NULL, the well known computer object container will be used as published in the domain.</span></span>|
|<span data-ttu-id="be2ff-169">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="be2ff-169">roleScopeTagIds</span></span>|<span data-ttu-id="be2ff-170">Colección String</span><span class="sxs-lookup"><span data-stu-id="be2ff-170">String collection</span></span>|<span data-ttu-id="be2ff-171">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="be2ff-171">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="be2ff-172">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-172">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-173">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="be2ff-173">supportsScopeTags</span></span>|<span data-ttu-id="be2ff-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="be2ff-174">Boolean</span></span>|<span data-ttu-id="be2ff-175">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="be2ff-175">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="be2ff-176">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="be2ff-176">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="be2ff-177">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="be2ff-177">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="be2ff-178">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="be2ff-178">This property is read-only.</span></span> <span data-ttu-id="be2ff-179">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-179">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="be2ff-180">version</span><span class="sxs-lookup"><span data-stu-id="be2ff-180">version</span></span>|<span data-ttu-id="be2ff-181">Int32</span><span class="sxs-lookup"><span data-stu-id="be2ff-181">Int32</span></span>|<span data-ttu-id="be2ff-182">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="be2ff-182">Version of the device configuration.</span></span> <span data-ttu-id="be2ff-183">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be2ff-183">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="be2ff-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be2ff-184">Response</span></span>

<span data-ttu-id="be2ff-185">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="be2ff-185">If successful, this method returns a `201 Created` response code and a [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="be2ff-186">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="be2ff-186">Example</span></span>

### <a name="request"></a><span data-ttu-id="be2ff-187">Solicitud</span><span class="sxs-lookup"><span data-stu-id="be2ff-187">Request</span></span>

<span data-ttu-id="be2ff-188">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="be2ff-188">Here is an example of the request.</span></span>

``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 559

{
  "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "computerNameStaticPrefix": "Computer Name Static Prefix value",
  "computerNameSuffixRandomCharCount": 1,
  "activeDirectoryDomainName": "Active Directory Domain Name value",
  "organizationalUnit": "Organizational Unit value"
}
```

### <a name="response"></a><span data-ttu-id="be2ff-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="be2ff-189">Response</span></span>

<span data-ttu-id="be2ff-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="be2ff-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 667

{
  "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
  "id": "40118d08-8d08-4011-088d-1140088d1140",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "computerNameStaticPrefix": "Computer Name Static Prefix value",
  "computerNameSuffixRandomCharCount": 1,
  "activeDirectoryDomainName": "Active Directory Domain Name value",
  "organizationalUnit": "Organizational Unit value"
}
```



