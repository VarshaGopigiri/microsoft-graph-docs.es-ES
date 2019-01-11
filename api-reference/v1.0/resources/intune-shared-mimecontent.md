---
title: Tipo de recurso mimeContent
description: Contiene las propiedades de un contenido MIME genérico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a0b63289b3d7666eb27de7e6dc4e643dd9fa4772
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857046"
---
# <a name="mimecontent-resource-type"></a><span data-ttu-id="2524f-103">Tipo de recurso mimeContent</span><span class="sxs-lookup"><span data-stu-id="2524f-103">mimeContent resource type</span></span>

> <span data-ttu-id="2524f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2524f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2524f-105">Contiene las propiedades de un contenido MIME genérico.</span><span class="sxs-lookup"><span data-stu-id="2524f-105">Contains properties for a generic mime content.</span></span>
## <a name="properties"></a><span data-ttu-id="2524f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2524f-106">Properties</span></span>
|<span data-ttu-id="2524f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2524f-107">Property</span></span>|<span data-ttu-id="2524f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2524f-108">Type</span></span>|<span data-ttu-id="2524f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2524f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2524f-110">type</span><span class="sxs-lookup"><span data-stu-id="2524f-110">type</span></span>|<span data-ttu-id="2524f-111">String</span><span class="sxs-lookup"><span data-stu-id="2524f-111">String</span></span>|<span data-ttu-id="2524f-112">Indica el tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="2524f-112">Indicates the content mime type.</span></span>|
|<span data-ttu-id="2524f-113">valor</span><span class="sxs-lookup"><span data-stu-id="2524f-113">value</span></span>|<span data-ttu-id="2524f-114">Binario</span><span class="sxs-lookup"><span data-stu-id="2524f-114">Binary</span></span>|<span data-ttu-id="2524f-115">Matriz de bytes que contiene el contenido real.</span><span class="sxs-lookup"><span data-stu-id="2524f-115">The byte array that contains the actual content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2524f-116">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2524f-116">Relationships</span></span>
<span data-ttu-id="2524f-117">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2524f-117">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2524f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2524f-118">JSON Representation</span></span>
<span data-ttu-id="2524f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2524f-119">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mimeContent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mimeContent",
  "type": "String",
  "value": "binary"
}
```



