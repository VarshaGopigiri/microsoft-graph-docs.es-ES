---
title: Crear windows10TeamGeneralConfiguration
description: Cree un objeto windows10TeamGeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b1b1061e1aba8f1f3aaccc8cdc2d85565a52dadf
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836620"
---
# <a name="create-windows10teamgeneralconfiguration"></a><span data-ttu-id="f9848-103">Crear windows10TeamGeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9848-103">Create windows10TeamGeneralConfiguration</span></span>

> <span data-ttu-id="f9848-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f9848-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f9848-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f9848-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f9848-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9848-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9848-107">Cree un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f9848-107">Create a new [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9848-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9848-108">Prerequisites</span></span>
<span data-ttu-id="f9848-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f9848-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f9848-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9848-111">Permission type</span></span>|<span data-ttu-id="f9848-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9848-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9848-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9848-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f9848-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f9848-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f9848-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9848-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9848-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9848-116">Not supported.</span></span>|
|<span data-ttu-id="f9848-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9848-117">Application</span></span>|<span data-ttu-id="f9848-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9848-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9848-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9848-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f9848-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9848-120">Request headers</span></span>
|<span data-ttu-id="f9848-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9848-121">Header</span></span>|<span data-ttu-id="f9848-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f9848-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9848-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f9848-123">Authorization</span></span>|<span data-ttu-id="f9848-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9848-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f9848-125">Accept</span><span class="sxs-lookup"><span data-stu-id="f9848-125">Accept</span></span>|<span data-ttu-id="f9848-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f9848-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9848-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9848-127">Request body</span></span>
<span data-ttu-id="f9848-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9848-128">In the request body, supply a JSON representation for the windows10TeamGeneralConfiguration object.</span></span>

<span data-ttu-id="f9848-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f9848-129">The following table shows the properties that are required when you create the windows10TeamGeneralConfiguration.</span></span>

|<span data-ttu-id="f9848-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9848-130">Property</span></span>|<span data-ttu-id="f9848-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9848-131">Type</span></span>|<span data-ttu-id="f9848-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9848-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f9848-133">id</span><span class="sxs-lookup"><span data-stu-id="f9848-133">id</span></span>|<span data-ttu-id="f9848-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-134">String</span></span>|<span data-ttu-id="f9848-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f9848-135">Key of the entity.</span></span> <span data-ttu-id="f9848-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="f9848-137">lastModifiedDateTime</span></span>|<span data-ttu-id="f9848-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f9848-138">DateTimeOffset</span></span>|<span data-ttu-id="f9848-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="f9848-139">DateTime the object was last modified.</span></span> <span data-ttu-id="f9848-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="f9848-141">roleScopeTagIds</span></span>|<span data-ttu-id="f9848-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="f9848-142">String collection</span></span>|<span data-ttu-id="f9848-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="f9848-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="f9848-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="f9848-145">supportsScopeTags</span></span>|<span data-ttu-id="f9848-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-146">Boolean</span></span>|<span data-ttu-id="f9848-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="f9848-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="f9848-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="f9848-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="f9848-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="f9848-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="f9848-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="f9848-150">This property is read-only.</span></span> <span data-ttu-id="f9848-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="f9848-152">createdDateTime</span></span>|<span data-ttu-id="f9848-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f9848-153">DateTimeOffset</span></span>|<span data-ttu-id="f9848-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f9848-154">DateTime the object was created.</span></span> <span data-ttu-id="f9848-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-156">descripción</span><span class="sxs-lookup"><span data-stu-id="f9848-156">description</span></span>|<span data-ttu-id="f9848-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-157">String</span></span>|<span data-ttu-id="f9848-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="f9848-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-160">displayName</span><span class="sxs-lookup"><span data-stu-id="f9848-160">displayName</span></span>|<span data-ttu-id="f9848-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-161">String</span></span>|<span data-ttu-id="f9848-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="f9848-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-164">version</span><span class="sxs-lookup"><span data-stu-id="f9848-164">version</span></span>|<span data-ttu-id="f9848-165">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-165">Int32</span></span>|<span data-ttu-id="f9848-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-166">Version of the device configuration.</span></span> <span data-ttu-id="f9848-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="f9848-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="f9848-168">azureOperationalInsightsBlockTelemetry</span><span class="sxs-lookup"><span data-stu-id="f9848-168">azureOperationalInsightsBlockTelemetry</span></span>|<span data-ttu-id="f9848-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-169">Boolean</span></span>|<span data-ttu-id="f9848-170">Indica si se va a bloquear Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="f9848-170">Indicates whether or not to Block Azure Operational Insights.</span></span>|
|<span data-ttu-id="f9848-171">azureOperationalInsightsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f9848-171">azureOperationalInsightsWorkspaceId</span></span>|<span data-ttu-id="f9848-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-172">String</span></span>|<span data-ttu-id="f9848-173">Identificador del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="f9848-173">The Azure Operational Insights workspace id.</span></span>|
|<span data-ttu-id="f9848-174">azureOperationalInsightsWorkspaceKey</span><span class="sxs-lookup"><span data-stu-id="f9848-174">azureOperationalInsightsWorkspaceKey</span></span>|<span data-ttu-id="f9848-175">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-175">String</span></span>|<span data-ttu-id="f9848-176">Clave del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="f9848-176">The Azure Operational Insights Workspace key.</span></span>|
|<span data-ttu-id="f9848-177">connectAppBlockAutoLaunch</span><span class="sxs-lookup"><span data-stu-id="f9848-177">connectAppBlockAutoLaunch</span></span>|<span data-ttu-id="f9848-178">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-178">Boolean</span></span>|<span data-ttu-id="f9848-179">Especifica si se iniciará automáticamente la aplicación Conectar cada vez que se inicie un proyecto.</span><span class="sxs-lookup"><span data-stu-id="f9848-179">Specifies whether to automatically launch the Connect app whenever a projection is initiated.</span></span>|
|<span data-ttu-id="f9848-180">maintenanceWindowBlocked</span><span class="sxs-lookup"><span data-stu-id="f9848-180">maintenanceWindowBlocked</span></span>|<span data-ttu-id="f9848-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-181">Boolean</span></span>|<span data-ttu-id="f9848-182">Indica si se va a bloquear la configuración de un período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-182">Indicates whether or not to Block setting a maintenance window for device updates.</span></span>|
|<span data-ttu-id="f9848-183">maintenanceWindowDurationInHours</span><span class="sxs-lookup"><span data-stu-id="f9848-183">maintenanceWindowDurationInHours</span></span>|<span data-ttu-id="f9848-184">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-184">Int32</span></span>|<span data-ttu-id="f9848-185">Duración del período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-185">Maintenance window duration for device updates.</span></span> <span data-ttu-id="f9848-186">Valores válidos de 0 a 5</span><span class="sxs-lookup"><span data-stu-id="f9848-186">Valid values 0 to 5</span></span>|
|<span data-ttu-id="f9848-187">maintenanceWindowStartTime</span><span class="sxs-lookup"><span data-stu-id="f9848-187">maintenanceWindowStartTime</span></span>|<span data-ttu-id="f9848-188">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="f9848-188">TimeOfDay</span></span>|<span data-ttu-id="f9848-189">Hora de inicio del periodo de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9848-189">Maintenance window start time for device updates.</span></span>|
|<span data-ttu-id="f9848-190">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="f9848-190">miracastChannel</span></span>|[<span data-ttu-id="f9848-191">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="f9848-191">miracastChannel</span></span>](../resources/intune-deviceconfig-miracastchannel.md)|<span data-ttu-id="f9848-192">Canal.</span><span class="sxs-lookup"><span data-stu-id="f9848-192">The channel.</span></span> <span data-ttu-id="f9848-193">Los valores posibles son: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne` y `oneHundredSixtyFive`.</span><span class="sxs-lookup"><span data-stu-id="f9848-193">Possible values are: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne`, `oneHundredSixtyFive`.</span></span>|
|<span data-ttu-id="f9848-194">miracastBlocked</span><span class="sxs-lookup"><span data-stu-id="f9848-194">miracastBlocked</span></span>|<span data-ttu-id="f9848-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-195">Boolean</span></span>|<span data-ttu-id="f9848-196">Indica si se van a bloquear las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="f9848-196">Indicates whether or not to Block wireless projection.</span></span>|
|<span data-ttu-id="f9848-197">miracastRequirePin</span><span class="sxs-lookup"><span data-stu-id="f9848-197">miracastRequirePin</span></span>|<span data-ttu-id="f9848-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-198">Boolean</span></span>|<span data-ttu-id="f9848-199">Indica si se va a requerir un PIN para las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="f9848-199">Indicates whether or not to require a pin for wireless projection.</span></span>|
|<span data-ttu-id="f9848-200">settingsBlockMyMeetingsAndFiles</span><span class="sxs-lookup"><span data-stu-id="f9848-200">settingsBlockMyMeetingsAndFiles</span></span>|<span data-ttu-id="f9848-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-201">Boolean</span></span>|<span data-ttu-id="f9848-202">Especifica si se deshabilita la característica "Mis reuniones y archivos" en el menú Inicio, que muestra las reuniones y los archivos del usuario que ha iniciado sesión en Office 365.</span><span class="sxs-lookup"><span data-stu-id="f9848-202">Specifies whether to disable the "My meetings and files" feature in the Start menu, which shows the signed-in user's meetings and files from Office 365.</span></span>|
|<span data-ttu-id="f9848-203">settingsBlockSessionResume</span><span class="sxs-lookup"><span data-stu-id="f9848-203">settingsBlockSessionResume</span></span>|<span data-ttu-id="f9848-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-204">Boolean</span></span>|<span data-ttu-id="f9848-205">Especifica si se permite la posibilidad de reanudar una sesión cuando se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f9848-205">Specifies whether to allow the ability to resume a session when the session times out.</span></span>|
|<span data-ttu-id="f9848-206">settingsBlockSigninSuggestions</span><span class="sxs-lookup"><span data-stu-id="f9848-206">settingsBlockSigninSuggestions</span></span>|<span data-ttu-id="f9848-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-207">Boolean</span></span>|<span data-ttu-id="f9848-208">Especifica si se deshabilita la opción de rellenar automáticamente el cuadro de diálogo de inicio de sesión con invitados de reuniones programadas.</span><span class="sxs-lookup"><span data-stu-id="f9848-208">Specifies whether to disable auto-populating of the sign-in dialog with invitees from scheduled meetings.</span></span>|
|<span data-ttu-id="f9848-209">settingsDefaultVolume</span><span class="sxs-lookup"><span data-stu-id="f9848-209">settingsDefaultVolume</span></span>|<span data-ttu-id="f9848-210">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-210">Int32</span></span>|<span data-ttu-id="f9848-211">Especifica el valor de volumen predeterminado para una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="f9848-211">Specifies the default volume value for a new session.</span></span> <span data-ttu-id="f9848-212">Los valores permitidos son de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="f9848-212">Permitted values are 0-100.</span></span> <span data-ttu-id="f9848-213">El valor predeterminado es 45.</span><span class="sxs-lookup"><span data-stu-id="f9848-213">The default is 45.</span></span> <span data-ttu-id="f9848-214">Valores válidos de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="f9848-214">Valid values 0 to 100</span></span>|
|<span data-ttu-id="f9848-215">settingsScreenTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f9848-215">settingsScreenTimeoutInMinutes</span></span>|<span data-ttu-id="f9848-216">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-216">Int32</span></span>|<span data-ttu-id="f9848-217">Especifica el número de minutos hasta que se desconecta la pantalla Concentrador.</span><span class="sxs-lookup"><span data-stu-id="f9848-217">Specifies the number of minutes until the Hub screen turns off.</span></span>|
|<span data-ttu-id="f9848-218">settingsSessionTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f9848-218">settingsSessionTimeoutInMinutes</span></span>|<span data-ttu-id="f9848-219">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-219">Int32</span></span>|<span data-ttu-id="f9848-220">Especifica el número de minutos hasta que se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f9848-220">Specifies the number of minutes until the session times out.</span></span>|
|<span data-ttu-id="f9848-221">settingsSleepTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f9848-221">settingsSleepTimeoutInMinutes</span></span>|<span data-ttu-id="f9848-222">Int32</span><span class="sxs-lookup"><span data-stu-id="f9848-222">Int32</span></span>|<span data-ttu-id="f9848-223">Especifica el número de minutos hasta que el concentrador entra en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="f9848-223">Specifies the number of minutes until the Hub enters sleep mode.</span></span>|
|<span data-ttu-id="f9848-224">welcomeScreenBlockAutomaticWakeUp</span><span class="sxs-lookup"><span data-stu-id="f9848-224">welcomeScreenBlockAutomaticWakeUp</span></span>|<span data-ttu-id="f9848-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="f9848-225">Boolean</span></span>|<span data-ttu-id="f9848-226">Indica si se va a impedir que la pantalla de inicio de sesión se reactive automáticamente cuando alguien entre en la sala.</span><span class="sxs-lookup"><span data-stu-id="f9848-226">Indicates whether or not to Block the welcome screen from waking up automatically when someone enters the room.</span></span>|
|<span data-ttu-id="f9848-227">welcomeScreenBackgroundImageUrl</span><span class="sxs-lookup"><span data-stu-id="f9848-227">welcomeScreenBackgroundImageUrl</span></span>|<span data-ttu-id="f9848-228">Cadena</span><span class="sxs-lookup"><span data-stu-id="f9848-228">String</span></span>|<span data-ttu-id="f9848-229">Dirección URL de la imagen de fondo de la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="f9848-229">The welcome screen background image URL.</span></span> <span data-ttu-id="f9848-230">La dirección URL debe utilizar el protocolo HTTPS y devolver una imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="f9848-230">The URL must use the HTTPS protocol and return a PNG image.</span></span>|
|<span data-ttu-id="f9848-231">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="f9848-231">welcomeScreenMeetingInformation</span></span>|[<span data-ttu-id="f9848-232">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="f9848-232">welcomeScreenMeetingInformation</span></span>](../resources/intune-deviceconfig-welcomescreenmeetinginformation.md)|<span data-ttu-id="f9848-233">Información de la reunión que se muestra en la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="f9848-233">The welcome screen meeting information shown.</span></span> <span data-ttu-id="f9848-234">Los valores posibles son: `userDefined`, `showOrganizerAndTimeOnly` y `showOrganizerAndTimeAndSubject`.</span><span class="sxs-lookup"><span data-stu-id="f9848-234">Possible values are: `userDefined`, `showOrganizerAndTimeOnly`, `showOrganizerAndTimeAndSubject`.</span></span>|



## <a name="response"></a><span data-ttu-id="f9848-235">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9848-235">Response</span></span>
<span data-ttu-id="f9848-236">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9848-236">If successful, this method returns a `201 Created` response code and a [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9848-237">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9848-237">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9848-238">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9848-238">Request</span></span>
<span data-ttu-id="f9848-239">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9848-239">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1306

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```

### <a name="response"></a><span data-ttu-id="f9848-240">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9848-240">Response</span></span>
<span data-ttu-id="f9848-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9848-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1414

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```





