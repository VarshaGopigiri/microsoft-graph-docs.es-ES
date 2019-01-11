---
title: tipo de recurso auditActivityInitiator
description: El objeto de recurso que inicia la actividad de identidad. El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)
localization_priority: Normal
ms.openlocfilehash: 14c92a4df42c3d8dbcd6836695df8d6caac3cf87
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884612"
---
# <a name="auditactivityinitiator-resource-type"></a><span data-ttu-id="a415e-104">tipo de recurso auditActivityInitiator</span><span class="sxs-lookup"><span data-stu-id="a415e-104">auditActivityInitiator resource type</span></span>
<span data-ttu-id="a415e-105">El objeto de recurso que inicia la actividad de identidad.</span><span class="sxs-lookup"><span data-stu-id="a415e-105">Identity the resource object that initiates the activity.</span></span> <span data-ttu-id="a415e-106">El iniciador puede ser un usuario, una aplicación o un sistema (que se considera como una aplicación)</span><span class="sxs-lookup"><span data-stu-id="a415e-106">The initiator can be a user, an app or a system (which is considered as an app)</span></span>



## <a name="properties"></a><span data-ttu-id="a415e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a415e-107">Properties</span></span>
| <span data-ttu-id="a415e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a415e-108">Property</span></span>     | <span data-ttu-id="a415e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a415e-109">Type</span></span>   |<span data-ttu-id="a415e-110">Description</span><span class="sxs-lookup"><span data-stu-id="a415e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a415e-111">aplicación</span><span class="sxs-lookup"><span data-stu-id="a415e-111">app</span></span>|[<span data-ttu-id="a415e-112">appIdentity</span><span class="sxs-lookup"><span data-stu-id="a415e-112">appIdentity</span></span>](appidentity.md)|<span data-ttu-id="a415e-113">Si el recurso de inicio de la actividad es una aplicación, esta propiedad indica todos los de las aplicaciones relacionadas con la información como appId, nombre, servicePrincipalId, nombre.</span><span class="sxs-lookup"><span data-stu-id="a415e-113">If the resource initiating the activity is an app, this property indicates all the app related information like appId, Name, servicePrincipalId, Name.</span></span>|
|<span data-ttu-id="a415e-114">usuario</span><span class="sxs-lookup"><span data-stu-id="a415e-114">user</span></span>|[<span data-ttu-id="a415e-115">IdentidadDeUsuario</span><span class="sxs-lookup"><span data-stu-id="a415e-115">userIdentity</span></span>](useridentity.md)|<span data-ttu-id="a415e-116">Si el recurso de inicio de la actividad es un usuario, esta propiedad indica todos los el usuario relacionadas con la información como userId, nombre, UserPrinicpalName.</span><span class="sxs-lookup"><span data-stu-id="a415e-116">If the resource initiating the activity is a user, this property Indicates all the user related information like userId, Name, UserPrinicpalName.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a415e-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a415e-117">JSON representation</span></span>

<span data-ttu-id="a415e-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a415e-118">Here is a JSON representation of the resource.</span></span>

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
