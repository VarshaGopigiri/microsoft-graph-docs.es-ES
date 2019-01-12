---
title: tipo de recurso teamsAppInstallation
description: 'Un teamsApp instalado en un equipo. '
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 30a7f05d7b814fbb36c632a88f2f4e71f135d781
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955348"
---
# <a name="teamsappinstallation-resource-type"></a><span data-ttu-id="483cd-103">tipo de recurso teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="483cd-103">teamsAppInstallation resource type</span></span>

> <span data-ttu-id="483cd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="483cd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="483cd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="483cd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="483cd-106">[TeamsApp](teamsapp.md) instalado en un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="483cd-106">A [teamsApp](teamsapp.md) installed in a [team](team.md).</span></span> <span data-ttu-id="483cd-107">Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.</span><span class="sxs-lookup"><span data-stu-id="483cd-107">Any bots that are part of the app will become part of any team the app is added to.</span></span>

## <a name="methods"></a><span data-ttu-id="483cd-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="483cd-108">Methods</span></span>

| <span data-ttu-id="483cd-109">Método</span><span class="sxs-lookup"><span data-stu-id="483cd-109">Method</span></span>       | <span data-ttu-id="483cd-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="483cd-110">Return Type</span></span>  |<span data-ttu-id="483cd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="483cd-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="483cd-112">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="483cd-112">List apps</span></span>](../api/teamsappinstallation-list.md) | [<span data-ttu-id="483cd-113">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="483cd-113">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="483cd-114">Enumera aplicaciones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="483cd-114">Lists apps installed in a team.</span></span>|
|[<span data-ttu-id="483cd-115">Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="483cd-115">Add app</span></span>](../api/teamsappinstallation-add.md) | [<span data-ttu-id="483cd-116">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="483cd-116">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="483cd-117">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="483cd-117">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="483cd-118">Quitar aplicación</span><span class="sxs-lookup"><span data-stu-id="483cd-118">Remove app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="483cd-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="483cd-119">None</span></span> | <span data-ttu-id="483cd-120">Quita (desinstala) una aplicación desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="483cd-120">Removes (uninstalls) an app from a team.</span></span>|
|[<span data-ttu-id="483cd-121">Actualizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="483cd-121">Upgrade app</span></span>](../api/teamsappinstallation-delete.md) | <span data-ttu-id="483cd-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="483cd-122">None</span></span> | <span data-ttu-id="483cd-123">Actualizaciones a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="483cd-123">Upgrades to the latest version of the app.</span></span>|

## <a name="properties"></a><span data-ttu-id="483cd-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="483cd-124">Properties</span></span>

| <span data-ttu-id="483cd-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="483cd-125">Property</span></span>            | <span data-ttu-id="483cd-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="483cd-126">Type</span></span>     | <span data-ttu-id="483cd-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="483cd-127">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="483cd-128">id</span><span class="sxs-lookup"><span data-stu-id="483cd-128">id</span></span>                  | <span data-ttu-id="483cd-129">string</span><span class="sxs-lookup"><span data-stu-id="483cd-129">string</span></span>   | <span data-ttu-id="483cd-130">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="483cd-130">A unique id (not the teams appid).</span></span> |

## <a name="relationships"></a><span data-ttu-id="483cd-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="483cd-131">Relationships</span></span>

| <span data-ttu-id="483cd-132">Relación</span><span class="sxs-lookup"><span data-stu-id="483cd-132">Relationship</span></span>   | <span data-ttu-id="483cd-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="483cd-133">Type</span></span>    | <span data-ttu-id="483cd-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="483cd-134">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="483cd-135">teamsApp</span><span class="sxs-lookup"><span data-stu-id="483cd-135">teamsApp</span></span>|[<span data-ttu-id="483cd-136">teamsApp</span><span class="sxs-lookup"><span data-stu-id="483cd-136">teamsApp</span></span>](teamsapp.md)| <span data-ttu-id="483cd-137">La aplicación que está instalada.</span><span class="sxs-lookup"><span data-stu-id="483cd-137">The app that is installed.</span></span> |
|<span data-ttu-id="483cd-138">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="483cd-138">teamsAppDefinition</span></span>|[<span data-ttu-id="483cd-139">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="483cd-139">teamsAppDefinition</span></span>](teamsapp.md)| <span data-ttu-id="483cd-140">Los detalles de esta versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="483cd-140">The details of this version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="483cd-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="483cd-141">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="483cd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="483cd-142">See also</span></span>

- [<span data-ttu-id="483cd-143">teamsApp</span><span class="sxs-lookup"><span data-stu-id="483cd-143">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="483cd-144">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="483cd-144">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="483cd-145">teamsTab</span><span class="sxs-lookup"><span data-stu-id="483cd-145">teamsTab</span></span>](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

