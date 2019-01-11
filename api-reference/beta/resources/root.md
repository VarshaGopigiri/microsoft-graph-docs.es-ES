---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Raíz
localization_priority: Normal
ms.openlocfilehash: 017a4571288839d8d92f182a3a1a44023c4737e2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27866139"
---
# <a name="root-resource-type"></a><span data-ttu-id="30466-102">Tipo de recurso Root</span><span class="sxs-lookup"><span data-stu-id="30466-102">Root resource type</span></span>

> <span data-ttu-id="30466-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30466-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30466-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30466-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="30466-105">La faceta **Root** indica que un objeto es el primero de su jerarquía.</span><span class="sxs-lookup"><span data-stu-id="30466-105">The **Root** facet indicates that an object is the top-most one in its hierarchy.</span></span>
<span data-ttu-id="30466-106">La presencia (valor no NULL) del valor de la faceta indica que el objeto es la raíz.</span><span class="sxs-lookup"><span data-stu-id="30466-106">The presence (non-null) of the facet value indicates that the object is the root.</span></span>
<span data-ttu-id="30466-107">Un valor NULL (o ausente) indica que el objeto no es la raíz.</span><span class="sxs-lookup"><span data-stu-id="30466-107">A null (or missing) value indicates the object is not the root.</span></span>

<span data-ttu-id="30466-108">**Nota**: Aunque actualmente esta faceta está vacía, en futuras revisiones de la API, la faceta puede rellenarse con propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="30466-108">**Note**: While this facet is empty today, in future API revisions the facet may be populated with additional properties.</span></span>

## <a name="json-representation"></a><span data-ttu-id="30466-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="30466-109">JSON representation</span></span>

<!-- { "blockType": "resource", "@type": "microsoft.graph.root" } -->

```json
{
}
```

## <a name="properties"></a><span data-ttu-id="30466-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30466-110">Properties</span></span>

<span data-ttu-id="30466-111">El recurso **Root** no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="30466-111">The **Root** resource has no properties.</span></span>


<!-- {
  "type": "#page.annotation",
  "section": "documentation",
  "tocPath": "Facets/Root"
} -->
