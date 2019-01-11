---
title: Tipo de recurso plannerUserIds
description: El recurso **plannerUserIds** representa la lista de identificadores de usuario con los que se comparte un plan. Este es un tipo abierto. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos para compartir el plan del grupo. También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.
localization_priority: Normal
ms.openlocfilehash: b553d7bdfc2a0a041681b200d3e07f3899acf1c3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885970"
---
# <a name="planneruserids-resource-type"></a><span data-ttu-id="fdd58-106">Tipo de recurso plannerUserIds</span><span class="sxs-lookup"><span data-stu-id="fdd58-106">plannerUserIds resource type</span></span>

> <span data-ttu-id="fdd58-107">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fdd58-107">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fdd58-108">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fdd58-108">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fdd58-p103">El recurso **plannerUserIds** representa la lista de identificadores de usuario con los que se comparte un [plan](plannerplan.md). Este es un tipo abierto. Si está aprovechando los grupos de Office 365, use la API de grupos para administrar la pertenencia a los grupos para compartir el plan del [grupo](group.md). También puede agregar los miembros existentes del grupo a esta colección, aunque no es necesario que obtengan acceso al plan propiedad del grupo.</span><span class="sxs-lookup"><span data-stu-id="fdd58-p103">The **plannerUserIds** resource represents the list of users ids that a [plan](plannerplan.md) is shared with. This is an Open Type. If you are leveraging Office 365 Groups, use the Groups API to manage group membership to share the [group's](group.md) plan. You can also add existing members of the group to this collection though it is not required for them to access the plan owned by the group.</span></span>


## <a name="properties"></a><span data-ttu-id="fdd58-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fdd58-113">Properties</span></span>
<span data-ttu-id="fdd58-p104">El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los id. de usuario como propiedades y sus valores deben ser el booleano `true`. Si los id. de usuario ya no se comparten, las propiedades se quitarán automáticamente estableciendo sus valores en el booleano `false`.</span><span class="sxs-lookup"><span data-stu-id="fdd58-p104">Properties of an Open Type can be defined by the client. In this case, the client should provide user ids as properties with their values being the `true` boolean. When user ids are no longer shared with, properties are automatically removed by setting their values to the `false` boolean.</span></span>


## <a name="json-representation"></a><span data-ttu-id="fdd58-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fdd58-117">JSON representation</span></span>

<span data-ttu-id="fdd58-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fdd58-118">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerUserIds"
}-->

```json
{
  "String-value": true
}
```

<span data-ttu-id="fdd58-119">// Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fdd58-119">// Example</span></span>
```json
{
  "400723e1-102b-43aa-aba9-f35524827084": true, // property name is user id
  "f117339e-c914-4a9c-9b66-1c062b027556": true,
  "e886d105-23b9-47e2-bde1-757e75ee4a28": true
}

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerUserIds resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
