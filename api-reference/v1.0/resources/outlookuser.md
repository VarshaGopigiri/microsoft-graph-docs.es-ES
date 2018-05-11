# <a name="outlookuser-resource-type"></a><span data-ttu-id="ff8e1-101">Tipo de recurso outlookUser</span><span class="sxs-lookup"><span data-stu-id="ff8e1-101">outlookUser resource type</span></span>


<span data-ttu-id="ff8e1-102">Representa los servicios de Outlook disponibles para un usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-102">Represents the Outlook services available to a user.</span></span>


## <a name="methods"></a><span data-ttu-id="ff8e1-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff8e1-103">Methods</span></span>

| <span data-ttu-id="ff8e1-104">Método</span><span class="sxs-lookup"><span data-stu-id="ff8e1-104">Method</span></span>           | <span data-ttu-id="ff8e1-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff8e1-105">Return Type</span></span>    |<span data-ttu-id="ff8e1-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff8e1-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ff8e1-107">Crear categoría</span><span class="sxs-lookup"><span data-stu-id="ff8e1-107">Create category</span></span>](../api/outlookuser_post_mastercategories.md) | [<span data-ttu-id="ff8e1-108">outlookCategory</span><span class="sxs-lookup"><span data-stu-id="ff8e1-108">outlookCategory</span></span>](outlookcategory.md) |<span data-ttu-id="ff8e1-109">Crear un objeto **outlookCategory** en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-109">Create an **outlookCategory** object in the user's master list of categories.</span></span>|
|[<span data-ttu-id="ff8e1-110">Enumerar categorías</span><span class="sxs-lookup"><span data-stu-id="ff8e1-110">List categories</span></span>](../api/outlookuser_list_mastercategories.md) | <span data-ttu-id="ff8e1-111">Colección [outlookCategory](outlookcategory.md)</span><span class="sxs-lookup"><span data-stu-id="ff8e1-111">[outlookCategory](outlookcategory.md) collection</span></span> |<span data-ttu-id="ff8e1-112">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-112">Get all the categories that have been defined for the user.</span></span>|
|[<span data-ttu-id="ff8e1-113">supportedLanguages</span><span class="sxs-lookup"><span data-stu-id="ff8e1-113">supportedLanguages</span></span>](../api/outlookuser_supportedlanguages.md) | <span data-ttu-id="ff8e1-114">Colección [localeInfo](localeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ff8e1-114">[localeInfo](localeinfo.md) collection</span></span> | <span data-ttu-id="ff8e1-115">Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-115">Get the list of locales and languages that is supported for the user, as configured on the user's mailbox server.</span></span> |
|[<span data-ttu-id="ff8e1-116">supportedTimeZones</span><span class="sxs-lookup"><span data-stu-id="ff8e1-116">supportedTimeZones</span></span>](../api/outlookuser_supportedtimezones.md) | <span data-ttu-id="ff8e1-117">Colección [timeZoneInformation](timezoneinformation.md)</span><span class="sxs-lookup"><span data-stu-id="ff8e1-117">[timeZoneInformation](timezoneinformation.md) collection</span></span> | <span data-ttu-id="ff8e1-118">Obtener una lista de zonas horarias compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-118">Get the list of time zones that is supported for the user, as configured on the user's mailbox server.</span></span> |


## <a name="properties"></a><span data-ttu-id="ff8e1-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff8e1-119">Properties</span></span>
<span data-ttu-id="ff8e1-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ff8e1-120">None</span></span>

## <a name="relationships"></a><span data-ttu-id="ff8e1-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ff8e1-121">Relationships</span></span>
| <span data-ttu-id="ff8e1-122">Relación</span><span class="sxs-lookup"><span data-stu-id="ff8e1-122">Relationship</span></span> | <span data-ttu-id="ff8e1-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff8e1-123">Type</span></span>   |<span data-ttu-id="ff8e1-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff8e1-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ff8e1-125">masterCategories</span><span class="sxs-lookup"><span data-stu-id="ff8e1-125">masterCategories</span></span>|<span data-ttu-id="ff8e1-126">Colección [outlookCategory](../resources/outlookCategory.md)</span><span class="sxs-lookup"><span data-stu-id="ff8e1-126">[outlookCategory](../resources/outlookCategory.md) collection</span></span>| <span data-ttu-id="ff8e1-127">Lista de categorías definidas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ff8e1-127">A list of categories defined for the user.</span></span> | 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->