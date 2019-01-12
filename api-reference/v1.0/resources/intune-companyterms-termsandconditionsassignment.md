---
title: Tipo de recurso termsAndConditionsAssignment
description: C) de la directiva a un grupo determinado. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a7fca6763ec7214b2dfd111996e965f9e9c995ec
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979484"
---
# <a name="termsandconditionsassignment-resource-type"></a><span data-ttu-id="12c79-104">Tipo de recurso termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-104">termsAndConditionsAssignment resource type</span></span>

> <span data-ttu-id="12c79-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="12c79-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="12c79-106">Una entidad termsAndConditionsAssignment representa la asignación de una directiva de Términos y condiciones (TyC) determinada para un grupo específico.</span><span class="sxs-lookup"><span data-stu-id="12c79-106">A termsAndConditionsAssignment entity represents the assignment of a given Terms and Conditions (T&C) policy to a given group.</span></span> <span data-ttu-id="12c79-107">Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.</span><span class="sxs-lookup"><span data-stu-id="12c79-107">Users in the group will be required to accept the terms in order to have devices enrolled into Intune.</span></span>
## <a name="methods"></a><span data-ttu-id="12c79-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="12c79-108">Methods</span></span>
|<span data-ttu-id="12c79-109">Método</span><span class="sxs-lookup"><span data-stu-id="12c79-109">Method</span></span>|<span data-ttu-id="12c79-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12c79-110">Return Type</span></span>|<span data-ttu-id="12c79-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="12c79-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="12c79-112">Enumerar termsAndConditionsAssignments</span><span class="sxs-lookup"><span data-stu-id="12c79-112">List termsAndConditionsAssignments</span></span>](../api/intune-companyterms-termsandconditionsassignment-list.md)|<span data-ttu-id="12c79-113">Colección [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-113">[termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) collection</span></span>|<span data-ttu-id="12c79-114">Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="12c79-114">List properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) objects.</span></span>|
|[<span data-ttu-id="12c79-115">Obtener termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-115">Get termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-get.md)|[<span data-ttu-id="12c79-116">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-116">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="12c79-117">Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="12c79-117">Read properties and relationships of the [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|
|[<span data-ttu-id="12c79-118">Crear termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-118">Create termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-create.md)|[<span data-ttu-id="12c79-119">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-119">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="12c79-120">Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="12c79-120">Create a new [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|
|[<span data-ttu-id="12c79-121">Eliminar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-121">Delete termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-delete.md)|<span data-ttu-id="12c79-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="12c79-122">None</span></span>|<span data-ttu-id="12c79-123">Elimina un [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-123">Deletes a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span></span>|
|[<span data-ttu-id="12c79-124">Actualizar termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-124">Update termsAndConditionsAssignment</span></span>](../api/intune-companyterms-termsandconditionsassignment-update.md)|[<span data-ttu-id="12c79-125">termsAndConditionsAssignment</span><span class="sxs-lookup"><span data-stu-id="12c79-125">termsAndConditionsAssignment</span></span>](../resources/intune-companyterms-termsandconditionsassignment.md)|<span data-ttu-id="12c79-126">Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).</span><span class="sxs-lookup"><span data-stu-id="12c79-126">Update the properties of a [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="12c79-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12c79-127">Properties</span></span>
|<span data-ttu-id="12c79-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="12c79-128">Property</span></span>|<span data-ttu-id="12c79-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="12c79-129">Type</span></span>|<span data-ttu-id="12c79-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="12c79-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="12c79-131">id</span><span class="sxs-lookup"><span data-stu-id="12c79-131">id</span></span>|<span data-ttu-id="12c79-132">String</span><span class="sxs-lookup"><span data-stu-id="12c79-132">String</span></span>|<span data-ttu-id="12c79-133">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="12c79-133">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="12c79-134">target</span><span class="sxs-lookup"><span data-stu-id="12c79-134">target</span></span>|[<span data-ttu-id="12c79-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="12c79-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="12c79-136">Destino de asignación al que está asignada la directiva de términos y condiciones.</span><span class="sxs-lookup"><span data-stu-id="12c79-136">Assignment target that the T&C policy is assigned to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="12c79-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="12c79-137">Relationships</span></span>
<span data-ttu-id="12c79-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="12c79-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="12c79-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="12c79-139">JSON Representation</span></span>
<span data-ttu-id="12c79-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="12c79-140">Here is a JSON representation of the resource.</span></span>
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



