---
title: Actualizar windowsDomainJoinConfiguration
description: Actualizar las propiedades de un objeto windowsDomainJoinConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5e6a1430cf53326bb1d3c603f1ac30e1d0160b6a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933669"
---
# <a name="update-windowsdomainjoinconfiguration"></a><span data-ttu-id="37459-103">Actualizar windowsDomainJoinConfiguration</span><span class="sxs-lookup"><span data-stu-id="37459-103">Update windowsDomainJoinConfiguration</span></span>

> <span data-ttu-id="37459-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37459-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37459-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37459-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37459-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37459-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37459-107">Actualizar las propiedades de un objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-107">Update the properties of a [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="37459-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37459-108">Prerequisites</span></span>
<span data-ttu-id="37459-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37459-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37459-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37459-111">Permission type</span></span>|<span data-ttu-id="37459-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37459-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37459-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37459-113">Delegated (work or school account)</span></span>||
| <span data-ttu-id="37459-114">&nbsp; &nbsp; **Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="37459-114">&nbsp; &nbsp; **Device configuration**</span></span> | <span data-ttu-id="37459-115">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="37459-115">DeviceManagementConfiguration.ReadWrite.All</span></span> |
| <span data-ttu-id="37459-116">&nbsp; &nbsp; **Inscripción**</span><span class="sxs-lookup"><span data-stu-id="37459-116">&nbsp; &nbsp; **Enrollment**</span></span> | <span data-ttu-id="37459-117">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="37459-117">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="37459-118">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37459-118">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37459-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37459-119">Not supported.</span></span>|
|<span data-ttu-id="37459-120">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37459-120">Application</span></span>|<span data-ttu-id="37459-121">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37459-121">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37459-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37459-122">HTTP Request</span></span>

<span data-ttu-id="37459-123">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="37459-123">**Device configuration**</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

<span data-ttu-id="37459-124">**Inscripción**</span><span class="sxs-lookup"><span data-stu-id="37459-124">**Enrollment**</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsAutopilotDeviceIdentities/{windowsAutopilotDeviceIdentityId}/deploymentProfile/microsoft.graph.activeDirectoryWindowsAutopilotDeploymentProfile/domainJoinConfiguration
```

## <a name="request-headers"></a><span data-ttu-id="37459-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37459-125">Request headers</span></span>
|<span data-ttu-id="37459-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37459-126">Header</span></span>|<span data-ttu-id="37459-127">Valor</span><span class="sxs-lookup"><span data-stu-id="37459-127">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37459-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="37459-128">Authorization</span></span>|<span data-ttu-id="37459-129">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37459-129">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37459-130">Accept</span><span class="sxs-lookup"><span data-stu-id="37459-130">Accept</span></span>|<span data-ttu-id="37459-131">application/json</span><span class="sxs-lookup"><span data-stu-id="37459-131">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37459-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37459-132">Request body</span></span>
<span data-ttu-id="37459-133">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="37459-133">In the request body, supply a JSON representation for the [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object.</span></span>

<span data-ttu-id="37459-134">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="37459-134">The following table shows the properties that are required when you create the [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md).</span></span>

|<span data-ttu-id="37459-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37459-135">Property</span></span>|<span data-ttu-id="37459-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="37459-136">Type</span></span>|<span data-ttu-id="37459-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="37459-137">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37459-138">id</span><span class="sxs-lookup"><span data-stu-id="37459-138">id</span></span>|<span data-ttu-id="37459-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-139">String</span></span>|<span data-ttu-id="37459-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="37459-140">Key of the entity.</span></span> <span data-ttu-id="37459-141">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-141">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-142">**Configuración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="37459-142">**Device configuration**</span></span>|
|<span data-ttu-id="37459-143">activeDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="37459-143">activeDirectoryDomainName</span></span>|<span data-ttu-id="37459-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-144">String</span></span>|<span data-ttu-id="37459-145">Nombre de dominio de Active Directory para unirse a.</span><span class="sxs-lookup"><span data-stu-id="37459-145">Active Directory domain name to join.</span></span>|
|<span data-ttu-id="37459-146">computerNameStaticPrefix</span><span class="sxs-lookup"><span data-stu-id="37459-146">computerNameStaticPrefix</span></span>|<span data-ttu-id="37459-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-147">String</span></span>|<span data-ttu-id="37459-148">Prefijo fijo que se usará para el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="37459-148">Fixed prefix to be used for computer name.</span></span>|
|<span data-ttu-id="37459-149">computerNameSuffixRandomCharCount</span><span class="sxs-lookup"><span data-stu-id="37459-149">computerNameSuffixRandomCharCount</span></span>|<span data-ttu-id="37459-150">Int32</span><span class="sxs-lookup"><span data-stu-id="37459-150">Int32</span></span>|<span data-ttu-id="37459-151">Genera de forma dinámica los caracteres que se utilizan como sufijo de nombre de equipo.</span><span class="sxs-lookup"><span data-stu-id="37459-151">Dynamically generated characters used as suffix for computer name.</span></span> <span data-ttu-id="37459-152">Valores válidos 3 a 14</span><span class="sxs-lookup"><span data-stu-id="37459-152">Valid values 3 to 14</span></span>|
|<span data-ttu-id="37459-153">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="37459-153">createdDateTime</span></span>|<span data-ttu-id="37459-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="37459-154">DateTimeOffset</span></span>|<span data-ttu-id="37459-155">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="37459-155">DateTime the object was created.</span></span> <span data-ttu-id="37459-156">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-156">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-157">descripción</span><span class="sxs-lookup"><span data-stu-id="37459-157">description</span></span>|<span data-ttu-id="37459-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-158">String</span></span>|<span data-ttu-id="37459-159">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37459-159">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="37459-160">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-160">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-161">displayName</span><span class="sxs-lookup"><span data-stu-id="37459-161">displayName</span></span>|<span data-ttu-id="37459-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-162">String</span></span>|<span data-ttu-id="37459-163">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37459-163">Admin provided name of the device configuration.</span></span> <span data-ttu-id="37459-164">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-164">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-165">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="37459-165">lastModifiedDateTime</span></span>|<span data-ttu-id="37459-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="37459-166">DateTimeOffset</span></span>|<span data-ttu-id="37459-167">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="37459-167">DateTime the object was last modified.</span></span> <span data-ttu-id="37459-168">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-168">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-169">organizationalUnit</span><span class="sxs-lookup"><span data-stu-id="37459-169">organizationalUnit</span></span>|<span data-ttu-id="37459-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="37459-170">String</span></span>|<span data-ttu-id="37459-171">Unidad organizativa (OU) donde se creará la cuenta de equipo.</span><span class="sxs-lookup"><span data-stu-id="37459-171">Organizational unit (OU) where the computer account will be created.</span></span> <span data-ttu-id="37459-172">Si este parámetro es NULL, se usará el contenedor de objetos de equipo conocido como publicado en el dominio.</span><span class="sxs-lookup"><span data-stu-id="37459-172">If this parameter is NULL, the well known computer object container will be used as published in the domain.</span></span>|
|<span data-ttu-id="37459-173">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="37459-173">roleScopeTagIds</span></span>|<span data-ttu-id="37459-174">Colección String</span><span class="sxs-lookup"><span data-stu-id="37459-174">String collection</span></span>|<span data-ttu-id="37459-175">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="37459-175">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="37459-176">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-176">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-177">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="37459-177">supportsScopeTags</span></span>|<span data-ttu-id="37459-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="37459-178">Boolean</span></span>|<span data-ttu-id="37459-179">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="37459-179">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="37459-180">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="37459-180">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="37459-181">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="37459-181">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="37459-182">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="37459-182">This property is read-only.</span></span> <span data-ttu-id="37459-183">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-183">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="37459-184">version</span><span class="sxs-lookup"><span data-stu-id="37459-184">version</span></span>|<span data-ttu-id="37459-185">Int32</span><span class="sxs-lookup"><span data-stu-id="37459-185">Int32</span></span>|<span data-ttu-id="37459-186">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37459-186">Version of the device configuration.</span></span> <span data-ttu-id="37459-187">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="37459-187">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|



<span data-ttu-id="37459-188">Nota: Compatibilidad con las propiedades de cuerpo de solicitud depende del contexto de la llamada.</span><span class="sxs-lookup"><span data-stu-id="37459-188">Note: Request body properties support depends on the context of the call.</span></span>  <span data-ttu-id="37459-189">No todas las propiedades son adecuadas para todos los flujos de trabajo.</span><span class="sxs-lookup"><span data-stu-id="37459-189">Not all properties are appropriate for all workflows.</span></span>

## <a name="response"></a><span data-ttu-id="37459-190">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37459-190">Response</span></span>
<span data-ttu-id="37459-191">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37459-191">If successful, this method returns a `200 OK` response code and an updated [windowsDomainJoinConfiguration](../resources/intune-shared-windowsdomainjoinconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37459-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37459-192">Example</span></span>
### <a name="request"></a><span data-ttu-id="37459-193">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37459-193">Request</span></span>
<span data-ttu-id="37459-194">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37459-194">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 344

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "computerNameStaticPrefix": "Computer Name Static Prefix value",
  "computerNameSuffixRandomCharCount": 1,
  "activeDirectoryDomainName": "Active Directory Domain Name value"
}
```

### <a name="response"></a><span data-ttu-id="37459-195">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37459-195">Response</span></span>
<span data-ttu-id="37459-196">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37459-196">Here is an example of the response.</span></span> <span data-ttu-id="37459-197">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="37459-197">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="37459-198">Propiedades devueltas por las llamadas reales pueden variar según el contexto.</span><span class="sxs-lookup"><span data-stu-id="37459-198">Properties returned by actual calls vary according to the context.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 521

{
  "@odata.type": "#microsoft.graph.windowsDomainJoinConfiguration",
  "id": "40118d08-8d08-4011-088d-1140088d1140",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "computerNameStaticPrefix": "Computer Name Static Prefix value",
  "computerNameSuffixRandomCharCount": 1,
  "activeDirectoryDomainName": "Active Directory Domain Name value"
}
```



