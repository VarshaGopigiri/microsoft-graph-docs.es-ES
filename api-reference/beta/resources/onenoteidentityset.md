---
title: tipo de recurso oneNoteIdentitySet
description: '**Compatibilidad con próximamente**'
localization_priority: Normal
author: jewan-microsoft
ms.prod: onenote
ms.openlocfilehash: 9043b08a8586bcc9a0043a2fde13f0d5d9eea4a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947172"
---
# <a name="onenoteidentityset-resource-type"></a><span data-ttu-id="60c0f-103">tipo de recurso oneNoteIdentitySet</span><span class="sxs-lookup"><span data-stu-id="60c0f-103">oneNoteIdentitySet resource type</span></span>

> <span data-ttu-id="60c0f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="60c0f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="60c0f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="60c0f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="60c0f-106">**Compatibilidad con próximamente**</span><span class="sxs-lookup"><span data-stu-id="60c0f-106">**Support coming soon**</span></span>

<span data-ttu-id="60c0f-107">El tipo de OneNoteIdentitySet es una colección de claves de objetos [OneNoteIdentity](onenoteidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="60c0f-107">The OneNoteIdentitySet type is a keyed collection of [OneNoteIdentity](onenoteidentity.md) objects.</span></span>
<span data-ttu-id="60c0f-108">Se usa para representar un conjunto de identidades asociado con varios eventos para un _Bloc de notas_, _sección_ o _página_, como _creado por_ o _modificado por última vez_.</span><span class="sxs-lookup"><span data-stu-id="60c0f-108">It is used to represent a set of identities associated with various events for a _Notebook_, _Section_ or _Page_, such as _created by_ or _last modified by_.</span></span> 
 
<span data-ttu-id="60c0f-109">Actualmente contiene una clave, un solo _**usuario**_.</span><span class="sxs-lookup"><span data-stu-id="60c0f-109">Currently it contains a single key, _**user**_.</span></span>  <span data-ttu-id="60c0f-110">En el futuro, se pueden agregar claves como el dispositivo o la aplicación para cambiar el elemento.</span><span class="sxs-lookup"><span data-stu-id="60c0f-110">In future, keys such as the device or application to change the item may be added.</span></span>

<span data-ttu-id="60c0f-111">En el futuro, este tipo se combinarán con [IdentitySet](identityset.md)</span><span class="sxs-lookup"><span data-stu-id="60c0f-111">In future, this type will be merged with [IdentitySet](identityset.md)</span></span>

## <a name="json-representation"></a><span data-ttu-id="60c0f-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60c0f-112">JSON representation</span></span>

<span data-ttu-id="60c0f-113">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="60c0f-113">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteidentityset"
}-->

```json
{
  "user": {"@odata.type": "microsoft.graph.oneNoteIdentity"}
}

```
## <a name="properties"></a><span data-ttu-id="60c0f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60c0f-114">Properties</span></span>
| <span data-ttu-id="60c0f-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60c0f-115">Property</span></span>     | <span data-ttu-id="60c0f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="60c0f-116">Type</span></span>   |<span data-ttu-id="60c0f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="60c0f-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="60c0f-118">usuario</span><span class="sxs-lookup"><span data-stu-id="60c0f-118">user</span></span>|[<span data-ttu-id="60c0f-119">oneNoteIdentity</span><span class="sxs-lookup"><span data-stu-id="60c0f-119">oneNoteIdentity</span></span>](onenoteidentity.md)|<span data-ttu-id="60c0f-120">Un recurso de OneNoteIdentity que representa a un usuario.</span><span class="sxs-lookup"><span data-stu-id="60c0f-120">A OneNoteIdentity resource that represents a user.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oneNoteIdentitySet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
