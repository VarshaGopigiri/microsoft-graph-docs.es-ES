---
title: tipo de recurso chatMessageMention
description: 'Representa una mención en una entidad de chatMessage. Puede ser la mención a un usuario, equipo, bot o canal. '
localization_priority: Normal
ms.openlocfilehash: 7b24d2af6f61f3da69480557e1c5b5f32c009c25
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876142"
---
# <a name="chatmessagemention-resource-type"></a><span data-ttu-id="fca6e-104">tipo de recurso chatMessageMention</span><span class="sxs-lookup"><span data-stu-id="fca6e-104">chatMessageMention resource type</span></span>

> <span data-ttu-id="fca6e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fca6e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fca6e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fca6e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fca6e-107">Representa una mención en una entidad de [chatMessage](chatmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="fca6e-107">Represents a mention in a [chatMessage](chatmessage.md) entity.</span></span> <span data-ttu-id="fca6e-108">Puede ser la mención a un usuario, equipo, bot o canal.</span><span class="sxs-lookup"><span data-stu-id="fca6e-108">The mention can be to a user, team, bot or channel.</span></span> 

## <a name="properties"></a><span data-ttu-id="fca6e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fca6e-109">Properties</span></span>
| <span data-ttu-id="fca6e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fca6e-110">Property</span></span>     | <span data-ttu-id="fca6e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="fca6e-111">Type</span></span>   |<span data-ttu-id="fca6e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fca6e-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fca6e-113">id</span><span class="sxs-lookup"><span data-stu-id="fca6e-113">id</span></span>|<span data-ttu-id="fca6e-114">string</span><span class="sxs-lookup"><span data-stu-id="fca6e-114">string</span></span>|<span data-ttu-id="fca6e-115">Identificador de la entidad que se menciona</span><span class="sxs-lookup"><span data-stu-id="fca6e-115">Id of the entity being mentioned</span></span>|
|<span data-ttu-id="fca6e-116">mentionText</span><span class="sxs-lookup"><span data-stu-id="fca6e-116">mentionText</span></span>|<span data-ttu-id="fca6e-117">string</span><span class="sxs-lookup"><span data-stu-id="fca6e-117">string</span></span>|<span data-ttu-id="fca6e-118">Cadena que se utiliza para representar la mención ej: nombre de usuario para mostrar, nombre de equipo etcetera</span><span class="sxs-lookup"><span data-stu-id="fca6e-118">String used to represent the mention Ex: User display name, Team name etc</span></span>|
|<span data-ttu-id="fca6e-119">mencionado</span><span class="sxs-lookup"><span data-stu-id="fca6e-119">mentioned</span></span>|[<span data-ttu-id="fca6e-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="fca6e-120">identitySet</span></span>](identityset.md)|<span data-ttu-id="fca6e-121">El usuario que se ha mencionado</span><span class="sxs-lookup"><span data-stu-id="fca6e-121">The user that was mentioned</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fca6e-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fca6e-122">JSON representation</span></span>

<span data-ttu-id="fca6e-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fca6e-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessageMention"
}-->

```json
{
  "id": "string (identifier)",
  "mentionText": "string",
  "mentioned": "microsoft.graph.identitySet"
 }

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat mention resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
