---
title: tipo de recurso teamsTemplate
description: Describe la entidad teamsTemplate.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 9bd5047950ed1ed3c57950d2c4b708a78b570649
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940088"
---
# <a name="teamstemplate-resource-type"></a><span data-ttu-id="7dab3-103">tipo de recurso teamsTemplate</span><span class="sxs-lookup"><span data-stu-id="7dab3-103">teamsTemplate resource type</span></span>

> <span data-ttu-id="7dab3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7dab3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7dab3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7dab3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7dab3-106">Una plantilla de equipo es un blueprint para la creación de un [equipo](../resources/team.md) en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7dab3-106">A team template is a blueprint for creating a [team](../resources/team.md) in Microsoft Teams.</span></span> <span data-ttu-id="7dab3-107">Una plantilla especifica la estructura, configuración y, incluso un contenido que se debe aprovisionar en un nuevo equipo creado mediante la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7dab3-107">A template specifies the structure, settings, and even content that should be provisioned in a new team created using the template.</span></span> <span data-ttu-id="7dab3-108">Microsoft proporciona un conjunto de plantillas de bases y los clientes pueden guardar sus propias plantillas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7dab3-108">Microsoft provides a suite of base templates and customers can save their own custom templates.</span></span>

## <a name="properties"></a><span data-ttu-id="7dab3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7dab3-109">Properties</span></span>

| <span data-ttu-id="7dab3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7dab3-110">Property</span></span>            | <span data-ttu-id="7dab3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dab3-111">Type</span></span>     | <span data-ttu-id="7dab3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dab3-112">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="7dab3-113">id</span><span class="sxs-lookup"><span data-stu-id="7dab3-113">id</span></span>                  | <span data-ttu-id="7dab3-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="7dab3-114">String</span></span>   | <span data-ttu-id="7dab3-115">Identificador único de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7dab3-115">Unique identifier of the template.</span></span> <span data-ttu-id="7dab3-116">No puede ser null.</span><span class="sxs-lookup"><span data-stu-id="7dab3-116">Cannot be null.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="7dab3-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7dab3-117">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="7dab3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7dab3-118">See also</span></span>

- [<span data-ttu-id="7dab3-119">equipo</span><span class="sxs-lookup"><span data-stu-id="7dab3-119">team</span></span>](team.md)

