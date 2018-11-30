---
title: tipo de recurso teamsApp
description: Una aplicación en el catálogo de aplicaciones de Microsoft Teams.
ms.openlocfilehash: bb9081306cbcc5d8537c86e7f3f59afff89a03b0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086149"
---
# <a name="teamsapp-resource-type"></a><span data-ttu-id="210cb-103">tipo de recurso teamsApp</span><span class="sxs-lookup"><span data-stu-id="210cb-103">teamsApp resource type</span></span>

> <span data-ttu-id="210cb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="210cb-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="210cb-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="210cb-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="210cb-106">Una aplicación en el catálogo de aplicaciones de [Los equipos de Microsoft](teams-api-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="210cb-106">An app in the [Microsoft Teams](teams-api-overview.md) app catalog.</span></span>

<span data-ttu-id="210cb-107">Los usuarios pueden ver estas aplicaciones en la Store Teams Microsoft, y estas aplicaciones se pueden instalar en [los equipos](team.md) mediante el método de [aplicación de agregar al equipo](../api/teamsappinstallation-add.md) .</span><span class="sxs-lookup"><span data-stu-id="210cb-107">Users can see these apps in the Microsoft Teams Store, and these apps can be installed in [teams](team.md) using the [Add app to team](../api/teamsappinstallation-add.md) method.</span></span>

## <a name="methods"></a><span data-ttu-id="210cb-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="210cb-108">Methods</span></span>

| <span data-ttu-id="210cb-109">Método</span><span class="sxs-lookup"><span data-stu-id="210cb-109">Method</span></span>       | <span data-ttu-id="210cb-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="210cb-110">Return Type</span></span>  |<span data-ttu-id="210cb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="210cb-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="210cb-112">Lista de aplicaciones publicadas</span><span class="sxs-lookup"><span data-stu-id="210cb-112">List published apps</span></span>](../api/teamsapp-list.md) | <span data-ttu-id="210cb-113">colección de [teamsApp](teamsapp.md)</span><span class="sxs-lookup"><span data-stu-id="210cb-113">[teamsApp](teamsapp.md) collection</span></span> | <span data-ttu-id="210cb-114">Lista de aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="210cb-114">List published apps from the Microsoft Teams apps catalog.</span></span>|
|[<span data-ttu-id="210cb-115">Publicar una aplicación</span><span class="sxs-lookup"><span data-stu-id="210cb-115">Publish an app</span></span>](../api/teamsapp-publish.md) | [<span data-ttu-id="210cb-116">teamsApp</span><span class="sxs-lookup"><span data-stu-id="210cb-116">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="210cb-117">Publicar una aplicación al catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="210cb-117">Publish an app to your organization's app catalog.</span></span>|
|[<span data-ttu-id="210cb-118">Actualizar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="210cb-118">Update a published app</span></span>](../api/teamsapp-update.md) | [<span data-ttu-id="210cb-119">teamsApp</span><span class="sxs-lookup"><span data-stu-id="210cb-119">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="210cb-120">Actualizar una aplicación publicada en el catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="210cb-120">Update a published app in your organization's app catalog.</span></span>|
|[<span data-ttu-id="210cb-121">Quitar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="210cb-121">Remove a published app</span></span>](../api/teamsapp-delete.md) | <span data-ttu-id="210cb-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="210cb-122">None</span></span> | <span data-ttu-id="210cb-123">Quitar una aplicación publicada de catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="210cb-123">Remove a published app from your organization's app catalog.</span></span>|

## <a name="properties"></a><span data-ttu-id="210cb-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="210cb-124">Properties</span></span>

| <span data-ttu-id="210cb-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="210cb-125">Property</span></span>            | <span data-ttu-id="210cb-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="210cb-126">Type</span></span>     | <span data-ttu-id="210cb-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="210cb-127">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="210cb-128">id</span><span class="sxs-lookup"><span data-stu-id="210cb-128">id</span></span>                  | <span data-ttu-id="210cb-129">string</span><span class="sxs-lookup"><span data-stu-id="210cb-129">string</span></span>   | <span data-ttu-id="210cb-130">La aplicación de catálogo genera el identificador de la aplicación (diferente desde el identificador proporcionado para desarrolladores en el [paquete de la aplicación de los equipos de Microsoft zip](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="210cb-130">The catalog app's generated app ID (different from the developer-provided ID in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="210cb-131">externalId</span><span class="sxs-lookup"><span data-stu-id="210cb-131">externalId</span></span>          | <span data-ttu-id="210cb-132">string</span><span class="sxs-lookup"><span data-stu-id="210cb-132">string</span></span>   | <span data-ttu-id="210cb-133">El identificador del catálogo proporcionado por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="210cb-133">The ID of the catalog provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="210cb-134">displayName</span><span class="sxs-lookup"><span data-stu-id="210cb-134">displayName</span></span>                | <span data-ttu-id="210cb-135">string</span><span class="sxs-lookup"><span data-stu-id="210cb-135">string</span></span>   | <span data-ttu-id="210cb-136">El nombre de la aplicación de catálogo proporcionada por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="210cb-136">The name of the catalog app provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="210cb-137">distributionMethod</span><span class="sxs-lookup"><span data-stu-id="210cb-137">distributionMethod</span></span>  | <span data-ttu-id="210cb-138">teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="210cb-138">teamsAppDistributionMethod</span></span>     | <span data-ttu-id="210cb-139">El método de distribución para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="210cb-139">The method of distribution for the app.</span></span> |

### <a name="teamsappdistributionmethod-values"></a><span data-ttu-id="210cb-140">valores de teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="210cb-140">teamsAppDistributionMethod values</span></span>

|<span data-ttu-id="210cb-141">Member</span><span class="sxs-lookup"><span data-stu-id="210cb-141">Member</span></span>|<span data-ttu-id="210cb-142">Valor</span><span class="sxs-lookup"><span data-stu-id="210cb-142">Value</span></span>|<span data-ttu-id="210cb-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="210cb-143">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="210cb-144">almacén</span><span class="sxs-lookup"><span data-stu-id="210cb-144">store</span></span>|<span data-ttu-id="210cb-145">0</span><span class="sxs-lookup"><span data-stu-id="210cb-145">0</span></span>| <span data-ttu-id="210cb-146">La aplicación está disponible para todos los inquilinos a través de la tienda de aplicaciones Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="210cb-146">The app is available to all tenants through the Microsoft Teams app store.</span></span>|
|<span data-ttu-id="210cb-147">organización</span><span class="sxs-lookup"><span data-stu-id="210cb-147">organization</span></span>|<span data-ttu-id="210cb-148">1</span><span class="sxs-lookup"><span data-stu-id="210cb-148">1</span></span>|<span data-ttu-id="210cb-149">La aplicación sólo está disponible en este inquilino.</span><span class="sxs-lookup"><span data-stu-id="210cb-149">The app is available only in this tenant.</span></span>|
|<span data-ttu-id="210cb-150">sideloaded</span><span class="sxs-lookup"><span data-stu-id="210cb-150">sideloaded</span></span>|<span data-ttu-id="210cb-151">2</span><span class="sxs-lookup"><span data-stu-id="210cb-151">2</span></span>|<span data-ttu-id="210cb-152">La aplicación sólo está disponible para el usuario o equipo instalado a.</span><span class="sxs-lookup"><span data-stu-id="210cb-152">The app is available only to the user/team its installed to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="210cb-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="210cb-153">Relationships</span></span>

| <span data-ttu-id="210cb-154">Relación</span><span class="sxs-lookup"><span data-stu-id="210cb-154">Relationship</span></span> | <span data-ttu-id="210cb-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="210cb-155">Type</span></span>   | <span data-ttu-id="210cb-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="210cb-156">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="210cb-157">appDefinitions</span><span class="sxs-lookup"><span data-stu-id="210cb-157">appDefinitions</span></span>|<span data-ttu-id="210cb-158">colección de [teamsAppDefinition](teamsappdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="210cb-158">[teamsAppDefinition](teamsappdefinition.md) collection</span></span>| <span data-ttu-id="210cb-159">Los detalles de cada versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="210cb-159">The details for each version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="210cb-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="210cb-160">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="210cb-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="210cb-161">See also</span></span>

- [<span data-ttu-id="210cb-162">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="210cb-162">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="210cb-163">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="210cb-163">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="210cb-164">teamsTab</span><span class="sxs-lookup"><span data-stu-id="210cb-164">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

