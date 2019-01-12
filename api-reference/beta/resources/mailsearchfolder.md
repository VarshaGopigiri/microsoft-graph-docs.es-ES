---
title: tipo de recurso mailSearchFolder
description: Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada. mailSearchFolder hereda de mailFolder.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 1ba9ce248071e3d806383b4cd7e7550c1e3aa145
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920915"
---
# <a name="mailsearchfolder-resource-type"></a><span data-ttu-id="af09f-104">tipo de recurso mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="af09f-104">mailSearchFolder resource type</span></span>

> <span data-ttu-id="af09f-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af09f-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af09f-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af09f-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="af09f-107">Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="af09f-107">A mailSearchFolder is a virtual folder in the user's mailbox that contains all the email items matching specified search criteria.</span></span> <span data-ttu-id="af09f-108">mailSearchFolder hereda de [mailFolder](mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="af09f-108">mailSearchFolder inherits from [mailFolder](mailfolder.md).</span></span>

## <a name="methods"></a><span data-ttu-id="af09f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="af09f-109">Methods</span></span>

| <span data-ttu-id="af09f-110">Método</span><span class="sxs-lookup"><span data-stu-id="af09f-110">Method</span></span> | <span data-ttu-id="af09f-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af09f-111">Return Type</span></span>  | <span data-ttu-id="af09f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="af09f-112">Description</span></span> |
|:---------------|:--------|:----------|
| [<span data-ttu-id="af09f-113">Crear una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="af09f-113">Create a search folder</span></span>](../api/mailsearchfolder-post.md) | [<span data-ttu-id="af09f-114">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="af09f-114">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="af09f-115">Cree una carpeta de búsqueda en el buzón de este usuario.</span><span class="sxs-lookup"><span data-stu-id="af09f-115">Create a search folder in this user's mailbox.</span></span> |
| [<span data-ttu-id="af09f-116">Carpetas de búsqueda de lista</span><span class="sxs-lookup"><span data-stu-id="af09f-116">List search folders</span></span>](../api/mailfolder-list-childfolders.md) | <span data-ttu-id="af09f-117">Colección [mailFolder](mailfolder.md)</span><span class="sxs-lookup"><span data-stu-id="af09f-117">[mailFolder](mailfolder.md) collection</span></span> | <span data-ttu-id="af09f-118">Lista de todas las carpetas de este buzón de usuario, incluidas las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="af09f-118">List all the folders in this user's mailbox, including search folders.</span></span> |
| [<span data-ttu-id="af09f-119">Obtener una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="af09f-119">Get a search folder</span></span>](../api/mailfolder-get.md) | [<span data-ttu-id="af09f-120">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="af09f-120">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="af09f-121">Obtener la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="af09f-121">Get the specified search folder.</span></span> |
| [<span data-ttu-id="af09f-122">Actualización de una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="af09f-122">Update a search folder</span></span>](../api/mailsearchfolder-update.md) | [<span data-ttu-id="af09f-123">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="af09f-123">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="af09f-124">Actualice la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="af09f-124">Update the specified search folder.</span></span> |
| [<span data-ttu-id="af09f-125">Eliminar una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="af09f-125">Delete a search folder</span></span>](../api/mailfolder-delete.md) | <span data-ttu-id="af09f-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="af09f-126">None</span></span> | <span data-ttu-id="af09f-127">Elimine la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="af09f-127">Delete the specified search folder.</span></span> |
| [<span data-ttu-id="af09f-128">Lista de todos los mensajes en una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="af09f-128">List all messages in a search folder</span></span>](../api/mailfolder-list-messages.md) | <span data-ttu-id="af09f-129">Colección [message](message.md)</span><span class="sxs-lookup"><span data-stu-id="af09f-129">[message](message.md) collection</span></span> | <span data-ttu-id="af09f-130">Lista de todos los mensajes en la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="af09f-130">List all the messages in the specified search folder.</span></span> |

## <a name="properties"></a><span data-ttu-id="af09f-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af09f-131">Properties</span></span>

| <span data-ttu-id="af09f-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af09f-132">Property</span></span> | <span data-ttu-id="af09f-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="af09f-133">Type</span></span> | <span data-ttu-id="af09f-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="af09f-134">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="af09f-135">isSupported</span><span class="sxs-lookup"><span data-stu-id="af09f-135">isSupported</span></span> | <span data-ttu-id="af09f-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="af09f-136">Boolean</span></span> | <span data-ttu-id="af09f-137">Indica si una carpeta de búsqueda se puede editar mediante la API de REST.</span><span class="sxs-lookup"><span data-stu-id="af09f-137">Indicates whether a search folder is editable using REST APIs.</span></span> |
| <span data-ttu-id="af09f-138">includeNestedFolders</span><span class="sxs-lookup"><span data-stu-id="af09f-138">includeNestedFolders</span></span> | <span data-ttu-id="af09f-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="af09f-139">Boolean</span></span> | <span data-ttu-id="af09f-140">Indica cómo se debe pasar por la jerarquía de carpetas de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="af09f-140">Indicates how the mailbox folder hierarchy should be traversed.</span></span> <span data-ttu-id="af09f-141">`true`significa que debe ser una búsqueda en profundidad mientras `false` significa que se debe realizar una búsqueda no exhaustivos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="af09f-141">`true` means that a deep search should be done while `false` means a shallow search should be done instead.</span></span> |
| <span data-ttu-id="af09f-142">sourceFolderIDs</span><span class="sxs-lookup"><span data-stu-id="af09f-142">sourceFolderIDs</span></span> | <span data-ttu-id="af09f-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="af09f-143">String collection</span></span> | <span data-ttu-id="af09f-144">Las carpetas de buzón de correo que deben ser extraídas.</span><span class="sxs-lookup"><span data-stu-id="af09f-144">The mailbox folders that should be mined.</span></span> |
| <span data-ttu-id="af09f-145">filterQuery</span><span class="sxs-lookup"><span data-stu-id="af09f-145">filterQuery</span></span> | <span data-ttu-id="af09f-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="af09f-146">String</span></span> | <span data-ttu-id="af09f-147">La consulta de OData para filtrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="af09f-147">The OData query to filter the messages.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="af09f-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af09f-148">JSON representation</span></span>

<span data-ttu-id="af09f-149">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="af09f-149">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mailSearchFolder"
}-->

```json
{
  "isSupported": true,
  "includeNestedFolders": true,
  "sourceFolderIDs": ["string"],
  "filterQuery": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2018-01-23 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailSearchFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
