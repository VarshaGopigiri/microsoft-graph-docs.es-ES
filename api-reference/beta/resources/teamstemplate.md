---
title: tipo de recurso teamsTemplate
description: Describe la entidad teamsTemplate.
ms.openlocfilehash: 76b2921e884d38a57097789b1ba64df3309d141c
ms.sourcegitcommit: 12c6e82f1417022540e534ebadbd0e8d7fb5abde
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210167"
---
# <a name="teamstemplate-resource-type"></a><span data-ttu-id="dfd4a-103">tipo de recurso teamsTemplate</span><span class="sxs-lookup"><span data-stu-id="dfd4a-103">teamsTemplate resource type</span></span>

> <span data-ttu-id="dfd4a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dfd4a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dfd4a-106">Una plantilla de equipo es un blueprint para la creación de un [equipo](../resources/team.md) en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-106">A team template is a blueprint for creating a [team](../resources/team.md) in Microsoft Teams.</span></span> <span data-ttu-id="dfd4a-107">Una plantilla especifica la estructura, configuración y, incluso un contenido que se debe aprovisionar en un nuevo equipo creado mediante la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-107">A template specifies the structure, settings, and even content that should be provisioned in a new team created using the template.</span></span> <span data-ttu-id="dfd4a-108">Microsoft proporciona un conjunto de plantillas de bases y los clientes pueden guardar sus propias plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-108">Microsoft provides a suite of base templates and customers can save their own custom templates.</span></span>

## <a name="properties"></a><span data-ttu-id="dfd4a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfd4a-109">Properties</span></span>

| <span data-ttu-id="dfd4a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dfd4a-110">Property</span></span>            | <span data-ttu-id="dfd4a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfd4a-111">Type</span></span>     | <span data-ttu-id="dfd4a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfd4a-112">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="dfd4a-113">id</span><span class="sxs-lookup"><span data-stu-id="dfd4a-113">id</span></span>                  | <span data-ttu-id="dfd4a-114">String</span><span class="sxs-lookup"><span data-stu-id="dfd4a-114">String</span></span>   | <span data-ttu-id="dfd4a-115">Identificador único de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-115">Unique identifier of the template.</span></span> <span data-ttu-id="dfd4a-116">No puede ser null.</span><span class="sxs-lookup"><span data-stu-id="dfd4a-116">Cannot be null.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="dfd4a-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dfd4a-117">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTemplate",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string"
}
```

# <a name="see-also"></a><span data-ttu-id="dfd4a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfd4a-118">See also</span></span>

- [<span data-ttu-id="dfd4a-119">equipo</span><span class="sxs-lookup"><span data-stu-id="dfd4a-119">team</span></span>](team.md)

