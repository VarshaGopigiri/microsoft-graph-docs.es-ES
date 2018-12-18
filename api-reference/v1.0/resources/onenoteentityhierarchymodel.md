---
title: recursos de onenoteEntityHierarchyModel
description: Éste es un tipo base para las entidades de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: a142e9206aefbb118f21b2f1a85d00cbc4a3a315
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27362023"
---
# <a name="onenoteentityhierarchymodel-resource"></a><span data-ttu-id="32f16-103">recursos de onenoteEntityHierarchyModel</span><span class="sxs-lookup"><span data-stu-id="32f16-103">onenoteEntityHierarchyModel resource</span></span>

<span data-ttu-id="32f16-104">Éste es un tipo base para las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="32f16-104">This is a base type for OneNote entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="32f16-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32f16-105">JSON representation</span></span>

<span data-ttu-id="32f16-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="32f16-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntityHierarchyModel"
}-->

```json
{
  "displayName": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="32f16-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32f16-107">Properties</span></span>
## <a name="properties"></a><span data-ttu-id="32f16-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32f16-108">Properties</span></span>
| <span data-ttu-id="32f16-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32f16-109">Property</span></span>     | <span data-ttu-id="32f16-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="32f16-110">Type</span></span>   |<span data-ttu-id="32f16-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="32f16-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="32f16-112">displayName</span><span class="sxs-lookup"><span data-stu-id="32f16-112">displayName</span></span>|<span data-ttu-id="32f16-113">String</span><span class="sxs-lookup"><span data-stu-id="32f16-113">String</span></span>|<span data-ttu-id="32f16-114">El nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="32f16-114">The name of the notebook.</span></span>|
|<span data-ttu-id="32f16-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="32f16-115">createdBy</span></span>|[<span data-ttu-id="32f16-116">identitySet</span><span class="sxs-lookup"><span data-stu-id="32f16-116">identitySet</span></span>](identityset.md)|<span data-ttu-id="32f16-p101">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32f16-p101">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="32f16-119">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="32f16-119">lastModifiedBy</span></span>|[<span data-ttu-id="32f16-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="32f16-120">identitySet</span></span>](identityset.md)|<span data-ttu-id="32f16-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32f16-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="32f16-123">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="32f16-123">lastModifiedDateTime</span></span>|<span data-ttu-id="32f16-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="32f16-124">DateTimeOffset</span></span>|<span data-ttu-id="32f16-p103">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="32f16-p103">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|

<!-- uuid: 8b1af557-1a7c-4432-86eb-94989c2d4b54
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->