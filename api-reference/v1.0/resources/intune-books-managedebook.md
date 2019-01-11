---
title: Tipo de recurso managedEBook
description: Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 61a4098850f9b3b4a6b82f2fcee5d1ce89b0696d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830257"
---
# <a name="managedebook-resource-type"></a><span data-ttu-id="559a4-103">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="559a4-103">managedEBook resource type</span></span>

> <span data-ttu-id="559a4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="559a4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="559a4-105">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="559a4-105">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="559a4-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="559a4-106">Methods</span></span>
|<span data-ttu-id="559a4-107">Método</span><span class="sxs-lookup"><span data-stu-id="559a4-107">Method</span></span>|<span data-ttu-id="559a4-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="559a4-108">Return Type</span></span>|<span data-ttu-id="559a4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="559a4-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="559a4-110">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="559a4-110">List managedEBooks</span></span>](../api/intune-books-managedebook-list.md)|<span data-ttu-id="559a4-111">Colección [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="559a4-111">[managedEBook](../resources/intune-books-managedebook.md) collection</span></span>|<span data-ttu-id="559a4-112">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="559a4-112">List properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) objects.</span></span>|
|[<span data-ttu-id="559a4-113">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="559a4-113">Get managedEBook</span></span>](../api/intune-books-managedebook-get.md)|[<span data-ttu-id="559a4-114">managedEBook</span><span class="sxs-lookup"><span data-stu-id="559a4-114">managedEBook</span></span>](../resources/intune-books-managedebook.md)|<span data-ttu-id="559a4-115">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="559a4-115">Read properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) object.</span></span>|
|[<span data-ttu-id="559a4-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="559a4-116">assign action</span></span>](../api/intune-books-managedebook-assign.md)|<span data-ttu-id="559a4-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="559a4-117">None</span></span>|<span data-ttu-id="559a4-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="559a4-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="559a4-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="559a4-119">Properties</span></span>
|<span data-ttu-id="559a4-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="559a4-120">Property</span></span>|<span data-ttu-id="559a4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="559a4-121">Type</span></span>|<span data-ttu-id="559a4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="559a4-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="559a4-123">id</span><span class="sxs-lookup"><span data-stu-id="559a4-123">id</span></span>|<span data-ttu-id="559a4-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-124">String</span></span>|<span data-ttu-id="559a4-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="559a4-125">Key of the entity.</span></span>|
|<span data-ttu-id="559a4-126">displayName</span><span class="sxs-lookup"><span data-stu-id="559a4-126">displayName</span></span>|<span data-ttu-id="559a4-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-127">String</span></span>|<span data-ttu-id="559a4-128">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="559a4-128">Name of the eBook.</span></span>|
|<span data-ttu-id="559a4-129">descripción</span><span class="sxs-lookup"><span data-stu-id="559a4-129">description</span></span>|<span data-ttu-id="559a4-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-130">String</span></span>|<span data-ttu-id="559a4-131">Descripción.</span><span class="sxs-lookup"><span data-stu-id="559a4-131">Description.</span></span>|
|<span data-ttu-id="559a4-132">publicador</span><span class="sxs-lookup"><span data-stu-id="559a4-132">publisher</span></span>|<span data-ttu-id="559a4-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-133">String</span></span>|<span data-ttu-id="559a4-134">Publicador.</span><span class="sxs-lookup"><span data-stu-id="559a4-134">Publisher.</span></span>|
|<span data-ttu-id="559a4-135">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="559a4-135">publishedDateTime</span></span>|<span data-ttu-id="559a4-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="559a4-136">DateTimeOffset</span></span>|<span data-ttu-id="559a4-137">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-137">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="559a4-138">largeCover</span><span class="sxs-lookup"><span data-stu-id="559a4-138">largeCover</span></span>|[<span data-ttu-id="559a4-139">mimeContent</span><span class="sxs-lookup"><span data-stu-id="559a4-139">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="559a4-140">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="559a4-140">Book cover.</span></span>|
|<span data-ttu-id="559a4-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="559a4-141">createdDateTime</span></span>|<span data-ttu-id="559a4-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="559a4-142">DateTimeOffset</span></span>|<span data-ttu-id="559a4-143">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-143">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="559a4-144">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="559a4-144">lastModifiedDateTime</span></span>|<span data-ttu-id="559a4-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="559a4-145">DateTimeOffset</span></span>|<span data-ttu-id="559a4-146">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-146">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="559a4-147">informationUrl</span><span class="sxs-lookup"><span data-stu-id="559a4-147">informationUrl</span></span>|<span data-ttu-id="559a4-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-148">String</span></span>|<span data-ttu-id="559a4-149">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="559a4-149">The more information Url.</span></span>|
|<span data-ttu-id="559a4-150">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="559a4-150">privacyInformationUrl</span></span>|<span data-ttu-id="559a4-151">Cadena</span><span class="sxs-lookup"><span data-stu-id="559a4-151">String</span></span>|<span data-ttu-id="559a4-152">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="559a4-152">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="559a4-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="559a4-153">Relationships</span></span>
|<span data-ttu-id="559a4-154">Relación</span><span class="sxs-lookup"><span data-stu-id="559a4-154">Relationship</span></span>|<span data-ttu-id="559a4-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="559a4-155">Type</span></span>|<span data-ttu-id="559a4-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="559a4-156">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="559a4-157">asignaciones</span><span class="sxs-lookup"><span data-stu-id="559a4-157">assignments</span></span>|<span data-ttu-id="559a4-158">Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="559a4-158">[managedEBookAssignment](../resources/intune-books-managedebookassignment.md) collection</span></span>|<span data-ttu-id="559a4-159">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-159">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="559a4-160">installSummary</span><span class="sxs-lookup"><span data-stu-id="559a4-160">installSummary</span></span>|[<span data-ttu-id="559a4-161">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="559a4-161">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="559a4-162">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="559a4-162">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="559a4-163">deviceStates</span><span class="sxs-lookup"><span data-stu-id="559a4-163">deviceStates</span></span>|<span data-ttu-id="559a4-164">Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="559a4-164">[deviceInstallState](../resources/intune-books-deviceinstallstate.md) collection</span></span>|<span data-ttu-id="559a4-165">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-165">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="559a4-166">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="559a4-166">userStateSummary</span></span>|<span data-ttu-id="559a4-167">Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="559a4-167">[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="559a4-168">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="559a4-168">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="559a4-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="559a4-169">JSON Representation</span></span>
<span data-ttu-id="559a4-170">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="559a4-170">Here is a JSON representation of the resource.</span></span>
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



