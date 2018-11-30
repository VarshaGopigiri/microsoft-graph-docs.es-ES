---
title: tipo de recurso mailSearchFolder
description: Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada. mailSearchFolder hereda de mailFolder.
ms.openlocfilehash: abce7c86e44fcee98042aecf753f0fdf4172365e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088210"
---
# <a name="mailsearchfolder-resource-type"></a><span data-ttu-id="6916e-104">tipo de recurso mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="6916e-104">mailSearchFolder resource type</span></span>

> <span data-ttu-id="6916e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6916e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6916e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6916e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6916e-107">Una mailSearchFolder es una carpeta virtual en el buzón del usuario que contiene todos los elementos de correo electrónico que coincidan con los criterios de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="6916e-107">A mailSearchFolder is a virtual folder in the user's mailbox that contains all the email items matching specified search criteria.</span></span> <span data-ttu-id="6916e-108">mailSearchFolder hereda de [mailFolder](mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="6916e-108">mailSearchFolder inherits from [mailFolder](mailfolder.md).</span></span>

## <a name="methods"></a><span data-ttu-id="6916e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6916e-109">Methods</span></span>

| <span data-ttu-id="6916e-110">Método</span><span class="sxs-lookup"><span data-stu-id="6916e-110">Method</span></span> | <span data-ttu-id="6916e-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6916e-111">Return Type</span></span>  | <span data-ttu-id="6916e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6916e-112">Description</span></span> |
|:---------------|:--------|:----------|
| [<span data-ttu-id="6916e-113">Crear una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6916e-113">Create a search folder</span></span>](../api/mailsearchfolder-post.md) | [<span data-ttu-id="6916e-114">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="6916e-114">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="6916e-115">Cree una carpeta de búsqueda en el buzón de este usuario.</span><span class="sxs-lookup"><span data-stu-id="6916e-115">Create a search folder in this user's mailbox.</span></span> |
| [<span data-ttu-id="6916e-116">Carpetas de búsqueda de lista</span><span class="sxs-lookup"><span data-stu-id="6916e-116">List search folders</span></span>](../api/mailfolder-list-childfolders.md) | <span data-ttu-id="6916e-117">Colección [mailFolder](mailfolder.md)</span><span class="sxs-lookup"><span data-stu-id="6916e-117">[mailFolder](mailfolder.md) collection</span></span> | <span data-ttu-id="6916e-118">Lista de todas las carpetas de este buzón de usuario, incluidas las carpetas de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6916e-118">List all the folders in this user's mailbox, including search folders.</span></span> |
| [<span data-ttu-id="6916e-119">Obtener una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6916e-119">Get a search folder</span></span>](../api/mailfolder-get.md) | [<span data-ttu-id="6916e-120">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="6916e-120">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="6916e-121">Obtener la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="6916e-121">Get the specified search folder.</span></span> |
| [<span data-ttu-id="6916e-122">Actualización de una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6916e-122">Update a search folder</span></span>](../api/mailsearchfolder-update.md) | [<span data-ttu-id="6916e-123">mailSearchFolder</span><span class="sxs-lookup"><span data-stu-id="6916e-123">mailSearchFolder</span></span>](mailsearchfolder.md) | <span data-ttu-id="6916e-124">Actualice la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="6916e-124">Update the specified search folder.</span></span> |
| [<span data-ttu-id="6916e-125">Eliminar una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6916e-125">Delete a search folder</span></span>](../api/mailfolder-delete.md) | <span data-ttu-id="6916e-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6916e-126">None</span></span> | <span data-ttu-id="6916e-127">Elimine la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="6916e-127">Delete the specified search folder.</span></span> |
| [<span data-ttu-id="6916e-128">Lista de todos los mensajes en una carpeta de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6916e-128">List all messages in a search folder</span></span>](../api/mailfolder-list-messages.md) | <span data-ttu-id="6916e-129">Colección [message](message.md)</span><span class="sxs-lookup"><span data-stu-id="6916e-129">[message](message.md) collection</span></span> | <span data-ttu-id="6916e-130">Lista de todos los mensajes en la carpeta de búsqueda especificada.</span><span class="sxs-lookup"><span data-stu-id="6916e-130">List all the messages in the specified search folder.</span></span> |

## <a name="properties"></a><span data-ttu-id="6916e-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6916e-131">Properties</span></span>

| <span data-ttu-id="6916e-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6916e-132">Property</span></span> | <span data-ttu-id="6916e-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="6916e-133">Type</span></span> | <span data-ttu-id="6916e-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6916e-134">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="6916e-135">isSupported</span><span class="sxs-lookup"><span data-stu-id="6916e-135">isSupported</span></span> | <span data-ttu-id="6916e-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="6916e-136">Boolean</span></span> | <span data-ttu-id="6916e-137">Indica si una carpeta de búsqueda se puede editar mediante la API de REST.</span><span class="sxs-lookup"><span data-stu-id="6916e-137">Indicates whether a search folder is editable using REST APIs.</span></span> |
| <span data-ttu-id="6916e-138">includeNestedFolders</span><span class="sxs-lookup"><span data-stu-id="6916e-138">includeNestedFolders</span></span> | <span data-ttu-id="6916e-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="6916e-139">Boolean</span></span> | <span data-ttu-id="6916e-140">Indica cómo se debe pasar por la jerarquía de carpetas de buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="6916e-140">Indicates how the mailbox folder hierarchy should be traversed.</span></span> <span data-ttu-id="6916e-141">`true`significa que debe ser una búsqueda en profundidad mientras `false` significa que se debe realizar una búsqueda no exhaustivos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6916e-141">`true` means that a deep search should be done while `false` means a shallow search should be done instead.</span></span> |
| <span data-ttu-id="6916e-142">sourceFolderIDs</span><span class="sxs-lookup"><span data-stu-id="6916e-142">sourceFolderIDs</span></span> | <span data-ttu-id="6916e-143">Colección String</span><span class="sxs-lookup"><span data-stu-id="6916e-143">String collection</span></span> | <span data-ttu-id="6916e-144">Las carpetas de buzón de correo que deben ser extraídas.</span><span class="sxs-lookup"><span data-stu-id="6916e-144">The mailbox folders that should be mined.</span></span> |
| <span data-ttu-id="6916e-145">filterQuery</span><span class="sxs-lookup"><span data-stu-id="6916e-145">filterQuery</span></span> | <span data-ttu-id="6916e-146">String</span><span class="sxs-lookup"><span data-stu-id="6916e-146">String</span></span> | <span data-ttu-id="6916e-147">La consulta de OData para filtrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6916e-147">The OData query to filter the messages.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6916e-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6916e-148">JSON representation</span></span>

<span data-ttu-id="6916e-149">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6916e-149">The following is a JSON representation of the resource.</span></span>

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
