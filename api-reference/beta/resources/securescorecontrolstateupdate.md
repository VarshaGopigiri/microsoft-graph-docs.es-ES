---
title: " tipo de recurso secureScoreControlStateUpdate"
description: Este recurso contiene el historial de Estados del control actualizado por usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).
localization_priority: Normal
ms.openlocfilehash: 8d8c3122a6263ebc7b10b5edfb823953e2d587fc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888924"
---
 #  <a name="securescorecontrolstateupdate-resource-type"></a><span data-ttu-id="27fe6-103">tipo de recurso secureScoreControlStateUpdate</span><span class="sxs-lookup"><span data-stu-id="27fe6-103">secureScoreControlStateUpdate resource type</span></span>
<span data-ttu-id="27fe6-104">Contiene el historial de los Estados de control actualizado por el usuario (los Estados de control incluyen predeterminado, Ignored, otros, revisada).</span><span class="sxs-lookup"><span data-stu-id="27fe6-104">Contains the history of the control states updated by the user (control states include Default, Ignored, ThirdParty, Reviewed).</span></span>

|<span data-ttu-id="27fe6-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27fe6-105">Property</span></span> |<span data-ttu-id="27fe6-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="27fe6-106">Type</span></span> |<span data-ttu-id="27fe6-107">Description</span><span class="sxs-lookup"><span data-stu-id="27fe6-107">Description</span></span> |
|:--|:--|:--|
|<span data-ttu-id="27fe6-108">assignedTo</span><span class="sxs-lookup"><span data-stu-id="27fe6-108">assignedTo</span></span> | <span data-ttu-id="27fe6-109">string</span><span class="sxs-lookup"><span data-stu-id="27fe6-109">string</span></span> | <span data-ttu-id="27fe6-110">Asignar el control para el usuario que llevará a cabo la acción</span><span class="sxs-lookup"><span data-stu-id="27fe6-110">Assign the control to the user who will take the action</span></span> |
|<span data-ttu-id="27fe6-111">comment</span><span class="sxs-lookup"><span data-stu-id="27fe6-111">comment</span></span> | <span data-ttu-id="27fe6-112">string</span><span class="sxs-lookup"><span data-stu-id="27fe6-112">string</span></span> | <span data-ttu-id="27fe6-113">Proporciona un comentario opcional sobre el control</span><span class="sxs-lookup"><span data-stu-id="27fe6-113">Provides optional comment about the control</span></span> |
|<span data-ttu-id="27fe6-114">state</span><span class="sxs-lookup"><span data-stu-id="27fe6-114">state</span></span> | <span data-ttu-id="27fe6-115">string</span><span class="sxs-lookup"><span data-stu-id="27fe6-115">string</span></span> | <span data-ttu-id="27fe6-116">Estado del control se puede modificar mediante el comando de revisión (ej: omite otros etcetera)</span><span class="sxs-lookup"><span data-stu-id="27fe6-116">State of the control can be modified using PATCH command(Ex: ignored, thirdParty etc)</span></span> |
|<span data-ttu-id="27fe6-117">updatedBy</span><span class="sxs-lookup"><span data-stu-id="27fe6-117">updatedBy</span></span> | <span data-ttu-id="27fe6-118">string</span><span class="sxs-lookup"><span data-stu-id="27fe6-118">string</span></span> |<span data-ttu-id="27fe6-119">Identificador del usuario que se actualizó el estado de inquilinos</span><span class="sxs-lookup"><span data-stu-id="27fe6-119">ID of the user who updated tenant state</span></span> |
|<span data-ttu-id="27fe6-120">updatedDateTime</span><span class="sxs-lookup"><span data-stu-id="27fe6-120">updatedDateTime</span></span> | <span data-ttu-id="27fe6-121">¿DateTimeOffset?</span><span class="sxs-lookup"><span data-stu-id="27fe6-121">DateTimeOffset?</span></span> |<span data-ttu-id="27fe6-122">En el control que se actualizó el estado de tiempo</span><span class="sxs-lookup"><span data-stu-id="27fe6-122">Time at which control state was updated</span></span> |
 ## <a name="json-representation"></a><span data-ttu-id="27fe6-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27fe6-123">JSON representation</span></span>
 <span data-ttu-id="27fe6-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="27fe6-124">The following is a JSON representation of the resource.</span></span>
 <!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.secureScoreControlStateUpdate"
}-->
 ```json
{
  "assignedTo": "String",
  "comment": "Double",
  "state": "Double",
  "updatedBy": "Double",
  "updatedDateTime": "Double"
}
 ```
 <!-- {
  "type": "#page.annotation",
  "description": "secureScoreControlStateUpdate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
