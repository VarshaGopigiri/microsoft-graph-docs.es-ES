---
title: tipo de recurso resultInfo
description: El tipo de resultInfo.
ms.openlocfilehash: 93dc08407608a87cbc1cfa027f5c8f20483834e6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085233"
---
# <a name="resultinfo-resource-type"></a><span data-ttu-id="9deb2-103">tipo de recurso resultInfo</span><span class="sxs-lookup"><span data-stu-id="9deb2-103">resultInfo resource type</span></span>

> <span data-ttu-id="9deb2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9deb2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9deb2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9deb2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9deb2-106">El tipo de resultInfo.</span><span class="sxs-lookup"><span data-stu-id="9deb2-106">The resultInfo type.</span></span>

## <a name="properties"></a><span data-ttu-id="9deb2-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9deb2-107">Properties</span></span>

| <span data-ttu-id="9deb2-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9deb2-108">Property</span></span> | <span data-ttu-id="9deb2-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9deb2-109">Type</span></span>   | <span data-ttu-id="9deb2-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9deb2-110">Description</span></span>          |
| :------- | :----- | :------------------  |
| <span data-ttu-id="9deb2-111">código</span><span class="sxs-lookup"><span data-stu-id="9deb2-111">code</span></span>     | <span data-ttu-id="9deb2-112">String</span><span class="sxs-lookup"><span data-stu-id="9deb2-112">String</span></span> | <span data-ttu-id="9deb2-113">El código de resultado.</span><span class="sxs-lookup"><span data-stu-id="9deb2-113">The result code.</span></span>     |
| <span data-ttu-id="9deb2-114">message</span><span class="sxs-lookup"><span data-stu-id="9deb2-114">message</span></span>  | <span data-ttu-id="9deb2-115">String</span><span class="sxs-lookup"><span data-stu-id="9deb2-115">String</span></span> | <span data-ttu-id="9deb2-116">El mensaje.</span><span class="sxs-lookup"><span data-stu-id="9deb2-116">The message.</span></span>         |
| <span data-ttu-id="9deb2-117">subCode</span><span class="sxs-lookup"><span data-stu-id="9deb2-117">subCode</span></span>  | <span data-ttu-id="9deb2-118">String</span><span class="sxs-lookup"><span data-stu-id="9deb2-118">String</span></span> | <span data-ttu-id="9deb2-119">El código de resultado subcaracterística.</span><span class="sxs-lookup"><span data-stu-id="9deb2-119">The result sub-code.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9deb2-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9deb2-120">JSON representation</span></span>

<span data-ttu-id="9deb2-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9deb2-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.resultInfo"
}-->
```json
{
  "code": "String",
  "message": "String",
  "subCode": "String"
}
```

## <a name="example-error-result"></a><span data-ttu-id="9deb2-122">Resultado de Error de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9deb2-122">Example Error result</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.resultInfo"
}-->
```json
{
  "code": "100",
  "message": "Internal Server Error.",
  "subCode": "20"
}
```

## <a name="example-generic-success-result"></a><span data-ttu-id="9deb2-123">Resultados de ejemplo genérico de éxito</span><span class="sxs-lookup"><span data-stu-id="9deb2-123">Example Generic success result</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.resultInfo"
}-->
```json
{
  "code": "200",
  "message": "",
  "subCode": "0"
}
```

## <a name="example-record-success-result"></a><span data-ttu-id="9deb2-124">Resultado de correcto de registro de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9deb2-124">Example Record Success result</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.resultInfo"
}-->
```json
{
  "code": "200",
  "message": "",
  "subCode": "completedSilenceDetected"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resultInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
