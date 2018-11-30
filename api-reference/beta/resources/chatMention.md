---
title: tipo de recurso chatMessageMention
description: 'Representa una mención en una entidad de chatMessage. Puede ser la mención a un usuario, equipo, bot o canal. '
ms.openlocfilehash: 5f1e427b0ed2b8ffcfbc86417beb4719dc6fb2a3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083433"
---
# <a name="chatmessagemention-resource-type"></a><span data-ttu-id="b9699-104">tipo de recurso chatMessageMention</span><span class="sxs-lookup"><span data-stu-id="b9699-104">chatMessageMention resource type</span></span>

> <span data-ttu-id="b9699-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b9699-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b9699-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b9699-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b9699-107">Representa una mención en una entidad de [chatMessage](chatmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="b9699-107">Represents a mention in a [chatMessage](chatmessage.md) entity.</span></span> <span data-ttu-id="b9699-108">Puede ser la mención a un usuario, equipo, bot o canal.</span><span class="sxs-lookup"><span data-stu-id="b9699-108">The mention can be to a user, team, bot or channel.</span></span> 

## <a name="properties"></a><span data-ttu-id="b9699-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9699-109">Properties</span></span>
| <span data-ttu-id="b9699-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9699-110">Property</span></span>     | <span data-ttu-id="b9699-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9699-111">Type</span></span>   |<span data-ttu-id="b9699-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9699-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9699-113">id</span><span class="sxs-lookup"><span data-stu-id="b9699-113">id</span></span>|<span data-ttu-id="b9699-114">string</span><span class="sxs-lookup"><span data-stu-id="b9699-114">string</span></span>|<span data-ttu-id="b9699-115">Identificador de la entidad que se menciona</span><span class="sxs-lookup"><span data-stu-id="b9699-115">Id of the entity being mentioned</span></span>|
|<span data-ttu-id="b9699-116">mentionText</span><span class="sxs-lookup"><span data-stu-id="b9699-116">mentionText</span></span>|<span data-ttu-id="b9699-117">string</span><span class="sxs-lookup"><span data-stu-id="b9699-117">string</span></span>|<span data-ttu-id="b9699-118">Cadena que se utiliza para representar la mención ej: nombre de usuario para mostrar, nombre de equipo etcetera</span><span class="sxs-lookup"><span data-stu-id="b9699-118">String used to represent the mention Ex: User display name, Team name etc</span></span>|
|<span data-ttu-id="b9699-119">mencionado</span><span class="sxs-lookup"><span data-stu-id="b9699-119">mentioned</span></span>|[<span data-ttu-id="b9699-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="b9699-120">identitySet</span></span>](identityset.md)|<span data-ttu-id="b9699-121">El usuario que se ha mencionado</span><span class="sxs-lookup"><span data-stu-id="b9699-121">The user that was mentioned</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b9699-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9699-122">JSON representation</span></span>

<span data-ttu-id="b9699-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b9699-123">The following is a JSON representation of the resource.</span></span>

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
