---
title: Actualizar windows10TeamGeneralConfiguration
description: Actualice las propiedades de un objeto windows10TeamGeneralConfiguration.
ms.openlocfilehash: f3eeccfdb5d632e19e533ea9ec2bb07fc9ade297
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030070"
---
# <a name="update-windows10teamgeneralconfiguration"></a><span data-ttu-id="cf4fa-103">Actualizar windows10TeamGeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf4fa-103">Update windows10TeamGeneralConfiguration</span></span>

> <span data-ttu-id="cf4fa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf4fa-105">Actualice las propiedades de un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf4fa-105">Update the properties of a [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf4fa-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf4fa-106">Prerequisites</span></span>
<span data-ttu-id="cf4fa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cf4fa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cf4fa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf4fa-109">Permission type</span></span>|<span data-ttu-id="cf4fa-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf4fa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cf4fa-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cf4fa-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="cf4fa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf4fa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-114">Not supported.</span></span>|
|<span data-ttu-id="cf4fa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf4fa-115">Application</span></span>|<span data-ttu-id="cf4fa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf4fa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf4fa-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="cf4fa-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf4fa-118">Request headers</span></span>
|<span data-ttu-id="cf4fa-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf4fa-119">Header</span></span>|<span data-ttu-id="cf4fa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf4fa-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf4fa-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf4fa-121">Authorization</span></span>|<span data-ttu-id="cf4fa-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf4fa-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cf4fa-123">Accept</span></span>|<span data-ttu-id="cf4fa-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cf4fa-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf4fa-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf4fa-125">Request body</span></span>
<span data-ttu-id="cf4fa-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf4fa-126">In the request body, supply a JSON representation for the [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object.</span></span>

<span data-ttu-id="cf4fa-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf4fa-127">The following table shows the properties that are required when you create the [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span></span>

|<span data-ttu-id="cf4fa-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf4fa-128">Property</span></span>|<span data-ttu-id="cf4fa-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf4fa-129">Type</span></span>|<span data-ttu-id="cf4fa-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf4fa-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf4fa-131">id</span><span class="sxs-lookup"><span data-stu-id="cf4fa-131">id</span></span>|<span data-ttu-id="cf4fa-132">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-132">String</span></span>|<span data-ttu-id="cf4fa-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-133">Key of the entity.</span></span> <span data-ttu-id="cf4fa-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cf4fa-135">lastModifiedDateTime</span></span>|<span data-ttu-id="cf4fa-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf4fa-136">DateTimeOffset</span></span>|<span data-ttu-id="cf4fa-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-137">DateTime the object was last modified.</span></span> <span data-ttu-id="cf4fa-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cf4fa-139">createdDateTime</span></span>|<span data-ttu-id="cf4fa-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cf4fa-140">DateTimeOffset</span></span>|<span data-ttu-id="cf4fa-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-141">DateTime the object was created.</span></span> <span data-ttu-id="cf4fa-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-143">descripción</span><span class="sxs-lookup"><span data-stu-id="cf4fa-143">description</span></span>|<span data-ttu-id="cf4fa-144">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-144">String</span></span>|<span data-ttu-id="cf4fa-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="cf4fa-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-147">displayName</span><span class="sxs-lookup"><span data-stu-id="cf4fa-147">displayName</span></span>|<span data-ttu-id="cf4fa-148">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-148">String</span></span>|<span data-ttu-id="cf4fa-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="cf4fa-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-151">version</span><span class="sxs-lookup"><span data-stu-id="cf4fa-151">version</span></span>|<span data-ttu-id="cf4fa-152">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-152">Int32</span></span>|<span data-ttu-id="cf4fa-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-153">Version of the device configuration.</span></span> <span data-ttu-id="cf4fa-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cf4fa-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cf4fa-155">azureOperationalInsightsBlockTelemetry</span><span class="sxs-lookup"><span data-stu-id="cf4fa-155">azureOperationalInsightsBlockTelemetry</span></span>|<span data-ttu-id="cf4fa-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-156">Boolean</span></span>|<span data-ttu-id="cf4fa-157">Indica si se va a bloquear Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-157">Indicates whether or not to Block Azure Operational Insights.</span></span>|
|<span data-ttu-id="cf4fa-158">azureOperationalInsightsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="cf4fa-158">azureOperationalInsightsWorkspaceId</span></span>|<span data-ttu-id="cf4fa-159">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-159">String</span></span>|<span data-ttu-id="cf4fa-160">Identificador del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-160">The Azure Operational Insights workspace id.</span></span>|
|<span data-ttu-id="cf4fa-161">azureOperationalInsightsWorkspaceKey</span><span class="sxs-lookup"><span data-stu-id="cf4fa-161">azureOperationalInsightsWorkspaceKey</span></span>|<span data-ttu-id="cf4fa-162">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-162">String</span></span>|<span data-ttu-id="cf4fa-163">Clave del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-163">The Azure Operational Insights Workspace key.</span></span>|
|<span data-ttu-id="cf4fa-164">connectAppBlockAutoLaunch</span><span class="sxs-lookup"><span data-stu-id="cf4fa-164">connectAppBlockAutoLaunch</span></span>|<span data-ttu-id="cf4fa-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-165">Boolean</span></span>|<span data-ttu-id="cf4fa-166">Especifica si se iniciará automáticamente la aplicación Conectar cada vez que se inicie un proyecto.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-166">Specifies whether to automatically launch the Connect app whenever a projection is initiated.</span></span>|
|<span data-ttu-id="cf4fa-167">maintenanceWindowBlocked</span><span class="sxs-lookup"><span data-stu-id="cf4fa-167">maintenanceWindowBlocked</span></span>|<span data-ttu-id="cf4fa-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-168">Boolean</span></span>|<span data-ttu-id="cf4fa-169">Indica si se va a bloquear la configuración de un período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-169">Indicates whether or not to Block setting a maintenance window for device updates.</span></span>|
|<span data-ttu-id="cf4fa-170">maintenanceWindowDurationInHours</span><span class="sxs-lookup"><span data-stu-id="cf4fa-170">maintenanceWindowDurationInHours</span></span>|<span data-ttu-id="cf4fa-171">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-171">Int32</span></span>|<span data-ttu-id="cf4fa-172">Duración del período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-172">Maintenance window duration for device updates.</span></span> <span data-ttu-id="cf4fa-173">Valores válidos de 0 a 5</span><span class="sxs-lookup"><span data-stu-id="cf4fa-173">Valid values 0 to 5</span></span>|
|<span data-ttu-id="cf4fa-174">maintenanceWindowStartTime</span><span class="sxs-lookup"><span data-stu-id="cf4fa-174">maintenanceWindowStartTime</span></span>|<span data-ttu-id="cf4fa-175">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="cf4fa-175">TimeOfDay</span></span>|<span data-ttu-id="cf4fa-176">Hora de inicio del periodo de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-176">Maintenance window start time for device updates.</span></span>|
|<span data-ttu-id="cf4fa-177">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="cf4fa-177">miracastChannel</span></span>|[<span data-ttu-id="cf4fa-178">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="cf4fa-178">miracastChannel</span></span>](../resources/intune-deviceconfig-miracastchannel.md)|<span data-ttu-id="cf4fa-179">Canal.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-179">The channel.</span></span> <span data-ttu-id="cf4fa-180">Los valores posibles son: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne` y `oneHundredSixtyFive`.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-180">Possible values are: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne`, `oneHundredSixtyFive`.</span></span>|
|<span data-ttu-id="cf4fa-181">miracastBlocked</span><span class="sxs-lookup"><span data-stu-id="cf4fa-181">miracastBlocked</span></span>|<span data-ttu-id="cf4fa-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-182">Boolean</span></span>|<span data-ttu-id="cf4fa-183">Indica si se van a bloquear las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-183">Indicates whether or not to Block wireless projection.</span></span>|
|<span data-ttu-id="cf4fa-184">miracastRequirePin</span><span class="sxs-lookup"><span data-stu-id="cf4fa-184">miracastRequirePin</span></span>|<span data-ttu-id="cf4fa-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-185">Boolean</span></span>|<span data-ttu-id="cf4fa-186">Indica si se va a requerir un PIN para las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-186">Indicates whether or not to require a pin for wireless projection.</span></span>|
|<span data-ttu-id="cf4fa-187">settingsBlockMyMeetingsAndFiles</span><span class="sxs-lookup"><span data-stu-id="cf4fa-187">settingsBlockMyMeetingsAndFiles</span></span>|<span data-ttu-id="cf4fa-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-188">Boolean</span></span>|<span data-ttu-id="cf4fa-189">Especifica si se deshabilita la característica "Mis reuniones y archivos" en el menú Inicio, que muestra las reuniones y los archivos del usuario que ha iniciado sesión en Office 365.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-189">Specifies whether to disable the "My meetings and files" feature in the Start menu, which shows the signed-in user's meetings and files from Office 365.</span></span>|
|<span data-ttu-id="cf4fa-190">settingsBlockSessionResume</span><span class="sxs-lookup"><span data-stu-id="cf4fa-190">settingsBlockSessionResume</span></span>|<span data-ttu-id="cf4fa-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-191">Boolean</span></span>|<span data-ttu-id="cf4fa-192">Especifica si se permite la posibilidad de reanudar una sesión cuando se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-192">Specifies whether to allow the ability to resume a session when the session times out.</span></span>|
|<span data-ttu-id="cf4fa-193">settingsBlockSigninSuggestions</span><span class="sxs-lookup"><span data-stu-id="cf4fa-193">settingsBlockSigninSuggestions</span></span>|<span data-ttu-id="cf4fa-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-194">Boolean</span></span>|<span data-ttu-id="cf4fa-195">Especifica si se deshabilita la opción de rellenar automáticamente el cuadro de diálogo de inicio de sesión con invitados de reuniones programadas.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-195">Specifies whether to disable auto-populating of the sign-in dialog with invitees from scheduled meetings.</span></span>|
|<span data-ttu-id="cf4fa-196">settingsDefaultVolume</span><span class="sxs-lookup"><span data-stu-id="cf4fa-196">settingsDefaultVolume</span></span>|<span data-ttu-id="cf4fa-197">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-197">Int32</span></span>|<span data-ttu-id="cf4fa-198">Especifica el valor de volumen predeterminado para una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-198">Specifies the default volume value for a new session.</span></span> <span data-ttu-id="cf4fa-199">Los valores permitidos son de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-199">Permitted values are 0-100.</span></span> <span data-ttu-id="cf4fa-200">El valor predeterminado es 45.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-200">The default is 45.</span></span> <span data-ttu-id="cf4fa-201">Valores válidos de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-201">Valid values 0 to 100</span></span>|
|<span data-ttu-id="cf4fa-202">settingsScreenTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cf4fa-202">settingsScreenTimeoutInMinutes</span></span>|<span data-ttu-id="cf4fa-203">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-203">Int32</span></span>|<span data-ttu-id="cf4fa-204">Especifica el número de minutos hasta que se desconecta la pantalla Concentrador.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-204">Specifies the number of minutes until the Hub screen turns off.</span></span>|
|<span data-ttu-id="cf4fa-205">settingsSessionTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cf4fa-205">settingsSessionTimeoutInMinutes</span></span>|<span data-ttu-id="cf4fa-206">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-206">Int32</span></span>|<span data-ttu-id="cf4fa-207">Especifica el número de minutos hasta que se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-207">Specifies the number of minutes until the session times out.</span></span>|
|<span data-ttu-id="cf4fa-208">settingsSleepTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cf4fa-208">settingsSleepTimeoutInMinutes</span></span>|<span data-ttu-id="cf4fa-209">Int32</span><span class="sxs-lookup"><span data-stu-id="cf4fa-209">Int32</span></span>|<span data-ttu-id="cf4fa-210">Especifica el número de minutos hasta que el concentrador entra en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-210">Specifies the number of minutes until the Hub enters sleep mode.</span></span>|
|<span data-ttu-id="cf4fa-211">welcomeScreenBlockAutomaticWakeUp</span><span class="sxs-lookup"><span data-stu-id="cf4fa-211">welcomeScreenBlockAutomaticWakeUp</span></span>|<span data-ttu-id="cf4fa-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="cf4fa-212">Boolean</span></span>|<span data-ttu-id="cf4fa-213">Indica si se va a impedir que la pantalla de inicio de sesión se reactive automáticamente cuando alguien entre en la sala.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-213">Indicates whether or not to Block the welcome screen from waking up automatically when someone enters the room.</span></span>|
|<span data-ttu-id="cf4fa-214">welcomeScreenBackgroundImageUrl</span><span class="sxs-lookup"><span data-stu-id="cf4fa-214">welcomeScreenBackgroundImageUrl</span></span>|<span data-ttu-id="cf4fa-215">String</span><span class="sxs-lookup"><span data-stu-id="cf4fa-215">String</span></span>|<span data-ttu-id="cf4fa-216">Dirección URL de la imagen de fondo de la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-216">The welcome screen background image URL.</span></span> <span data-ttu-id="cf4fa-217">La dirección URL debe utilizar el protocolo HTTPS y devolver una imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-217">The URL must use the HTTPS protocol and return a PNG image.</span></span>|
|<span data-ttu-id="cf4fa-218">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="cf4fa-218">welcomeScreenMeetingInformation</span></span>|[<span data-ttu-id="cf4fa-219">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="cf4fa-219">welcomeScreenMeetingInformation</span></span>](../resources/intune-deviceconfig-welcomescreenmeetinginformation.md)|<span data-ttu-id="cf4fa-220">Información de la reunión que se muestra en la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-220">The welcome screen meeting information shown.</span></span> <span data-ttu-id="cf4fa-221">Los valores posibles son: `userDefined`, `showOrganizerAndTimeOnly` y `showOrganizerAndTimeAndSubject`.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-221">Possible values are: `userDefined`, `showOrganizerAndTimeOnly`, `showOrganizerAndTimeAndSubject`.</span></span>|



## <a name="response"></a><span data-ttu-id="cf4fa-222">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf4fa-222">Response</span></span>
<span data-ttu-id="cf4fa-223">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-223">If successful, this method returns a `200 OK` response code and an updated [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf4fa-224">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf4fa-224">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf4fa-225">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf4fa-225">Request</span></span>
<span data-ttu-id="cf4fa-226">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-226">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1150

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
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

### <a name="response"></a><span data-ttu-id="cf4fa-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf4fa-227">Response</span></span>
<span data-ttu-id="cf4fa-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf4fa-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1322

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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



