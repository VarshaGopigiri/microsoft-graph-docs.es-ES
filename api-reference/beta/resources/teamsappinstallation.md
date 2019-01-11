---
title: tipo de recurso teamsAppInstallation
description: 'Un teamsApp instalado en un equipo. '
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 5eca63cb3385fa03f8dffadff0482dc79a1dcfe3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871515"
---
# <a name="teamsappinstallation-resource-type"></a><span data-ttu-id="9b611-103">tipo de recurso teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="9b611-103">teamsAppInstallation resource type</span></span>

> <span data-ttu-id="9b611-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b611-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b611-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b611-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b611-106">[TeamsApp](teamsapp.md) instalado en un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="9b611-106">A [teamsApp](teamsapp.md) installed in a [team](team.md).</span></span> <span data-ttu-id="9b611-107">Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.</span><span class="sxs-lookup"><span data-stu-id="9b611-107">Any bots that are part of the app will become part of any team the app is added to.</span></span>

## <a name="methods"></a><span data-ttu-id="9b611-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b611-108">Methods</span></span>

| <span data-ttu-id="9b611-109">Método</span><span class="sxs-lookup"><span data-stu-id="9b611-109">Method</span></span>       | <span data-ttu-id="9b611-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b611-110">Return Type</span></span>  |<span data-ttu-id="9b611-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b611-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9b611-112">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="9b611-112">List apps</span></span>](../api/teamsappinstallation-list.md) | [<span data-ttu-id="9b611-113">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="9b611-113">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="9b611-114">Enumera aplicaciones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="9b611-114">Lists apps installed in a team.</span></span>|
|[<span data-ttu-id="9b611-115">Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="9b611-115">Add app</span></span>](../api/teamsappinstallation-add.md) | [<span data-ttu-id="9b611-116">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="9b611-116">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="9b611-117">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="9b611-117">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="9b611-118">Quitar aplicación</span><span class="sxs-lookup"><span data-stu-id="9b611-118">Remove app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="9b611-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b611-119">None</span></span> | <span data-ttu-id="9b611-120">Quita (desinstala) una aplicación desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="9b611-120">Removes (uninstalls) an app from a team.</span></span>|
|[<span data-ttu-id="9b611-121">Actualizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="9b611-121">Upgrade app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="9b611-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b611-122">None</span></span> | <span data-ttu-id="9b611-123">Actualizaciones a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b611-123">Upgrades to the latest version of the app.</span></span>|

## <a name="properties"></a><span data-ttu-id="9b611-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b611-124">Properties</span></span>

| <span data-ttu-id="9b611-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b611-125">Property</span></span>            | <span data-ttu-id="9b611-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b611-126">Type</span></span>     | <span data-ttu-id="9b611-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b611-127">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="9b611-128">id</span><span class="sxs-lookup"><span data-stu-id="9b611-128">id</span></span>                  | <span data-ttu-id="9b611-129">string</span><span class="sxs-lookup"><span data-stu-id="9b611-129">string</span></span>   | <span data-ttu-id="9b611-130">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="9b611-130">A unique id (not the teams appid).</span></span> |

## <a name="relationships"></a><span data-ttu-id="9b611-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b611-131">Relationships</span></span>

| <span data-ttu-id="9b611-132">Relación</span><span class="sxs-lookup"><span data-stu-id="9b611-132">Relationship</span></span>   | <span data-ttu-id="9b611-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b611-133">Type</span></span>    | <span data-ttu-id="9b611-134">Description</span><span class="sxs-lookup"><span data-stu-id="9b611-134">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="9b611-135">teamsApp</span><span class="sxs-lookup"><span data-stu-id="9b611-135">teamsApp</span></span>|[<span data-ttu-id="9b611-136">teamsApp</span><span class="sxs-lookup"><span data-stu-id="9b611-136">teamsApp</span></span>](teamsapp.md)| <span data-ttu-id="9b611-137">La aplicación que está instalada.</span><span class="sxs-lookup"><span data-stu-id="9b611-137">The app that is installed.</span></span> |
|<span data-ttu-id="9b611-138">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="9b611-138">teamsAppDefinition</span></span>|[<span data-ttu-id="9b611-139">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="9b611-139">teamsAppDefinition</span></span>](teamsapp.md)| <span data-ttu-id="9b611-140">Los detalles de esta versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9b611-140">The details of this version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9b611-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b611-141">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsAppInstallation",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
}
```

# <a name="see-also"></a><span data-ttu-id="9b611-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b611-142">See also</span></span>

- [<span data-ttu-id="9b611-143">teamsApp</span><span class="sxs-lookup"><span data-stu-id="9b611-143">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="9b611-144">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="9b611-144">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="9b611-145">teamsTab</span><span class="sxs-lookup"><span data-stu-id="9b611-145">teamsTab</span></span>](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

