---
title: tipo de recurso businessFlowTemplate
description: En el anuncio de Azure access revisa la característica, el `businesFlowTemplate` representa una plantilla de flujo de profesionales de Azure AD. El identificador de una plantilla, por ejemplo, para revisar a los miembros de invitado de un grupo, se proporciona el autor de la llamada al crear una revisión de access.
ms.openlocfilehash: 8faf1a1381f5cdcf4bfaab78adc7a6554479b427
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089880"
---
# <a name="businessflowtemplate-resource-type"></a><span data-ttu-id="759c8-104">tipo de recurso businessFlowTemplate</span><span class="sxs-lookup"><span data-stu-id="759c8-104">businessFlowTemplate resource type</span></span>

> <span data-ttu-id="759c8-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="759c8-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="759c8-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="759c8-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="759c8-107">En la característica de [acceso revisa](accessreviews-root.md) Azure AD, el `businesFlowTemplate` representa una plantilla de flujo de profesionales de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="759c8-107">In the Azure AD [access reviews](accessreviews-root.md) feature, the `businesFlowTemplate` represents an Azure AD business flow template.</span></span> <span data-ttu-id="759c8-108">El identificador de una plantilla, por ejemplo, para revisar a los miembros de invitado de un grupo, se proporciona el autor de la llamada al crear una revisión de access.</span><span class="sxs-lookup"><span data-stu-id="759c8-108">The identifier of a template, such as to review guest members of a group, is supplied by the caller when creating an access review.</span></span>

<span data-ttu-id="759c8-109">Los objetos de plantilla de flujo de negocios se generan automáticamente cuando el onboards el inquilino de para usar el acceso de administrador global revisa la característica.</span><span class="sxs-lookup"><span data-stu-id="759c8-109">The business flow template objects are automatically generated when the global administrator onboards the tenant to use the access reviews feature.</span></span>  <span data-ttu-id="759c8-110">No hay plantillas de flujo de negocio adicionales se pueden crear.</span><span class="sxs-lookup"><span data-stu-id="759c8-110">No additional business flow templates can be created.</span></span>


## <a name="methods"></a><span data-ttu-id="759c8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="759c8-111">Methods</span></span>

| <span data-ttu-id="759c8-112">Método</span><span class="sxs-lookup"><span data-stu-id="759c8-112">Method</span></span>           | <span data-ttu-id="759c8-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="759c8-113">Return Type</span></span>    |<span data-ttu-id="759c8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="759c8-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="759c8-115">Lista businessFlowTemplates</span><span class="sxs-lookup"><span data-stu-id="759c8-115">List businessFlowTemplates</span></span>](../api/businessflowtemplate-list.md) | <span data-ttu-id="759c8-116">colección de [businessFlowTemplate](businessflowtemplate.md)</span><span class="sxs-lookup"><span data-stu-id="759c8-116">[businessFlowTemplate](businessflowtemplate.md) collection</span></span>| <span data-ttu-id="759c8-117">Obtener las plantillas de flujo de negocio adecuados tener acceso a las revisiones.</span><span class="sxs-lookup"><span data-stu-id="759c8-117">Get the business flow templates appropriate to access reviews.</span></span>|

## <a name="properties"></a><span data-ttu-id="759c8-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="759c8-118">Properties</span></span>
| <span data-ttu-id="759c8-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="759c8-119">Property</span></span>     | <span data-ttu-id="759c8-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="759c8-120">Type</span></span>   |<span data-ttu-id="759c8-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="759c8-121">Description</span></span>|
|:---------------|:--------|:----------|
| `id`                     |`String`                | <span data-ttu-id="759c8-122">El identificador asignado a la característica de la plantilla de flujo de negocio</span><span class="sxs-lookup"><span data-stu-id="759c8-122">The feature-assigned identifier of the business flow template</span></span>                                      |
| `displayName`            |`String`                | <span data-ttu-id="759c8-123">El nombre de la plantilla de flujo de negocio</span><span class="sxs-lookup"><span data-stu-id="759c8-123">The name of the business flow template</span></span>                                                             |


## <a name="relationships"></a><span data-ttu-id="759c8-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="759c8-124">Relationships</span></span>

<span data-ttu-id="759c8-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="759c8-125">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="759c8-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="759c8-126">See also</span></span>

| <span data-ttu-id="759c8-127">Método</span><span class="sxs-lookup"><span data-stu-id="759c8-127">Method</span></span>           | <span data-ttu-id="759c8-128">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="759c8-128">Return Type</span></span>    |<span data-ttu-id="759c8-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="759c8-129">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="759c8-130">Crear accessReview</span><span class="sxs-lookup"><span data-stu-id="759c8-130">Create accessReview</span></span>](../api/accessreview-create.md) | [<span data-ttu-id="759c8-131">accessReview</span><span class="sxs-lookup"><span data-stu-id="759c8-131">accessReview</span></span>](accessreview.md) |   <span data-ttu-id="759c8-132">Crear un nuevo accessReview.</span><span class="sxs-lookup"><span data-stu-id="759c8-132">Create a new accessReview.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="759c8-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="759c8-133">JSON representation</span></span>

<span data-ttu-id="759c8-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="759c8-134">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.businessFlowTemplate"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "businessFlowTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->