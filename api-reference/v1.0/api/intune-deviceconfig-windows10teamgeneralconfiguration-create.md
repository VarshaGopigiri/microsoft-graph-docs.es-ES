---
title: Crear windows10TeamGeneralConfiguration
description: Cree un objeto windows10TeamGeneralConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8ef95d24823abd5a125ad210a4eed81a61e1de1b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846616"
---
# <a name="create-windows10teamgeneralconfiguration"></a><span data-ttu-id="1d2d1-103">Crear windows10TeamGeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d2d1-103">Create windows10TeamGeneralConfiguration</span></span>

> <span data-ttu-id="1d2d1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1d2d1-105">Cree un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1d2d1-105">Create a new [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1d2d1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d2d1-106">Prerequisites</span></span>
<span data-ttu-id="1d2d1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1d2d1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1d2d1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1d2d1-109">Permission type</span></span>|<span data-ttu-id="1d2d1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1d2d1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1d2d1-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1d2d1-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1d2d1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1d2d1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-114">Not supported.</span></span>|
|<span data-ttu-id="1d2d1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1d2d1-115">Application</span></span>|<span data-ttu-id="1d2d1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1d2d1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d2d1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1d2d1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d2d1-118">Request headers</span></span>
|<span data-ttu-id="1d2d1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d2d1-119">Header</span></span>|<span data-ttu-id="1d2d1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2d1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1d2d1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1d2d1-121">Authorization</span></span>|<span data-ttu-id="1d2d1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1d2d1-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1d2d1-123">Accept</span></span>|<span data-ttu-id="1d2d1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1d2d1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d2d1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1d2d1-125">Request body</span></span>
<span data-ttu-id="1d2d1-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-126">In the request body, supply a JSON representation for the windows10TeamGeneralConfiguration object.</span></span>

<span data-ttu-id="1d2d1-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windows10TeamGeneralConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-127">The following table shows the properties that are required when you create the windows10TeamGeneralConfiguration.</span></span>

|<span data-ttu-id="1d2d1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1d2d1-128">Property</span></span>|<span data-ttu-id="1d2d1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d2d1-129">Type</span></span>|<span data-ttu-id="1d2d1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d2d1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1d2d1-131">id</span><span class="sxs-lookup"><span data-stu-id="1d2d1-131">id</span></span>|<span data-ttu-id="1d2d1-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-132">String</span></span>|<span data-ttu-id="1d2d1-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-133">Key of the entity.</span></span> <span data-ttu-id="1d2d1-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1d2d1-135">lastModifiedDateTime</span></span>|<span data-ttu-id="1d2d1-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d2d1-136">DateTimeOffset</span></span>|<span data-ttu-id="1d2d1-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-137">DateTime the object was last modified.</span></span> <span data-ttu-id="1d2d1-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1d2d1-139">createdDateTime</span></span>|<span data-ttu-id="1d2d1-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1d2d1-140">DateTimeOffset</span></span>|<span data-ttu-id="1d2d1-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-141">DateTime the object was created.</span></span> <span data-ttu-id="1d2d1-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-143">descripción</span><span class="sxs-lookup"><span data-stu-id="1d2d1-143">description</span></span>|<span data-ttu-id="1d2d1-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-144">String</span></span>|<span data-ttu-id="1d2d1-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1d2d1-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-147">displayName</span><span class="sxs-lookup"><span data-stu-id="1d2d1-147">displayName</span></span>|<span data-ttu-id="1d2d1-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-148">String</span></span>|<span data-ttu-id="1d2d1-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1d2d1-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-151">version</span><span class="sxs-lookup"><span data-stu-id="1d2d1-151">version</span></span>|<span data-ttu-id="1d2d1-152">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-152">Int32</span></span>|<span data-ttu-id="1d2d1-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-153">Version of the device configuration.</span></span> <span data-ttu-id="1d2d1-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1d2d1-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1d2d1-155">azureOperationalInsightsBlockTelemetry</span><span class="sxs-lookup"><span data-stu-id="1d2d1-155">azureOperationalInsightsBlockTelemetry</span></span>|<span data-ttu-id="1d2d1-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-156">Boolean</span></span>|<span data-ttu-id="1d2d1-157">Indica si se va a bloquear Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-157">Indicates whether or not to Block Azure Operational Insights.</span></span>|
|<span data-ttu-id="1d2d1-158">azureOperationalInsightsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="1d2d1-158">azureOperationalInsightsWorkspaceId</span></span>|<span data-ttu-id="1d2d1-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-159">String</span></span>|<span data-ttu-id="1d2d1-160">Identificador del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-160">The Azure Operational Insights workspace id.</span></span>|
|<span data-ttu-id="1d2d1-161">azureOperationalInsightsWorkspaceKey</span><span class="sxs-lookup"><span data-stu-id="1d2d1-161">azureOperationalInsightsWorkspaceKey</span></span>|<span data-ttu-id="1d2d1-162">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-162">String</span></span>|<span data-ttu-id="1d2d1-163">Clave del área de trabajo de Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-163">The Azure Operational Insights Workspace key.</span></span>|
|<span data-ttu-id="1d2d1-164">connectAppBlockAutoLaunch</span><span class="sxs-lookup"><span data-stu-id="1d2d1-164">connectAppBlockAutoLaunch</span></span>|<span data-ttu-id="1d2d1-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-165">Boolean</span></span>|<span data-ttu-id="1d2d1-166">Especifica si se iniciará automáticamente la aplicación Conectar cada vez que se inicie un proyecto.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-166">Specifies whether to automatically launch the Connect app whenever a projection is initiated.</span></span>|
|<span data-ttu-id="1d2d1-167">maintenanceWindowBlocked</span><span class="sxs-lookup"><span data-stu-id="1d2d1-167">maintenanceWindowBlocked</span></span>|<span data-ttu-id="1d2d1-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-168">Boolean</span></span>|<span data-ttu-id="1d2d1-169">Indica si se va a bloquear la configuración de un período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-169">Indicates whether or not to Block setting a maintenance window for device updates.</span></span>|
|<span data-ttu-id="1d2d1-170">maintenanceWindowDurationInHours</span><span class="sxs-lookup"><span data-stu-id="1d2d1-170">maintenanceWindowDurationInHours</span></span>|<span data-ttu-id="1d2d1-171">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-171">Int32</span></span>|<span data-ttu-id="1d2d1-172">Duración del período de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-172">Maintenance window duration for device updates.</span></span> <span data-ttu-id="1d2d1-173">Valores válidos de 0 a 5</span><span class="sxs-lookup"><span data-stu-id="1d2d1-173">Valid values 0 to 5</span></span>|
|<span data-ttu-id="1d2d1-174">maintenanceWindowStartTime</span><span class="sxs-lookup"><span data-stu-id="1d2d1-174">maintenanceWindowStartTime</span></span>|<span data-ttu-id="1d2d1-175">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="1d2d1-175">TimeOfDay</span></span>|<span data-ttu-id="1d2d1-176">Hora de inicio del periodo de mantenimiento para las actualizaciones del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-176">Maintenance window start time for device updates.</span></span>|
|<span data-ttu-id="1d2d1-177">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="1d2d1-177">miracastChannel</span></span>|[<span data-ttu-id="1d2d1-178">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="1d2d1-178">miracastChannel</span></span>](../resources/intune-deviceconfig-miracastchannel.md)|<span data-ttu-id="1d2d1-179">Canal.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-179">The channel.</span></span> <span data-ttu-id="1d2d1-180">Los valores posibles son: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne` y `oneHundredSixtyFive`.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-180">Possible values are: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne`, `oneHundredSixtyFive`.</span></span>|
|<span data-ttu-id="1d2d1-181">miracastBlocked</span><span class="sxs-lookup"><span data-stu-id="1d2d1-181">miracastBlocked</span></span>|<span data-ttu-id="1d2d1-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-182">Boolean</span></span>|<span data-ttu-id="1d2d1-183">Indica si se van a bloquear las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-183">Indicates whether or not to Block wireless projection.</span></span>|
|<span data-ttu-id="1d2d1-184">miracastRequirePin</span><span class="sxs-lookup"><span data-stu-id="1d2d1-184">miracastRequirePin</span></span>|<span data-ttu-id="1d2d1-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-185">Boolean</span></span>|<span data-ttu-id="1d2d1-186">Indica si se va a requerir un PIN para las proyecciones inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-186">Indicates whether or not to require a pin for wireless projection.</span></span>|
|<span data-ttu-id="1d2d1-187">settingsBlockMyMeetingsAndFiles</span><span class="sxs-lookup"><span data-stu-id="1d2d1-187">settingsBlockMyMeetingsAndFiles</span></span>|<span data-ttu-id="1d2d1-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-188">Boolean</span></span>|<span data-ttu-id="1d2d1-189">Especifica si se deshabilita la característica "Mis reuniones y archivos" en el menú Inicio, que muestra las reuniones y los archivos del usuario que ha iniciado sesión en Office 365.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-189">Specifies whether to disable the "My meetings and files" feature in the Start menu, which shows the signed-in user's meetings and files from Office 365.</span></span>|
|<span data-ttu-id="1d2d1-190">settingsBlockSessionResume</span><span class="sxs-lookup"><span data-stu-id="1d2d1-190">settingsBlockSessionResume</span></span>|<span data-ttu-id="1d2d1-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-191">Boolean</span></span>|<span data-ttu-id="1d2d1-192">Especifica si se permite la posibilidad de reanudar una sesión cuando se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-192">Specifies whether to allow the ability to resume a session when the session times out.</span></span>|
|<span data-ttu-id="1d2d1-193">settingsBlockSigninSuggestions</span><span class="sxs-lookup"><span data-stu-id="1d2d1-193">settingsBlockSigninSuggestions</span></span>|<span data-ttu-id="1d2d1-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-194">Boolean</span></span>|<span data-ttu-id="1d2d1-195">Especifica si se deshabilita la opción de rellenar automáticamente el cuadro de diálogo de inicio de sesión con invitados de reuniones programadas.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-195">Specifies whether to disable auto-populating of the sign-in dialog with invitees from scheduled meetings.</span></span>|
|<span data-ttu-id="1d2d1-196">settingsDefaultVolume</span><span class="sxs-lookup"><span data-stu-id="1d2d1-196">settingsDefaultVolume</span></span>|<span data-ttu-id="1d2d1-197">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-197">Int32</span></span>|<span data-ttu-id="1d2d1-198">Especifica el valor de volumen predeterminado para una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-198">Specifies the default volume value for a new session.</span></span> <span data-ttu-id="1d2d1-199">Los valores permitidos son de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-199">Permitted values are 0-100.</span></span> <span data-ttu-id="1d2d1-200">El valor predeterminado es 45.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-200">The default is 45.</span></span> <span data-ttu-id="1d2d1-201">Valores válidos de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-201">Valid values 0 to 100</span></span>|
|<span data-ttu-id="1d2d1-202">settingsScreenTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1d2d1-202">settingsScreenTimeoutInMinutes</span></span>|<span data-ttu-id="1d2d1-203">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-203">Int32</span></span>|<span data-ttu-id="1d2d1-204">Especifica el número de minutos hasta que se desconecta la pantalla Concentrador.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-204">Specifies the number of minutes until the Hub screen turns off.</span></span>|
|<span data-ttu-id="1d2d1-205">settingsSessionTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1d2d1-205">settingsSessionTimeoutInMinutes</span></span>|<span data-ttu-id="1d2d1-206">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-206">Int32</span></span>|<span data-ttu-id="1d2d1-207">Especifica el número de minutos hasta que se agota el tiempo de espera de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-207">Specifies the number of minutes until the session times out.</span></span>|
|<span data-ttu-id="1d2d1-208">settingsSleepTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1d2d1-208">settingsSleepTimeoutInMinutes</span></span>|<span data-ttu-id="1d2d1-209">Int32</span><span class="sxs-lookup"><span data-stu-id="1d2d1-209">Int32</span></span>|<span data-ttu-id="1d2d1-210">Especifica el número de minutos hasta que el concentrador entra en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-210">Specifies the number of minutes until the Hub enters sleep mode.</span></span>|
|<span data-ttu-id="1d2d1-211">welcomeScreenBlockAutomaticWakeUp</span><span class="sxs-lookup"><span data-stu-id="1d2d1-211">welcomeScreenBlockAutomaticWakeUp</span></span>|<span data-ttu-id="1d2d1-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="1d2d1-212">Boolean</span></span>|<span data-ttu-id="1d2d1-213">Indica si se va a impedir que la pantalla de inicio de sesión se reactive automáticamente cuando alguien entre en la sala.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-213">Indicates whether or not to Block the welcome screen from waking up automatically when someone enters the room.</span></span>|
|<span data-ttu-id="1d2d1-214">welcomeScreenBackgroundImageUrl</span><span class="sxs-lookup"><span data-stu-id="1d2d1-214">welcomeScreenBackgroundImageUrl</span></span>|<span data-ttu-id="1d2d1-215">Cadena</span><span class="sxs-lookup"><span data-stu-id="1d2d1-215">String</span></span>|<span data-ttu-id="1d2d1-216">Dirección URL de la imagen de fondo de la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-216">The welcome screen background image URL.</span></span> <span data-ttu-id="1d2d1-217">La dirección URL debe utilizar el protocolo HTTPS y devolver una imagen PNG.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-217">The URL must use the HTTPS protocol and return a PNG image.</span></span>|
|<span data-ttu-id="1d2d1-218">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="1d2d1-218">welcomeScreenMeetingInformation</span></span>|[<span data-ttu-id="1d2d1-219">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="1d2d1-219">welcomeScreenMeetingInformation</span></span>](../resources/intune-deviceconfig-welcomescreenmeetinginformation.md)|<span data-ttu-id="1d2d1-220">Información de la reunión que se muestra en la pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-220">The welcome screen meeting information shown.</span></span> <span data-ttu-id="1d2d1-221">Los valores posibles son: `userDefined`, `showOrganizerAndTimeOnly` y `showOrganizerAndTimeAndSubject`.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-221">Possible values are: `userDefined`, `showOrganizerAndTimeOnly`, `showOrganizerAndTimeAndSubject`.</span></span>|



## <a name="response"></a><span data-ttu-id="1d2d1-222">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d2d1-222">Response</span></span>
<span data-ttu-id="1d2d1-223">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-223">If successful, this method returns a `201 Created` response code and a [windows10TeamGeneralConfiguration](../resources/intune-deviceconfig-windows10teamgeneralconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d2d1-224">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d2d1-224">Example</span></span>
### <a name="request"></a><span data-ttu-id="1d2d1-225">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d2d1-225">Request</span></span>
<span data-ttu-id="1d2d1-226">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-226">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="1d2d1-227">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d2d1-227">Response</span></span>
<span data-ttu-id="1d2d1-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d2d1-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



