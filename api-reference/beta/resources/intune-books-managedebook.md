---
title: Tipo de recurso managedEBook
description: Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 6fd4fd3caef3aab90257805a48e53bee9c6b8764
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962600"
---
# <a name="managedebook-resource-type"></a><span data-ttu-id="285cf-103">Tipo de recurso managedEBook</span><span class="sxs-lookup"><span data-stu-id="285cf-103">managedEBook resource type</span></span>

> <span data-ttu-id="285cf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="285cf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="285cf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="285cf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="285cf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="285cf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="285cf-107">Una clase abstracta que contiene las propiedades base para el libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="285cf-107">An abstract class containing the base properties for Managed eBook.</span></span>
## <a name="methods"></a><span data-ttu-id="285cf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="285cf-108">Methods</span></span>
|<span data-ttu-id="285cf-109">Método</span><span class="sxs-lookup"><span data-stu-id="285cf-109">Method</span></span>|<span data-ttu-id="285cf-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="285cf-110">Return Type</span></span>|<span data-ttu-id="285cf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="285cf-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="285cf-112">Enumerar managedEBooks</span><span class="sxs-lookup"><span data-stu-id="285cf-112">List managedEBooks</span></span>](../api/intune-books-managedebook-list.md)|<span data-ttu-id="285cf-113">Colección [managedEBook](../resources/intune-books-managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="285cf-113">[managedEBook](../resources/intune-books-managedebook.md) collection</span></span>|<span data-ttu-id="285cf-114">Enumere las propiedades y las relaciones de los objetos [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="285cf-114">List properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) objects.</span></span>|
|[<span data-ttu-id="285cf-115">Obtener managedEBook</span><span class="sxs-lookup"><span data-stu-id="285cf-115">Get managedEBook</span></span>](../api/intune-books-managedebook-get.md)|[<span data-ttu-id="285cf-116">managedEBook</span><span class="sxs-lookup"><span data-stu-id="285cf-116">managedEBook</span></span>](../resources/intune-books-managedebook.md)|<span data-ttu-id="285cf-117">Lea las propiedades y las relaciones del objeto [managedEBook](../resources/intune-books-managedebook.md).</span><span class="sxs-lookup"><span data-stu-id="285cf-117">Read properties and relationships of the [managedEBook](../resources/intune-books-managedebook.md) object.</span></span>|
|[<span data-ttu-id="285cf-118">Acción assign</span><span class="sxs-lookup"><span data-stu-id="285cf-118">assign action</span></span>](../api/intune-books-managedebook-assign.md)|<span data-ttu-id="285cf-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="285cf-119">None</span></span>|<span data-ttu-id="285cf-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="285cf-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="285cf-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="285cf-121">Properties</span></span>
|<span data-ttu-id="285cf-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="285cf-122">Property</span></span>|<span data-ttu-id="285cf-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="285cf-123">Type</span></span>|<span data-ttu-id="285cf-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="285cf-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="285cf-125">id</span><span class="sxs-lookup"><span data-stu-id="285cf-125">id</span></span>|<span data-ttu-id="285cf-126">String</span><span class="sxs-lookup"><span data-stu-id="285cf-126">String</span></span>|<span data-ttu-id="285cf-127">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="285cf-127">Key of the entity.</span></span>|
|<span data-ttu-id="285cf-128">displayName</span><span class="sxs-lookup"><span data-stu-id="285cf-128">displayName</span></span>|<span data-ttu-id="285cf-129">String</span><span class="sxs-lookup"><span data-stu-id="285cf-129">String</span></span>|<span data-ttu-id="285cf-130">Nombre del libro electrónico</span><span class="sxs-lookup"><span data-stu-id="285cf-130">Name of the eBook.</span></span>|
|<span data-ttu-id="285cf-131">descripción</span><span class="sxs-lookup"><span data-stu-id="285cf-131">description</span></span>|<span data-ttu-id="285cf-132">String</span><span class="sxs-lookup"><span data-stu-id="285cf-132">String</span></span>|<span data-ttu-id="285cf-133">Descripción.</span><span class="sxs-lookup"><span data-stu-id="285cf-133">Description.</span></span>|
|<span data-ttu-id="285cf-134">publicador</span><span class="sxs-lookup"><span data-stu-id="285cf-134">publisher</span></span>|<span data-ttu-id="285cf-135">String</span><span class="sxs-lookup"><span data-stu-id="285cf-135">String</span></span>|<span data-ttu-id="285cf-136">Publicador.</span><span class="sxs-lookup"><span data-stu-id="285cf-136">Publisher.</span></span>|
|<span data-ttu-id="285cf-137">publishedDateTime</span><span class="sxs-lookup"><span data-stu-id="285cf-137">publishedDateTime</span></span>|<span data-ttu-id="285cf-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="285cf-138">DateTimeOffset</span></span>|<span data-ttu-id="285cf-139">La fecha y la hora en que se publicó el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-139">The date and time when the eBook was published.</span></span>|
|<span data-ttu-id="285cf-140">largeCover</span><span class="sxs-lookup"><span data-stu-id="285cf-140">largeCover</span></span>|[<span data-ttu-id="285cf-141">mimeContent</span><span class="sxs-lookup"><span data-stu-id="285cf-141">mimeContent</span></span>](../resources/intune-shared-mimecontent.md)|<span data-ttu-id="285cf-142">Cubierta de libro.</span><span class="sxs-lookup"><span data-stu-id="285cf-142">Book cover.</span></span>|
|<span data-ttu-id="285cf-143">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="285cf-143">createdDateTime</span></span>|<span data-ttu-id="285cf-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="285cf-144">DateTimeOffset</span></span>|<span data-ttu-id="285cf-145">La fecha y la hora en que se creó el archivo del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-145">The date and time when the eBook file was created.</span></span>|
|<span data-ttu-id="285cf-146">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="285cf-146">lastModifiedDateTime</span></span>|<span data-ttu-id="285cf-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="285cf-147">DateTimeOffset</span></span>|<span data-ttu-id="285cf-148">La fecha y la hora en que se modificó por última vez el libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-148">The date and time when the eBook was last modified.</span></span>|
|<span data-ttu-id="285cf-149">informationUrl</span><span class="sxs-lookup"><span data-stu-id="285cf-149">informationUrl</span></span>|<span data-ttu-id="285cf-150">String</span><span class="sxs-lookup"><span data-stu-id="285cf-150">String</span></span>|<span data-ttu-id="285cf-151">La dirección URL para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="285cf-151">The more information Url.</span></span>|
|<span data-ttu-id="285cf-152">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="285cf-152">privacyInformationUrl</span></span>|<span data-ttu-id="285cf-153">String</span><span class="sxs-lookup"><span data-stu-id="285cf-153">String</span></span>|<span data-ttu-id="285cf-154">La dirección URL de la declaración de privacidad.</span><span class="sxs-lookup"><span data-stu-id="285cf-154">The privacy statement Url.</span></span>|

## <a name="relationships"></a><span data-ttu-id="285cf-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="285cf-155">Relationships</span></span>
|<span data-ttu-id="285cf-156">Relación</span><span class="sxs-lookup"><span data-stu-id="285cf-156">Relationship</span></span>|<span data-ttu-id="285cf-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="285cf-157">Type</span></span>|<span data-ttu-id="285cf-158">Descripción</span><span class="sxs-lookup"><span data-stu-id="285cf-158">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="285cf-159">categories</span><span class="sxs-lookup"><span data-stu-id="285cf-159">categories</span></span>|<span data-ttu-id="285cf-160">colección de [managedEBookCategory](../resources/intune-books-managedebookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="285cf-160">[managedEBookCategory](../resources/intune-books-managedebookcategory.md) collection</span></span>|<span data-ttu-id="285cf-161">La lista de categorías para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-161">The list of categories for this eBook.</span></span>|
|<span data-ttu-id="285cf-162">asignaciones</span><span class="sxs-lookup"><span data-stu-id="285cf-162">assignments</span></span>|<span data-ttu-id="285cf-163">Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)</span><span class="sxs-lookup"><span data-stu-id="285cf-163">[managedEBookAssignment](../resources/intune-books-managedebookassignment.md) collection</span></span>|<span data-ttu-id="285cf-164">La lista de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-164">The list of assignments for this eBook.</span></span>|
|<span data-ttu-id="285cf-165">installSummary</span><span class="sxs-lookup"><span data-stu-id="285cf-165">installSummary</span></span>|[<span data-ttu-id="285cf-166">eBookInstallSummary</span><span class="sxs-lookup"><span data-stu-id="285cf-166">eBookInstallSummary</span></span>](../resources/intune-books-ebookinstallsummary.md)|<span data-ttu-id="285cf-167">Resumen de instalación de las aplicaciones para móviles.</span><span class="sxs-lookup"><span data-stu-id="285cf-167">Mobile App Install Summary.</span></span>|
|<span data-ttu-id="285cf-168">deviceStates</span><span class="sxs-lookup"><span data-stu-id="285cf-168">deviceStates</span></span>|<span data-ttu-id="285cf-169">Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="285cf-169">[deviceInstallState](../resources/intune-books-deviceinstallstate.md) collection</span></span>|<span data-ttu-id="285cf-170">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-170">The list of installation states for this eBook.</span></span>|
|<span data-ttu-id="285cf-171">userStateSummary</span><span class="sxs-lookup"><span data-stu-id="285cf-171">userStateSummary</span></span>|<span data-ttu-id="285cf-172">Colección [userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md)</span><span class="sxs-lookup"><span data-stu-id="285cf-172">[userInstallStateSummary](../resources/intune-books-userinstallstatesummary.md) collection</span></span>|<span data-ttu-id="285cf-173">La lista de estados de asignaciones para este libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="285cf-173">The list of installation states for this eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="285cf-174">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="285cf-174">JSON Representation</span></span>
<span data-ttu-id="285cf-175">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="285cf-175">Here is a JSON representation of the resource.</span></span>
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





