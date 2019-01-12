---
title: tipo de recurso teamsApp
description: Una aplicación en el catálogo de aplicaciones de Microsoft Teams.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 2f1b45f60e9586d148a08310e9d19b1a3e6c52e4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912060"
---
# <a name="teamsapp-resource-type"></a><span data-ttu-id="6f4a5-103">tipo de recurso teamsApp</span><span class="sxs-lookup"><span data-stu-id="6f4a5-103">teamsApp resource type</span></span>

> <span data-ttu-id="6f4a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6f4a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6f4a5-106">Una aplicación en el catálogo de aplicaciones de [Los equipos de Microsoft](teams-api-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="6f4a5-106">An app in the [Microsoft Teams](teams-api-overview.md) app catalog.</span></span>

<span data-ttu-id="6f4a5-107">Los usuarios pueden ver estas aplicaciones en la Store Teams Microsoft, y estas aplicaciones se pueden instalar en [los equipos](team.md) mediante el método de [aplicación de agregar al equipo](../api/teamsappinstallation-add.md) .</span><span class="sxs-lookup"><span data-stu-id="6f4a5-107">Users can see these apps in the Microsoft Teams Store, and these apps can be installed in [teams](team.md) using the [Add app to team](../api/teamsappinstallation-add.md) method.</span></span>

## <a name="methods"></a><span data-ttu-id="6f4a5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6f4a5-108">Methods</span></span>

| <span data-ttu-id="6f4a5-109">Método</span><span class="sxs-lookup"><span data-stu-id="6f4a5-109">Method</span></span>       | <span data-ttu-id="6f4a5-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f4a5-110">Return Type</span></span>  |<span data-ttu-id="6f4a5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a5-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6f4a5-112">Lista de aplicaciones publicadas</span><span class="sxs-lookup"><span data-stu-id="6f4a5-112">List published apps</span></span>](../api/teamsapp-list.md) | <span data-ttu-id="6f4a5-113">colección de [teamsApp](teamsapp.md)</span><span class="sxs-lookup"><span data-stu-id="6f4a5-113">[teamsApp](teamsapp.md) collection</span></span> | <span data-ttu-id="6f4a5-114">Lista de aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-114">List published apps from the Microsoft Teams apps catalog.</span></span>|
|[<span data-ttu-id="6f4a5-115">Publicar una aplicación</span><span class="sxs-lookup"><span data-stu-id="6f4a5-115">Publish an app</span></span>](../api/teamsapp-publish.md) | [<span data-ttu-id="6f4a5-116">teamsApp</span><span class="sxs-lookup"><span data-stu-id="6f4a5-116">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="6f4a5-117">Publicar una aplicación al catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-117">Publish an app to your organization's app catalog.</span></span>|
|[<span data-ttu-id="6f4a5-118">Actualizar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="6f4a5-118">Update a published app</span></span>](../api/teamsapp-update.md) | [<span data-ttu-id="6f4a5-119">teamsApp</span><span class="sxs-lookup"><span data-stu-id="6f4a5-119">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="6f4a5-120">Actualizar una aplicación publicada en el catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-120">Update a published app in your organization's app catalog.</span></span>|
|[<span data-ttu-id="6f4a5-121">Quitar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="6f4a5-121">Remove a published app</span></span>](../api/teamsapp-delete.md) | <span data-ttu-id="6f4a5-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6f4a5-122">None</span></span> | <span data-ttu-id="6f4a5-123">Quitar una aplicación publicada de catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-123">Remove a published app from your organization's app catalog.</span></span>|

## <a name="properties"></a><span data-ttu-id="6f4a5-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f4a5-124">Properties</span></span>

| <span data-ttu-id="6f4a5-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f4a5-125">Property</span></span>            | <span data-ttu-id="6f4a5-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f4a5-126">Type</span></span>     | <span data-ttu-id="6f4a5-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a5-127">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="6f4a5-128">id</span><span class="sxs-lookup"><span data-stu-id="6f4a5-128">id</span></span>                  | <span data-ttu-id="6f4a5-129">string</span><span class="sxs-lookup"><span data-stu-id="6f4a5-129">string</span></span>   | <span data-ttu-id="6f4a5-130">La aplicación de catálogo genera el identificador de la aplicación (diferente desde el identificador proporcionado para desarrolladores en el [paquete de la aplicación de los equipos de Microsoft zip](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="6f4a5-130">The catalog app's generated app ID (different from the developer-provided ID in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="6f4a5-131">externalId</span><span class="sxs-lookup"><span data-stu-id="6f4a5-131">externalId</span></span>          | <span data-ttu-id="6f4a5-132">string</span><span class="sxs-lookup"><span data-stu-id="6f4a5-132">string</span></span>   | <span data-ttu-id="6f4a5-133">El identificador del catálogo proporcionado por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="6f4a5-133">The ID of the catalog provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="6f4a5-134">displayName</span><span class="sxs-lookup"><span data-stu-id="6f4a5-134">displayName</span></span>                | <span data-ttu-id="6f4a5-135">string</span><span class="sxs-lookup"><span data-stu-id="6f4a5-135">string</span></span>   | <span data-ttu-id="6f4a5-136">El nombre de la aplicación de catálogo proporcionada por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="6f4a5-136">The name of the catalog app provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="6f4a5-137">distributionMethod</span><span class="sxs-lookup"><span data-stu-id="6f4a5-137">distributionMethod</span></span>  | <span data-ttu-id="6f4a5-138">teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="6f4a5-138">teamsAppDistributionMethod</span></span>     | <span data-ttu-id="6f4a5-139">El método de distribución para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-139">The method of distribution for the app.</span></span> |

### <a name="teamsappdistributionmethod-values"></a><span data-ttu-id="6f4a5-140">valores de teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="6f4a5-140">teamsAppDistributionMethod values</span></span>

|<span data-ttu-id="6f4a5-141">Miembro	</span><span class="sxs-lookup"><span data-stu-id="6f4a5-141">Member</span></span>|<span data-ttu-id="6f4a5-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6f4a5-142">Value</span></span>|<span data-ttu-id="6f4a5-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a5-143">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6f4a5-144">almacén</span><span class="sxs-lookup"><span data-stu-id="6f4a5-144">store</span></span>|<span data-ttu-id="6f4a5-145">0</span><span class="sxs-lookup"><span data-stu-id="6f4a5-145">0</span></span>| <span data-ttu-id="6f4a5-146">La aplicación está disponible para todos los inquilinos a través de la tienda de aplicaciones Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-146">The app is available to all tenants through the Microsoft Teams app store.</span></span>|
|<span data-ttu-id="6f4a5-147">organización</span><span class="sxs-lookup"><span data-stu-id="6f4a5-147">organization</span></span>|<span data-ttu-id="6f4a5-148">1</span><span class="sxs-lookup"><span data-stu-id="6f4a5-148">1</span></span>|<span data-ttu-id="6f4a5-149">La aplicación sólo está disponible en este inquilino.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-149">The app is available only in this tenant.</span></span>|
|<span data-ttu-id="6f4a5-150">sideloaded</span><span class="sxs-lookup"><span data-stu-id="6f4a5-150">sideloaded</span></span>|<span data-ttu-id="6f4a5-151">2</span><span class="sxs-lookup"><span data-stu-id="6f4a5-151">2</span></span>|<span data-ttu-id="6f4a5-152">La aplicación sólo está disponible para el usuario o equipo instalado a.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-152">The app is available only to the user/team its installed to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6f4a5-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6f4a5-153">Relationships</span></span>

| <span data-ttu-id="6f4a5-154">Relación</span><span class="sxs-lookup"><span data-stu-id="6f4a5-154">Relationship</span></span> | <span data-ttu-id="6f4a5-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f4a5-155">Type</span></span>   | <span data-ttu-id="6f4a5-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f4a5-156">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="6f4a5-157">appDefinitions</span><span class="sxs-lookup"><span data-stu-id="6f4a5-157">appDefinitions</span></span>|<span data-ttu-id="6f4a5-158">colección de [teamsAppDefinition](teamsappdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="6f4a5-158">[teamsAppDefinition](teamsappdefinition.md) collection</span></span>| <span data-ttu-id="6f4a5-159">Los detalles de cada versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f4a5-159">The details for each version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="6f4a5-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6f4a5-160">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsApp",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "externalId": "string",
  "displayName": "Test App",
  "distributionMethod": "Organization"
}
```

# <a name="see-also"></a><span data-ttu-id="6f4a5-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f4a5-161">See also</span></span>

- [<span data-ttu-id="6f4a5-162">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="6f4a5-162">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="6f4a5-163">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="6f4a5-163">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="6f4a5-164">teamsTab</span><span class="sxs-lookup"><span data-stu-id="6f4a5-164">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

