---
title: tipo de recurso educationFileResource
description: Una subclase de educationResource que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 96c03dc1571e0f8686116f169706aa35003f92a3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953661"
---
# <a name="educationfileresource-resource-type"></a><span data-ttu-id="602b1-105">tipo de recurso educationFileResource</span><span class="sxs-lookup"><span data-stu-id="602b1-105">educationFileResource resource type</span></span>

> <span data-ttu-id="602b1-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="602b1-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="602b1-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="602b1-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="602b1-108">Una subclase de [educationResource](educationresource.md) que representa un objeto de archivo que está asociado con la asignación o el envío.</span><span class="sxs-lookup"><span data-stu-id="602b1-108">A subclass of [educationResource](educationresource.md) that represents a file object that is associated with the assignment or submission.</span></span>  <span data-ttu-id="602b1-109">En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema.</span><span class="sxs-lookup"><span data-stu-id="602b1-109">In this case, the file is not one of the special files (Word, Excel, and so on) but is a file that does not have special handling within the system.</span></span> <span data-ttu-id="602b1-110">El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.</span><span class="sxs-lookup"><span data-stu-id="602b1-110">The file resource must be stored in the **resourceFolder** that is associated with the assignment or submission this resource is attached to.</span></span>

## <a name="properties"></a><span data-ttu-id="602b1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="602b1-111">Properties</span></span>
| <span data-ttu-id="602b1-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="602b1-112">Property</span></span>     | <span data-ttu-id="602b1-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="602b1-113">Type</span></span>   |<span data-ttu-id="602b1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="602b1-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="602b1-115">fileUrl</span><span class="sxs-lookup"><span data-stu-id="602b1-115">fileUrl</span></span>|<span data-ttu-id="602b1-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="602b1-116">String</span></span>|<span data-ttu-id="602b1-117">Ubicación en el disco del recurso de archivo.</span><span class="sxs-lookup"><span data-stu-id="602b1-117">Location on disk of the file resource.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="602b1-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="602b1-118">JSON representation</span></span>

<span data-ttu-id="602b1-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="602b1-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFileResource"
}-->

```json
{
  "fileUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationFileResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
