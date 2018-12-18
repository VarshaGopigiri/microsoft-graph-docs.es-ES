---
title: Crear iosUpdateConfiguration
description: Cree un objeto iosUpdateConfiguration.
author: tfitzmac
ms.openlocfilehash: 1b3077496ad606906ff842c0983632184e88c6c3
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357557"
---
# <a name="create-iosupdateconfiguration"></a><span data-ttu-id="e0d66-103">Crear iosUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e0d66-103">Create iosUpdateConfiguration</span></span>

> <span data-ttu-id="e0d66-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e0d66-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e0d66-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e0d66-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="e0d66-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e0d66-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e0d66-107">Cree un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e0d66-107">Create a new [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e0d66-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0d66-108">Prerequisites</span></span>
<span data-ttu-id="e0d66-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e0d66-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e0d66-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e0d66-111">Permission type</span></span>|<span data-ttu-id="e0d66-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e0d66-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e0d66-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e0d66-113">Delegated (work or school account)</span></span>|<span data-ttu-id="e0d66-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e0d66-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e0d66-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e0d66-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e0d66-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0d66-116">Not supported.</span></span>|
|<span data-ttu-id="e0d66-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e0d66-117">Application</span></span>|<span data-ttu-id="e0d66-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e0d66-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e0d66-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0d66-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="e0d66-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d66-120">Request headers</span></span>
|<span data-ttu-id="e0d66-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0d66-121">Header</span></span>|<span data-ttu-id="e0d66-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e0d66-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e0d66-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e0d66-123">Authorization</span></span>|<span data-ttu-id="e0d66-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e0d66-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e0d66-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e0d66-125">Accept</span></span>|<span data-ttu-id="e0d66-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e0d66-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e0d66-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d66-127">Request body</span></span>
<span data-ttu-id="e0d66-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0d66-128">In the request body, supply a JSON representation for the iosUpdateConfiguration object.</span></span>

<span data-ttu-id="e0d66-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e0d66-129">The following table shows the properties that are required when you create the iosUpdateConfiguration.</span></span>

|<span data-ttu-id="e0d66-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e0d66-130">Property</span></span>|<span data-ttu-id="e0d66-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0d66-131">Type</span></span>|<span data-ttu-id="e0d66-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0d66-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e0d66-133">id</span><span class="sxs-lookup"><span data-stu-id="e0d66-133">id</span></span>|<span data-ttu-id="e0d66-134">String</span><span class="sxs-lookup"><span data-stu-id="e0d66-134">String</span></span>|<span data-ttu-id="e0d66-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e0d66-135">Key of the entity.</span></span> <span data-ttu-id="e0d66-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e0d66-137">lastModifiedDateTime</span></span>|<span data-ttu-id="e0d66-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0d66-138">DateTimeOffset</span></span>|<span data-ttu-id="e0d66-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e0d66-139">DateTime the object was last modified.</span></span> <span data-ttu-id="e0d66-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="e0d66-141">roleScopeTagIds</span></span>|<span data-ttu-id="e0d66-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="e0d66-142">String collection</span></span>|<span data-ttu-id="e0d66-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="e0d66-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="e0d66-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="e0d66-145">supportsScopeTags</span></span>|<span data-ttu-id="e0d66-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="e0d66-146">Boolean</span></span>|<span data-ttu-id="e0d66-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="e0d66-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="e0d66-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="e0d66-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="e0d66-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d66-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="e0d66-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="e0d66-150">This property is read-only.</span></span> <span data-ttu-id="e0d66-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e0d66-152">createdDateTime</span></span>|<span data-ttu-id="e0d66-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e0d66-153">DateTimeOffset</span></span>|<span data-ttu-id="e0d66-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e0d66-154">DateTime the object was created.</span></span> <span data-ttu-id="e0d66-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-156">descripción</span><span class="sxs-lookup"><span data-stu-id="e0d66-156">description</span></span>|<span data-ttu-id="e0d66-157">String</span><span class="sxs-lookup"><span data-stu-id="e0d66-157">String</span></span>|<span data-ttu-id="e0d66-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0d66-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e0d66-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-160">displayName</span><span class="sxs-lookup"><span data-stu-id="e0d66-160">displayName</span></span>|<span data-ttu-id="e0d66-161">String</span><span class="sxs-lookup"><span data-stu-id="e0d66-161">String</span></span>|<span data-ttu-id="e0d66-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0d66-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e0d66-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-164">version</span><span class="sxs-lookup"><span data-stu-id="e0d66-164">version</span></span>|<span data-ttu-id="e0d66-165">Int32</span><span class="sxs-lookup"><span data-stu-id="e0d66-165">Int32</span></span>|<span data-ttu-id="e0d66-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0d66-166">Version of the device configuration.</span></span> <span data-ttu-id="e0d66-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e0d66-168">isEnabled</span><span class="sxs-lookup"><span data-stu-id="e0d66-168">isEnabled</span></span>|<span data-ttu-id="e0d66-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="e0d66-169">Boolean</span></span>|<span data-ttu-id="e0d66-170">Está habilitada la configuración en la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="e0d66-170">Is setting enabled in UI</span></span>|
|<span data-ttu-id="e0d66-171">activeHoursStart</span><span class="sxs-lookup"><span data-stu-id="e0d66-171">activeHoursStart</span></span>|<span data-ttu-id="e0d66-172">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="e0d66-172">TimeOfDay</span></span>|<span data-ttu-id="e0d66-173">Inicio de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="e0d66-173">Active Hours Start (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="e0d66-174">activeHoursEnd</span><span class="sxs-lookup"><span data-stu-id="e0d66-174">activeHoursEnd</span></span>|<span data-ttu-id="e0d66-175">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="e0d66-175">TimeOfDay</span></span>|<span data-ttu-id="e0d66-176">Fin de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="e0d66-176">Active Hours End (active hours mean the time window when updates install should not happen)</span></span>|
|<span data-ttu-id="e0d66-177">scheduledInstallDays</span><span class="sxs-lookup"><span data-stu-id="e0d66-177">scheduledInstallDays</span></span>|<span data-ttu-id="e0d66-178">colección de [dayOfWeek](../resources/intune-deviceconfig-dayofweek.md)</span><span class="sxs-lookup"><span data-stu-id="e0d66-178">[dayOfWeek](../resources/intune-deviceconfig-dayofweek.md) collection</span></span>|<span data-ttu-id="e0d66-179">Días de la semana para los que se configuran las horas activas.</span><span class="sxs-lookup"><span data-stu-id="e0d66-179">Days in week for which active hours are configured.</span></span> <span data-ttu-id="e0d66-180">Esta colección puede contener un máximo de 7 elementos.</span><span class="sxs-lookup"><span data-stu-id="e0d66-180">This collection can contain a maximum of 7 elements.</span></span> <span data-ttu-id="e0d66-181">Valores posibles: `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday` y `sunday`.</span><span class="sxs-lookup"><span data-stu-id="e0d66-181">Possible values are: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`.</span></span>|
|<span data-ttu-id="e0d66-182">utcTimeOffsetInMinutes</span><span class="sxs-lookup"><span data-stu-id="e0d66-182">utcTimeOffsetInMinutes</span></span>|<span data-ttu-id="e0d66-183">Int32</span><span class="sxs-lookup"><span data-stu-id="e0d66-183">Int32</span></span>|<span data-ttu-id="e0d66-184">Diferencia horaria UTC indicada en minutos</span><span class="sxs-lookup"><span data-stu-id="e0d66-184">UTC Time Offset indicated in minutes</span></span>|
|<span data-ttu-id="e0d66-185">enforcedSoftwareUpdateDelayInDays</span><span class="sxs-lookup"><span data-stu-id="e0d66-185">enforcedSoftwareUpdateDelayInDays</span></span>|<span data-ttu-id="e0d66-186">Int32</span><span class="sxs-lookup"><span data-stu-id="e0d66-186">Int32</span></span>|<span data-ttu-id="e0d66-187">Días antes de las actualizaciones de software son visibles para los dispositivos iOS comprendido entre 0 y 90 inclusive</span><span class="sxs-lookup"><span data-stu-id="e0d66-187">Days before software updates are visible to iOS devices ranging from 0 to 90 inclusive</span></span>|



## <a name="response"></a><span data-ttu-id="e0d66-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d66-188">Response</span></span>
<span data-ttu-id="e0d66-189">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0d66-189">If successful, this method returns a `201 Created` response code and a [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e0d66-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0d66-190">Example</span></span>
### <a name="request"></a><span data-ttu-id="e0d66-191">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d66-191">Request</span></span>
<span data-ttu-id="e0d66-192">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0d66-192">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 546

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "isEnabled": true,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6,
  "enforcedSoftwareUpdateDelayInDays": 1
}
```

### <a name="response"></a><span data-ttu-id="e0d66-193">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d66-193">Response</span></span>
<span data-ttu-id="e0d66-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e0d66-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 654

{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "id": "321aef09-ef09-321a-09ef-1a3209ef1a32",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "isEnabled": true,
  "activeHoursStart": "12:00:05.5020000",
  "activeHoursEnd": "11:59:00.8990000",
  "scheduledInstallDays": [
    "monday"
  ],
  "utcTimeOffsetInMinutes": 6,
  "enforcedSoftwareUpdateDelayInDays": 1
}
```





