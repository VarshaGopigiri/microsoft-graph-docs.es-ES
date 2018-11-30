---
title: tipo de recurso auditActivityInitiator
description: El objeto de recurso que inicia la actividad de identidad. El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)
ms.openlocfilehash: 834b39f67a9a3a251c61f15d3b1fa8aa964870e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087869"
---
# <a name="auditactivityinitiator-resource-type"></a><span data-ttu-id="3648f-104">tipo de recurso auditActivityInitiator</span><span class="sxs-lookup"><span data-stu-id="3648f-104">auditActivityInitiator resource type</span></span>
<span data-ttu-id="3648f-105">El objeto de recurso que inicia la actividad de identidad.</span><span class="sxs-lookup"><span data-stu-id="3648f-105">Identity the resource object that initiates the activity.</span></span> <span data-ttu-id="3648f-106">El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)</span><span class="sxs-lookup"><span data-stu-id="3648f-106">The initiator can be a user, an app or a system (which is considered as an app)</span></span>



## <a name="properties"></a><span data-ttu-id="3648f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3648f-107">Properties</span></span>
| <span data-ttu-id="3648f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3648f-108">Property</span></span>     | <span data-ttu-id="3648f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3648f-109">Type</span></span>   |<span data-ttu-id="3648f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3648f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3648f-111">aplicación</span><span class="sxs-lookup"><span data-stu-id="3648f-111">app</span></span>|[<span data-ttu-id="3648f-112">appIdentity</span><span class="sxs-lookup"><span data-stu-id="3648f-112">appIdentity</span></span>](appidentity.md)|<span data-ttu-id="3648f-113">Si el recurso de inicio de la actividad es una aplicación, esta propiedad indica todos los de las aplicaciones relacionadas con la información como appId, nombre, servicePrincipalId, nombre.</span><span class="sxs-lookup"><span data-stu-id="3648f-113">If the resource initiating the activity is an app, this property indicates all the app related information like appId, Name, servicePrincipalId, Name.</span></span>|
|<span data-ttu-id="3648f-114">usuario</span><span class="sxs-lookup"><span data-stu-id="3648f-114">user</span></span>|[<span data-ttu-id="3648f-115">IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="3648f-115">userIdentity</span></span>](useridentity.md)|<span data-ttu-id="3648f-116">Si el recurso de inicio de la actividad es un usuario, esta propiedad indica todos los el usuario relacionadas con la información como userId, nombre, UserPrinicpalName.</span><span class="sxs-lookup"><span data-stu-id="3648f-116">If the resource initiating the activity is a user, this property Indicates all the user related information like userId, Name, UserPrinicpalName.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3648f-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3648f-117">JSON representation</span></span>

<span data-ttu-id="3648f-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3648f-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.auditActivityInitiator"
}-->

```json
{
  "app": {"@odata.type": "microsoft.graph.appIdentity"},
  "user": {"@odata.type": "microsoft.graph.userIdentity"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "auditActivityInitiator resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->