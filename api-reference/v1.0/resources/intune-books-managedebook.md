---
title: Tipo de recurso managedEBook
description: Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a2da2254b5d86a16d3a0e60fae0c0ea4215d54a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917863"
---
# <a name="managedebook-resource-type"></a><span data-ttu-id="01731-103">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="01731-103">managedEBook resource type</span></span>

> <span data-ttu-id="01731-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01731-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01731-105">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="01731-105">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="01731-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="01731-106">Methods</span></span>
|<span data-ttu-id="01731-107">Método</span><span class="sxs-lookup"><span data-stu-id="01731-107">Method</span></span>|<span data-ttu-id="01731-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01731-108">Return Type</span></span>|<span data-ttu-id="01731-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="01731-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="01731-110">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="01731-110">List managedEBooks</span></span>](../api/intune-books-managedebook-list.md)|<span data-ttu-id="01731-111">Colección [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="01731-111">[managedEBook](../resources/intune-books-managedebook.md) collection</span></span>|<span data-ttu-id="01731-112">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="01731-112">List properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) objects.</span></span>|
|[<span data-ttu-id="01731-113">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="01731-113">Get managedEBook</span></span>](../api/intune-books-managedebook-get.md)|[<span data-ttu-id="01731-114">managedEBook</span><span class="sxs-lookup"><span data-stu-id="01731-114">managedEBook</span></span>](../resources/intune-books-managedebook.md)|<span data-ttu-id="01731-115">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="01731-115">Read properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) object.</span></span>|
|[<span data-ttu-id="01731-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="01731-116">assign action</span></span>](../api/intune-books-managedebook-assign.md)|<span data-ttu-id="01731-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01731-117">None</span></span>|<span data-ttu-id="01731-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="01731-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="01731-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01731-119">Properties</span></span>
|<span data-ttu-id="01731-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01731-120">Property</span></span>|<span data-ttu-id="01731-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="01731-121">Type</span></span>|<span data-ttu-id="01731-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="01731-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01731-123">id</span><span class="sxs-lookup"><span data-stu-id="01731-123">id</span></span>|<span data-ttu-id="01731-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-124">String</span></span>|<span data-ttu-id="01731-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="01731-125">Key of the entity.</span></span>|
|<span data-ttu-id="01731-126">displayName</span><span class="sxs-lookup"><span data-stu-id="01731-126">displayName</span></span>|<span data-ttu-id="01731-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-127">String</span></span>|<span data-ttu-id="01731-128">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="01731-128">Name of the eBook.</span></span>|
|<span data-ttu-id="01731-129">descripción</span><span class="sxs-lookup"><span data-stu-id="01731-129">description</span></span>|<span data-ttu-id="01731-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-130">String</span></span>|<span data-ttu-id="01731-131">Descripción.</span><span class="sxs-lookup"><span data-stu-id="01731-131">Description.</span></span>|
|<span data-ttu-id="01731-132">publicador</span><span class="sxs-lookup"><span data-stu-id="01731-132">publisher</span></span>|<span data-ttu-id="01731-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-133">String</span></span>|<span data-ttu-id="01731-134">Publicador.</span><span class="sxs-lookup"><span data-stu-id="01731-134">Publisher.</span></span>|
|<span data-ttu-id="01731-135">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="01731-135">publishedDateTime</span></span>|<span data-ttu-id="01731-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01731-136">DateTimeOffset</span></span>|<span data-ttu-id="01731-137">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-137">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="01731-138">largeCover</span><span class="sxs-lookup"><span data-stu-id="01731-138">largeCover</span></span>|[<span data-ttu-id="01731-139">mimeContent</span><span class="sxs-lookup"><span data-stu-id="01731-139">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="01731-140">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="01731-140">Book cover.</span></span>|
|<span data-ttu-id="01731-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="01731-141">createdDateTime</span></span>|<span data-ttu-id="01731-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01731-142">DateTimeOffset</span></span>|<span data-ttu-id="01731-143">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-143">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="01731-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="01731-144">lastModifiedDateTime</span></span>|<span data-ttu-id="01731-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01731-145">DateTimeOffset</span></span>|<span data-ttu-id="01731-146">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-146">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="01731-147">informationUrl</span><span class="sxs-lookup"><span data-stu-id="01731-147">informationUrl</span></span>|<span data-ttu-id="01731-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-148">String</span></span>|<span data-ttu-id="01731-149">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="01731-149">The more information Url.</span></span>|
|<span data-ttu-id="01731-150">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="01731-150">privacyInformationUrl</span></span>|<span data-ttu-id="01731-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="01731-151">String</span></span>|<span data-ttu-id="01731-152">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="01731-152">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="01731-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01731-153">Relationships</span></span>
|<span data-ttu-id="01731-154">Relación</span><span class="sxs-lookup"><span data-stu-id="01731-154">Relationship</span></span>|<span data-ttu-id="01731-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="01731-155">Type</span></span>|<span data-ttu-id="01731-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="01731-156">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01731-157">asignaciones</span><span class="sxs-lookup"><span data-stu-id="01731-157">assignments</span></span>|<span data-ttu-id="01731-158">Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="01731-158">[managedEBookAssignment](../resources/intune-books-managedebookassignment.md) collection</span></span>|<span data-ttu-id="01731-159">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-159">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="01731-160">installSummary</span><span class="sxs-lookup"><span data-stu-id="01731-160">installSummary</span></span>|[<span data-ttu-id="01731-161">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="01731-161">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="01731-162">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="01731-162">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="01731-163">deviceStates</span><span class="sxs-lookup"><span data-stu-id="01731-163">deviceStates</span></span>|<span data-ttu-id="01731-164">Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="01731-164">[deviceInstallState](../resources/intune-books-deviceinstallstate.md) collection</span></span>|<span data-ttu-id="01731-165">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-165">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="01731-166">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="01731-166">userStateSummary</span></span>|<span data-ttu-id="01731-167">Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="01731-167">[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="01731-168">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="01731-168">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="01731-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01731-169">JSON Representation</span></span>
<span data-ttu-id="01731-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="01731-170">Here is a JSON representation of the resource.</span></span>
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



