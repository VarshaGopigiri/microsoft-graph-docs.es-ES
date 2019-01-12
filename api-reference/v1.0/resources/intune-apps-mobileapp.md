---
title: Tipo de recurso mobileApp
description: Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 69992ad07c5a0d97168db44cca8474c021d9a230
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947480"
---
# <a name="mobileapp-resource-type"></a><span data-ttu-id="7e5a1-103">Tipo de recurso mobileApp</span><span class="sxs-lookup"><span data-stu-id="7e5a1-103">mobileApp resource type</span></span>

> <span data-ttu-id="7e5a1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e5a1-105">Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-105">An abstract class containing the base properties for Intune mobile apps.</span></span>
## <a name="methods"></a><span data-ttu-id="7e5a1-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e5a1-106">Methods</span></span>
|<span data-ttu-id="7e5a1-107">Método</span><span class="sxs-lookup"><span data-stu-id="7e5a1-107">Method</span></span>|<span data-ttu-id="7e5a1-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e5a1-108">Return Type</span></span>|<span data-ttu-id="7e5a1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e5a1-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7e5a1-110">Enumerar mobileApps</span><span class="sxs-lookup"><span data-stu-id="7e5a1-110">List mobileApps</span></span>](../api/intune-apps-mobileapp-list.md)|<span data-ttu-id="7e5a1-111">Colección [mobileApp](../resources/intune-apps-mobileapp.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a1-111">[mobileApp](../resources/intune-apps-mobileapp.md) collection</span></span>|<span data-ttu-id="7e5a1-112">Enumere las propiedades y las relaciones de los objetos [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7e5a1-112">List properties and relationships of the [mobileApp](../resources/intune-apps-mobileapp.md) objects.</span></span>|
|[<span data-ttu-id="7e5a1-113">Obtener mobileApp</span><span class="sxs-lookup"><span data-stu-id="7e5a1-113">Get mobileApp</span></span>](../api/intune-apps-mobileapp-get.md)|[<span data-ttu-id="7e5a1-114">mobileApp</span><span class="sxs-lookup"><span data-stu-id="7e5a1-114">mobileApp</span></span>](../resources/intune-apps-mobileapp.md)|<span data-ttu-id="7e5a1-115">Lea las propiedades y las relaciones del objeto [mobileApp](../resources/intune-apps-mobileapp.md).</span><span class="sxs-lookup"><span data-stu-id="7e5a1-115">Read properties and relationships of the [mobileApp](../resources/intune-apps-mobileapp.md) object.</span></span>|
|[<span data-ttu-id="7e5a1-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="7e5a1-116">assign action</span></span>](../api/intune-apps-mobileapp-assign.md)|<span data-ttu-id="7e5a1-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7e5a1-117">None</span></span>|<span data-ttu-id="7e5a1-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7e5a1-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="7e5a1-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e5a1-119">Properties</span></span>
|<span data-ttu-id="7e5a1-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e5a1-120">Property</span></span>|<span data-ttu-id="7e5a1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e5a1-121">Type</span></span>|<span data-ttu-id="7e5a1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e5a1-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e5a1-123">id</span><span class="sxs-lookup"><span data-stu-id="7e5a1-123">id</span></span>|<span data-ttu-id="7e5a1-124">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-124">String</span></span>|<span data-ttu-id="7e5a1-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-125">Key of the entity.</span></span>|
|<span data-ttu-id="7e5a1-126">displayName</span><span class="sxs-lookup"><span data-stu-id="7e5a1-126">displayName</span></span>|<span data-ttu-id="7e5a1-127">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-127">String</span></span>|<span data-ttu-id="7e5a1-128">El título de la aplicación importado o proporcionado por el administrador.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-128">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="7e5a1-129">descripción</span><span class="sxs-lookup"><span data-stu-id="7e5a1-129">description</span></span>|<span data-ttu-id="7e5a1-130">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-130">String</span></span>|<span data-ttu-id="7e5a1-131">La descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-131">The description of the app.</span></span>|
|<span data-ttu-id="7e5a1-132">publicador</span><span class="sxs-lookup"><span data-stu-id="7e5a1-132">publisher</span></span>|<span data-ttu-id="7e5a1-133">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-133">String</span></span>|<span data-ttu-id="7e5a1-134">El publicador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-134">The publisher of the app.</span></span>|
|<span data-ttu-id="7e5a1-135">largeIcon</span><span class="sxs-lookup"><span data-stu-id="7e5a1-135">largeIcon</span></span>|[<span data-ttu-id="7e5a1-136">mimeContent</span><span class="sxs-lookup"><span data-stu-id="7e5a1-136">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="7e5a1-137">El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-137">The large icon, to be displayed in the app details and used for upload of the icon.</span></span>|
|<span data-ttu-id="7e5a1-138">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7e5a1-138">createdDateTime</span></span>|<span data-ttu-id="7e5a1-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e5a1-139">DateTimeOffset</span></span>|<span data-ttu-id="7e5a1-140">La fecha y la hora de creación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-140">The date and time the app was created.</span></span>|
|<span data-ttu-id="7e5a1-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7e5a1-141">lastModifiedDateTime</span></span>|<span data-ttu-id="7e5a1-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e5a1-142">DateTimeOffset</span></span>|<span data-ttu-id="7e5a1-143">Fecha y hora de la última modificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-143">The date and time the app was last modified.</span></span>|
|<span data-ttu-id="7e5a1-144">isFeatured</span><span class="sxs-lookup"><span data-stu-id="7e5a1-144">isFeatured</span></span>|<span data-ttu-id="7e5a1-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="7e5a1-145">Boolean</span></span>|<span data-ttu-id="7e5a1-146">El valor que indica si el administrador ha marcado la aplicación como destacada.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-146">The value indicating whether the app is marked as featured by the admin.</span></span>|
|<span data-ttu-id="7e5a1-147">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="7e5a1-147">privacyInformationUrl</span></span>|<span data-ttu-id="7e5a1-148">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-148">String</span></span>|<span data-ttu-id="7e5a1-149">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-149">The privacy statement Url.</span></span>|
|<span data-ttu-id="7e5a1-150">informationUrl</span><span class="sxs-lookup"><span data-stu-id="7e5a1-150">informationUrl</span></span>|<span data-ttu-id="7e5a1-151">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-151">String</span></span>|<span data-ttu-id="7e5a1-152">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-152">The more information Url.</span></span>|
|<span data-ttu-id="7e5a1-153">propietario</span><span class="sxs-lookup"><span data-stu-id="7e5a1-153">owner</span></span>|<span data-ttu-id="7e5a1-154">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-154">String</span></span>|<span data-ttu-id="7e5a1-155">Propietario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-155">The owner of the app.</span></span>|
|<span data-ttu-id="7e5a1-156">desarrollador</span><span class="sxs-lookup"><span data-stu-id="7e5a1-156">developer</span></span>|<span data-ttu-id="7e5a1-157">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-157">String</span></span>|<span data-ttu-id="7e5a1-158">El desarrollador de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-158">The developer of the app.</span></span>|
|<span data-ttu-id="7e5a1-159">notas</span><span class="sxs-lookup"><span data-stu-id="7e5a1-159">notes</span></span>|<span data-ttu-id="7e5a1-160">String</span><span class="sxs-lookup"><span data-stu-id="7e5a1-160">String</span></span>|<span data-ttu-id="7e5a1-161">Notas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-161">Notes for the app.</span></span>|
|<span data-ttu-id="7e5a1-162">publishingState</span><span class="sxs-lookup"><span data-stu-id="7e5a1-162">publishingState</span></span>|[<span data-ttu-id="7e5a1-163">mobileAppPublishingState</span><span class="sxs-lookup"><span data-stu-id="7e5a1-163">mobileAppPublishingState</span></span>](../resources/intune-apps-mobileapppublishingstate.md)|<span data-ttu-id="7e5a1-164">Estado de publicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-164">The publishing state for the app.</span></span> <span data-ttu-id="7e5a1-165">La aplicación no puede asignarse a menos que se publique.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-165">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="7e5a1-166">Los valores posibles son: `notPublished`, `processing` y `published`.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-166">Possible values are: `notPublished`, `processing`, `published`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7e5a1-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7e5a1-167">Relationships</span></span>
|<span data-ttu-id="7e5a1-168">Relación</span><span class="sxs-lookup"><span data-stu-id="7e5a1-168">Relationship</span></span>|<span data-ttu-id="7e5a1-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e5a1-169">Type</span></span>|<span data-ttu-id="7e5a1-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e5a1-170">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e5a1-171">categorías</span><span class="sxs-lookup"><span data-stu-id="7e5a1-171">categories</span></span>|<span data-ttu-id="7e5a1-172">Colección [mobileAppCategory](../resources/intune-apps-mobileappcategory.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a1-172">[mobileAppCategory](../resources/intune-apps-mobileappcategory.md) collection</span></span>|<span data-ttu-id="7e5a1-173">La lista de categorías para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-173">The list of categories for this app.</span></span>|
|<span data-ttu-id="7e5a1-174">asignaciones</span><span class="sxs-lookup"><span data-stu-id="7e5a1-174">assignments</span></span>|<span data-ttu-id="7e5a1-175">Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a1-175">[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md) collection</span></span>|<span data-ttu-id="7e5a1-176">La lista de asignaciones de grupo para esta aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-176">The list of group assignments for this mobile app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7e5a1-177">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7e5a1-177">JSON Representation</span></span>
<span data-ttu-id="7e5a1-178">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7e5a1-178">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String"
}
```



