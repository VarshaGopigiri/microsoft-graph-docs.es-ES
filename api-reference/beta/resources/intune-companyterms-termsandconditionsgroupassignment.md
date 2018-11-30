---
title: tipo de recurso termsAndConditionsGroupAssignment
description: C) de la directiva a un grupo determinado. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
ms.openlocfilehash: 071cd73ba36aaab74c7f5c36522c03014711286e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088751"
---
# <a name="termsandconditionsgroupassignment-resource-type"></a><span data-ttu-id="31fd6-104">tipo de recurso termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-104">termsAndConditionsGroupAssignment resource type</span></span>

> <span data-ttu-id="31fd6-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="31fd6-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="31fd6-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="31fd6-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="31fd6-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="31fd6-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="31fd6-108">Una entidad termsAndConditionsGroupAssignment representa la asignación de una determinada términos y condiciones (T & C) Directiva a un grupo determinado.</span><span class="sxs-lookup"><span data-stu-id="31fd6-108">A termsAndConditionsGroupAssignment entity represents the assignment of a given Terms and Conditions (T&C) policy to a given group.</span></span> <span data-ttu-id="31fd6-109">Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.</span><span class="sxs-lookup"><span data-stu-id="31fd6-109">Users in the group will be required to accept the terms in order to have devices enrolled into Intune.</span></span>
## <a name="methods"></a><span data-ttu-id="31fd6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="31fd6-110">Methods</span></span>
|<span data-ttu-id="31fd6-111">Método</span><span class="sxs-lookup"><span data-stu-id="31fd6-111">Method</span></span>|<span data-ttu-id="31fd6-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31fd6-112">Return Type</span></span>|<span data-ttu-id="31fd6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="31fd6-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="31fd6-114">Lista termsAndConditionsGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="31fd6-114">List termsAndConditionsGroupAssignments</span></span>](../api/intune-companyterms-termsandconditionsgroupassignment-list.md)|<span data-ttu-id="31fd6-115">colección de [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="31fd6-115">[termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) collection</span></span>|<span data-ttu-id="31fd6-116">Propiedades de la lista y relaciones de los objetos [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd6-116">List properties and relationships of the [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) objects.</span></span>|
|[<span data-ttu-id="31fd6-117">Obtener termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-117">Get termsAndConditionsGroupAssignment</span></span>](../api/intune-companyterms-termsandconditionsgroupassignment-get.md)|[<span data-ttu-id="31fd6-118">termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-118">termsAndConditionsGroupAssignment</span></span>](../resources/intune-companyterms-termsandconditionsgroupassignment.md)|<span data-ttu-id="31fd6-119">Leer las propiedades y las relaciones del objeto [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd6-119">Read properties and relationships of the [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object.</span></span>|
|[<span data-ttu-id="31fd6-120">Crear termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-120">Create termsAndConditionsGroupAssignment</span></span>](../api/intune-companyterms-termsandconditionsgroupassignment-create.md)|[<span data-ttu-id="31fd6-121">termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-121">termsAndConditionsGroupAssignment</span></span>](../resources/intune-companyterms-termsandconditionsgroupassignment.md)|<span data-ttu-id="31fd6-122">Crear un nuevo objeto [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd6-122">Create a new [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object.</span></span>|
|[<span data-ttu-id="31fd6-123">Eliminar termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-123">Delete termsAndConditionsGroupAssignment</span></span>](../api/intune-companyterms-termsandconditionsgroupassignment-delete.md)|<span data-ttu-id="31fd6-124">Ninguno</span><span class="sxs-lookup"><span data-stu-id="31fd6-124">None</span></span>|<span data-ttu-id="31fd6-125">Elimina un [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="31fd6-125">Deletes a [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md).</span></span>|
|[<span data-ttu-id="31fd6-126">Actualizar termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-126">Update termsAndConditionsGroupAssignment</span></span>](../api/intune-companyterms-termsandconditionsgroupassignment-update.md)|[<span data-ttu-id="31fd6-127">termsAndConditionsGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="31fd6-127">termsAndConditionsGroupAssignment</span></span>](../resources/intune-companyterms-termsandconditionsgroupassignment.md)|<span data-ttu-id="31fd6-128">Actualizar las propiedades de un objeto [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="31fd6-128">Update the properties of a [termsAndConditionsGroupAssignment](../resources/intune-companyterms-termsandconditionsgroupassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="31fd6-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31fd6-129">Properties</span></span>
|<span data-ttu-id="31fd6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31fd6-130">Property</span></span>|<span data-ttu-id="31fd6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="31fd6-131">Type</span></span>|<span data-ttu-id="31fd6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="31fd6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31fd6-133">id</span><span class="sxs-lookup"><span data-stu-id="31fd6-133">id</span></span>|<span data-ttu-id="31fd6-134">String</span><span class="sxs-lookup"><span data-stu-id="31fd6-134">String</span></span>|<span data-ttu-id="31fd6-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="31fd6-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="31fd6-136">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="31fd6-136">targetGroupId</span></span>|<span data-ttu-id="31fd6-137">String</span><span class="sxs-lookup"><span data-stu-id="31fd6-137">String</span></span>|<span data-ttu-id="31fd6-138">Identificador único de un grupo que se asigna la directiva T & C a.</span><span class="sxs-lookup"><span data-stu-id="31fd6-138">Unique identifier of a group that the T&C policy is assigned to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="31fd6-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="31fd6-139">Relationships</span></span>
|<span data-ttu-id="31fd6-140">Relación</span><span class="sxs-lookup"><span data-stu-id="31fd6-140">Relationship</span></span>|<span data-ttu-id="31fd6-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="31fd6-141">Type</span></span>|<span data-ttu-id="31fd6-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="31fd6-142">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="31fd6-143">termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="31fd6-143">termsAndConditions</span></span>|[<span data-ttu-id="31fd6-144">termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="31fd6-144">termsAndConditions</span></span>](../resources/intune-companyterms-termsandconditions.md)|<span data-ttu-id="31fd6-145">Vínculo de navegación a los términos y condiciones asignados.</span><span class="sxs-lookup"><span data-stu-id="31fd6-145">Navigation link to the terms and conditions that are assigned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="31fd6-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="31fd6-146">JSON Representation</span></span>
<span data-ttu-id="31fd6-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="31fd6-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditionsGroupAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsGroupAssignment",
  "id": "String (identifier)",
  "targetGroupId": "String"
}
```




