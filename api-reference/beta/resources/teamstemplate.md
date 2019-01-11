---
title: tipo de recurso teamsTemplate
description: Describe la entidad teamsTemplate.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 6e847c7ef0b13dd9c4281c17939164128be8b6a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818875"
---
# <a name="teamstemplate-resource-type"></a><span data-ttu-id="08bff-103">tipo de recurso teamsTemplate</span><span class="sxs-lookup"><span data-stu-id="08bff-103">teamsTemplate resource type</span></span>

> <span data-ttu-id="08bff-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="08bff-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="08bff-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="08bff-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="08bff-106">Una plantilla de equipo es un blueprint para la creación de un [equipo](../resources/team.md) en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="08bff-106">A team template is a blueprint for creating a [team](../resources/team.md) in Microsoft Teams.</span></span> <span data-ttu-id="08bff-107">Una plantilla especifica la estructura, configuración y, incluso un contenido que se debe aprovisionar en un nuevo equipo creado mediante la plantilla.</span><span class="sxs-lookup"><span data-stu-id="08bff-107">A template specifies the structure, settings, and even content that should be provisioned in a new team created using the template.</span></span> <span data-ttu-id="08bff-108">Microsoft proporciona un conjunto de plantillas de bases y los clientes pueden guardar sus propias plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="08bff-108">Microsoft provides a suite of base templates and customers can save their own custom templates.</span></span>

## <a name="properties"></a><span data-ttu-id="08bff-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08bff-109">Properties</span></span>

| <span data-ttu-id="08bff-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="08bff-110">Property</span></span>            | <span data-ttu-id="08bff-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="08bff-111">Type</span></span>     | <span data-ttu-id="08bff-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="08bff-112">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="08bff-113">id</span><span class="sxs-lookup"><span data-stu-id="08bff-113">id</span></span>                  | <span data-ttu-id="08bff-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="08bff-114">String</span></span>   | <span data-ttu-id="08bff-115">Identificador único de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="08bff-115">Unique identifier of the template.</span></span> <span data-ttu-id="08bff-116">No puede ser null.</span><span class="sxs-lookup"><span data-stu-id="08bff-116">Cannot be null.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="08bff-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="08bff-117">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="08bff-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="08bff-118">See also</span></span>

- [<span data-ttu-id="08bff-119">equipo</span><span class="sxs-lookup"><span data-stu-id="08bff-119">team</span></span>](team.md)

