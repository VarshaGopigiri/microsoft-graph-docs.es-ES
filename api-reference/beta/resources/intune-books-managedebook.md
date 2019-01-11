---
title: Tipo de recurso managedEBook
description: Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3bf01c2115f4a0224ab09e59a9049324e82fa855
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834191"
---
# <a name="managedebook-resource-type"></a><span data-ttu-id="860a8-103">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="860a8-103">managedEBook resource type</span></span>

> <span data-ttu-id="860a8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="860a8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="860a8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="860a8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="860a8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="860a8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="860a8-107">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="860a8-107">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="860a8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="860a8-108">Methods</span></span>
|<span data-ttu-id="860a8-109">Método</span><span class="sxs-lookup"><span data-stu-id="860a8-109">Method</span></span>|<span data-ttu-id="860a8-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="860a8-110">Return Type</span></span>|<span data-ttu-id="860a8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="860a8-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="860a8-112">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="860a8-112">List managedEBooks</span></span>](../api/intune-books-managedebook-list.md)|<span data-ttu-id="860a8-113">Colección [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="860a8-113">[managedEBook](../resources/intune-books-managedebook.md) collection</span></span>|<span data-ttu-id="860a8-114">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="860a8-114">List properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) objects.</span></span>|
|[<span data-ttu-id="860a8-115">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="860a8-115">Get managedEBook</span></span>](../api/intune-books-managedebook-get.md)|[<span data-ttu-id="860a8-116">managedEBook</span><span class="sxs-lookup"><span data-stu-id="860a8-116">managedEBook</span></span>](../resources/intune-books-managedebook.md)|<span data-ttu-id="860a8-117">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="860a8-117">Read properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) object.</span></span>|
|[<span data-ttu-id="860a8-118">Acción assign</span><span class="sxs-lookup"><span data-stu-id="860a8-118">assign action</span></span>](../api/intune-books-managedebook-assign.md)|<span data-ttu-id="860a8-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="860a8-119">None</span></span>|<span data-ttu-id="860a8-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="860a8-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="860a8-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="860a8-121">Properties</span></span>
|<span data-ttu-id="860a8-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="860a8-122">Property</span></span>|<span data-ttu-id="860a8-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="860a8-123">Type</span></span>|<span data-ttu-id="860a8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="860a8-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="860a8-125">id</span><span class="sxs-lookup"><span data-stu-id="860a8-125">id</span></span>|<span data-ttu-id="860a8-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-126">String</span></span>|<span data-ttu-id="860a8-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="860a8-127">Key of the entity.</span></span>|
|<span data-ttu-id="860a8-128">displayName</span><span class="sxs-lookup"><span data-stu-id="860a8-128">displayName</span></span>|<span data-ttu-id="860a8-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-129">String</span></span>|<span data-ttu-id="860a8-130">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="860a8-130">Name of the eBook.</span></span>|
|<span data-ttu-id="860a8-131">descripción</span><span class="sxs-lookup"><span data-stu-id="860a8-131">description</span></span>|<span data-ttu-id="860a8-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-132">String</span></span>|<span data-ttu-id="860a8-133">Descripción.</span><span class="sxs-lookup"><span data-stu-id="860a8-133">Description.</span></span>|
|<span data-ttu-id="860a8-134">publicador</span><span class="sxs-lookup"><span data-stu-id="860a8-134">publisher</span></span>|<span data-ttu-id="860a8-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-135">String</span></span>|<span data-ttu-id="860a8-136">Publicador.</span><span class="sxs-lookup"><span data-stu-id="860a8-136">Publisher.</span></span>|
|<span data-ttu-id="860a8-137">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="860a8-137">publishedDateTime</span></span>|<span data-ttu-id="860a8-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="860a8-138">DateTimeOffset</span></span>|<span data-ttu-id="860a8-139">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-139">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="860a8-140">largeCover</span><span class="sxs-lookup"><span data-stu-id="860a8-140">largeCover</span></span>|[<span data-ttu-id="860a8-141">mimeContent</span><span class="sxs-lookup"><span data-stu-id="860a8-141">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="860a8-142">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="860a8-142">Book cover.</span></span>|
|<span data-ttu-id="860a8-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="860a8-143">createdDateTime</span></span>|<span data-ttu-id="860a8-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="860a8-144">DateTimeOffset</span></span>|<span data-ttu-id="860a8-145">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-145">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="860a8-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="860a8-146">lastModifiedDateTime</span></span>|<span data-ttu-id="860a8-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="860a8-147">DateTimeOffset</span></span>|<span data-ttu-id="860a8-148">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-148">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="860a8-149">informationUrl</span><span class="sxs-lookup"><span data-stu-id="860a8-149">informationUrl</span></span>|<span data-ttu-id="860a8-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-150">String</span></span>|<span data-ttu-id="860a8-151">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="860a8-151">The more information Url.</span></span>|
|<span data-ttu-id="860a8-152">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="860a8-152">privacyInformationUrl</span></span>|<span data-ttu-id="860a8-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="860a8-153">String</span></span>|<span data-ttu-id="860a8-154">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="860a8-154">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="860a8-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="860a8-155">Relationships</span></span>
|<span data-ttu-id="860a8-156">Relación</span><span class="sxs-lookup"><span data-stu-id="860a8-156">Relationship</span></span>|<span data-ttu-id="860a8-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="860a8-157">Type</span></span>|<span data-ttu-id="860a8-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="860a8-158">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="860a8-159">categories</span><span class="sxs-lookup"><span data-stu-id="860a8-159">categories</span></span>|<span data-ttu-id="860a8-160">colección de [managedEBookCategory](../resources/intune-books-managedebookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="860a8-160">[managedEBookCategory](../resources/intune-books-managedebookcategory.md) collection</span></span>|<span data-ttu-id="860a8-161">La lista de categorías para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-161">The list of categories for this eBook.</span></span>|
|<span data-ttu-id="860a8-162">asignaciones</span><span class="sxs-lookup"><span data-stu-id="860a8-162">assignments</span></span>|<span data-ttu-id="860a8-163">Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="860a8-163">[managedEBookAssignment](../resources/intune-books-managedebookassignment.md) collection</span></span>|<span data-ttu-id="860a8-164">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-164">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="860a8-165">installSummary</span><span class="sxs-lookup"><span data-stu-id="860a8-165">installSummary</span></span>|[<span data-ttu-id="860a8-166">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="860a8-166">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="860a8-167">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="860a8-167">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="860a8-168">deviceStates</span><span class="sxs-lookup"><span data-stu-id="860a8-168">deviceStates</span></span>|<span data-ttu-id="860a8-169">Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="860a8-169">[deviceInstallState](../resources/intune-books-deviceinstallstate.md) collection</span></span>|<span data-ttu-id="860a8-170">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-170">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="860a8-171">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="860a8-171">userStateSummary</span></span>|<span data-ttu-id="860a8-172">Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="860a8-172">[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="860a8-173">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="860a8-173">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="860a8-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="860a8-174">JSON Representation</span></span>
<span data-ttu-id="860a8-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="860a8-175">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBook"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBook",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "publishedDateTime": "String (timestamp)",
  "largeCover": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "informationUrl": "String",
  "privacyInformationUrl": "String"
}
```





