# <a name="teamsappinstallation-resource-type"></a><span data-ttu-id="54598-101">tipo de recurso teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="54598-101">teamsAppInstallation resource type</span></span>



<span data-ttu-id="54598-102">[TeamsApp](teamsapp.md) instalado en un [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="54598-102">A [teamsApp](teamsapp.md) installed in a [team](team.md).</span></span> <span data-ttu-id="54598-103">Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.</span><span class="sxs-lookup"><span data-stu-id="54598-103">Any bots that are part of the app will become part of any team the app is added to.</span></span>

## <a name="methods"></a><span data-ttu-id="54598-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="54598-104">Methods</span></span>

| <span data-ttu-id="54598-105">Método</span><span class="sxs-lookup"><span data-stu-id="54598-105">Method</span></span>       | <span data-ttu-id="54598-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54598-106">Return Type</span></span>  |<span data-ttu-id="54598-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="54598-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="54598-108">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="54598-108">List apps</span></span>](../api/teamsappinstallation_list.md) | [<span data-ttu-id="54598-109">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="54598-109">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="54598-110">Enumera aplicaciones instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="54598-110">Lists apps installed in a team.</span></span>|
|[<span data-ttu-id="54598-111">Agregar aplicación</span><span class="sxs-lookup"><span data-stu-id="54598-111">Add app</span></span>](../api/teamsappinstallation_add.md) | [<span data-ttu-id="54598-112">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="54598-112">teamsAppInstallation</span></span>](teamsapp.md) | <span data-ttu-id="54598-113">Agrega (se instala) una aplicación a un equipo.</span><span class="sxs-lookup"><span data-stu-id="54598-113">Adds (installs) an app to a team.</span></span>|
|[<span data-ttu-id="54598-114">Quitar aplicación</span><span class="sxs-lookup"><span data-stu-id="54598-114">Remove app</span></span>](../api/teamsappinstallation_delete.md) | <span data-ttu-id="54598-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="54598-115">None</span></span> | <span data-ttu-id="54598-116">Quita (desinstala) una aplicación desde un equipo.</span><span class="sxs-lookup"><span data-stu-id="54598-116">Removes (uninstalls) an app from a team.</span></span>|
|[<span data-ttu-id="54598-117">Actualizar la aplicación</span><span class="sxs-lookup"><span data-stu-id="54598-117">Upgrade app</span></span>](../api/teamsappinstallation_delete.md) | <span data-ttu-id="54598-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="54598-118">None</span></span> | <span data-ttu-id="54598-119">Actualizaciones a la versión más reciente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54598-119">Upgrades to the latest version of the app.</span></span>|

## <a name="properties"></a><span data-ttu-id="54598-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54598-120">Properties</span></span>

| <span data-ttu-id="54598-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54598-121">Property</span></span>            | <span data-ttu-id="54598-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="54598-122">Type</span></span>     | <span data-ttu-id="54598-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="54598-123">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="54598-124">id</span><span class="sxs-lookup"><span data-stu-id="54598-124">id</span></span>                  | <span data-ttu-id="54598-125">string</span><span class="sxs-lookup"><span data-stu-id="54598-125">string</span></span>   | <span data-ttu-id="54598-126">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="54598-126">A unique id (not the teams appid).</span></span> |

## <a name="relationships"></a><span data-ttu-id="54598-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="54598-127">Relationships</span></span>

| <span data-ttu-id="54598-128">Relación</span><span class="sxs-lookup"><span data-stu-id="54598-128">Relationship</span></span>   | <span data-ttu-id="54598-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="54598-129">Type</span></span>    | <span data-ttu-id="54598-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="54598-130">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="54598-131">teamsApp</span><span class="sxs-lookup"><span data-stu-id="54598-131">teamsApp</span></span>|[<span data-ttu-id="54598-132">teamsApp</span><span class="sxs-lookup"><span data-stu-id="54598-132">teamsApp</span></span>](teamsapp.md)| <span data-ttu-id="54598-133">La aplicación que está instalada.</span><span class="sxs-lookup"><span data-stu-id="54598-133">The app that is installed.</span></span> |
|<span data-ttu-id="54598-134">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="54598-134">teamsAppDefinition</span></span>|[<span data-ttu-id="54598-135">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="54598-135">teamsAppDefinition</span></span>](teamsapp.md)| <span data-ttu-id="54598-136">Los detalles de esta versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="54598-136">The details of this version of the app.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="54598-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="54598-137">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="54598-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="54598-138">See also</span></span>

- [<span data-ttu-id="54598-139">teamsApp</span><span class="sxs-lookup"><span data-stu-id="54598-139">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="54598-140">teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="54598-140">teamsAppDefinition</span></span>](teamsappdefinition.md)
- [<span data-ttu-id="54598-141">teamsTab</span><span class="sxs-lookup"><span data-stu-id="54598-141">teamsTab</span></span>](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

