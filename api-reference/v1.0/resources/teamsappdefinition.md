# <a name="teamsappdefinition-resource-type"></a><span data-ttu-id="4da61-101">tipo de recurso teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="4da61-101">teamsAppDefinition resource type</span></span>



<span data-ttu-id="4da61-102">Los detalles de una versión de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="4da61-102">The details of one version of a [teamsApp](teamsapp.md).</span></span>

## <a name="properties"></a><span data-ttu-id="4da61-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4da61-103">Properties</span></span>

| <span data-ttu-id="4da61-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4da61-104">Property</span></span>            | <span data-ttu-id="4da61-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="4da61-105">Type</span></span>     | <span data-ttu-id="4da61-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="4da61-106">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="4da61-107">id</span><span class="sxs-lookup"><span data-stu-id="4da61-107">id</span></span>                  | <span data-ttu-id="4da61-108">string</span><span class="sxs-lookup"><span data-stu-id="4da61-108">string</span></span>   | <span data-ttu-id="4da61-109">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="4da61-109">A unique id (not the teams appid).</span></span> |
| <span data-ttu-id="4da61-110">teamsAppId</span><span class="sxs-lookup"><span data-stu-id="4da61-110">teamsAppId</span></span>          | <span data-ttu-id="4da61-111">string</span><span class="sxs-lookup"><span data-stu-id="4da61-111">string</span></span>   | <span data-ttu-id="4da61-112">El identificador de manifiesto de la aplicación de los equipos.</span><span class="sxs-lookup"><span data-stu-id="4da61-112">The id from the Teams App manifest.</span></span> |
| <span data-ttu-id="4da61-113">displayName</span><span class="sxs-lookup"><span data-stu-id="4da61-113">displayName</span></span>         | <span data-ttu-id="4da61-114">string</span><span class="sxs-lookup"><span data-stu-id="4da61-114">string</span></span>   | <span data-ttu-id="4da61-115">El nombre de la aplicación proporcionada por el desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4da61-115">The name of the app provided by the app developer.</span></span> |
| <span data-ttu-id="4da61-116">version</span><span class="sxs-lookup"><span data-stu-id="4da61-116">version</span></span>             | <span data-ttu-id="4da61-117">string</span><span class="sxs-lookup"><span data-stu-id="4da61-117">string</span></span>   | <span data-ttu-id="4da61-118">El número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4da61-118">The version number of the application.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4da61-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4da61-119">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsAppDefinition",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "teamsAppId": "string",
  "displayName": "Test App",
  "version": "1.0.0",
}
```

# <a name="see-also"></a><span data-ttu-id="4da61-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4da61-120">See also</span></span>

- [<span data-ttu-id="4da61-121">teamsApp</span><span class="sxs-lookup"><span data-stu-id="4da61-121">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="4da61-122">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="4da61-122">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="4da61-123">teamsTab</span><span class="sxs-lookup"><span data-stu-id="4da61-123">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

