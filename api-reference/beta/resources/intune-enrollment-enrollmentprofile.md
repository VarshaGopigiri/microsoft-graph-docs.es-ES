---
title: tipo de recurso enrollmentProfile
description: El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases. Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: b88745c060e71e32199a96b23f94fa0d3229d451
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27935594"
---
# <a name="enrollmentprofile-resource-type"></a><span data-ttu-id="f3db4-104">tipo de recurso enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-104">enrollmentProfile resource type</span></span>

> <span data-ttu-id="f3db4-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3db4-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3db4-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3db4-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f3db4-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3db4-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3db4-108">El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases.</span><span class="sxs-lookup"><span data-stu-id="f3db4-108">The enrollmentProfile resource represents a collection of configurations which must be provided pre-enrollment to enable enrolling certain devices whose identities have been pre-staged.</span></span> <span data-ttu-id="f3db4-109">Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f3db4-109">Pre-staged device identities are assigned to this type of profile to apply the profile's configurations at enrollment of the corresponding device.</span></span>
## <a name="methods"></a><span data-ttu-id="f3db4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f3db4-110">Methods</span></span>
|<span data-ttu-id="f3db4-111">Método</span><span class="sxs-lookup"><span data-stu-id="f3db4-111">Method</span></span>|<span data-ttu-id="f3db4-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3db4-112">Return Type</span></span>|<span data-ttu-id="f3db4-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3db4-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f3db4-114">Lista enrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="f3db4-114">List enrollmentProfiles</span></span>](../api/intune-enrollment-enrollmentprofile-list.md)|<span data-ttu-id="f3db4-115">colección de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="f3db4-115">[enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) collection</span></span>|<span data-ttu-id="f3db4-116">Propiedades de la lista y relaciones de los objetos [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db4-116">List properties and relationships of the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) objects.</span></span>|
|[<span data-ttu-id="f3db4-117">Obtener enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-117">Get enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-get.md)|[<span data-ttu-id="f3db4-118">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-118">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="f3db4-119">Leer las propiedades y las relaciones del objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db4-119">Read properties and relationships of the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="f3db4-120">Crear enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-120">Create enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-create.md)|[<span data-ttu-id="f3db4-121">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-121">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="f3db4-122">Crear un nuevo objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db4-122">Create a new [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="f3db4-123">Eliminar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-123">Delete enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-delete.md)|<span data-ttu-id="f3db4-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3db4-124">None</span></span>|<span data-ttu-id="f3db4-125">Elimina un [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="f3db4-125">Deletes a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span></span>|
|[<span data-ttu-id="f3db4-126">Actualizar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-126">Update enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-update.md)|[<span data-ttu-id="f3db4-127">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-127">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="f3db4-128">Actualizar las propiedades de un objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db4-128">Update the properties of a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="f3db4-129">acción setDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3db4-129">setDefaultProfile action</span></span>](../api/intune-enrollment-enrollmentprofile-setdefaultprofile.md)|<span data-ttu-id="f3db4-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3db4-130">None</span></span>|<span data-ttu-id="f3db4-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f3db4-131">Not yet documented</span></span>|
|[<span data-ttu-id="f3db4-132">exportMobileConfig (función)</span><span class="sxs-lookup"><span data-stu-id="f3db4-132">exportMobileConfig function</span></span>](../api/intune-enrollment-enrollmentprofile-exportmobileconfig.md)|<span data-ttu-id="f3db4-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3db4-133">String</span></span>|<span data-ttu-id="f3db4-134">Exporta la configuración móvil</span><span class="sxs-lookup"><span data-stu-id="f3db4-134">Exports the mobile configuration</span></span>|
|[<span data-ttu-id="f3db4-135">acción updateDeviceProfileAssignment</span><span class="sxs-lookup"><span data-stu-id="f3db4-135">updateDeviceProfileAssignment action</span></span>](../api/intune-enrollment-enrollmentprofile-updatedeviceprofileassignment.md)|<span data-ttu-id="f3db4-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f3db4-136">None</span></span>|<span data-ttu-id="f3db4-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f3db4-137">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="f3db4-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3db4-138">Properties</span></span>
|<span data-ttu-id="f3db4-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3db4-139">Property</span></span>|<span data-ttu-id="f3db4-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3db4-140">Type</span></span>|<span data-ttu-id="f3db4-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3db4-141">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f3db4-142">id</span><span class="sxs-lookup"><span data-stu-id="f3db4-142">id</span></span>|<span data-ttu-id="f3db4-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3db4-143">String</span></span>|<span data-ttu-id="f3db4-144">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="f3db4-144">The GUID for the object</span></span>|
|<span data-ttu-id="f3db4-145">displayName</span><span class="sxs-lookup"><span data-stu-id="f3db4-145">displayName</span></span>|<span data-ttu-id="f3db4-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3db4-146">String</span></span>|<span data-ttu-id="f3db4-147">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="f3db4-147">Name of the profile</span></span>|
|<span data-ttu-id="f3db4-148">descripción</span><span class="sxs-lookup"><span data-stu-id="f3db4-148">description</span></span>|<span data-ttu-id="f3db4-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3db4-149">String</span></span>|<span data-ttu-id="f3db4-150">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="f3db4-150">Description of the profile</span></span>|
|<span data-ttu-id="f3db4-151">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="f3db4-151">requiresUserAuthentication</span></span>|<span data-ttu-id="f3db4-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="f3db4-152">Boolean</span></span>|<span data-ttu-id="f3db4-153">Indica si el perfil requiere autenticación de usuario</span><span class="sxs-lookup"><span data-stu-id="f3db4-153">Indicates if the profile requires user authentication</span></span>|
|<span data-ttu-id="f3db4-154">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f3db4-154">configurationEndpointUrl</span></span>|<span data-ttu-id="f3db4-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3db4-155">String</span></span>|<span data-ttu-id="f3db4-156">Dirección url de extremo de configuración que se usará para inscripción</span><span class="sxs-lookup"><span data-stu-id="f3db4-156">Configuration endpoint url to use for Enrollment</span></span>|
|<span data-ttu-id="f3db4-157">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="f3db4-157">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="f3db4-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="f3db4-158">Boolean</span></span>|<span data-ttu-id="f3db4-159">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="f3db4-159">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f3db4-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f3db4-160">Relationships</span></span>
<span data-ttu-id="f3db4-161">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f3db4-161">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f3db4-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f3db4-162">JSON Representation</span></span>
<span data-ttu-id="f3db4-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f3db4-163">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.enrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.enrollmentProfile",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "requiresUserAuthentication": true,
  "configurationEndpointUrl": "String",
  "enableAuthenticationViaCompanyPortal": true
}
```





