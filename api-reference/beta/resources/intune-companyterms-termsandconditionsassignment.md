---
title: Tipo de recurso termsAndConditionsAssignment
description: C) de la directiva a un grupo determinado. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
author: tfitzmac
ms.openlocfilehash: a7b0e9deb391b9431be1ed4f282cb6e5a63ced6e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351054"
---
# <a name="termsandconditionsassignment-resource-type"></a><span data-ttu-id="6c1a3-104">Tipo de recurso termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-104">termsAndConditionsAssignment resource type</span></span>

> <span data-ttu-id="6c1a3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c1a3-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="6c1a3-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c1a3-108">Una entidad termsAndConditionsAssignment representa la asignación de una directiva de Términos y condiciones (TyC) determinada para un grupo específico.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-108">A termsAndConditionsAssignment entity represents the assignment of a given Terms and Conditions (T&C) policy to a given group.</span></span> <span data-ttu-id="6c1a3-109">Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-109">Users in the group will be required to accept the terms in order to have devices enrolled into Intune.</span></span>
## <a name="methods"></a><span data-ttu-id="6c1a3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c1a3-110">Methods</span></span>
|<span data-ttu-id="6c1a3-111">Método</span><span class="sxs-lookup"><span data-stu-id="6c1a3-111">Method</span></span>|<span data-ttu-id="6c1a3-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c1a3-112">Return Type</span></span>|<span data-ttu-id="6c1a3-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c1a3-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="6c1a3-114">Enumerar termsAndConditionsAssignments</span><span class="sxs-lookup"><span data-stu-id="6c1a3-114">List termsAndConditionsAssignments</span></span>](../api/intune-companyterms-termsandconditionsassignment-list.md)|<span data-ttu-id="6c1a3-115">Colección [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)</span><span class="sxs-lookup"><span data-stu-id="6c1a3-115">[termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) collection</span></span>|<span data-ttu-id="6c1a3-116">Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c1a3-116">List properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects.</span></span>|
|[<span data-ttu-id="6c1a3-117">Obtener termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-117">Get termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-get.md)|[<span data-ttu-id="6c1a3-118">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-118">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="6c1a3-119">Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c1a3-119">Read properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|
|[<span data-ttu-id="6c1a3-120">Crear termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-120">Create termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-create.md)|[<span data-ttu-id="6c1a3-121">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-121">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="6c1a3-122">Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c1a3-122">Create a new [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|
|[<span data-ttu-id="6c1a3-123">Eliminar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-123">Delete termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-delete.md)|<span data-ttu-id="6c1a3-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6c1a3-124">None</span></span>|<span data-ttu-id="6c1a3-125">Elimina un [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)</span><span class="sxs-lookup"><span data-stu-id="6c1a3-125">Deletes a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span></span>|
|[<span data-ttu-id="6c1a3-126">Actualizar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-126">Update termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-update.md)|[<span data-ttu-id="6c1a3-127">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="6c1a3-127">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="6c1a3-128">Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6c1a3-128">Update the properties of a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6c1a3-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c1a3-129">Properties</span></span>
|<span data-ttu-id="6c1a3-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c1a3-130">Property</span></span>|<span data-ttu-id="6c1a3-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c1a3-131">Type</span></span>|<span data-ttu-id="6c1a3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c1a3-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6c1a3-133">id</span><span class="sxs-lookup"><span data-stu-id="6c1a3-133">id</span></span>|<span data-ttu-id="6c1a3-134">String</span><span class="sxs-lookup"><span data-stu-id="6c1a3-134">String</span></span>|<span data-ttu-id="6c1a3-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="6c1a3-136">target</span><span class="sxs-lookup"><span data-stu-id="6c1a3-136">target</span></span>|[<span data-ttu-id="6c1a3-137">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="6c1a3-137">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="6c1a3-138">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-138">Assignment target that the T&C policy is assigned to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6c1a3-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6c1a3-139">Relationships</span></span>
<span data-ttu-id="6c1a3-140">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6c1a3-140">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6c1a3-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c1a3-141">JSON Representation</span></span>
<span data-ttu-id="6c1a3-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6c1a3-142">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditionsAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





