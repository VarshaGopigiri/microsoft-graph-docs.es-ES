---
title: tipo de recurso teamsApp
description: Una aplicación en el catálogo de aplicaciones de Microsoft Teams.
ms.openlocfilehash: f8a96355c572287fc8bacc48f9a72e5da8d0f380
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031123"
---
# <a name="teamsapp-resource-type"></a><span data-ttu-id="75831-103">tipo de recurso teamsApp</span><span class="sxs-lookup"><span data-stu-id="75831-103">teamsApp resource type</span></span>



<span data-ttu-id="75831-104">Una aplicación en el catálogo de aplicaciones de [Los equipos de Microsoft](teams-api-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="75831-104">An app in the [Microsoft Teams](teams-api-overview.md) app catalog.</span></span>

<span data-ttu-id="75831-105">Los usuarios pueden ver estas aplicaciones en la Store Teams Microsoft, y estas aplicaciones se pueden instalar en [los equipos](team.md) mediante el método de [aplicación de agregar al equipo](../api/teamsappinstallation-add.md) .</span><span class="sxs-lookup"><span data-stu-id="75831-105">Users can see these apps in the Microsoft Teams Store, and these apps can be installed in [teams](team.md) using the [Add app to team](../api/teamsappinstallation-add.md) method.</span></span>

## <a name="methods"></a><span data-ttu-id="75831-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="75831-106">Methods</span></span>

| <span data-ttu-id="75831-107">Método</span><span class="sxs-lookup"><span data-stu-id="75831-107">Method</span></span>       | <span data-ttu-id="75831-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75831-108">Return Type</span></span>  |<span data-ttu-id="75831-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="75831-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="75831-110">Lista de aplicaciones publicadas</span><span class="sxs-lookup"><span data-stu-id="75831-110">List published apps</span></span>](../api/teamsapp-list.md) | <span data-ttu-id="75831-111">colección de [teamsApp](teamsapp.md)</span><span class="sxs-lookup"><span data-stu-id="75831-111">[teamsApp](teamsapp.md) collection</span></span> | <span data-ttu-id="75831-112">Lista de aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="75831-112">List published apps from the Microsoft Teams apps catalog.</span></span>|
|[<span data-ttu-id="75831-113">Publicar una aplicación</span><span class="sxs-lookup"><span data-stu-id="75831-113">Publish an app</span></span>](../api/teamsapp-publish.md) | [<span data-ttu-id="75831-114">teamsApp</span><span class="sxs-lookup"><span data-stu-id="75831-114">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="75831-115">Publicar una aplicación al catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="75831-115">Publish an app to your organization's app catalog.</span></span>|
|[<span data-ttu-id="75831-116">Actualizar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="75831-116">Update a published app</span></span>](../api/teamsapp-update.md) | [<span data-ttu-id="75831-117">teamsApp</span><span class="sxs-lookup"><span data-stu-id="75831-117">teamsApp</span></span>](teamsapp.md) | <span data-ttu-id="75831-118">Actualizar una aplicación publicada en el catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="75831-118">Update a published app in your organization's app catalog.</span></span>|
|[<span data-ttu-id="75831-119">Quitar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="75831-119">Remove a published app</span></span>](../api/teamsapp-delete.md) | <span data-ttu-id="75831-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="75831-120">None</span></span> | <span data-ttu-id="75831-121">Quitar una aplicación publicada de catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="75831-121">Remove a published app from your organization's app catalog.</span></span>|

## <a name="properties"></a><span data-ttu-id="75831-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75831-122">Properties</span></span>

| <span data-ttu-id="75831-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="75831-123">Property</span></span>            | <span data-ttu-id="75831-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="75831-124">Type</span></span>     | <span data-ttu-id="75831-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="75831-125">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="75831-126">id</span><span class="sxs-lookup"><span data-stu-id="75831-126">id</span></span>                  | <span data-ttu-id="75831-127">string</span><span class="sxs-lookup"><span data-stu-id="75831-127">string</span></span>   | <span data-ttu-id="75831-128">La aplicación de catálogo genera el identificador de la aplicación (diferente desde el identificador proporcionado para desarrolladores en el [paquete de la aplicación de los equipos de Microsoft zip](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="75831-128">The catalog app's generated app ID (different from the developer-provided ID in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="75831-129">externalId</span><span class="sxs-lookup"><span data-stu-id="75831-129">externalId</span></span>          | <span data-ttu-id="75831-130">string</span><span class="sxs-lookup"><span data-stu-id="75831-130">string</span></span>   | <span data-ttu-id="75831-131">El identificador del catálogo proporcionado por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="75831-131">The ID of the catalog provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="75831-132">displayName</span><span class="sxs-lookup"><span data-stu-id="75831-132">displayName</span></span>                | <span data-ttu-id="75831-133">string</span><span class="sxs-lookup"><span data-stu-id="75831-133">string</span></span>   | <span data-ttu-id="75831-134">El nombre de la aplicación de catálogo proporcionada por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="75831-134">The name of the catalog app provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="75831-135">distributionMethod</span><span class="sxs-lookup"><span data-stu-id="75831-135">distributionMethod</span></span>  | <span data-ttu-id="75831-136">teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="75831-136">teamsAppDistributionMethod</span></span>     | <span data-ttu-id="75831-137">El método de distribución para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75831-137">The method of distribution for the app.</span></span> |

### <a name="teamsappdistributionmethod-values"></a><span data-ttu-id="75831-138">valores de teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="75831-138">teamsAppDistributionMethod values</span></span>

|<span data-ttu-id="75831-139">Member</span><span class="sxs-lookup"><span data-stu-id="75831-139">Member</span></span>|<span data-ttu-id="75831-140">Valor</span><span class="sxs-lookup"><span data-stu-id="75831-140">Value</span></span>|<span data-ttu-id="75831-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="75831-141">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="75831-142">almacén</span><span class="sxs-lookup"><span data-stu-id="75831-142">store</span></span>|<span data-ttu-id="75831-143">0</span><span class="sxs-lookup"><span data-stu-id="75831-143">0</span></span>| <span data-ttu-id="75831-144">La aplicación está disponible para todos los inquilinos a través de la tienda de aplicaciones Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="75831-144">The app is available to all tenants through the Microsoft Teams app store.</span></span>|
|<span data-ttu-id="75831-145">organización</span><span class="sxs-lookup"><span data-stu-id="75831-145">organization</span></span>|<span data-ttu-id="75831-146">1</span><span class="sxs-lookup"><span data-stu-id="75831-146">1</span></span>|<span data-ttu-id="75831-147">La aplicación sólo está disponible en este inquilino.</span><span class="sxs-lookup"><span data-stu-id="75831-147">The app is available only in this tenant.</span></span>|
|<span data-ttu-id="75831-148">sideloaded</span><span class="sxs-lookup"><span data-stu-id="75831-148">sideloaded</span></span>|<span data-ttu-id="75831-149">2</span><span class="sxs-lookup"><span data-stu-id="75831-149">2</span></span>|<span data-ttu-id="75831-150">La aplicación sólo está disponible para el usuario o equipo instalado a.</span><span class="sxs-lookup"><span data-stu-id="75831-150">The app is available only to the user/team its installed to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="75831-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="75831-151">Relationships</span></span>

| <span data-ttu-id="75831-152">Relación</span><span class="sxs-lookup"><span data-stu-id="75831-152">Relationship</span></span> | <span data-ttu-id="75831-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="75831-153">Type</span></span>   | <span data-ttu-id="75831-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="75831-154">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="75831-155">appDefinitions</span><span class="sxs-lookup"><span data-stu-id="75831-155">appDefinitions</span></span>|<span data-ttu-id="75831-156">colección de [teamsAppDefinition](teamsappdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="75831-156">[teamsAppDefinition](teamsappdefinition.md) collection</span></span>| <span data-ttu-id="75831-157">Los detalles de cada versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75831-157">The details for each version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="75831-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="75831-158">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="75831-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="75831-159">See also</span></span>

- [<span data-ttu-id="75831-160">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="75831-160">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="75831-161">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="75831-161">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="75831-162">teamsTab</span><span class="sxs-lookup"><span data-stu-id="75831-162">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
