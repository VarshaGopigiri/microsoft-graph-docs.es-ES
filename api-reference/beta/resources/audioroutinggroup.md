---
title: tipo de recurso audioRoutingGroup
description: El grupo de enrutamiento de audio almacena una ruta de audio privada entre los participantes en una conversación entre varias partes. Origen es el participante propio y los receptores son un subconjunto de los otros participantes de la conversación entre varias partes.
ms.openlocfilehash: 98c58e39773567f13a2723e94c0413efd2841cd0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083500"
---
# <a name="audioroutinggroup-resource-type"></a><span data-ttu-id="2aa21-104">tipo de recurso audioRoutingGroup</span><span class="sxs-lookup"><span data-stu-id="2aa21-104">audioRoutingGroup resource type</span></span>

> <span data-ttu-id="2aa21-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2aa21-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2aa21-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2aa21-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2aa21-107">El grupo de enrutamiento de audio almacena una ruta de audio privada entre los participantes en una conversación entre varias partes.</span><span class="sxs-lookup"><span data-stu-id="2aa21-107">The audio routing group stores a private audio route between participants in a multiparty conversation.</span></span> <span data-ttu-id="2aa21-108">Origen es el participante propio y los receptores son un subconjunto de los otros participantes de la conversación entre varias partes.</span><span class="sxs-lookup"><span data-stu-id="2aa21-108">Source is the participant itself and the receivers are a subset of other participants in the multiparty conversation.</span></span>

> <span data-ttu-id="2aa21-109">**Nota:** [ConfigureMixer](../api/participant-configuremixer.md) implican las rutas, para toda la llamada para establecer los niveles de volumen para combinaciones de receptor de origen.</span><span class="sxs-lookup"><span data-stu-id="2aa21-109">**Note:** [ConfigureMixer](../api/participant-configuremixer.md) does not involve any routes, it is for the entire call for setting the volume levels for source-receiver combinations.</span></span>

## <a name="methods"></a><span data-ttu-id="2aa21-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2aa21-110">Methods</span></span>

| <span data-ttu-id="2aa21-111">Método</span><span class="sxs-lookup"><span data-stu-id="2aa21-111">Method</span></span>                                                  | <span data-ttu-id="2aa21-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2aa21-112">Return Type</span></span>                               | <span data-ttu-id="2aa21-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2aa21-113">Description</span></span>                                  |
|:--------------------------------------------------------|:------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="2aa21-114">Obtener audioRoutingGroup</span><span class="sxs-lookup"><span data-stu-id="2aa21-114">Get audioRoutingGroup</span></span>](../api/audioroutinggroup-get.md)| [<span data-ttu-id="2aa21-115">audioRoutingGroup</span><span class="sxs-lookup"><span data-stu-id="2aa21-115">audioRoutingGroup</span></span>](audioroutinggroup.md) | <span data-ttu-id="2aa21-116">Leer las propiedades y las relaciones del objeto audioRoutingGroup.</span><span class="sxs-lookup"><span data-stu-id="2aa21-116">Read properties and relationships of audioRoutingGroup object.</span></span>|
| [<span data-ttu-id="2aa21-117">Update</span><span class="sxs-lookup"><span data-stu-id="2aa21-117">Update</span></span>](../api/audioroutinggroup-update.md)            | [<span data-ttu-id="2aa21-118">audioRoutingGroup</span><span class="sxs-lookup"><span data-stu-id="2aa21-118">audioRoutingGroup</span></span>](audioroutinggroup.md) | <span data-ttu-id="2aa21-119">Actualizar lista de receptores.</span><span class="sxs-lookup"><span data-stu-id="2aa21-119">Update receivers list.</span></span>                       |
| [<span data-ttu-id="2aa21-120">Delete</span><span class="sxs-lookup"><span data-stu-id="2aa21-120">Delete</span></span>](../api/audioroutinggroup-delete.md)            | <span data-ttu-id="2aa21-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2aa21-121">None</span></span>                                      | <span data-ttu-id="2aa21-122">Eliminar el grupo de enrutamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="2aa21-122">Delete the audio routing group.</span></span>              |

## <a name="properties"></a><span data-ttu-id="2aa21-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2aa21-123">Properties</span></span>

| <span data-ttu-id="2aa21-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2aa21-124">Property</span></span>      | <span data-ttu-id="2aa21-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="2aa21-125">Type</span></span>              | <span data-ttu-id="2aa21-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2aa21-126">Description</span></span>                                                          |
| :----------   | :---------------- | :--------------------------------------------------------------------|
| <span data-ttu-id="2aa21-127">id</span><span class="sxs-lookup"><span data-stu-id="2aa21-127">id</span></span>            | <span data-ttu-id="2aa21-128">String</span><span class="sxs-lookup"><span data-stu-id="2aa21-128">String</span></span>            | <span data-ttu-id="2aa21-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2aa21-129">Read-only.</span></span> <span data-ttu-id="2aa21-130">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="2aa21-130">Server generated.</span></span>                                         |
| <span data-ttu-id="2aa21-131">receptores de</span><span class="sxs-lookup"><span data-stu-id="2aa21-131">receivers</span></span>     | <span data-ttu-id="2aa21-132">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="2aa21-132">String Collection</span></span> | <span data-ttu-id="2aa21-133">Lista de la recepción de los identificadores de participantes.</span><span class="sxs-lookup"><span data-stu-id="2aa21-133">List of receiving participant ids.</span></span>                                   |
| <span data-ttu-id="2aa21-134">routingMode</span><span class="sxs-lookup"><span data-stu-id="2aa21-134">routingMode</span></span>   | <span data-ttu-id="2aa21-135">String</span><span class="sxs-lookup"><span data-stu-id="2aa21-135">String</span></span>            | <span data-ttu-id="2aa21-136">Modo de grupo de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="2aa21-136">Routing group mode.</span></span>  <span data-ttu-id="2aa21-137">Los valores posibles son: `oneToOne` y `multicast`.</span><span class="sxs-lookup"><span data-stu-id="2aa21-137">Possible values are: `oneToOne`, `multicast`.</span></span>   |
| <span data-ttu-id="2aa21-138">orígenes</span><span class="sxs-lookup"><span data-stu-id="2aa21-138">sources</span></span>       | <span data-ttu-id="2aa21-139">Colección de cadenas</span><span class="sxs-lookup"><span data-stu-id="2aa21-139">String Collection</span></span> | <span data-ttu-id="2aa21-140">Lista de identificadores de participantes de origen.</span><span class="sxs-lookup"><span data-stu-id="2aa21-140">List of source participant ids.</span></span>                                      |

> <span data-ttu-id="2aa21-141">**Nota:** Modo de enrutamiento determina las restricciones en los orígenes y receptores.</span><span class="sxs-lookup"><span data-stu-id="2aa21-141">**Note:** Routing mode determines the restrictions on the sources and receivers.</span></span> <span data-ttu-id="2aa21-142">Se admiten sólo los siguientes grupos de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="2aa21-142">Only the following routing groups are supported.</span></span>
> - <span data-ttu-id="2aa21-143">`oneToOne`-orígenes y receptores tienen un único participante.</span><span class="sxs-lookup"><span data-stu-id="2aa21-143">`oneToOne` - sources and receivers have only one participant each.</span></span>
> - <span data-ttu-id="2aa21-144">`multicast`-origen tiene un participante pero hay varios receptores.</span><span class="sxs-lookup"><span data-stu-id="2aa21-144">`multicast` - source has one participant but there are multiple receivers.</span></span> <span data-ttu-id="2aa21-145">Lista de receptores puede actualizarse.</span><span class="sxs-lookup"><span data-stu-id="2aa21-145">Receivers list may be updated.</span></span>

> <span data-ttu-id="2aa21-146">**Nota:** Si crea varios grupos de enrutamiento Audioconferencias (por ejemplo, un bot por participante), se transfiere sólo el sonido de los altavoces dominantes 4 superiores.</span><span class="sxs-lookup"><span data-stu-id="2aa21-146">**Note:** If you create many audio routing groups (e.g. a bot per participant), only the audio of the top 4 dominant speakers is forwarded.</span></span> <span data-ttu-id="2aa21-147">Significa incluso con el grupo de enrutamiento de audio personalizado, si el altavoz no es lo suficientemente alto como en el mezclador principal, éste no podrán oír el robot incluso si hay un grupo de audio privado solo para este altavoz y el robot.</span><span class="sxs-lookup"><span data-stu-id="2aa21-147">It means even with customized audio routing group, if the speaker is not loud enough in the main mixer, he/she cannot be heard by the bot even if there is a private audio group just for this speaker and the bot.</span></span>

## <a name="relationships"></a><span data-ttu-id="2aa21-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2aa21-148">Relationships</span></span>
<span data-ttu-id="2aa21-149">Ninguno</span><span class="sxs-lookup"><span data-stu-id="2aa21-149">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="2aa21-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2aa21-150">JSON representation</span></span>

<span data-ttu-id="2aa21-151">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="2aa21-151">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioRoutingGroup"
}-->
```json
{
  "id": "String (identifier)",
  "receivers": [ "String" ],
  "routingMode": "oneToOne | multicast",
  "sources": [ "String" ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioRoutingGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->