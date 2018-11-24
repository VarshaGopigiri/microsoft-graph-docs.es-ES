# <a name="teamsapp-resource-type"></a><span data-ttu-id="1e6e5-101">tipo de recurso teamsApp</span><span class="sxs-lookup"><span data-stu-id="1e6e5-101">teamsApp resource type</span></span>



<span data-ttu-id="1e6e5-102">Una aplicación en el catálogo de aplicaciones de [Los equipos de Microsoft](teams_api_overview.md) .</span><span class="sxs-lookup"><span data-stu-id="1e6e5-102">An app in the [Microsoft Teams](teams_api_overview.md) app catalog.</span></span>

<span data-ttu-id="1e6e5-103">Los usuarios pueden ver estas aplicaciones en la Store Teams Microsoft, y estas aplicaciones se pueden instalar en [los equipos](team.md) mediante el método de [aplicación de agregar al equipo](../api/teamsappinstallation_add.md) .</span><span class="sxs-lookup"><span data-stu-id="1e6e5-103">Users can see these apps in the Microsoft Teams Store, and these apps can be installed in [teams](team.md) using the [Add app to team](../api/teamsappinstallation_add.md) method.</span></span>

## <a name="methods"></a><span data-ttu-id="1e6e5-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e6e5-104">Methods</span></span>

| <span data-ttu-id="1e6e5-105">Método</span><span class="sxs-lookup"><span data-stu-id="1e6e5-105">Method</span></span>       | <span data-ttu-id="1e6e5-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e6e5-106">Return Type</span></span>  |<span data-ttu-id="1e6e5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e6e5-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1e6e5-108">Lista de aplicaciones publicadas</span><span class="sxs-lookup"><span data-stu-id="1e6e5-108">List published apps</span></span>](../api/teamsapp_list.md) | <span data-ttu-id="1e6e5-109">colección de [teamsApp](teamsApp.md)</span><span class="sxs-lookup"><span data-stu-id="1e6e5-109">[teamsApp](teamsApp.md) collection</span></span> | <span data-ttu-id="1e6e5-110">Lista de aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-110">List published apps from the Microsoft Teams apps catalog.</span></span>|
|[<span data-ttu-id="1e6e5-111">Publicar una aplicación</span><span class="sxs-lookup"><span data-stu-id="1e6e5-111">Publish an app</span></span>](../api/teamsapp_publish.md) | [<span data-ttu-id="1e6e5-112">teamsApp</span><span class="sxs-lookup"><span data-stu-id="1e6e5-112">teamsApp</span></span>](teamsApp.md) | <span data-ttu-id="1e6e5-113">Publicar una aplicación al catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-113">Publish an app to your organization's app catalog.</span></span>|
|[<span data-ttu-id="1e6e5-114">Actualizar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="1e6e5-114">Update a published app</span></span>](../api/teamsapp_update.md) | [<span data-ttu-id="1e6e5-115">teamsApp</span><span class="sxs-lookup"><span data-stu-id="1e6e5-115">teamsApp</span></span>](teamsApp.md) | <span data-ttu-id="1e6e5-116">Actualizar una aplicación publicada en el catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-116">Update a published app in your organization's app catalog.</span></span>|
|[<span data-ttu-id="1e6e5-117">Quitar una aplicación publicada</span><span class="sxs-lookup"><span data-stu-id="1e6e5-117">Remove a published app</span></span>](../api/teamsapp_delete.md) | <span data-ttu-id="1e6e5-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1e6e5-118">None</span></span> | <span data-ttu-id="1e6e5-119">Quitar una aplicación publicada de catálogo de aplicaciones de la organización.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-119">Remove a published app from your organization's app catalog.</span></span>|

## <a name="properties"></a><span data-ttu-id="1e6e5-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e6e5-120">Properties</span></span>

| <span data-ttu-id="1e6e5-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e6e5-121">Property</span></span>            | <span data-ttu-id="1e6e5-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e6e5-122">Type</span></span>     | <span data-ttu-id="1e6e5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e6e5-123">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="1e6e5-124">id</span><span class="sxs-lookup"><span data-stu-id="1e6e5-124">id</span></span>                  | <span data-ttu-id="1e6e5-125">string</span><span class="sxs-lookup"><span data-stu-id="1e6e5-125">string</span></span>   | <span data-ttu-id="1e6e5-126">La aplicación de catálogo genera el identificador de la aplicación (diferente desde el identificador proporcionado para desarrolladores en el [paquete de la aplicación de los equipos de Microsoft zip](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="1e6e5-126">The catalog app's generated app ID (different from the developer-provided ID in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="1e6e5-127">externalId</span><span class="sxs-lookup"><span data-stu-id="1e6e5-127">externalId</span></span>          | <span data-ttu-id="1e6e5-128">string</span><span class="sxs-lookup"><span data-stu-id="1e6e5-128">string</span></span>   | <span data-ttu-id="1e6e5-129">El identificador del catálogo proporcionado por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="1e6e5-129">The ID of the catalog provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="1e6e5-130">displayName</span><span class="sxs-lookup"><span data-stu-id="1e6e5-130">displayName</span></span>                | <span data-ttu-id="1e6e5-131">string</span><span class="sxs-lookup"><span data-stu-id="1e6e5-131">string</span></span>   | <span data-ttu-id="1e6e5-132">El nombre de la aplicación de catálogo proporcionada por el desarrollador de aplicaciones en los [equipos de Microsoft zip de paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="1e6e5-132">The name of the catalog app provided by the app developer in the [Microsoft Teams zip app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> |
| <span data-ttu-id="1e6e5-133">distributionMethod</span><span class="sxs-lookup"><span data-stu-id="1e6e5-133">distributionMethod</span></span>  | <span data-ttu-id="1e6e5-134">teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="1e6e5-134">teamsAppDistributionMethod</span></span>     | <span data-ttu-id="1e6e5-135">El método de distribución para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-135">The method of distribution for the app.</span></span> |

### <a name="teamsappdistributionmethod-values"></a><span data-ttu-id="1e6e5-136">valores de teamsAppDistributionMethod</span><span class="sxs-lookup"><span data-stu-id="1e6e5-136">teamsAppDistributionMethod values</span></span>

|<span data-ttu-id="1e6e5-137">Member</span><span class="sxs-lookup"><span data-stu-id="1e6e5-137">Member</span></span>|<span data-ttu-id="1e6e5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="1e6e5-138">Value</span></span>|<span data-ttu-id="1e6e5-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e6e5-139">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1e6e5-140">almacén</span><span class="sxs-lookup"><span data-stu-id="1e6e5-140">store</span></span>|<span data-ttu-id="1e6e5-141">0</span><span class="sxs-lookup"><span data-stu-id="1e6e5-141">0</span></span>| <span data-ttu-id="1e6e5-142">La aplicación está disponible para todos los inquilinos a través de la tienda de aplicaciones Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-142">The app is available to all tenants through the Microsoft Teams app store.</span></span>|
|<span data-ttu-id="1e6e5-143">organización</span><span class="sxs-lookup"><span data-stu-id="1e6e5-143">organization</span></span>|<span data-ttu-id="1e6e5-144">1</span><span class="sxs-lookup"><span data-stu-id="1e6e5-144">1</span></span>|<span data-ttu-id="1e6e5-145">La aplicación sólo está disponible en este inquilino.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-145">The app is available only in this tenant.</span></span>|
|<span data-ttu-id="1e6e5-146">sideloaded</span><span class="sxs-lookup"><span data-stu-id="1e6e5-146">sideloaded</span></span>|<span data-ttu-id="1e6e5-147">2</span><span class="sxs-lookup"><span data-stu-id="1e6e5-147">2</span></span>|<span data-ttu-id="1e6e5-148">La aplicación sólo está disponible para el usuario o equipo instalado a.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-148">The app is available only to the user/team its installed to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="1e6e5-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1e6e5-149">Relationships</span></span>

| <span data-ttu-id="1e6e5-150">Relación</span><span class="sxs-lookup"><span data-stu-id="1e6e5-150">Relationship</span></span> | <span data-ttu-id="1e6e5-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e6e5-151">Type</span></span>   | <span data-ttu-id="1e6e5-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e6e5-152">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="1e6e5-153">appDefinitions</span><span class="sxs-lookup"><span data-stu-id="1e6e5-153">appDefinitions</span></span>|<span data-ttu-id="1e6e5-154">colección de [teamsAppDefinition](teamsappdefinition.md)</span><span class="sxs-lookup"><span data-stu-id="1e6e5-154">[teamsAppDefinition](teamsappdefinition.md) collection</span></span>| <span data-ttu-id="1e6e5-155">Los detalles de cada versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1e6e5-155">The details for each version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1e6e5-156">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e6e5-156">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="1e6e5-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e6e5-157">See also</span></span>

- [<span data-ttu-id="1e6e5-158">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="1e6e5-158">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="1e6e5-159">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="1e6e5-159">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="1e6e5-160">teamsTab</span><span class="sxs-lookup"><span data-stu-id="1e6e5-160">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

