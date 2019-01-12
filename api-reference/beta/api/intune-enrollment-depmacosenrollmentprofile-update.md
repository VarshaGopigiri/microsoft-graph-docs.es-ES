---
title: Actualizar depMacOSEnrollmentProfile
description: Actualizar las propiedades de un objeto depMacOSEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a4fc28628e493c0691ad683d905cdffba3505fdb
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934033"
---
# <a name="update-depmacosenrollmentprofile"></a><span data-ttu-id="280de-103">Actualizar depMacOSEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="280de-103">Update depMacOSEnrollmentProfile</span></span>

> <span data-ttu-id="280de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="280de-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="280de-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="280de-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="280de-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="280de-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="280de-107">Actualizar las propiedades de un objeto [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="280de-107">Update the properties of a [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="280de-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="280de-108">Prerequisites</span></span>
<span data-ttu-id="280de-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="280de-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="280de-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="280de-111">Permission type</span></span>|<span data-ttu-id="280de-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="280de-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="280de-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="280de-113">Delegated (work or school account)</span></span>|<span data-ttu-id="280de-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="280de-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="280de-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="280de-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="280de-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="280de-116">Not supported.</span></span>|
|<span data-ttu-id="280de-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="280de-117">Application</span></span>|<span data-ttu-id="280de-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="280de-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="280de-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="280de-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/defaultMacOsEnrollmentProfile
```

## <a name="request-headers"></a><span data-ttu-id="280de-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="280de-120">Request headers</span></span>
|<span data-ttu-id="280de-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="280de-121">Header</span></span>|<span data-ttu-id="280de-122">Valor</span><span class="sxs-lookup"><span data-stu-id="280de-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="280de-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="280de-123">Authorization</span></span>|<span data-ttu-id="280de-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="280de-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="280de-125">Accept</span><span class="sxs-lookup"><span data-stu-id="280de-125">Accept</span></span>|<span data-ttu-id="280de-126">application/json</span><span class="sxs-lookup"><span data-stu-id="280de-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="280de-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="280de-127">Request body</span></span>
<span data-ttu-id="280de-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="280de-128">In the request body, supply a JSON representation for the [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) object.</span></span>

<span data-ttu-id="280de-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="280de-129">The following table shows the properties that are required when you create the [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md).</span></span>

|<span data-ttu-id="280de-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="280de-130">Property</span></span>|<span data-ttu-id="280de-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="280de-131">Type</span></span>|<span data-ttu-id="280de-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="280de-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="280de-133">id</span><span class="sxs-lookup"><span data-stu-id="280de-133">id</span></span>|<span data-ttu-id="280de-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-134">String</span></span>|<span data-ttu-id="280de-135">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-135">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-136">displayName</span><span class="sxs-lookup"><span data-stu-id="280de-136">displayName</span></span>|<span data-ttu-id="280de-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-137">String</span></span>|<span data-ttu-id="280de-138">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-138">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-139">descripción</span><span class="sxs-lookup"><span data-stu-id="280de-139">description</span></span>|<span data-ttu-id="280de-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-140">String</span></span>|<span data-ttu-id="280de-141">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-141">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="280de-142">requiresUserAuthentication</span></span>|<span data-ttu-id="280de-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-143">Boolean</span></span>|<span data-ttu-id="280de-144">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-144">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="280de-145">configurationEndpointUrl</span></span>|<span data-ttu-id="280de-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-146">String</span></span>|<span data-ttu-id="280de-147">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-147">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="280de-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="280de-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-149">Boolean</span></span>|<span data-ttu-id="280de-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="280de-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="280de-151">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-151">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="280de-152">isDefault</span><span class="sxs-lookup"><span data-stu-id="280de-152">isDefault</span></span>|<span data-ttu-id="280de-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-153">Boolean</span></span>|<span data-ttu-id="280de-154">Indica si este es el perfil predeterminado heredado de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-154">Indicates if this is the default profile Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-155">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="280de-155">supervisedModeEnabled</span></span>|<span data-ttu-id="280de-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-156">Boolean</span></span>|<span data-ttu-id="280de-157">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="280de-157">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="280de-158">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="280de-158">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span> <span data-ttu-id="280de-159">Se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-159">Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-160">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="280de-160">supportDepartment</span></span>|<span data-ttu-id="280de-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-161">String</span></span>|<span data-ttu-id="280de-162">Información de departamento de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-162">Support department information Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-163">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-163">passCodeDisabled</span></span>|<span data-ttu-id="280de-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-164">Boolean</span></span>|<span data-ttu-id="280de-165">Indica si el código de acceso del programa de instalación panel está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-165">Indicates if Passcode setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-166">isMandatory</span><span class="sxs-lookup"><span data-stu-id="280de-166">isMandatory</span></span>|<span data-ttu-id="280de-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-167">Boolean</span></span>|<span data-ttu-id="280de-168">Indica si el perfil es obligatorio heredada de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-168">Indicates if the profile is mandatory Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-169">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-169">locationDisabled</span></span>|<span data-ttu-id="280de-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-170">Boolean</span></span>|<span data-ttu-id="280de-171">Indica si la ubicación de panel de servicio del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-171">Indicates if Location service setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-172">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="280de-172">supportPhoneNumber</span></span>|<span data-ttu-id="280de-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="280de-173">String</span></span>|<span data-ttu-id="280de-174">Número de teléfono de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-174">Support phone number Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-175">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-175">profileRemovalDisabled</span></span>|<span data-ttu-id="280de-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-176">Boolean</span></span>|<span data-ttu-id="280de-177">Indica si está deshabilitada la opción de eliminación de perfiles se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-177">Indicates if the profile removal option is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-178">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="280de-178">restoreBlocked</span></span>|<span data-ttu-id="280de-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-179">Boolean</span></span>|<span data-ttu-id="280de-180">Indica si se bloquea el panel del programa de instalación de restauración se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-180">Indicates if Restore setup pane is blocked Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-181">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-181">appleIdDisabled</span></span>|<span data-ttu-id="280de-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-182">Boolean</span></span>|<span data-ttu-id="280de-183">Indica si Apple panel de identificador del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-183">Indicates if Apple id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-184">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-184">termsAndConditionsDisabled</span></span>|<span data-ttu-id="280de-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-185">Boolean</span></span>|<span data-ttu-id="280de-186">Indica si se deshabilita el panel del programa de instalación 'Términos y condiciones' se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-186">Indicates if 'Terms and Conditions' setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-187">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-187">touchIdDisabled</span></span>|<span data-ttu-id="280de-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-188">Boolean</span></span>|<span data-ttu-id="280de-189">Indica si se deshabilita el panel de táctil identificador del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-189">Indicates if touch id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-190">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-190">applePayDisabled</span></span>|<span data-ttu-id="280de-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-191">Boolean</span></span>|<span data-ttu-id="280de-192">Indica si se deshabilita el panel de Apple pago del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-192">Indicates if Apple pay setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-193">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-193">zoomDisabled</span></span>|<span data-ttu-id="280de-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-194">Boolean</span></span>|<span data-ttu-id="280de-195">Indica si se deshabilita el panel de zoom del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-195">Indicates if zoom setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-196">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-196">siriDisabled</span></span>|<span data-ttu-id="280de-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-197">Boolean</span></span>|<span data-ttu-id="280de-198">Indica si se deshabilita el panel de siri el programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-198">Indicates if siri setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-199">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-199">diagnosticsDisabled</span></span>|<span data-ttu-id="280de-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-200">Boolean</span></span>|<span data-ttu-id="280de-201">Indica si el diagnóstico panel del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="280de-201">Indicates if diagnostics setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="280de-202">registrationDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-202">registrationDisabled</span></span>|<span data-ttu-id="280de-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-203">Boolean</span></span>|<span data-ttu-id="280de-204">Indica si el registro está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="280de-204">Indicates if registration is disabled</span></span>|
|<span data-ttu-id="280de-205">fileVaultDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-205">fileVaultDisabled</span></span>|<span data-ttu-id="280de-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-206">Boolean</span></span>|<span data-ttu-id="280de-207">Indica si está deshabilitada la cámara de archivo</span><span class="sxs-lookup"><span data-stu-id="280de-207">Indicates if file vault is disabled</span></span>|
|<span data-ttu-id="280de-208">iCloudDiagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="280de-208">iCloudDiagnosticsDisabled</span></span>|<span data-ttu-id="280de-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="280de-209">Boolean</span></span>|<span data-ttu-id="280de-210">Indica si se deshabilita la pantalla de análisis iCloud</span><span class="sxs-lookup"><span data-stu-id="280de-210">Indicates if iCloud Analytics screen is disabled</span></span>|



## <a name="response"></a><span data-ttu-id="280de-211">Respuesta</span><span class="sxs-lookup"><span data-stu-id="280de-211">Response</span></span>
<span data-ttu-id="280de-212">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="280de-212">If successful, this method returns a `200 OK` response code and an updated [depMacOSEnrollmentProfile](../resources/intune-enrollment-depmacosenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="280de-213">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="280de-213">Example</span></span>
### <a name="request"></a><span data-ttu-id="280de-214">Solicitud</span><span class="sxs-lookup"><span data-stu-id="280de-214">Request</span></span>
<span data-ttu-id="280de-215">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="280de-215">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/defaultMacOsEnrollmentProfile
Content-type: application/json
Content-length: 864

{
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "Support Department value",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "Support Phone Number value",
  "profileRemovalDisabled": true,
  "restoreBlocked": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "registrationDisabled": true,
  "fileVaultDisabled": true,
  "iCloudDiagnosticsDisabled": true
}
```

### <a name="response"></a><span data-ttu-id="280de-216">Respuesta</span><span class="sxs-lookup"><span data-stu-id="280de-216">Response</span></span>
<span data-ttu-id="280de-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="280de-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 977

{
  "@odata.type": "#microsoft.graph.depMacOSEnrollmentProfile",
  "id": "e433c95c-c95c-e433-5cc9-33e45cc933e4",
  "displayName": "Display Name value",
  "description": "Description value",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "https://example.com/configurationEndpointUrl/",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "Support Department value",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "Support Phone Number value",
  "profileRemovalDisabled": true,
  "restoreBlocked": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "registrationDisabled": true,
  "fileVaultDisabled": true,
  "iCloudDiagnosticsDisabled": true
}
```





