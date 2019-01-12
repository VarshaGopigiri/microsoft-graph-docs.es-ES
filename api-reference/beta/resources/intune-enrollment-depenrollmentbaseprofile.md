---
title: tipo de recurso depEnrollmentBaseProfile
description: El recurso DepEnrollmentBaseProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP). Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9e1383048b08a309ea0ecf60eb1ad07c2636e7e5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937673"
---
# <a name="depenrollmentbaseprofile-resource-type"></a><span data-ttu-id="82321-104">tipo de recurso depEnrollmentBaseProfile</span><span class="sxs-lookup"><span data-stu-id="82321-104">depEnrollmentBaseProfile resource type</span></span>

> <span data-ttu-id="82321-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="82321-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="82321-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="82321-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="82321-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82321-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82321-108">El recurso DepEnrollmentBaseProfile representa un perfil de inscripción de programa de inscripción de dispositivos de Apple (DEP).</span><span class="sxs-lookup"><span data-stu-id="82321-108">The DepEnrollmentBaseProfile resource represents an Apple Device Enrollment Program (DEP) enrollment profile.</span></span> <span data-ttu-id="82321-109">Este tipo de perfil debe asignarse a los números de serie de Apple DEP antes de que los dispositivos correspondientes pueden inscribirse a través de DEP.</span><span class="sxs-lookup"><span data-stu-id="82321-109">This type of profile must be assigned to Apple DEP serial numbers before the corresponding devices can enroll via DEP.</span></span>

<span data-ttu-id="82321-110">Hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-110">Inherits from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>

## <a name="methods"></a><span data-ttu-id="82321-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="82321-111">Methods</span></span>
|<span data-ttu-id="82321-112">Método</span><span class="sxs-lookup"><span data-stu-id="82321-112">Method</span></span>|<span data-ttu-id="82321-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82321-113">Return Type</span></span>|<span data-ttu-id="82321-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="82321-114">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="82321-115">Lista depEnrollmentBaseProfiles</span><span class="sxs-lookup"><span data-stu-id="82321-115">List depEnrollmentBaseProfiles</span></span>](../api/intune-enrollment-depenrollmentbaseprofile-list.md)|<span data-ttu-id="82321-116">colección de [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-116">[depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) collection</span></span>|<span data-ttu-id="82321-117">Propiedades de la lista y relaciones de los objetos [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="82321-117">List properties and relationships of the [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) objects.</span></span>|
|[<span data-ttu-id="82321-118">Obtener depEnrollmentBaseProfile</span><span class="sxs-lookup"><span data-stu-id="82321-118">Get depEnrollmentBaseProfile</span></span>](../api/intune-enrollment-depenrollmentbaseprofile-get.md)|[<span data-ttu-id="82321-119">depEnrollmentBaseProfile</span><span class="sxs-lookup"><span data-stu-id="82321-119">depEnrollmentBaseProfile</span></span>](../resources/intune-enrollment-depenrollmentbaseprofile.md)|<span data-ttu-id="82321-120">Leer las propiedades y las relaciones del objeto [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="82321-120">Read properties and relationships of the [depEnrollmentBaseProfile](../resources/intune-enrollment-depenrollmentbaseprofile.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="82321-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82321-121">Properties</span></span>
|<span data-ttu-id="82321-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82321-122">Property</span></span>|<span data-ttu-id="82321-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="82321-123">Type</span></span>|<span data-ttu-id="82321-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="82321-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82321-125">id</span><span class="sxs-lookup"><span data-stu-id="82321-125">id</span></span>|<span data-ttu-id="82321-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-126">String</span></span>|<span data-ttu-id="82321-127">El GUID para el objeto Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-127">The GUID for the object Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-128">displayName</span><span class="sxs-lookup"><span data-stu-id="82321-128">displayName</span></span>|<span data-ttu-id="82321-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-129">String</span></span>|<span data-ttu-id="82321-130">Nombre del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-130">Name of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-131">descripción</span><span class="sxs-lookup"><span data-stu-id="82321-131">description</span></span>|<span data-ttu-id="82321-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-132">String</span></span>|<span data-ttu-id="82321-133">Descripción del perfil Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-133">Description of the profile Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-134">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="82321-134">requiresUserAuthentication</span></span>|<span data-ttu-id="82321-135">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-135">Boolean</span></span>|<span data-ttu-id="82321-136">Indica si el perfil requiere autenticación de usuario Inherited desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-136">Indicates if the profile requires user authentication Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-137">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="82321-137">configurationEndpointUrl</span></span>|<span data-ttu-id="82321-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-138">String</span></span>|<span data-ttu-id="82321-139">Dirección url de extremo de configuración se usa para inscripción se hereda desde [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-139">Configuration endpoint url to use for Enrollment Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-140">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="82321-140">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="82321-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-141">Boolean</span></span>|<span data-ttu-id="82321-142">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="82321-142">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span> <span data-ttu-id="82321-143">Se hereda de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="82321-143">Inherited from [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span></span>|
|<span data-ttu-id="82321-144">isDefault</span><span class="sxs-lookup"><span data-stu-id="82321-144">isDefault</span></span>|<span data-ttu-id="82321-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-145">Boolean</span></span>|<span data-ttu-id="82321-146">Indica si este es el perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="82321-146">Indicates if this is the default profile</span></span>|
|<span data-ttu-id="82321-147">supervisedModeEnabled</span><span class="sxs-lookup"><span data-stu-id="82321-147">supervisedModeEnabled</span></span>|<span data-ttu-id="82321-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-148">Boolean</span></span>|<span data-ttu-id="82321-149">Modo supervisado, True para habilitar, false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="82321-149">Supervised mode, True to enable, false otherwise.</span></span> <span data-ttu-id="82321-150">Vea https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune para obtener información adicional.</span><span class="sxs-lookup"><span data-stu-id="82321-150">See https://docs.microsoft.com/en-us/intune/deploy-use/enroll-devices-in-microsoft-intune for additional information.</span></span>|
|<span data-ttu-id="82321-151">supportDepartment</span><span class="sxs-lookup"><span data-stu-id="82321-151">supportDepartment</span></span>|<span data-ttu-id="82321-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-152">String</span></span>|<span data-ttu-id="82321-153">Información del departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="82321-153">Support department information</span></span>|
|<span data-ttu-id="82321-154">passCodeDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-154">passCodeDisabled</span></span>|<span data-ttu-id="82321-155">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-155">Boolean</span></span>|<span data-ttu-id="82321-156">Indica si se deshabilita el panel de código de acceso del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-156">Indicates if Passcode setup pane is disabled</span></span>|
|<span data-ttu-id="82321-157">isMandatory</span><span class="sxs-lookup"><span data-stu-id="82321-157">isMandatory</span></span>|<span data-ttu-id="82321-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-158">Boolean</span></span>|<span data-ttu-id="82321-159">Indica si el perfil es obligatorio</span><span class="sxs-lookup"><span data-stu-id="82321-159">Indicates if the profile is mandatory</span></span>|
|<span data-ttu-id="82321-160">locationDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-160">locationDisabled</span></span>|<span data-ttu-id="82321-161">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-161">Boolean</span></span>|<span data-ttu-id="82321-162">Indica si se deshabilita el panel del programa de instalación del servicio de ubicación</span><span class="sxs-lookup"><span data-stu-id="82321-162">Indicates if Location service setup pane is disabled</span></span>|
|<span data-ttu-id="82321-163">supportPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="82321-163">supportPhoneNumber</span></span>|<span data-ttu-id="82321-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="82321-164">String</span></span>|<span data-ttu-id="82321-165">Número de teléfono de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="82321-165">Support phone number</span></span>|
|<span data-ttu-id="82321-166">profileRemovalDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-166">profileRemovalDisabled</span></span>|<span data-ttu-id="82321-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-167">Boolean</span></span>|<span data-ttu-id="82321-168">Indica si está deshabilitada la opción de eliminación de perfiles</span><span class="sxs-lookup"><span data-stu-id="82321-168">Indicates if the profile removal option is disabled</span></span>|
|<span data-ttu-id="82321-169">restoreBlocked</span><span class="sxs-lookup"><span data-stu-id="82321-169">restoreBlocked</span></span>|<span data-ttu-id="82321-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-170">Boolean</span></span>|<span data-ttu-id="82321-171">Indica si se bloquea el panel de restauración del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-171">Indicates if Restore setup pane is blocked</span></span>|
|<span data-ttu-id="82321-172">appleIdDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-172">appleIdDisabled</span></span>|<span data-ttu-id="82321-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-173">Boolean</span></span>|<span data-ttu-id="82321-174">Indica si se deshabilita el panel de Apple identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-174">Indicates if Apple id setup pane is disabled</span></span>|
|<span data-ttu-id="82321-175">termsAndConditionsDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-175">termsAndConditionsDisabled</span></span>|<span data-ttu-id="82321-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-176">Boolean</span></span>|<span data-ttu-id="82321-177">Indica si el panel del programa de instalación 'Términos y condiciones' está deshabilitado</span><span class="sxs-lookup"><span data-stu-id="82321-177">Indicates if 'Terms and Conditions' setup pane is disabled</span></span>|
|<span data-ttu-id="82321-178">touchIdDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-178">touchIdDisabled</span></span>|<span data-ttu-id="82321-179">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-179">Boolean</span></span>|<span data-ttu-id="82321-180">Indica si se deshabilita el panel de táctil identificador del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-180">Indicates if touch id setup pane is disabled</span></span>|
|<span data-ttu-id="82321-181">applePayDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-181">applePayDisabled</span></span>|<span data-ttu-id="82321-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-182">Boolean</span></span>|<span data-ttu-id="82321-183">Indica si se deshabilita el panel de Apple pago del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-183">Indicates if Apple pay setup pane is disabled</span></span>|
|<span data-ttu-id="82321-184">zoomDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-184">zoomDisabled</span></span>|<span data-ttu-id="82321-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-185">Boolean</span></span>|<span data-ttu-id="82321-186">Indica si se deshabilita el panel de zoom del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-186">Indicates if zoom setup pane is disabled</span></span>|
|<span data-ttu-id="82321-187">siriDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-187">siriDisabled</span></span>|<span data-ttu-id="82321-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-188">Boolean</span></span>|<span data-ttu-id="82321-189">Indica si se deshabilita el panel de siri el programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-189">Indicates if siri setup pane is disabled</span></span>|
|<span data-ttu-id="82321-190">diagnosticsDisabled</span><span class="sxs-lookup"><span data-stu-id="82321-190">diagnosticsDisabled</span></span>|<span data-ttu-id="82321-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="82321-191">Boolean</span></span>|<span data-ttu-id="82321-192">Indica si se deshabilita el panel de diagnóstico del programa de instalación</span><span class="sxs-lookup"><span data-stu-id="82321-192">Indicates if diagnostics setup pane is disabled</span></span>|

## <a name="relationships"></a><span data-ttu-id="82321-193">Relaciones</span><span class="sxs-lookup"><span data-stu-id="82321-193">Relationships</span></span>
<span data-ttu-id="82321-194">Ninguna</span><span class="sxs-lookup"><span data-stu-id="82321-194">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="82321-195">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82321-195">JSON Representation</span></span>
<span data-ttu-id="82321-196">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82321-196">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.depEnrollmentBaseProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.depEnrollmentBaseProfile",
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
  "profileRemovalDisabled": true,
  "restoreBlocked": true,
  "appleIdDisabled": true,
  "termsAndConditionsDisabled": true,
  "touchIdDisabled": true,
  "applePayDisabled": true,
  "zoomDisabled": true,
  "siriDisabled": true,
  "diagnosticsDisabled": true
}
```





