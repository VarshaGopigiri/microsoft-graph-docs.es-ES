---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: DeleteAction
ms.openlocfilehash: 041552f88561981338fa2ea5719d5af102fb3574
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085651"
---
# <a name="deleteaction-resource-type"></a><span data-ttu-id="b0b25-102">Tipo de recurso DeleteAction</span><span class="sxs-lookup"><span data-stu-id="b0b25-102">DeleteAction resource type</span></span>

> <span data-ttu-id="b0b25-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b0b25-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b0b25-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b0b25-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b0b25-105">La presencia del recurso **DeleteAction** en un recurso [**itemActivity**][activity] indica que la actividad ha eliminado un elemento.</span><span class="sxs-lookup"><span data-stu-id="b0b25-105">The presence of the **DeleteAction** resource on an [**itemActivity**][activity] indicates that the activity deleted an item.</span></span>

[activity]: itemactivity.md

## <a name="json-representation"></a><span data-ttu-id="b0b25-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b0b25-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="b0b25-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b0b25-107">Properties</span></span>

| <span data-ttu-id="b0b25-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="b0b25-108">Property name</span></span> | <span data-ttu-id="b0b25-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0b25-109">Type</span></span>   | <span data-ttu-id="b0b25-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b25-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="b0b25-111">name</span><span class="sxs-lookup"><span data-stu-id="b0b25-111">name</span></span>          | <span data-ttu-id="b0b25-112">string</span><span class="sxs-lookup"><span data-stu-id="b0b25-112">string</span></span> | <span data-ttu-id="b0b25-113">El nombre del elemento que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="b0b25-113">The name of the item that was deleted.</span></span>
| <span data-ttu-id="b0b25-114">objectType</span><span class="sxs-lookup"><span data-stu-id="b0b25-114">objectType</span></span>    | <span data-ttu-id="b0b25-115">string</span><span class="sxs-lookup"><span data-stu-id="b0b25-115">string</span></span> | <span data-ttu-id="b0b25-116">`File`o `Folder`, en función del tipo de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b0b25-116">`File` or `Folder`, depending on the type of the deleted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0b25-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0b25-117">Remarks</span></span>

<span data-ttu-id="b0b25-118">Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="b0b25-118">Item activity records are currently only available on SharePoint and OneDrive for Business.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The DeleteAction object provides information about the deletion of an item.",
  "keywords": "activities,activity,action,delete,deletion",
  "section": "documentation",
  "tocPath": "Resources/DeleteAction"
} -->
