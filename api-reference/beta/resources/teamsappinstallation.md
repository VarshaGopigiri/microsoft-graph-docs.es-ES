---
title: tipo de recurso teamsAppInstallation
description: 'Un teamsApp instalado en un equipo. '
ms.openlocfilehash: 64573e163c0ec5ce9f3282e747dffd4ccc6718de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086147"
---
# <a name="teamsappinstallation-resource-type"></a><span data-ttu-id="39363-103">tipo de recurso teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="39363-103">teamsAppInstallation resource type</span></span>

> <span data-ttu-id="39363-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39363-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39363-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39363-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="39363-106">[TeamsApp](teamsapp.md) instalado en un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="39363-106">A [teamsApp](teamsapp.md) installed in a [team](team.md).</span></span> <span data-ttu-id="39363-107">Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.</span><span class="sxs-lookup"><span data-stu-id="39363-107">Any bots that are part of the app will become part of any team the app is added to.</span></span>

## <a name="methods"></a><span data-ttu-id="39363-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="39363-108">Methods</span></span>

| <span data-ttu-id="39363-109">Método</span><span class="sxs-lookup"><span data-stu-id="39363-109">Method</span></span>       | <span data-ttu-id="39363-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39363-110">Return Type</span></span>  |<span data-ttu-id="39363-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="39363-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="39363-112">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="39363-112">List apps</span></span>](../api/teamsappinstallation-list.md) | [<span data-ttu-id="39363-113">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="39363-113">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="39363-114">Enumera aplicaciones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="39363-114">Lists apps installed in a team.</span></span>|
|[<span data-ttu-id="39363-115">Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="39363-115">Add app</span></span>](../api/teamsappinstallation-add.md) | [<span data-ttu-id="39363-116">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="39363-116">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="39363-117">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="39363-117">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="39363-118">Quitar aplicación</span><span class="sxs-lookup"><span data-stu-id="39363-118">Remove app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="39363-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="39363-119">None</span></span> | <span data-ttu-id="39363-120">Quita (desinstala) una aplicación desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="39363-120">Removes (uninstalls) an app from a team.</span></span>|
|[<span data-ttu-id="39363-121">Actualizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="39363-121">Upgrade app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="39363-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="39363-122">None</span></span> | <span data-ttu-id="39363-123">Actualizaciones a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39363-123">Upgrades to the latest version of the app.</span></span>|

## <a name="properties"></a><span data-ttu-id="39363-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39363-124">Properties</span></span>

| <span data-ttu-id="39363-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39363-125">Property</span></span>            | <span data-ttu-id="39363-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="39363-126">Type</span></span>     | <span data-ttu-id="39363-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="39363-127">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="39363-128">id</span><span class="sxs-lookup"><span data-stu-id="39363-128">id</span></span>                  | <span data-ttu-id="39363-129">string</span><span class="sxs-lookup"><span data-stu-id="39363-129">string</span></span>   | <span data-ttu-id="39363-130">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="39363-130">A unique id (not the teams appid).</span></span> |

## <a name="relationships"></a><span data-ttu-id="39363-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="39363-131">Relationships</span></span>

| <span data-ttu-id="39363-132">Relación</span><span class="sxs-lookup"><span data-stu-id="39363-132">Relationship</span></span>   | <span data-ttu-id="39363-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="39363-133">Type</span></span>    | <span data-ttu-id="39363-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="39363-134">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="39363-135">teamsApp</span><span class="sxs-lookup"><span data-stu-id="39363-135">teamsApp</span></span>|[<span data-ttu-id="39363-136">teamsApp</span><span class="sxs-lookup"><span data-stu-id="39363-136">teamsApp</span></span>](teamsapp.md)| <span data-ttu-id="39363-137">La aplicación que está instalada.</span><span class="sxs-lookup"><span data-stu-id="39363-137">The app that is installed.</span></span> |
|<span data-ttu-id="39363-138">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="39363-138">teamsAppDefinition</span></span>|[<span data-ttu-id="39363-139">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="39363-139">teamsAppDefinition</span></span>](teamsapp.md)| <span data-ttu-id="39363-140">Los detalles de esta versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39363-140">The details of this version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="39363-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39363-141">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="39363-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="39363-142">See also</span></span>

- [<span data-ttu-id="39363-143">teamsApp</span><span class="sxs-lookup"><span data-stu-id="39363-143">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="39363-144">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="39363-144">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="39363-145">teamsTab</span><span class="sxs-lookup"><span data-stu-id="39363-145">teamsTab</span></span>](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

