---
title: tipo de recurso teamsAppInstallation
description: 'Un teamsApp instalado en un equipo. '
ms.openlocfilehash: 194a0525f46f57b9caca13f6308a31d56a84a299
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029813"
---
# <a name="teamsappinstallation-resource-type"></a><span data-ttu-id="e5622-103">tipo de recurso teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="e5622-103">teamsAppInstallation resource type</span></span>



<span data-ttu-id="e5622-104">[TeamsApp](teamsapp.md) instalado en un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="e5622-104">A [teamsApp](teamsapp.md) installed in a [team](team.md).</span></span> <span data-ttu-id="e5622-105">Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.</span><span class="sxs-lookup"><span data-stu-id="e5622-105">Any bots that are part of the app will become part of any team the app is added to.</span></span>

## <a name="methods"></a><span data-ttu-id="e5622-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e5622-106">Methods</span></span>

| <span data-ttu-id="e5622-107">Método</span><span class="sxs-lookup"><span data-stu-id="e5622-107">Method</span></span>       | <span data-ttu-id="e5622-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5622-108">Return Type</span></span>  |<span data-ttu-id="e5622-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5622-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e5622-110">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="e5622-110">List apps</span></span>](../api/teamsappinstallation-list.md) | [<span data-ttu-id="e5622-111">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="e5622-111">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="e5622-112">Enumera aplicaciones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="e5622-112">Lists apps installed in a team.</span></span>|
|[<span data-ttu-id="e5622-113">Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="e5622-113">Add app</span></span>](../api/teamsappinstallation-add.md) | [<span data-ttu-id="e5622-114">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="e5622-114">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="e5622-115">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="e5622-115">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="e5622-116">Quitar aplicación</span><span class="sxs-lookup"><span data-stu-id="e5622-116">Remove app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="e5622-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e5622-117">None</span></span> | <span data-ttu-id="e5622-118">Quita (desinstala) una aplicación desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="e5622-118">Removes (uninstalls) an app from a team.</span></span>|
|[<span data-ttu-id="e5622-119">Actualizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="e5622-119">Upgrade app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="e5622-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e5622-120">None</span></span> | <span data-ttu-id="e5622-121">Actualizaciones a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5622-121">Upgrades to the latest version of the app.</span></span>|

## <a name="properties"></a><span data-ttu-id="e5622-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e5622-122">Properties</span></span>

| <span data-ttu-id="e5622-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e5622-123">Property</span></span>            | <span data-ttu-id="e5622-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5622-124">Type</span></span>     | <span data-ttu-id="e5622-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5622-125">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="e5622-126">id</span><span class="sxs-lookup"><span data-stu-id="e5622-126">id</span></span>                  | <span data-ttu-id="e5622-127">string</span><span class="sxs-lookup"><span data-stu-id="e5622-127">string</span></span>   | <span data-ttu-id="e5622-128">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="e5622-128">A unique id (not the teams appid).</span></span> |

## <a name="relationships"></a><span data-ttu-id="e5622-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e5622-129">Relationships</span></span>

| <span data-ttu-id="e5622-130">Relación</span><span class="sxs-lookup"><span data-stu-id="e5622-130">Relationship</span></span>   | <span data-ttu-id="e5622-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5622-131">Type</span></span>    | <span data-ttu-id="e5622-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5622-132">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="e5622-133">teamsApp</span><span class="sxs-lookup"><span data-stu-id="e5622-133">teamsApp</span></span>|[<span data-ttu-id="e5622-134">teamsApp</span><span class="sxs-lookup"><span data-stu-id="e5622-134">teamsApp</span></span>](teamsapp.md)| <span data-ttu-id="e5622-135">La aplicación que está instalada.</span><span class="sxs-lookup"><span data-stu-id="e5622-135">The app that is installed.</span></span> |
|<span data-ttu-id="e5622-136">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="e5622-136">teamsAppDefinition</span></span>|[<span data-ttu-id="e5622-137">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="e5622-137">teamsAppDefinition</span></span>](teamsapp.md)| <span data-ttu-id="e5622-138">Los detalles de esta versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5622-138">The details of this version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e5622-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e5622-139">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="e5622-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5622-140">See also</span></span>

- [<span data-ttu-id="e5622-141">teamsApp</span><span class="sxs-lookup"><span data-stu-id="e5622-141">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="e5622-142">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="e5622-142">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="e5622-143">teamsTab</span><span class="sxs-lookup"><span data-stu-id="e5622-143">teamsTab</span></span>](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

