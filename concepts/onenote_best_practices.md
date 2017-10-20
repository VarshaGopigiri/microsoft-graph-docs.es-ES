# <a name="best-practices-for-working-with-the-onenote-api-in-microsoft-graph"></a><span data-ttu-id="1289b-101">Procedimientos recomendados para trabajar con las API de OneNote en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="1289b-101">Best practices for working with the OneNote API in Microsoft Graph</span></span>

<span data-ttu-id="1289b-102">Este artículo proporciona recomendaciones para el trabajo con las API de OneNote en Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="1289b-102">This article provides recommendations for working with the OneNote APIs in Microsoft Graph.</span></span> <span data-ttu-id="1289b-103">Estas recomendaciones se basan en respuestas a preguntas comunes que vemos en StackOverflow y Twitter.</span><span class="sxs-lookup"><span data-stu-id="1289b-103">These recommendations are based on answers to common questions we see on StackOverflow and Twitter.</span></span>

## <a name="use-select-to-select-the-minimum-set-of-properties-you-need"></a><span data-ttu-id="1289b-104">Use $select para seleccionar el conjunto mínimo de propiedades que necesita.</span><span class="sxs-lookup"><span data-stu-id="1289b-104">Use $select to select the minimum set of properties you need</span></span>
<span data-ttu-id="1289b-105">Cuando consulta un recurso (por ejemplo, las secciones dentro de un bloc de notas), realiza una solicitud similar a la siguiente.</span><span class="sxs-lookup"><span data-stu-id="1289b-105">When you query for a resource (for example, sections inside a notebook), you make a request similar to the following.</span></span>

```http
GET ~/notebooks/{id}/sections
```

<span data-ttu-id="1289b-106">Esto recupera todas las propiedades de las secciones.</span><span class="sxs-lookup"><span data-stu-id="1289b-106">This retrieves all the properties of the sections.</span></span> <span data-ttu-id="1289b-107">Pero puede que no necesite todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="1289b-107">However, you might not need all properties.</span></span> <span data-ttu-id="1289b-108">Puede usar el parámetro de consulta `$select` para que devuelva solo las propiedades que quiera, como se muestra en el siguiente ejemplo de consulta.</span><span class="sxs-lookup"><span data-stu-id="1289b-108">You can use the `$select` query parameter to return just the properties that you want, as shown in the following example.</span></span>

```http
GET ~/notebooks/{id}/sections?$select=id,displayName
```

<span data-ttu-id="1289b-109">El mismo enfoque se aplica a otras API de OneNote.</span><span class="sxs-lookup"><span data-stu-id="1289b-109">The same approach applies to other OneNote APIs.</span></span>

## <a name="use-expand-instead-of-making-multiple-api-calls"></a><span data-ttu-id="1289b-110">Use $expand en lugar de realizar varias llamadas a la API.</span><span class="sxs-lookup"><span data-stu-id="1289b-110">Use $expand instead of making multiple API calls</span></span>
<span data-ttu-id="1289b-111">Supongamos que quiere recuperar todos los grupos de sección, secciones y blocs de notas del usuario en una vista jerárquica.</span><span class="sxs-lookup"><span data-stu-id="1289b-111">Suppose you want to retrieve all of the user’s notebooks, sections, and section groups in a hierarchical view.</span></span> <span data-ttu-id="1289b-112">Pueden conseguirlo mediante el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="1289b-112">You might accomplish that by doing the following:</span></span>

* <span data-ttu-id="1289b-113">Llame a `GET ~/notebooks` para obtener la lista de blocs de notas.</span><span class="sxs-lookup"><span data-stu-id="1289b-113">Call `GET ~/notebooks` to get the list of notebooks.</span></span>
* <span data-ttu-id="1289b-114">Para todos los blocs de notas recuperados, llame a `GET ~/notebooks/{notebookId}/sections` para recuperar la lista de secciones.</span><span class="sxs-lookup"><span data-stu-id="1289b-114">For every retrieved notebook, call `GET ~/notebooks/{notebookId}/sections` to retrieve the list of sections.</span></span>
* <span data-ttu-id="1289b-115">Para todos los blocs de notas recuperados, llame a `GET ~/notebooks/{notebookId}/sectionGroups` para recuperar la lista de grupos de secciones.</span><span class="sxs-lookup"><span data-stu-id="1289b-115">For every retrieved notebook, call `GET ~/notebooks/{notebookId}/sectionGroups` to retrieve the list of section groups.</span></span>
* <span data-ttu-id="1289b-116">Opcionalmente, itere recursivamente por los grupos de sección.</span><span class="sxs-lookup"><span data-stu-id="1289b-116">Optionally recursively iterate through section groups.</span></span>

<span data-ttu-id="1289b-117">Aunque esto funcionará (con algunos ciclos de ida y vuelta al servicios adicionales), un enfoque mejor es usar el parámetro de consulta `$expand`.</span><span class="sxs-lookup"><span data-stu-id="1289b-117">While this will work (with a few extra sequential roundtrips to the service), a better approach is to use the `$expand` query parameter.</span></span> 

```http
GET ~/notebooks?$expand=sections,sectionGroups($expand=sections)
```

<span data-ttu-id="1289b-118">Esto producirá los mismos resultados en un solo ciclo de ida y vuelta, con un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1289b-118">This will yield the same results in one network roundtrip, with better performance.</span></span>

## <a name="when-getting-all-pages-for-a-user-do-so-for-each-section-separately"></a><span data-ttu-id="1289b-119">Cuando quiera obtener todas las páginas de un usuario, hágalo para cada sección por separado</span><span class="sxs-lookup"><span data-stu-id="1289b-119">When getting all pages for a user, do so for each section separately</span></span>

<span data-ttu-id="1289b-120">Aunque Microsoft Graph expone un punto de conexión para recuperar todas las páginas, esta no es la mejor forma de obtener todas las páginas a las que tiene acceso el usuario.</span><span class="sxs-lookup"><span data-stu-id="1289b-120">While Microsoft Graph exposes an endpoint to retrieve all pages, this isn't the best way to get all the pages the user has access to.</span></span> <span data-ttu-id="1289b-121">Cuando el usuario tiene demasiadas secciones, esto puede conducir a tiempos de espera o a un rendimiento incorrecto.</span><span class="sxs-lookup"><span data-stu-id="1289b-121">When the user has too many sections, this can lead to timeouts or bad performance.</span></span> <span data-ttu-id="1289b-122">Es mejor recorrer en iteración cada sección, y obtener las páginas para cada uno de ellos por separado.</span><span class="sxs-lookup"><span data-stu-id="1289b-122">It is better to iterate each section, getting pages for each one separately.</span></span>

<span data-ttu-id="1289b-123">Por ejemplo, en lugar de usar esta llamada (se pagina esta API, por lo que no podrá recuperar todas las páginas a la vez):</span><span class="sxs-lookup"><span data-stu-id="1289b-123">For example, instead of using this call (this API is paged, so you won't be able to fetch the pages all at once):</span></span>

```http
GET ~/pages
```

<span data-ttu-id="1289b-124">Es mejor usar la siguiente llamada varias veces (especialmente si no necesita todas las secciones):</span><span class="sxs-lookup"><span data-stu-id="1289b-124">It is better to use the following call several times (especially if you don't need all sections):</span></span>

```http
GET ~/sections/{id}/pages
```

<span data-ttu-id="1289b-125">Si se obtienen los metadatos de la página, se anula el orden predeterminado de `lastModifiedDateTime`.</span><span class="sxs-lookup"><span data-stu-id="1289b-125">When getting page metadata, override the default `lastModifiedDateTime` ordering.</span></span> <span data-ttu-id="1289b-126">Es más rápido obtener las páginas cuando hay que ordenarlas por `lastModifiedDateTime`.</span><span class="sxs-lookup"><span data-stu-id="1289b-126">It is faster to get pages when you don't have to sort them by `lastModifiedDateTime`.</span></span> <span data-ttu-id="1289b-127">Para ello, puede ordenarlas por cualquier otra propiedad; por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1289b-127">To do this, you can sort by any other property; for example:</span></span>

```http
GET ~/sections/{id}/pages?$select=id,title,createdDateTime&$orderby=createdDateTime
```
