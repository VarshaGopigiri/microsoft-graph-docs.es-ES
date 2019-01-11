---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: DeleteAction
localization_priority: Normal
ms.openlocfilehash: a845a6609991041f12266cd97e95460f96bf742f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876765"
---
# <a name="deleteaction-resource-type"></a><span data-ttu-id="b2e09-102">Tipo de recurso DeleteAction</span><span class="sxs-lookup"><span data-stu-id="b2e09-102">DeleteAction resource type</span></span>

> <span data-ttu-id="b2e09-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2e09-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2e09-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2e09-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b2e09-105">La presencia del recurso **DeleteAction** en un recurso [**itemActivity**][activity] indica que la actividad ha eliminado un elemento.</span><span class="sxs-lookup"><span data-stu-id="b2e09-105">The presence of the **DeleteAction** resource on an [**itemActivity**][activity] indicates that the activity deleted an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="b2e09-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2e09-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.deleteAction"
}-->

```json
{
  "name": "string",
  "objectType": "File | Folder"
}
```

## <a name="properties"></a><span data-ttu-id="b2e09-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2e09-107">Properties</span></span>

| <span data-ttu-id="b2e09-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="b2e09-108">Property name</span></span> | <span data-ttu-id="b2e09-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2e09-109">Type</span></span>   | <span data-ttu-id="b2e09-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2e09-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="b2e09-111">name</span><span class="sxs-lookup"><span data-stu-id="b2e09-111">name</span></span>          | <span data-ttu-id="b2e09-112">string</span><span class="sxs-lookup"><span data-stu-id="b2e09-112">string</span></span> | <span data-ttu-id="b2e09-113">El nombre del elemento que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="b2e09-113">The name of the item that was deleted.</span></span>
| <span data-ttu-id="b2e09-114">objectType</span><span class="sxs-lookup"><span data-stu-id="b2e09-114">objectType</span></span>    | <span data-ttu-id="b2e09-115">string</span><span class="sxs-lookup"><span data-stu-id="b2e09-115">string</span></span> | <span data-ttu-id="b2e09-116">`File`o `Folder`, en función del tipo de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b2e09-116">`File` or `Folder`, depending on the type of the deleted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e09-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2e09-117">Remarks</span></span>

<span data-ttu-id="b2e09-118">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="b2e09-118">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The DeleteAction object provides information about the deletion of an item.",
  "keywords": "activities,activity,action,delete,deletion",
  "section": "documentation",
  "tocPath": "Resources/DeleteAction"
} -->
