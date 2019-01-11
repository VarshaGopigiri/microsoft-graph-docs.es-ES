---
title: Crear depEnrollmentProfile
description: Crear un nuevo objeto depEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3c7936af86b25fbf0c4e022adef0bc387c56b196
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828150"
---
# <a name="create-depenrollmentprofile"></a><span data-ttu-id="fefbd-103">Crear depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="fefbd-103">Create depEnrollmentProfile</span></span>

> <span data-ttu-id="fefbd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fefbd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fefbd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fefbd-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="fefbd-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fefbd-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fefbd-107">Crear un nuevo objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="fefbd-107">Create a new [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fefbd-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fefbd-108">Prerequisites</span></span>
<span data-ttu-id="fefbd-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fefbd-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fefbd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fefbd-111">Permission type</span></span>|<span data-ttu-id="fefbd-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fefbd-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fefbd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fefbd-113">Delegated (work or school account)</span></span>|<span data-ttu-id="fefbd-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fefbd-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="fefbd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fefbd-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fefbd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fefbd-116">Not supported.</span></span>|
|<span data-ttu-id="fefbd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fefbd-117">Application</span></span>|<span data-ttu-id="fefbd-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fefbd-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fefbd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fefbd-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="fefbd-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fefbd-120">Request headers</span></span>
|<span data-ttu-id="fefbd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fefbd-121">Header</span></span>|<span data-ttu-id="fefbd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fefbd-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fefbd-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="fefbd-123">Authorization</span></span>|<span data-ttu-id="fefbd-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fefbd-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fefbd-125">Accept</span><span class="sxs-lookup"><span data-stu-id="fefbd-125">Accept</span></span>|<span data-ttu-id="fefbd-126">application/json</span><span class="sxs-lookup"><span data-stu-id="fefbd-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fefbd-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fefbd-127">Request body</span></span>
<span data-ttu-id="fefbd-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto depEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="fefbd-128">In the request body, supply a JSON representation for the depEnrollmentProfile object.</span></span>

<span data-ttu-id="fefbd-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el depEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="fefbd-129">The following table shows the properties that are required when you create the depEnrollmentProfile.</span></span>

|<span data-ttu-id="fefbd-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fefbd-130">Property</span></span>|<span data-ttu-id="fefbd-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fefbd-131">Type</span></span>|<span data-ttu-id="fefbd-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="fefbd-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fefbd-133">id</span><span class="sxs-lookup"><span data-stu-id="fefbd-133">id</span></span>|<span data-ttu-id="fefbd-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-134">String</span></span>|<span data-ttu-id="fefbd-135">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-135">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-136">displayName</span><span class="sxs-lookup"><span data-stu-id="fefbd-136">displayName</span></span>|<span data-ttu-id="fefbd-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-137">String</span></span>|<span data-ttu-id="fefbd-138">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-138">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-139">descripción</span><span class="sxs-lookup"><span data-stu-id="fefbd-139">description</span></span>|<span data-ttu-id="fefbd-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-140">String</span></span>|<span data-ttu-id="fefbd-141">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-141">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="fefbd-142">requiresUserAuthentication</span></span>|<span data-ttu-id="fefbd-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-143">Boolean</span></span>|<span data-ttu-id="fefbd-144">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-144">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="fefbd-145">configurationEndpointUrl</span></span>|<span data-ttu-id="fefbd-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-146">String</span></span>|<span data-ttu-id="fefbd-147">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-147">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="fefbd-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="fefbd-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-149">Boolean</span></span>|<span data-ttu-id="fefbd-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="fefbd-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="fefbd-151">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-151">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="fefbd-152">isDefault</span><span class="sxs-lookup"><span data-stu-id="fefbd-152">isDefault</span></span>|<span data-ttu-id="fefbd-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-153">Boolean</span></span>|<span data-ttu-id="fefbd-154">Indica si este es el perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="fefbd-154">Indicates if this is the default profile</span></span>|
|<span data-ttu-id="fefbd-155">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-155">supervisedModeEnabled</span></span>|<span data-ttu-id="fefbd-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-156">Boolean</span></span>|<span data-ttu-id="fefbd-157">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fefbd-157">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="fefbd-158">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="fefbd-158">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span>|
|<span data-ttu-id="fefbd-159">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="fefbd-159">supportDepartment</span></span>|<span data-ttu-id="fefbd-160">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-160">String</span></span>|<span data-ttu-id="fefbd-161">Información del departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="fefbd-161">Support department information</span></span>|
|<span data-ttu-id="fefbd-162">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-162">passCodeDisabled</span></span>|<span data-ttu-id="fefbd-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-163">Boolean</span></span>|<span data-ttu-id="fefbd-164">Indica si se deshabilita el panel de código de acceso del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-164">Indicates if Passcode setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-165">isMandatory</span><span class="sxs-lookup"><span data-stu-id="fefbd-165">isMandatory</span></span>|<span data-ttu-id="fefbd-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-166">Boolean</span></span>|<span data-ttu-id="fefbd-167">Indica si el perfil es obligatorio</span><span class="sxs-lookup"><span data-stu-id="fefbd-167">Indicates if the profile is mandatory</span></span>|
|<span data-ttu-id="fefbd-168">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-168">locationDisabled</span></span>|<span data-ttu-id="fefbd-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-169">Boolean</span></span>|<span data-ttu-id="fefbd-170">Indica si se deshabilita el panel del programa de instalación del servicio de ubicación</span><span class="sxs-lookup"><span data-stu-id="fefbd-170">Indicates if Location service setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-171">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="fefbd-171">supportPhoneNumber</span></span>|<span data-ttu-id="fefbd-172">Cadena</span><span class="sxs-lookup"><span data-stu-id="fefbd-172">String</span></span>|<span data-ttu-id="fefbd-173">Número de teléfono de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="fefbd-173">Support phone number</span></span>|
|<span data-ttu-id="fefbd-174">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="fefbd-174">iTunesPairingMode</span></span>|[<span data-ttu-id="fefbd-175">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="fefbd-175">iTunesPairingMode</span></span>](../resources/intune-enrollment-itunespairingmode.md)|<span data-ttu-id="fefbd-176">Indica el modo de emparejamiento de iTunes.</span><span class="sxs-lookup"><span data-stu-id="fefbd-176">Indicates the iTunes pairing mode.</span></span> <span data-ttu-id="fefbd-177">Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.</span><span class="sxs-lookup"><span data-stu-id="fefbd-177">Possible values are: `disallow`, `allow`, `requiresCertificate`.</span></span>|
|<span data-ttu-id="fefbd-178">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-178">profileRemovalDisabled</span></span>|<span data-ttu-id="fefbd-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-179">Boolean</span></span>|<span data-ttu-id="fefbd-180">Indica si está deshabilitada la opción de eliminación de perfiles</span><span class="sxs-lookup"><span data-stu-id="fefbd-180">Indicates if the profile removal option is disabled</span></span>|
|<span data-ttu-id="fefbd-181">managementCertificates</span><span class="sxs-lookup"><span data-stu-id="fefbd-181">managementCertificates</span></span>|<span data-ttu-id="fefbd-182">colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)</span><span class="sxs-lookup"><span data-stu-id="fefbd-182">[managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md) collection</span></span>|<span data-ttu-id="fefbd-183">Certificados de administración para Configurador de Apple</span><span class="sxs-lookup"><span data-stu-id="fefbd-183">Management certificates for Apple Configurator</span></span>|
|<span data-ttu-id="fefbd-184">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="fefbd-184">restoreBlocked</span></span>|<span data-ttu-id="fefbd-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-185">Boolean</span></span>|<span data-ttu-id="fefbd-186">Indica si se bloquea el panel de restauración del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-186">Indicates if Restore setup pane is blocked</span></span>|
|<span data-ttu-id="fefbd-187">restoreFromAndroidDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-187">restoreFromAndroidDisabled</span></span>|<span data-ttu-id="fefbd-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-188">Boolean</span></span>|<span data-ttu-id="fefbd-189">Indica si está deshabilitado restaurar a partir de Android</span><span class="sxs-lookup"><span data-stu-id="fefbd-189">Indicates if Restore from Android is disabled</span></span>|
|<span data-ttu-id="fefbd-190">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-190">appleIdDisabled</span></span>|<span data-ttu-id="fefbd-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-191">Boolean</span></span>|<span data-ttu-id="fefbd-192">Indica si se deshabilita el panel de Apple identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-192">Indicates if Apple id setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-193">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-193">termsAndConditionsDisabled</span></span>|<span data-ttu-id="fefbd-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-194">Boolean</span></span>|<span data-ttu-id="fefbd-195">Indica si el panel del programa de instalación 'Términos y condiciones' está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="fefbd-195">Indicates if 'Terms and Conditions' setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-196">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-196">touchIdDisabled</span></span>|<span data-ttu-id="fefbd-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-197">Boolean</span></span>|<span data-ttu-id="fefbd-198">Indica si se deshabilita el panel de táctil identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-198">Indicates if touch id setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-199">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-199">applePayDisabled</span></span>|<span data-ttu-id="fefbd-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-200">Boolean</span></span>|<span data-ttu-id="fefbd-201">Indica si se deshabilita el panel de Apple pago del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-201">Indicates if Apple pay setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-202">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-202">zoomDisabled</span></span>|<span data-ttu-id="fefbd-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-203">Boolean</span></span>|<span data-ttu-id="fefbd-204">Indica si se deshabilita el panel de zoom del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-204">Indicates if zoom setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-205">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-205">siriDisabled</span></span>|<span data-ttu-id="fefbd-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-206">Boolean</span></span>|<span data-ttu-id="fefbd-207">Indica si se deshabilita el panel de siri el programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-207">Indicates if siri setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-208">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-208">diagnosticsDisabled</span></span>|<span data-ttu-id="fefbd-209">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-209">Boolean</span></span>|<span data-ttu-id="fefbd-210">Indica si se deshabilita el panel de diagnóstico del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="fefbd-210">Indicates if diagnostics setup pane is disabled</span></span>|
|<span data-ttu-id="fefbd-211">macOSRegistrationDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-211">macOSRegistrationDisabled</span></span>|<span data-ttu-id="fefbd-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-212">Boolean</span></span>|<span data-ttu-id="fefbd-213">Indica si se deshabilita el registro de Mac OS</span><span class="sxs-lookup"><span data-stu-id="fefbd-213">Indicates if Mac OS registration is disabled</span></span>|
|<span data-ttu-id="fefbd-214">macOSFileVaultDisabled</span><span class="sxs-lookup"><span data-stu-id="fefbd-214">macOSFileVaultDisabled</span></span>|<span data-ttu-id="fefbd-215">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-215">Boolean</span></span>|<span data-ttu-id="fefbd-216">Indica si está deshabilitada la cámara de archivo Mac OS</span><span class="sxs-lookup"><span data-stu-id="fefbd-216">Indicates if Mac OS file vault is disabled</span></span>|
|<span data-ttu-id="fefbd-217">awaitDeviceConfiguredConfirmation</span><span class="sxs-lookup"><span data-stu-id="fefbd-217">awaitDeviceConfiguredConfirmation</span></span>|<span data-ttu-id="fefbd-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-218">Boolean</span></span>|<span data-ttu-id="fefbd-219">Indica si el dispositivo será necesario esperar confirmación configurado</span><span class="sxs-lookup"><span data-stu-id="fefbd-219">Indicates if the device will need to wait for configured confirmation</span></span>|
|<span data-ttu-id="fefbd-220">sharedIPadMaximumUserCount</span><span class="sxs-lookup"><span data-stu-id="fefbd-220">sharedIPadMaximumUserCount</span></span>|<span data-ttu-id="fefbd-221">Int32</span><span class="sxs-lookup"><span data-stu-id="fefbd-221">Int32</span></span>|<span data-ttu-id="fefbd-222">Especifica el número máximo de usuarios que pueden usar un iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="fefbd-222">This specifies the maximum number of users that can use a shared iPad.</span></span> <span data-ttu-id="fefbd-223">Solo se aplica en modo compartido iPad.</span><span class="sxs-lookup"><span data-stu-id="fefbd-223">Only applicable in shared iPad mode.</span></span>|
|<span data-ttu-id="fefbd-224">enableSharedIPad</span><span class="sxs-lookup"><span data-stu-id="fefbd-224">enableSharedIPad</span></span>|<span data-ttu-id="fefbd-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="fefbd-225">Boolean</span></span>|<span data-ttu-id="fefbd-226">Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple.</span><span class="sxs-lookup"><span data-stu-id="fefbd-226">This indicates whether the device is to be enrolled in a mode which enables multi user scenarios.</span></span> <span data-ttu-id="fefbd-227">Solo se aplica en iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="fefbd-227">Only applicable in shared iPads.</span></span>|



## <a name="response"></a><span data-ttu-id="fefbd-228">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fefbd-228">Response</span></span>
<span data-ttu-id="fefbd-229">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fefbd-229">If successful, this method returns a `201 Created` response code and a [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fefbd-230">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fefbd-230">Example</span></span>
### <a name="request"></a><span data-ttu-id="fefbd-231">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fefbd-231">Request</span></span>
<span data-ttu-id="fefbd-232">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fefbd-232">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
Content-type: application/json
Content-length: 1290

{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
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
  "iTunesPairingMode": "allow",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreBlocked": true,
  "restoreFromAndroidDisabled": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "macOSRegistrationDisabled": true,
  "macOSFileVaultDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true
}
```

### <a name="response"></a><span data-ttu-id="fefbd-233">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fefbd-233">Response</span></span>
<span data-ttu-id="fefbd-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fefbd-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1339

{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
  "id": "3d4534f7-34f7-3d45-f734-453df734453d",
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
  "iTunesPairingMode": "allow",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreBlocked": true,
  "restoreFromAndroidDisabled": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true,
  "macOSRegistrationDisabled": true,
  "macOSFileVaultDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true
}
```





