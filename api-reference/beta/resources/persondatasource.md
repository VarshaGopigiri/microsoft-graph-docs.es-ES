---
title: tipo de recurso personDataSource
description: Representa los orígenes de que los datos de usuario proceden de, como Active Directory y los contactos de Outlook.
localization_priority: Normal
author: simonhult
ms.prod: insights
ms.openlocfilehash: 540ffa81b20b40f9df2694ba634777250742daaf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978504"
---
# <a name="persondatasource-resource-type"></a><span data-ttu-id="1684f-103">tipo de recurso personDataSource</span><span class="sxs-lookup"><span data-stu-id="1684f-103">personDataSource resource type</span></span>

> <span data-ttu-id="1684f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1684f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1684f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1684f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1684f-106">Representa los orígenes de que los datos de usuario proceden de, como Active Directory y los contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="1684f-106">Represents the sources the user data comes from, such as Directory and Outlook Contacts.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1684f-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1684f-107">JSON representation</span></span>

<span data-ttu-id="1684f-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1684f-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.personDataSource"
}-->

```json
{
  "type": "string"
}

```
## <a name="properties"></a><span data-ttu-id="1684f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1684f-109">Properties</span></span>
| <span data-ttu-id="1684f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1684f-110">Property</span></span>     | <span data-ttu-id="1684f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1684f-111">Type</span></span>   |<span data-ttu-id="1684f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1684f-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1684f-113">type</span><span class="sxs-lookup"><span data-stu-id="1684f-113">type</span></span>|<span data-ttu-id="1684f-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="1684f-114">String</span></span>|<span data-ttu-id="1684f-115">El tipo de origen de datos.</span><span class="sxs-lookup"><span data-stu-id="1684f-115">The type of data source.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personDataSource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
