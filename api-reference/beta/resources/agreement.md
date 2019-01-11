---
title: tipo de recurso de contrato
description: Representa un condiciones de personalizable del inquilino de uso que se crean y administran con Azure Active Directory (AD Azure). Puede usar los siguientes métodos para crear y administrar la característica de Azure Active Directory condiciones de uso según su situación.
localization_priority: Normal
ms.openlocfilehash: 8c082ed6229b44cc3a3d4cba6dd8645feee5d07c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845349"
---
# <a name="agreement-resource-type"></a><span data-ttu-id="6c7a4-104">tipo de recurso de contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-104">agreement resource type</span></span>

> <span data-ttu-id="6c7a4-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6c7a4-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6c7a4-107">Representa un condiciones de personalizable del inquilino de uso que se crean y administran con Azure Active Directory (AD Azure).</span><span class="sxs-lookup"><span data-stu-id="6c7a4-107">Represents a tenant's customizable terms of use agreement that is created and managed with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="6c7a4-108">Puede usar los siguientes métodos para crear y administrar la [característica de Azure Active Directory condiciones de uso](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-tou) de acuerdo con su escenario.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-108">You can use the following methods to create and manage the [Azure Active Directory Terms of Use feature](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-tou) according to your scenario.</span></span>

## <a name="methods"></a><span data-ttu-id="6c7a4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6c7a4-109">Methods</span></span>

| <span data-ttu-id="6c7a4-110">Método</span><span class="sxs-lookup"><span data-stu-id="6c7a4-110">Method</span></span>       | <span data-ttu-id="6c7a4-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c7a4-111">Return Type</span></span> | <span data-ttu-id="6c7a4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c7a4-112">Description</span></span> |
|:-------------|:------------|:------------|
| [<span data-ttu-id="6c7a4-113">Crear contratos</span><span class="sxs-lookup"><span data-stu-id="6c7a4-113">Create agreements</span></span>](../api/agreement-post-agreements.md) | [<span data-ttu-id="6c7a4-114">contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-114">agreement</span></span>](agreement.md) | <span data-ttu-id="6c7a4-115">Crear un nuevo acuerdo de registro a la colección de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-115">Create a new agreement by posting to the agreement collection.</span></span> |
| [<span data-ttu-id="6c7a4-116">Contratos de lista</span><span class="sxs-lookup"><span data-stu-id="6c7a4-116">List agreements</span></span>](../api/agreement-list.md) | <span data-ttu-id="6c7a4-117">colección de [contrato](agreement.md)</span><span class="sxs-lookup"><span data-stu-id="6c7a4-117">[agreement](agreement.md) collection</span></span> | <span data-ttu-id="6c7a4-118">Obtener una colección de objetos de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-118">Get an agreement object collection.</span></span> |
| [<span data-ttu-id="6c7a4-119">Obtener el contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-119">Get agreement</span></span>](../api/agreement-get.md) | [<span data-ttu-id="6c7a4-120">contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-120">agreement</span></span>](agreement.md) | <span data-ttu-id="6c7a4-121">Leer las propiedades y relaciones de un objeto de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-121">Read properties and relationships of an agreement object.</span></span> |
| [<span data-ttu-id="6c7a4-122">Contrato de actualización</span><span class="sxs-lookup"><span data-stu-id="6c7a4-122">Update agreement</span></span>](../api/agreement-update.md) | [<span data-ttu-id="6c7a4-123">contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-123">agreement</span></span>](agreement.md) | <span data-ttu-id="6c7a4-124">Actualizar un objeto de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-124">Update an agreement object.</span></span> |
| [<span data-ttu-id="6c7a4-125">Eliminar contrato</span><span class="sxs-lookup"><span data-stu-id="6c7a4-125">Delete agreement</span></span>](../api/agreement-delete.md) | <span data-ttu-id="6c7a4-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6c7a4-126">None</span></span> | <span data-ttu-id="6c7a4-127">Eliminación de un objeto de contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-127">Delete an agreement object.</span></span> |
<!--
| [Create agreementFile](../api/agreement-post-files.md) | [agreementFile](agreementfile.md) | Create a new agreementFile by posting to the files collection. |
| [List files](../api/agreement-list-files.md) | [agreementFile](agreementfile.md) collection | Get an agreementFile object collection. |
-->

## <a name="properties"></a><span data-ttu-id="6c7a4-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6c7a4-128">Properties</span></span>
| <span data-ttu-id="6c7a4-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c7a4-129">Property</span></span>     | <span data-ttu-id="6c7a4-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c7a4-130">Type</span></span>        | <span data-ttu-id="6c7a4-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c7a4-131">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6c7a4-132">displayName</span><span class="sxs-lookup"><span data-stu-id="6c7a4-132">displayName</span></span>|<span data-ttu-id="6c7a4-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c7a4-133">String</span></span>|<span data-ttu-id="6c7a4-134">Nombre para mostrar del contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-134">Display name of the agreement.</span></span>|
|<span data-ttu-id="6c7a4-135">id</span><span class="sxs-lookup"><span data-stu-id="6c7a4-135">id</span></span>|<span data-ttu-id="6c7a4-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c7a4-136">String</span></span>| <span data-ttu-id="6c7a4-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-137">Read-only.</span></span>|
|<span data-ttu-id="6c7a4-138">isViewingBeforeAcceptanceRequired</span><span class="sxs-lookup"><span data-stu-id="6c7a4-138">isViewingBeforeAcceptanceRequired</span></span>|<span data-ttu-id="6c7a4-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="6c7a4-139">Boolean</span></span>|<span data-ttu-id="6c7a4-140">Indica si el usuario tiene que expandir y ver el contrato antes de Aceptar.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-140">Indicates whether the user has to expand and view the agreement before accepting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6c7a4-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6c7a4-141">Relationships</span></span>
| <span data-ttu-id="6c7a4-142">Relación</span><span class="sxs-lookup"><span data-stu-id="6c7a4-142">Relationship</span></span> | <span data-ttu-id="6c7a4-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c7a4-143">Type</span></span>        | <span data-ttu-id="6c7a4-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c7a4-144">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6c7a4-145">archivos</span><span class="sxs-lookup"><span data-stu-id="6c7a4-145">files</span></span>|<span data-ttu-id="6c7a4-146">colección de [agreementFile](agreementfile.md)</span><span class="sxs-lookup"><span data-stu-id="6c7a4-146">[agreementFile](agreementfile.md) collection</span></span>|<span data-ttu-id="6c7a4-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-147">Read-only.</span></span> <span data-ttu-id="6c7a4-148">Documentos PDF vinculan a este contrato.</span><span class="sxs-lookup"><span data-stu-id="6c7a4-148">PDFs linked to this agreement.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6c7a4-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6c7a4-149">JSON representation</span></span>

<span data-ttu-id="6c7a4-150">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6c7a4-150">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.agreement"
}-->

```json
{
  "displayName": "String",
  "id": "String (identifier)",
  "isViewingBeforeAcceptanceRequired": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "agreement resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
