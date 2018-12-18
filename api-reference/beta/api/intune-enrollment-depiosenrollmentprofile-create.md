---
title: Crear depIOSEnrollmentProfile
description: Crear un nuevo objeto depIOSEnrollmentProfile.
author: tfitzmac
ms.openlocfilehash: f06457571a2630c32842a202d45107f768d345f2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308578"
---
# <a name="create-depiosenrollmentprofile"></a><span data-ttu-id="52a44-103">Crear depIOSEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="52a44-103">Create depIOSEnrollmentProfile</span></span>

> <span data-ttu-id="52a44-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52a44-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52a44-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52a44-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="52a44-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52a44-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52a44-107">Crear un nuevo objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="52a44-107">Create a new [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="52a44-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52a44-108">Prerequisites</span></span>
<span data-ttu-id="52a44-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="52a44-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="52a44-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52a44-111">Permission type</span></span>|<span data-ttu-id="52a44-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52a44-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="52a44-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52a44-113">Delegated (work or school account)</span></span>|<span data-ttu-id="52a44-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="52a44-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="52a44-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52a44-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="52a44-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52a44-116">Not supported.</span></span>|
|<span data-ttu-id="52a44-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52a44-117">Application</span></span>|<span data-ttu-id="52a44-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52a44-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="52a44-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52a44-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
```

## <a name="request-headers"></a><span data-ttu-id="52a44-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52a44-120">Request headers</span></span>
|<span data-ttu-id="52a44-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52a44-121">Header</span></span>|<span data-ttu-id="52a44-122">Valor</span><span class="sxs-lookup"><span data-stu-id="52a44-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="52a44-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="52a44-123">Authorization</span></span>|<span data-ttu-id="52a44-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="52a44-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="52a44-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="52a44-125">Accept</span></span>|<span data-ttu-id="52a44-126">application/json</span><span class="sxs-lookup"><span data-stu-id="52a44-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="52a44-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52a44-127">Request body</span></span>
<span data-ttu-id="52a44-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto depIOSEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="52a44-128">In the request body, supply a JSON representation for the depIOSEnrollmentProfile object.</span></span>

<span data-ttu-id="52a44-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el depIOSEnrollmentProfile.</span><span class="sxs-lookup"><span data-stu-id="52a44-129">The following table shows the properties that are required when you create the depIOSEnrollmentProfile.</span></span>

|<span data-ttu-id="52a44-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52a44-130">Property</span></span>|<span data-ttu-id="52a44-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="52a44-131">Type</span></span>|<span data-ttu-id="52a44-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="52a44-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="52a44-133">id</span><span class="sxs-lookup"><span data-stu-id="52a44-133">id</span></span>|<span data-ttu-id="52a44-134">String</span><span class="sxs-lookup"><span data-stu-id="52a44-134">String</span></span>|<span data-ttu-id="52a44-135">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-135">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-136">displayName</span><span class="sxs-lookup"><span data-stu-id="52a44-136">displayName</span></span>|<span data-ttu-id="52a44-137">String</span><span class="sxs-lookup"><span data-stu-id="52a44-137">String</span></span>|<span data-ttu-id="52a44-138">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-138">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-139">descripción</span><span class="sxs-lookup"><span data-stu-id="52a44-139">description</span></span>|<span data-ttu-id="52a44-140">String</span><span class="sxs-lookup"><span data-stu-id="52a44-140">String</span></span>|<span data-ttu-id="52a44-141">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-141">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="52a44-142">requiresUserAuthentication</span></span>|<span data-ttu-id="52a44-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-143">Boolean</span></span>|<span data-ttu-id="52a44-144">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-144">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="52a44-145">configurationEndpointUrl</span></span>|<span data-ttu-id="52a44-146">String</span><span class="sxs-lookup"><span data-stu-id="52a44-146">String</span></span>|<span data-ttu-id="52a44-147">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-147">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="52a44-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="52a44-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-149">Boolean</span></span>|<span data-ttu-id="52a44-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="52a44-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="52a44-151">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-151">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="52a44-152">isDefault</span><span class="sxs-lookup"><span data-stu-id="52a44-152">isDefault</span></span>|<span data-ttu-id="52a44-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-153">Boolean</span></span>|<span data-ttu-id="52a44-154">Indica si este es el perfil predeterminado heredado de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-154">Indicates if this is the default profile Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-155">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="52a44-155">supervisedModeEnabled</span></span>|<span data-ttu-id="52a44-156">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-156">Boolean</span></span>|<span data-ttu-id="52a44-157">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="52a44-157">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="52a44-158">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="52a44-158">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span> <span data-ttu-id="52a44-159">Se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-159">Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-160">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="52a44-160">supportDepartment</span></span>|<span data-ttu-id="52a44-161">String</span><span class="sxs-lookup"><span data-stu-id="52a44-161">String</span></span>|<span data-ttu-id="52a44-162">Información de departamento de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-162">Support department information Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-163">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-163">passCodeDisabled</span></span>|<span data-ttu-id="52a44-164">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-164">Boolean</span></span>|<span data-ttu-id="52a44-165">Indica si el código de acceso del programa de instalación panel está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-165">Indicates if Passcode setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-166">isMandatory</span><span class="sxs-lookup"><span data-stu-id="52a44-166">isMandatory</span></span>|<span data-ttu-id="52a44-167">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-167">Boolean</span></span>|<span data-ttu-id="52a44-168">Indica si el perfil es obligatorio heredada de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-168">Indicates if the profile is mandatory Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-169">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-169">locationDisabled</span></span>|<span data-ttu-id="52a44-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-170">Boolean</span></span>|<span data-ttu-id="52a44-171">Indica si la ubicación de panel de servicio del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-171">Indicates if Location service setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-172">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="52a44-172">supportPhoneNumber</span></span>|<span data-ttu-id="52a44-173">String</span><span class="sxs-lookup"><span data-stu-id="52a44-173">String</span></span>|<span data-ttu-id="52a44-174">Número de teléfono de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-174">Support phone number Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-175">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-175">profileRemovalDisabled</span></span>|<span data-ttu-id="52a44-176">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-176">Boolean</span></span>|<span data-ttu-id="52a44-177">Indica si está deshabilitada la opción de eliminación de perfiles se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-177">Indicates if the profile removal option is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-178">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="52a44-178">restoreBlocked</span></span>|<span data-ttu-id="52a44-179">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-179">Boolean</span></span>|<span data-ttu-id="52a44-180">Indica si se bloquea el panel del programa de instalación de restauración se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-180">Indicates if Restore setup pane is blocked Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-181">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-181">appleIdDisabled</span></span>|<span data-ttu-id="52a44-182">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-182">Boolean</span></span>|<span data-ttu-id="52a44-183">Indica si Apple panel de identificador del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-183">Indicates if Apple id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-184">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-184">termsAndConditionsDisabled</span></span>|<span data-ttu-id="52a44-185">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-185">Boolean</span></span>|<span data-ttu-id="52a44-186">Indica si se deshabilita el panel del programa de instalación 'Términos y condiciones' se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-186">Indicates if 'Terms and Conditions' setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-187">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-187">touchIdDisabled</span></span>|<span data-ttu-id="52a44-188">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-188">Boolean</span></span>|<span data-ttu-id="52a44-189">Indica si se deshabilita el panel de táctil identificador del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-189">Indicates if touch id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-190">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-190">applePayDisabled</span></span>|<span data-ttu-id="52a44-191">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-191">Boolean</span></span>|<span data-ttu-id="52a44-192">Indica si se deshabilita el panel de Apple pago del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-192">Indicates if Apple pay setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-193">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-193">zoomDisabled</span></span>|<span data-ttu-id="52a44-194">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-194">Boolean</span></span>|<span data-ttu-id="52a44-195">Indica si se deshabilita el panel de zoom del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-195">Indicates if zoom setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-196">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-196">siriDisabled</span></span>|<span data-ttu-id="52a44-197">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-197">Boolean</span></span>|<span data-ttu-id="52a44-198">Indica si se deshabilita el panel de siri el programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-198">Indicates if siri setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-199">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-199">diagnosticsDisabled</span></span>|<span data-ttu-id="52a44-200">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-200">Boolean</span></span>|<span data-ttu-id="52a44-201">Indica si el diagnóstico panel del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-201">Indicates if diagnostics setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="52a44-202">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="52a44-202">iTunesPairingMode</span></span>|[<span data-ttu-id="52a44-203">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="52a44-203">iTunesPairingMode</span></span>](../resources/intune-enrollment-itunespairingmode.md)|<span data-ttu-id="52a44-204">Indica el modo de emparejamiento de iTunes.</span><span class="sxs-lookup"><span data-stu-id="52a44-204">Indicates the iTunes pairing mode.</span></span> <span data-ttu-id="52a44-205">Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.</span><span class="sxs-lookup"><span data-stu-id="52a44-205">Possible values are: `disallow`, `allow`, `requiresCertificate`.</span></span>|
|<span data-ttu-id="52a44-206">managementCertificates</span><span class="sxs-lookup"><span data-stu-id="52a44-206">managementCertificates</span></span>|<span data-ttu-id="52a44-207">colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)</span><span class="sxs-lookup"><span data-stu-id="52a44-207">[managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md) collection</span></span>|<span data-ttu-id="52a44-208">Certificados de administración para Configurador de Apple</span><span class="sxs-lookup"><span data-stu-id="52a44-208">Management certificates for Apple Configurator</span></span>|
|<span data-ttu-id="52a44-209">restoreFromAndroidDisabled</span><span class="sxs-lookup"><span data-stu-id="52a44-209">restoreFromAndroidDisabled</span></span>|<span data-ttu-id="52a44-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-210">Boolean</span></span>|<span data-ttu-id="52a44-211">Indica si está deshabilitado restaurar a partir de Android</span><span class="sxs-lookup"><span data-stu-id="52a44-211">Indicates if Restore from Android is disabled</span></span>|
|<span data-ttu-id="52a44-212">awaitDeviceConfiguredConfirmation</span><span class="sxs-lookup"><span data-stu-id="52a44-212">awaitDeviceConfiguredConfirmation</span></span>|<span data-ttu-id="52a44-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-213">Boolean</span></span>|<span data-ttu-id="52a44-214">Indica si el dispositivo será necesario esperar confirmación configurado</span><span class="sxs-lookup"><span data-stu-id="52a44-214">Indicates if the device will need to wait for configured confirmation</span></span>|
|<span data-ttu-id="52a44-215">sharedIPadMaximumUserCount</span><span class="sxs-lookup"><span data-stu-id="52a44-215">sharedIPadMaximumUserCount</span></span>|<span data-ttu-id="52a44-216">Int32</span><span class="sxs-lookup"><span data-stu-id="52a44-216">Int32</span></span>|<span data-ttu-id="52a44-217">Especifica el número máximo de usuarios que pueden usar un iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="52a44-217">This specifies the maximum number of users that can use a shared iPad.</span></span> <span data-ttu-id="52a44-218">Solo se aplica en modo compartido iPad.</span><span class="sxs-lookup"><span data-stu-id="52a44-218">Only applicable in shared iPad mode.</span></span>|
|<span data-ttu-id="52a44-219">enableSharedIPad</span><span class="sxs-lookup"><span data-stu-id="52a44-219">enableSharedIPad</span></span>|<span data-ttu-id="52a44-220">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-220">Boolean</span></span>|<span data-ttu-id="52a44-221">Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple.</span><span class="sxs-lookup"><span data-stu-id="52a44-221">This indicates whether the device is to be enrolled in a mode which enables multi user scenarios.</span></span> <span data-ttu-id="52a44-222">Solo se aplica en iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="52a44-222">Only applicable in shared iPads.</span></span>|
|<span data-ttu-id="52a44-223">companyPortalVppTokenId</span><span class="sxs-lookup"><span data-stu-id="52a44-223">companyPortalVppTokenId</span></span>|<span data-ttu-id="52a44-224">String</span><span class="sxs-lookup"><span data-stu-id="52a44-224">String</span></span>|<span data-ttu-id="52a44-225">Si establece, indica qué token Vpp debe usarse para implementar el Portal de la empresa con licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="52a44-225">If set, indicates which Vpp token should be used to deploy the Company Portal w/ device licensing.</span></span> <span data-ttu-id="52a44-226">'enableAuthenticationViaCompanyPortal' debe establecerse en orden establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="52a44-226">'enableAuthenticationViaCompanyPortal' must be set in order for this property to be set.</span></span>|
|<span data-ttu-id="52a44-227">enableSingleAppEnrollmentMode</span><span class="sxs-lookup"><span data-stu-id="52a44-227">enableSingleAppEnrollmentMode</span></span>|<span data-ttu-id="52a44-228">Boolean</span><span class="sxs-lookup"><span data-stu-id="52a44-228">Boolean</span></span>|<span data-ttu-id="52a44-229">Indica el dispositivo para habilitar el modo de aplicación único y aplicar el bloqueo de la aplicación durante la inscripción.</span><span class="sxs-lookup"><span data-stu-id="52a44-229">Tells the device to enable single app mode and apply app-lock during enrollment.</span></span> <span data-ttu-id="52a44-230">Valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="52a44-230">Default is false.</span></span> <span data-ttu-id="52a44-231">'enableAuthenticationViaCompanyPortal' y 'companyPortalVppTokenId' se deben establecer para que esta propiedad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="52a44-231">'enableAuthenticationViaCompanyPortal' and 'companyPortalVppTokenId' must be set for this property to be set.</span></span>|



## <a name="response"></a><span data-ttu-id="52a44-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52a44-232">Response</span></span>
<span data-ttu-id="52a44-233">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52a44-233">If successful, this method returns a `201 Created` response code and a [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52a44-234">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52a44-234">Example</span></span>
### <a name="request"></a><span data-ttu-id="52a44-235">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52a44-235">Request</span></span>
<span data-ttu-id="52a44-236">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52a44-236">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/enrollmentProfiles
Content-type: application/json
Content-length: 1329

{
  "@odata.type": "#microsoft.graph.depIOSEnrollmentProfile",
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
  "iTunesPairingMode": "allow",
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreFromAndroidDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true,
  "companyPortalVppTokenId": "Company Portal Vpp Token Id value",
  "enableSingleAppEnrollmentMode": true
}
```

### <a name="response"></a><span data-ttu-id="52a44-237">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52a44-237">Response</span></span>
<span data-ttu-id="52a44-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52a44-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1378

{
  "@odata.type": "#microsoft.graph.depIOSEnrollmentProfile",
  "id": "1ec10a60-0a60-1ec1-600a-c11e600ac11e",
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
  "iTunesPairingMode": "allow",
  "managementCertificates": [
    {
      "@odata.type": "microsoft.graph.managementCertificateWithThumbprint",
      "thumbprint": "Thumbprint value",
      "certificate": "Certificate value"
    }
  ],
  "restoreFromAndroidDisabled": true,
  "awaitDeviceConfiguredConfirmation": true,
  "sharedIPadMaximumUserCount": 10,
  "enableSharedIPad": true,
  "companyPortalVppTokenId": "Company Portal Vpp Token Id value",
  "enableSingleAppEnrollmentMode": true
}
```





