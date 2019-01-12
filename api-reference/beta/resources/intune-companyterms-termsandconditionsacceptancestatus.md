---
title: Tipo de recurso termsAndConditionsAcceptanceStatus
description: C) de la directiva a un usuario determinado. Los usuarios deben aceptar la versión más actualizada de los términos para conservar el acceso al Portal de empresa.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1c66b7ba799def675ab3b74ad2ea9b8ce2f7ec22
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961081"
---
# <a name="termsandconditionsacceptancestatus-resource-type"></a><span data-ttu-id="671c7-104">Tipo de recurso termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-104">termsAndConditionsAcceptanceStatus resource type</span></span>

> <span data-ttu-id="671c7-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="671c7-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="671c7-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="671c7-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="671c7-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="671c7-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="671c7-108">Una entidad termsAndConditionsAcceptanceStatus representa el estado de aceptación de una directiva de Términos y condiciones (TyC) determinada por un usuario determinado.</span><span class="sxs-lookup"><span data-stu-id="671c7-108">A termsAndConditionsAcceptanceStatus entity represents the acceptance status of a given Terms and Conditions (T&C) policy by a given user.</span></span> <span data-ttu-id="671c7-109">Los usuarios deben aceptar la versión más actualizada de los términos para conservar el acceso al Portal de empresa.</span><span class="sxs-lookup"><span data-stu-id="671c7-109">Users must accept the most up-to-date version of the terms in order to retain access to the Company Portal.</span></span>
## <a name="methods"></a><span data-ttu-id="671c7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="671c7-110">Methods</span></span>
|<span data-ttu-id="671c7-111">Método</span><span class="sxs-lookup"><span data-stu-id="671c7-111">Method</span></span>|<span data-ttu-id="671c7-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="671c7-112">Return Type</span></span>|<span data-ttu-id="671c7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="671c7-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="671c7-114">Enumerar termsAndConditionsAcceptanceStatuses</span><span class="sxs-lookup"><span data-stu-id="671c7-114">List termsAndConditionsAcceptanceStatuses</span></span>](../api/intune-companyterms-termsandconditionsacceptancestatus-list.md)|<span data-ttu-id="671c7-115">Colección [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)</span><span class="sxs-lookup"><span data-stu-id="671c7-115">[termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) collection</span></span>|<span data-ttu-id="671c7-116">Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="671c7-116">List properties and relationships of the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) objects.</span></span>|
|[<span data-ttu-id="671c7-117">Obtener termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-117">Get termsAndConditionsAcceptanceStatus</span></span>](../api/intune-companyterms-termsandconditionsacceptancestatus-get.md)|[<span data-ttu-id="671c7-118">termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-118">termsAndConditionsAcceptanceStatus</span></span>](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|<span data-ttu-id="671c7-119">Lea las propiedades y las relaciones del objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="671c7-119">Read properties and relationships of the [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>|
|[<span data-ttu-id="671c7-120">Crear termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-120">Create termsAndConditionsAcceptanceStatus</span></span>](../api/intune-companyterms-termsandconditionsacceptancestatus-create.md)|[<span data-ttu-id="671c7-121">termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-121">termsAndConditionsAcceptanceStatus</span></span>](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|<span data-ttu-id="671c7-122">Cree un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="671c7-122">Create a new [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>|
|[<span data-ttu-id="671c7-123">Eliminar termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-123">Delete termsAndConditionsAcceptanceStatus</span></span>](../api/intune-companyterms-termsandconditionsacceptancestatus-delete.md)|<span data-ttu-id="671c7-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="671c7-124">None</span></span>|<span data-ttu-id="671c7-125">Elimina un [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="671c7-125">Deletes a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span></span>|
|[<span data-ttu-id="671c7-126">Actualizar termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-126">Update termsAndConditionsAcceptanceStatus</span></span>](../api/intune-companyterms-termsandconditionsacceptancestatus-update.md)|[<span data-ttu-id="671c7-127">termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="671c7-127">termsAndConditionsAcceptanceStatus</span></span>](../resources/intune-companyterms-termsandconditionsacceptancestatus.md)|<span data-ttu-id="671c7-128">Actualice las propiedades de un objeto [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="671c7-128">Update the properties of a [termsAndConditionsAcceptanceStatus](../resources/intune-companyterms-termsandconditionsacceptancestatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="671c7-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="671c7-129">Properties</span></span>
|<span data-ttu-id="671c7-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="671c7-130">Property</span></span>|<span data-ttu-id="671c7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="671c7-131">Type</span></span>|<span data-ttu-id="671c7-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="671c7-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="671c7-133">id</span><span class="sxs-lookup"><span data-stu-id="671c7-133">id</span></span>|<span data-ttu-id="671c7-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="671c7-134">String</span></span>|<span data-ttu-id="671c7-135">Identificador único de la entidad.</span><span class="sxs-lookup"><span data-stu-id="671c7-135">Unique identifier of the entity.</span></span>|
|<span data-ttu-id="671c7-136">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="671c7-136">userDisplayName</span></span>|<span data-ttu-id="671c7-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="671c7-137">String</span></span>|<span data-ttu-id="671c7-138">Nombre para mostrar del usuario cuya aceptación representa la entidad.</span><span class="sxs-lookup"><span data-stu-id="671c7-138">Display name of the user whose acceptance the entity represents.</span></span>|
|<span data-ttu-id="671c7-139">acceptedVersion</span><span class="sxs-lookup"><span data-stu-id="671c7-139">acceptedVersion</span></span>|<span data-ttu-id="671c7-140">Int32</span><span class="sxs-lookup"><span data-stu-id="671c7-140">Int32</span></span>|<span data-ttu-id="671c7-141">Número de versión más reciente de los TyC aceptados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="671c7-141">Most recent version number of the T&C accepted by the user.</span></span>|
|<span data-ttu-id="671c7-142">acceptedDateTime</span><span class="sxs-lookup"><span data-stu-id="671c7-142">acceptedDateTime</span></span>|<span data-ttu-id="671c7-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="671c7-143">DateTimeOffset</span></span>|<span data-ttu-id="671c7-144">Fecha y hora en la que el usuario aceptó los términos por última vez.</span><span class="sxs-lookup"><span data-stu-id="671c7-144">DateTime when the terms were last accepted by the user.</span></span>|

## <a name="relationships"></a><span data-ttu-id="671c7-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="671c7-145">Relationships</span></span>
|<span data-ttu-id="671c7-146">Relación</span><span class="sxs-lookup"><span data-stu-id="671c7-146">Relationship</span></span>|<span data-ttu-id="671c7-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="671c7-147">Type</span></span>|<span data-ttu-id="671c7-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="671c7-148">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="671c7-149">termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="671c7-149">termsAndConditions</span></span>|[<span data-ttu-id="671c7-150">termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="671c7-150">termsAndConditions</span></span>](../resources/intune-companyterms-termsandconditions.md)|<span data-ttu-id="671c7-151">Vínculo de navegación a los términos y condiciones asignados.</span><span class="sxs-lookup"><span data-stu-id="671c7-151">Navigation link to the terms and conditions that are assigned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="671c7-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="671c7-152">JSON Representation</span></span>
<span data-ttu-id="671c7-153">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="671c7-153">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditionsAcceptanceStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
  "id": "String (identifier)",
  "userDisplayName": "String",
  "acceptedVersion": 1024,
  "acceptedDateTime": "String (timestamp)"
}
```





