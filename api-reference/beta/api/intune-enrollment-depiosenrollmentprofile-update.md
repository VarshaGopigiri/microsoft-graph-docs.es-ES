---
title: Actualizar depIOSEnrollmentProfile
description: Actualizar las propiedades de un objeto depIOSEnrollmentProfile.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cfbae59533112d69d4616f77d2dbeb79a6361332
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935965"
---
# <a name="update-depiosenrollmentprofile"></a><span data-ttu-id="5cbc7-103">Actualizar depIOSEnrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="5cbc7-103">Update depIOSEnrollmentProfile</span></span>

> <span data-ttu-id="5cbc7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5cbc7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5cbc7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5cbc7-107">Actualizar las propiedades de un objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbc7-107">Update the properties of a [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5cbc7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5cbc7-108">Prerequisites</span></span>
<span data-ttu-id="5cbc7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5cbc7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5cbc7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5cbc7-111">Permission type</span></span>|<span data-ttu-id="5cbc7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5cbc7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5cbc7-114">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5cbc7-114">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="5cbc7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5cbc7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-116">Not supported.</span></span>|
|<span data-ttu-id="5cbc7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5cbc7-117">Application</span></span>|<span data-ttu-id="5cbc7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5cbc7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5cbc7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/defaultIosEnrollmentProfile
```

## <a name="request-headers"></a><span data-ttu-id="5cbc7-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5cbc7-120">Request headers</span></span>
|<span data-ttu-id="5cbc7-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cbc7-121">Header</span></span>|<span data-ttu-id="5cbc7-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5cbc7-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5cbc7-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="5cbc7-123">Authorization</span></span>|<span data-ttu-id="5cbc7-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5cbc7-125">Accept</span><span class="sxs-lookup"><span data-stu-id="5cbc7-125">Accept</span></span>|<span data-ttu-id="5cbc7-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5cbc7-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5cbc7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5cbc7-127">Request body</span></span>
<span data-ttu-id="5cbc7-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5cbc7-128">In the request body, supply a JSON representation for the [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) object.</span></span>

<span data-ttu-id="5cbc7-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="5cbc7-129">The following table shows the properties that are required when you create the [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md).</span></span>

|<span data-ttu-id="5cbc7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5cbc7-130">Property</span></span>|<span data-ttu-id="5cbc7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cbc7-131">Type</span></span>|<span data-ttu-id="5cbc7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5cbc7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5cbc7-133">id</span><span class="sxs-lookup"><span data-stu-id="5cbc7-133">id</span></span>|<span data-ttu-id="5cbc7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-134">String</span></span>|<span data-ttu-id="5cbc7-135">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-135">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-136">displayName</span><span class="sxs-lookup"><span data-stu-id="5cbc7-136">displayName</span></span>|<span data-ttu-id="5cbc7-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-137">String</span></span>|<span data-ttu-id="5cbc7-138">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-138">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-139">descripción</span><span class="sxs-lookup"><span data-stu-id="5cbc7-139">description</span></span>|<span data-ttu-id="5cbc7-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-140">String</span></span>|<span data-ttu-id="5cbc7-141">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-141">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-142">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="5cbc7-142">requiresUserAuthentication</span></span>|<span data-ttu-id="5cbc7-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-143">Boolean</span></span>|<span data-ttu-id="5cbc7-144">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-144">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-145">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="5cbc7-145">configurationEndpointUrl</span></span>|<span data-ttu-id="5cbc7-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-146">String</span></span>|<span data-ttu-id="5cbc7-147">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-147">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-148">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="5cbc7-148">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="5cbc7-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-149">Boolean</span></span>|<span data-ttu-id="5cbc7-150">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-150">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="5cbc7-151">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-151">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-152">isDefault</span><span class="sxs-lookup"><span data-stu-id="5cbc7-152">isDefault</span></span>|<span data-ttu-id="5cbc7-153">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-153">Boolean</span></span>|<span data-ttu-id="5cbc7-154">Indica si este es el perfil predeterminado heredado de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-154">Indicates if this is the default profile Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-155">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-155">supervisedModeEnabled</span></span>|<span data-ttu-id="5cbc7-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-156">Boolean</span></span>|<span data-ttu-id="5cbc7-157">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-157">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="5cbc7-158">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-158">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span> <span data-ttu-id="5cbc7-159">Se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-159">Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-160">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="5cbc7-160">supportDepartment</span></span>|<span data-ttu-id="5cbc7-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-161">String</span></span>|<span data-ttu-id="5cbc7-162">Información de departamento de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-162">Support department information Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-163">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-163">passCodeDisabled</span></span>|<span data-ttu-id="5cbc7-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-164">Boolean</span></span>|<span data-ttu-id="5cbc7-165">Indica si el código de acceso del programa de instalación panel está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-165">Indicates if Passcode setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-166">isMandatory</span><span class="sxs-lookup"><span data-stu-id="5cbc7-166">isMandatory</span></span>|<span data-ttu-id="5cbc7-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-167">Boolean</span></span>|<span data-ttu-id="5cbc7-168">Indica si el perfil es obligatorio heredada de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-168">Indicates if the profile is mandatory Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-169">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-169">locationDisabled</span></span>|<span data-ttu-id="5cbc7-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-170">Boolean</span></span>|<span data-ttu-id="5cbc7-171">Indica si la ubicación de panel de servicio del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-171">Indicates if Location service setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-172">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5cbc7-172">supportPhoneNumber</span></span>|<span data-ttu-id="5cbc7-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-173">String</span></span>|<span data-ttu-id="5cbc7-174">Número de teléfono de soporte técnico Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-174">Support phone number Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-175">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-175">profileRemovalDisabled</span></span>|<span data-ttu-id="5cbc7-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-176">Boolean</span></span>|<span data-ttu-id="5cbc7-177">Indica si está deshabilitada la opción de eliminación de perfiles se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-177">Indicates if the profile removal option is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-178">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="5cbc7-178">restoreBlocked</span></span>|<span data-ttu-id="5cbc7-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-179">Boolean</span></span>|<span data-ttu-id="5cbc7-180">Indica si se bloquea el panel del programa de instalación de restauración se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-180">Indicates if Restore setup pane is blocked Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-181">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-181">appleIdDisabled</span></span>|<span data-ttu-id="5cbc7-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-182">Boolean</span></span>|<span data-ttu-id="5cbc7-183">Indica si Apple panel de identificador del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-183">Indicates if Apple id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-184">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-184">termsAndConditionsDisabled</span></span>|<span data-ttu-id="5cbc7-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-185">Boolean</span></span>|<span data-ttu-id="5cbc7-186">Indica si se deshabilita el panel del programa de instalación 'Términos y condiciones' se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-186">Indicates if 'Terms and Conditions' setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-187">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-187">touchIdDisabled</span></span>|<span data-ttu-id="5cbc7-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-188">Boolean</span></span>|<span data-ttu-id="5cbc7-189">Indica si se deshabilita el panel de táctil identificador del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-189">Indicates if touch id setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-190">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-190">applePayDisabled</span></span>|<span data-ttu-id="5cbc7-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-191">Boolean</span></span>|<span data-ttu-id="5cbc7-192">Indica si se deshabilita el panel de Apple pago del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-192">Indicates if Apple pay setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-193">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-193">zoomDisabled</span></span>|<span data-ttu-id="5cbc7-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-194">Boolean</span></span>|<span data-ttu-id="5cbc7-195">Indica si se deshabilita el panel de zoom del programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-195">Indicates if zoom setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-196">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-196">siriDisabled</span></span>|<span data-ttu-id="5cbc7-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-197">Boolean</span></span>|<span data-ttu-id="5cbc7-198">Indica si se deshabilita el panel de siri el programa de instalación se hereda de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-198">Indicates if siri setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-199">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-199">diagnosticsDisabled</span></span>|<span data-ttu-id="5cbc7-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-200">Boolean</span></span>|<span data-ttu-id="5cbc7-201">Indica si el diagnóstico panel del programa de instalación está deshabilitado Inherited desde [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-201">Indicates if diagnostics setup pane is disabled Inherited from [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span></span>|
|<span data-ttu-id="5cbc7-202">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="5cbc7-202">iTunesPairingMode</span></span>|[<span data-ttu-id="5cbc7-203">iTunesPairingMode</span><span class="sxs-lookup"><span data-stu-id="5cbc7-203">iTunesPairingMode</span></span>](../resources/intune-enrollment-itunespairingmode.md)|<span data-ttu-id="5cbc7-204">Indica el modo de emparejamiento de iTunes.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-204">Indicates the iTunes pairing mode.</span></span> <span data-ttu-id="5cbc7-205">Los valores posibles son: `disallow`, `allow` y `requiresCertificate`.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-205">Possible values are: `disallow`, `allow`, `requiresCertificate`.</span></span>|
|<span data-ttu-id="5cbc7-206">managementCertificates</span><span class="sxs-lookup"><span data-stu-id="5cbc7-206">managementCertificates</span></span>|<span data-ttu-id="5cbc7-207">colección de [managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md)</span><span class="sxs-lookup"><span data-stu-id="5cbc7-207">[managementCertificateWithThumbprint](../resources/intune-enrollment-managementcertificatewiththumbprint.md) collection</span></span>|<span data-ttu-id="5cbc7-208">Certificados de administración para Configurador de Apple</span><span class="sxs-lookup"><span data-stu-id="5cbc7-208">Management certificates for Apple Configurator</span></span>|
|<span data-ttu-id="5cbc7-209">restoreFromAndroidDisabled</span><span class="sxs-lookup"><span data-stu-id="5cbc7-209">restoreFromAndroidDisabled</span></span>|<span data-ttu-id="5cbc7-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-210">Boolean</span></span>|<span data-ttu-id="5cbc7-211">Indica si está deshabilitado restaurar a partir de Android</span><span class="sxs-lookup"><span data-stu-id="5cbc7-211">Indicates if Restore from Android is disabled</span></span>|
|<span data-ttu-id="5cbc7-212">awaitDeviceConfiguredConfirmation</span><span class="sxs-lookup"><span data-stu-id="5cbc7-212">awaitDeviceConfiguredConfirmation</span></span>|<span data-ttu-id="5cbc7-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-213">Boolean</span></span>|<span data-ttu-id="5cbc7-214">Indica si el dispositivo será necesario esperar confirmación configurado</span><span class="sxs-lookup"><span data-stu-id="5cbc7-214">Indicates if the device will need to wait for configured confirmation</span></span>|
|<span data-ttu-id="5cbc7-215">sharedIPadMaximumUserCount</span><span class="sxs-lookup"><span data-stu-id="5cbc7-215">sharedIPadMaximumUserCount</span></span>|<span data-ttu-id="5cbc7-216">Int32</span><span class="sxs-lookup"><span data-stu-id="5cbc7-216">Int32</span></span>|<span data-ttu-id="5cbc7-217">Especifica el número máximo de usuarios que pueden usar un iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-217">This specifies the maximum number of users that can use a shared iPad.</span></span> <span data-ttu-id="5cbc7-218">Solo se aplica en modo compartido iPad.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-218">Only applicable in shared iPad mode.</span></span>|
|<span data-ttu-id="5cbc7-219">enableSharedIPad</span><span class="sxs-lookup"><span data-stu-id="5cbc7-219">enableSharedIPad</span></span>|<span data-ttu-id="5cbc7-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-220">Boolean</span></span>|<span data-ttu-id="5cbc7-221">Esto indica si el dispositivo se se inscriben en un modo que permite los escenarios de usuario múltiple.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-221">This indicates whether the device is to be enrolled in a mode which enables multi user scenarios.</span></span> <span data-ttu-id="5cbc7-222">Solo se aplica en iPad compartida.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-222">Only applicable in shared iPads.</span></span>|
|<span data-ttu-id="5cbc7-223">companyPortalVppTokenId</span><span class="sxs-lookup"><span data-stu-id="5cbc7-223">companyPortalVppTokenId</span></span>|<span data-ttu-id="5cbc7-224">Cadena</span><span class="sxs-lookup"><span data-stu-id="5cbc7-224">String</span></span>|<span data-ttu-id="5cbc7-225">Si establece, indica qué token Vpp debe usarse para implementar el Portal de la empresa con licencias de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-225">If set, indicates which Vpp token should be used to deploy the Company Portal w/ device licensing.</span></span> <span data-ttu-id="5cbc7-226">'enableAuthenticationViaCompanyPortal' debe establecerse en orden establecer esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-226">'enableAuthenticationViaCompanyPortal' must be set in order for this property to be set.</span></span>|
|<span data-ttu-id="5cbc7-227">enableSingleAppEnrollmentMode</span><span class="sxs-lookup"><span data-stu-id="5cbc7-227">enableSingleAppEnrollmentMode</span></span>|<span data-ttu-id="5cbc7-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="5cbc7-228">Boolean</span></span>|<span data-ttu-id="5cbc7-229">Indica el dispositivo para habilitar el modo de aplicación único y aplicar el bloqueo de la aplicación durante la inscripción.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-229">Tells the device to enable single app mode and apply app-lock during enrollment.</span></span> <span data-ttu-id="5cbc7-230">Valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-230">Default is false.</span></span> <span data-ttu-id="5cbc7-231">'enableAuthenticationViaCompanyPortal' y 'companyPortalVppTokenId' se deben establecer para que esta propiedad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-231">'enableAuthenticationViaCompanyPortal' and 'companyPortalVppTokenId' must be set for this property to be set.</span></span>|



## <a name="response"></a><span data-ttu-id="5cbc7-232">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cbc7-232">Response</span></span>
<span data-ttu-id="5cbc7-233">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-233">If successful, this method returns a `200 OK` response code and an updated [depIOSEnrollmentProfile](../resources/intune-enrollment-depiosenrollmentprofile.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5cbc7-234">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5cbc7-234">Example</span></span>
### <a name="request"></a><span data-ttu-id="5cbc7-235">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5cbc7-235">Request</span></span>
<span data-ttu-id="5cbc7-236">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-236">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/defaultIosEnrollmentProfile
Content-type: application/json
Content-length: 1267

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

### <a name="response"></a><span data-ttu-id="5cbc7-237">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5cbc7-237">Response</span></span>
<span data-ttu-id="5cbc7-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5cbc7-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





