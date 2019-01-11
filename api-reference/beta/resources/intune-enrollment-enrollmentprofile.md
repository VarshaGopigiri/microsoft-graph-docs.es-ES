---
title: tipo de recurso enrollmentProfile
description: El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases. Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.
localization_priority: Normal
ms.openlocfilehash: 43aa6f5f3e8093da0c066012d763e5f0f6455da6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894309"
---
# <a name="enrollmentprofile-resource-type"></a><span data-ttu-id="a303f-104">tipo de recurso enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-104">enrollmentProfile resource type</span></span>

> <span data-ttu-id="a303f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a303f-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a303f-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a303f-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a303f-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a303f-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a303f-108">El recurso enrollmentProfile representa una colección de configuraciones que debe proporcionarse previo a la inscripción para habilitar la inscripción de ciertos dispositivos cuyas identidades han sido previamente por fases.</span><span class="sxs-lookup"><span data-stu-id="a303f-108">The enrollmentProfile resource represents a collection of configurations which must be provided pre-enrollment to enable enrolling certain devices whose identities have been pre-staged.</span></span> <span data-ttu-id="a303f-109">Las identidades del dispositivo previamente por fases se asignan a este tipo de perfil para aplicar las configuraciones del perfil en inscripción del dispositivo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a303f-109">Pre-staged device identities are assigned to this type of profile to apply the profile's configurations at enrollment of the corresponding device.</span></span>
## <a name="methods"></a><span data-ttu-id="a303f-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a303f-110">Methods</span></span>
|<span data-ttu-id="a303f-111">Método</span><span class="sxs-lookup"><span data-stu-id="a303f-111">Method</span></span>|<span data-ttu-id="a303f-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a303f-112">Return Type</span></span>|<span data-ttu-id="a303f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="a303f-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a303f-114">Lista enrollmentProfiles</span><span class="sxs-lookup"><span data-stu-id="a303f-114">List enrollmentProfiles</span></span>](../api/intune-enrollment-enrollmentprofile-list.md)|<span data-ttu-id="a303f-115">colección de [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md)</span><span class="sxs-lookup"><span data-stu-id="a303f-115">[enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) collection</span></span>|<span data-ttu-id="a303f-116">Propiedades de la lista y relaciones de los objetos [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a303f-116">List properties and relationships of the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) objects.</span></span>|
|[<span data-ttu-id="a303f-117">Obtener enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-117">Get enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-get.md)|[<span data-ttu-id="a303f-118">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-118">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="a303f-119">Leer las propiedades y las relaciones del objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a303f-119">Read properties and relationships of the [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="a303f-120">Crear enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-120">Create enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-create.md)|[<span data-ttu-id="a303f-121">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-121">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="a303f-122">Crear un nuevo objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a303f-122">Create a new [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="a303f-123">Eliminar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-123">Delete enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-delete.md)|<span data-ttu-id="a303f-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a303f-124">None</span></span>|<span data-ttu-id="a303f-125">Elimina un [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span><span class="sxs-lookup"><span data-stu-id="a303f-125">Deletes a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md).</span></span>|
|[<span data-ttu-id="a303f-126">Actualizar enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-126">Update enrollmentProfile</span></span>](../api/intune-enrollment-enrollmentprofile-update.md)|[<span data-ttu-id="a303f-127">enrollmentProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-127">enrollmentProfile</span></span>](../resources/intune-enrollment-enrollmentprofile.md)|<span data-ttu-id="a303f-128">Actualizar las propiedades de un objeto [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a303f-128">Update the properties of a [enrollmentProfile](../resources/intune-enrollment-enrollmentprofile.md) object.</span></span>|
|[<span data-ttu-id="a303f-129">acción setDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a303f-129">setDefaultProfile action</span></span>](../api/intune-enrollment-enrollmentprofile-setdefaultprofile.md)|<span data-ttu-id="a303f-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a303f-130">None</span></span>|<span data-ttu-id="a303f-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a303f-131">Not yet documented</span></span>|
|[<span data-ttu-id="a303f-132">exportMobileConfig (función)</span><span class="sxs-lookup"><span data-stu-id="a303f-132">exportMobileConfig function</span></span>](../api/intune-enrollment-enrollmentprofile-exportmobileconfig.md)|<span data-ttu-id="a303f-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="a303f-133">String</span></span>|<span data-ttu-id="a303f-134">Exporta la configuración móvil</span><span class="sxs-lookup"><span data-stu-id="a303f-134">Exports the mobile configuration</span></span>|
|[<span data-ttu-id="a303f-135">acción updateDeviceProfileAssignment</span><span class="sxs-lookup"><span data-stu-id="a303f-135">updateDeviceProfileAssignment action</span></span>](../api/intune-enrollment-enrollmentprofile-updatedeviceprofileassignment.md)|<span data-ttu-id="a303f-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="a303f-136">None</span></span>|<span data-ttu-id="a303f-137">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a303f-137">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="a303f-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a303f-138">Properties</span></span>
|<span data-ttu-id="a303f-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a303f-139">Property</span></span>|<span data-ttu-id="a303f-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="a303f-140">Type</span></span>|<span data-ttu-id="a303f-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="a303f-141">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a303f-142">id</span><span class="sxs-lookup"><span data-stu-id="a303f-142">id</span></span>|<span data-ttu-id="a303f-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="a303f-143">String</span></span>|<span data-ttu-id="a303f-144">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="a303f-144">The GUID for the object</span></span>|
|<span data-ttu-id="a303f-145">displayName</span><span class="sxs-lookup"><span data-stu-id="a303f-145">displayName</span></span>|<span data-ttu-id="a303f-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="a303f-146">String</span></span>|<span data-ttu-id="a303f-147">Nombre del perfil</span><span class="sxs-lookup"><span data-stu-id="a303f-147">Name of the profile</span></span>|
|<span data-ttu-id="a303f-148">descripción</span><span class="sxs-lookup"><span data-stu-id="a303f-148">description</span></span>|<span data-ttu-id="a303f-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="a303f-149">String</span></span>|<span data-ttu-id="a303f-150">Descripción del perfil</span><span class="sxs-lookup"><span data-stu-id="a303f-150">Description of the profile</span></span>|
|<span data-ttu-id="a303f-151">requiresUserAuthentication</span><span class="sxs-lookup"><span data-stu-id="a303f-151">requiresUserAuthentication</span></span>|<span data-ttu-id="a303f-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="a303f-152">Boolean</span></span>|<span data-ttu-id="a303f-153">Indica si el perfil requiere autenticación de usuario</span><span class="sxs-lookup"><span data-stu-id="a303f-153">Indicates if the profile requires user authentication</span></span>|
|<span data-ttu-id="a303f-154">configurationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="a303f-154">configurationEndpointUrl</span></span>|<span data-ttu-id="a303f-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="a303f-155">String</span></span>|<span data-ttu-id="a303f-156">Dirección url de extremo de configuración que se usará para inscripción</span><span class="sxs-lookup"><span data-stu-id="a303f-156">Configuration endpoint url to use for Enrollment</span></span>|
|<span data-ttu-id="a303f-157">enableAuthenticationViaCompanyPortal</span><span class="sxs-lookup"><span data-stu-id="a303f-157">enableAuthenticationViaCompanyPortal</span></span>|<span data-ttu-id="a303f-158">Booleano</span><span class="sxs-lookup"><span data-stu-id="a303f-158">Boolean</span></span>|<span data-ttu-id="a303f-159">Indica para autenticarse con Apple Asistente para la instalación en lugar de Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="a303f-159">Indicates to authenticate with Apple Setup Assistant instead of Company Portal.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a303f-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a303f-160">Relationships</span></span>
<span data-ttu-id="a303f-161">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a303f-161">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a303f-162">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a303f-162">JSON Representation</span></span>
<span data-ttu-id="a303f-163">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a303f-163">Here is a JSON representation of the resource.</span></span>
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





