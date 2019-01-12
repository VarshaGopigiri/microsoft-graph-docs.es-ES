---
title: Tipo de recurso mimeContent
description: Contiene las propiedades de un contenido MIME genérico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ee38eee9100982f6dc5f22315af480a783cc4252
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27962124"
---
# <a name="mimecontent-resource-type"></a><span data-ttu-id="c484a-103">Tipo de recurso mimeContent</span><span class="sxs-lookup"><span data-stu-id="c484a-103">mimeContent resource type</span></span>

> <span data-ttu-id="c484a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c484a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c484a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c484a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c484a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c484a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c484a-107">Contiene las propiedades de un contenido MIME genérico.</span><span class="sxs-lookup"><span data-stu-id="c484a-107">Contains properties for a generic mime content.</span></span>
## <a name="properties"></a><span data-ttu-id="c484a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c484a-108">Properties</span></span>
|<span data-ttu-id="c484a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c484a-109">Property</span></span>|<span data-ttu-id="c484a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c484a-110">Type</span></span>|<span data-ttu-id="c484a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c484a-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c484a-112">type</span><span class="sxs-lookup"><span data-stu-id="c484a-112">type</span></span>|<span data-ttu-id="c484a-113">String</span><span class="sxs-lookup"><span data-stu-id="c484a-113">String</span></span>|<span data-ttu-id="c484a-114">Indica el tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="c484a-114">Indicates the content mime type.</span></span>|
|<span data-ttu-id="c484a-115">valor</span><span class="sxs-lookup"><span data-stu-id="c484a-115">value</span></span>|<span data-ttu-id="c484a-116">Binario</span><span class="sxs-lookup"><span data-stu-id="c484a-116">Binary</span></span>|<span data-ttu-id="c484a-117">Matriz de bytes que contiene el contenido real.</span><span class="sxs-lookup"><span data-stu-id="c484a-117">The byte array that contains the actual content.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c484a-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c484a-118">Relationships</span></span>
<span data-ttu-id="c484a-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c484a-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c484a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c484a-120">JSON Representation</span></span>
<span data-ttu-id="c484a-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c484a-121">Here is a JSON representation of the resource.</span></span>
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





