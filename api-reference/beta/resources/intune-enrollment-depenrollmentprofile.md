---
title: tipo de recurso depEnrollmentProfile
description: El recurso depEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
ms.openlocfilehash: 5c09bac440d2dce8cb141787d0809c74aed747c0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090554"
---
# <a name="depenrollmentprofile-resource-type"></a><span data-ttu-id="390e1-104">tipo de recurso depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-104">depEnrollmentProfile resource type</span></span>

> <span data-ttu-id="390e1-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="390e1-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="390e1-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="390e1-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="390e1-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="390e1-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="390e1-108">El recurso depEnrollmentProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP).</span><span class="sxs-lookup"><span data-stu-id="390e1-108">The depEnrollmentProfile resource represents an Apple Device Enrollment Program (DEP) enrollment profile.</span></span> <span data-ttu-id="390e1-109">Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.</span><span class="sxs-lookup"><span data-stu-id="390e1-109">This type of profile must be assigned to Apple DEP serial numbers before the corresponding devices can enroll via DEP.</span></span>

<span data-ttu-id="390e1-110">Hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-110">Inherits from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>

## <a name="methods"></a><span data-ttu-id="390e1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="390e1-111">Methods</span></span>
|<span data-ttu-id="390e1-112">Método</span><span class="sxs-lookup"><span data-stu-id="390e1-112">Method</span></span>|<span data-ttu-id="390e1-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="390e1-113">Return Type</span></span>|<span data-ttu-id="390e1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="390e1-114">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="390e1-115">Lista depEnrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="390e1-115">List depEnrollmentProfiles</span></span>](../api/intune-enrollment-depenrollmentprofile-list.md)|<span data-ttu-id="390e1-116">colección de [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-116">[depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) collection</span></span>|<span data-ttu-id="390e1-117">Propiedades de la lista y relaciones de los objetos [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="390e1-117">List properties and relationships of the [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) objects.</span></span>|
|[<span data-ttu-id="390e1-118">Obtener depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-118">Get depEnrollmentProfile</span></span>](../api/intune-enrollment-depenrollmentprofile-get.md)|[<span data-ttu-id="390e1-119">depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-119">depEnrollmentProfile</span></span>](../resources/intune-enrollment-depenrollmentprofile.md)|<span data-ttu-id="390e1-120">Leer las propiedades y las relaciones del objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="390e1-120">Read properties and relationships of the [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="390e1-121">Crear depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-121">Create depEnrollmentProfile</span></span>](../api/intune-enrollment-depenrollmentprofile-create.md)|[<span data-ttu-id="390e1-122">depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-122">depEnrollmentProfile</span></span>](../resources/intune-enrollment-depenrollmentprofile.md)|<span data-ttu-id="390e1-123">Crear un nuevo objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="390e1-123">Create a new [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="390e1-124">Eliminar depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-124">Delete depEnrollmentProfile</span></span>](../api/intune-enrollment-depenrollmentprofile-delete.md)|<span data-ttu-id="390e1-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="390e1-125">None</span></span>|<span data-ttu-id="390e1-126">Elimina un [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="390e1-126">Deletes a [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md).</span></span>|
|[<span data-ttu-id="390e1-127">Actualizar depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-127">Update depEnrollmentProfile</span></span>](../api/intune-enrollment-depenrollmentprofile-update.md)|[<span data-ttu-id="390e1-128">depEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="390e1-128">depEnrollmentProfile</span></span>](../resources/intune-enrollment-depenrollmentprofile.md)|<span data-ttu-id="390e1-129">Actualizar las propiedades de un objeto [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="390e1-129">Update the properties of a [depEnrollmentProfile](../resources/intune-enrollment-depenrollmentprofile.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="390e1-130">Propiedades</span><span class="sxs-lookup"><span data-stu-id="390e1-130">Properties</span></span>
|<span data-ttu-id="390e1-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="390e1-131">Property</span></span>|<span data-ttu-id="390e1-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="390e1-132">Type</span></span>|<span data-ttu-id="390e1-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="390e1-133">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="390e1-134">id</span><span class="sxs-lookup"><span data-stu-id="390e1-134">id</span></span>|<span data-ttu-id="390e1-135">String</span><span class="sxs-lookup"><span data-stu-id="390e1-135">String</span></span>|<span data-ttu-id="390e1-136">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-136">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-137">displayName</span><span class="sxs-lookup"><span data-stu-id="390e1-137">displayName</span></span>|<span data-ttu-id="390e1-138">String</span><span class="sxs-lookup"><span data-stu-id="390e1-138">String</span></span>|<span data-ttu-id="390e1-139">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-139">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-140">descripción</span><span class="sxs-lookup"><span data-stu-id="390e1-140">description</span></span>|<span data-ttu-id="390e1-141">String</span><span class="sxs-lookup"><span data-stu-id="390e1-141">String</span></span>|<span data-ttu-id="390e1-142">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-142">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-143">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="390e1-143">requiresUserAuthentication</span></span>|<span data-ttu-id="390e1-144">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-144">Boolean</span></span>|<span data-ttu-id="390e1-145">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-145">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-146">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="390e1-146">configurationEndpointUrl</span></span>|<span data-ttu-id="390e1-147">String</span><span class="sxs-lookup"><span data-stu-id="390e1-147">String</span></span>|<span data-ttu-id="390e1-148">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-148">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-149">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="390e1-149">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="390e1-150">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-150">Boolean</span></span>|<span data-ttu-id="390e1-151">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="390e1-151">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="390e1-152">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-152">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="390e1-153">isDefault</span><span class="sxs-lookup"><span data-stu-id="390e1-153">isDefault</span></span>|<span data-ttu-id="390e1-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-154">Boolean</span></span>|<span data-ttu-id="390e1-155">Indica si este es el perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="390e1-155">Indicates if this is the default profile</span></span>|
|<span data-ttu-id="390e1-156">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="390e1-156">supervisedModeEnabled</span></span>|<span data-ttu-id="390e1-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-157">Boolean</span></span>|<span data-ttu-id="390e1-158">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="390e1-158">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="390e1-159">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="390e1-159">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span>|
|<span data-ttu-id="390e1-160">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="390e1-160">supportDepartment</span></span>|<span data-ttu-id="390e1-161">String</span><span class="sxs-lookup"><span data-stu-id="390e1-161">String</span></span>|<span data-ttu-id="390e1-162">Información del departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="390e1-162">Support department information</span></span>|
|<span data-ttu-id="390e1-163">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-163">passCodeDisabled</span></span>|<span data-ttu-id="390e1-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-164">Boolean</span></span>|<span data-ttu-id="390e1-165">Indica si se deshabilita el panel de código de acceso del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-165">Indicates if Passcode setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-166">isMandatory</span><span class="sxs-lookup"><span data-stu-id="390e1-166">isMandatory</span></span>|<span data-ttu-id="390e1-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-167">Boolean</span></span>|<span data-ttu-id="390e1-168">Indica si el perfil es obligatorio</span><span class="sxs-lookup"><span data-stu-id="390e1-168">Indicates if the profile is mandatory</span></span>|
|<span data-ttu-id="390e1-169">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-169">locationDisabled</span></span>|<span data-ttu-id="390e1-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-170">Boolean</span></span>|<span data-ttu-id="390e1-171">Indica si se deshabilita el panel del programa de instalación del servicio de ubicación</span><span class="sxs-lookup"><span data-stu-id="390e1-171">Indicates if Location service setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-172">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="390e1-172">supportPhoneNumber</span></span>|<span data-ttu-id="390e1-173">String</span><span class="sxs-lookup"><span data-stu-id="390e1-173">String</span></span>|<span data-ttu-id="390e1-174">Número de teléfono de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="390e1-174">Support phone number</span></span>|
|<span data-ttu-id="390e1-175">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="390e1-175">iTunesPairingMode</span></span>|[<span data-ttu-id="390e1-176">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="390e1-176">iTunesPairingMode</span></span>](../resources/intune-enrollment-itunespairingmode.md)|<span data-ttu-id="390e1-177">Indica el modo de emparejamiento de iTunes.</span><span class="sxs-lookup"><span data-stu-id="390e1-177">Indicates the iTunes pairing mode.</span></span> <span data-ttu-id="390e1-178">Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.</span><span class="sxs-lookup"><span data-stu-id="390e1-178">Possible values are: `disallow`, `allow`, `requiresCertificate`.</span></span>|
|<span data-ttu-id="390e1-179">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-179">profileRemovalDisabled</span></span>|<span data-ttu-id="390e1-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-180">Boolean</span></span>|<span data-ttu-id="390e1-181">Indica si está deshabilitada la opción de eliminación de perfiles</span><span class="sxs-lookup"><span data-stu-id="390e1-181">Indicates if the profile removal option is disabled</span></span>|
|<span data-ttu-id="390e1-182">managementCertificates</span><span class="sxs-lookup"><span data-stu-id="390e1-182">managementCertificates</span></span>|<span data-ttu-id="390e1-183">colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)</span><span class="sxs-lookup"><span data-stu-id="390e1-183">[managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md) collection</span></span>|<span data-ttu-id="390e1-184">Certificados de administración para Configurador de Apple</span><span class="sxs-lookup"><span data-stu-id="390e1-184">Management certificates for Apple Configurator</span></span>|
|<span data-ttu-id="390e1-185">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="390e1-185">restoreBlocked</span></span>|<span data-ttu-id="390e1-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-186">Boolean</span></span>|<span data-ttu-id="390e1-187">Indica si se bloquea el panel de restauración del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-187">Indicates if Restore setup pane is blocked</span></span>|
|<span data-ttu-id="390e1-188">restoreFromAndroidDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-188">restoreFromAndroidDisabled</span></span>|<span data-ttu-id="390e1-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-189">Boolean</span></span>|<span data-ttu-id="390e1-190">Indica si está deshabilitado restaurar a partir de Android</span><span class="sxs-lookup"><span data-stu-id="390e1-190">Indicates if Restore from Android is disabled</span></span>|
|<span data-ttu-id="390e1-191">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-191">appleIdDisabled</span></span>|<span data-ttu-id="390e1-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-192">Boolean</span></span>|<span data-ttu-id="390e1-193">Indica si se deshabilita el panel de Apple identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-193">Indicates if Apple id setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-194">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-194">termsAndConditionsDisabled</span></span>|<span data-ttu-id="390e1-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-195">Boolean</span></span>|<span data-ttu-id="390e1-196">Indica si el panel del programa de instalación 'Términos y condiciones' está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="390e1-196">Indicates if 'Terms and Conditions' setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-197">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-197">touchIdDisabled</span></span>|<span data-ttu-id="390e1-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-198">Boolean</span></span>|<span data-ttu-id="390e1-199">Indica si se deshabilita el panel de táctil identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-199">Indicates if touch id setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-200">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-200">applePayDisabled</span></span>|<span data-ttu-id="390e1-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-201">Boolean</span></span>|<span data-ttu-id="390e1-202">Indica si se deshabilita el panel de Apple pago del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-202">Indicates if Apple pay setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-203">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-203">zoomDisabled</span></span>|<span data-ttu-id="390e1-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-204">Boolean</span></span>|<span data-ttu-id="390e1-205">Indica si se deshabilita el panel de zoom del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-205">Indicates if zoom setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-206">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-206">siriDisabled</span></span>|<span data-ttu-id="390e1-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-207">Boolean</span></span>|<span data-ttu-id="390e1-208">Indica si se deshabilita el panel de siri el programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-208">Indicates if siri setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-209">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-209">diagnosticsDisabled</span></span>|<span data-ttu-id="390e1-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-210">Boolean</span></span>|<span data-ttu-id="390e1-211">Indica si se deshabilita el panel de diagnóstico del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="390e1-211">Indicates if diagnostics setup pane is disabled</span></span>|
|<span data-ttu-id="390e1-212">macOSRegistrationDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-212">macOSRegistrationDisabled</span></span>|<span data-ttu-id="390e1-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-213">Boolean</span></span>|<span data-ttu-id="390e1-214">Indica si se deshabilita el registro de Mac OS</span><span class="sxs-lookup"><span data-stu-id="390e1-214">Indicates if Mac OS registration is disabled</span></span>|
|<span data-ttu-id="390e1-215">macOSFileVaultDisabled</span><span class="sxs-lookup"><span data-stu-id="390e1-215">macOSFileVaultDisabled</span></span>|<span data-ttu-id="390e1-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-216">Boolean</span></span>|<span data-ttu-id="390e1-217">Indica si está deshabilitada la cámara de archivo Mac OS</span><span class="sxs-lookup"><span data-stu-id="390e1-217">Indicates if Mac OS file vault is disabled</span></span>|
|<span data-ttu-id="390e1-218">awaitDeviceConfiguredConfirmation</span><span class="sxs-lookup"><span data-stu-id="390e1-218">awaitDeviceConfiguredConfirmation</span></span>|<span data-ttu-id="390e1-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-219">Boolean</span></span>|<span data-ttu-id="390e1-220">Indica si el dispositivo será necesario esperar confirmación configurado</span><span class="sxs-lookup"><span data-stu-id="390e1-220">Indicates if the device will need to wait for configured confirmation</span></span>|
|<span data-ttu-id="390e1-221">sharedIPadMaximumUserCount</span><span class="sxs-lookup"><span data-stu-id="390e1-221">sharedIPadMaximumUserCount</span></span>|<span data-ttu-id="390e1-222">Int32</span><span class="sxs-lookup"><span data-stu-id="390e1-222">Int32</span></span>|<span data-ttu-id="390e1-223">Especifica el número máximo de usuarios que pueden usar un iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="390e1-223">This specifies the maximum number of users that can use a shared iPad.</span></span> <span data-ttu-id="390e1-224">Solo se aplica en modo compartido iPad.</span><span class="sxs-lookup"><span data-stu-id="390e1-224">Only applicable in shared iPad mode.</span></span>|
|<span data-ttu-id="390e1-225">enableSharedIPad</span><span class="sxs-lookup"><span data-stu-id="390e1-225">enableSharedIPad</span></span>|<span data-ttu-id="390e1-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="390e1-226">Boolean</span></span>|<span data-ttu-id="390e1-227">Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple.</span><span class="sxs-lookup"><span data-stu-id="390e1-227">This indicates whether the device is to be enrolled in a mode which enables multi user scenarios.</span></span> <span data-ttu-id="390e1-228">Solo se aplica en iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="390e1-228">Only applicable in shared iPads.</span></span>|

## <a name="relationships"></a><span data-ttu-id="390e1-229">Relaciones</span><span class="sxs-lookup"><span data-stu-id="390e1-229">Relationships</span></span>
<span data-ttu-id="390e1-230">Ninguna</span><span class="sxs-lookup"><span data-stu-id="390e1-230">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="390e1-231">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="390e1-231">JSON Representation</span></span>
<span data-ttu-id="390e1-232">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="390e1-232">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depEnrollmentProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "String",
  "enableAuthenticationViaCompanyPortal": true,
  "isDefault": true,
  "supervisedModeEnabled": true,
  "supportDepartment": "String",
  "passCodeDisabled": true,
  "isMandatory": true,
  "locationDisabled": true,
  "supportPhoneNumber": "String",
  "iTunesPairingMode": "String",
  "profileRemovalDisabled": true,
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "String",
      "certificate": "String"
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
  "sharedIPadMaximumUserCount": 1024,
  "enableSharedIPad": true
}
```




