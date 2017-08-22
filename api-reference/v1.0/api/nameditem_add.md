# <a name="add-named-item"></a><span data-ttu-id="744a0-101">Agregar un elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="744a0-101">Add Named Item</span></span>

<span data-ttu-id="744a0-102">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="744a0-102">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="744a0-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="744a0-103">Prerequisites</span></span>
<span data-ttu-id="744a0-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="744a0-104">One of the following **scopes** is required to execute this API:</span></span>

  * <span data-ttu-id="744a0-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="744a0-105">Files.ReadWrite</span></span>
  * <span data-ttu-id="744a0-106">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="744a0-106">Sites.Read.All</span></span>
  
## <a name="http-request"></a><span data-ttu-id="744a0-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="744a0-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="744a0-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="744a0-108">Request headers</span></span>
| <span data-ttu-id="744a0-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="744a0-109">Name</span></span>       | <span data-ttu-id="744a0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="744a0-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="744a0-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="744a0-111">Authorization</span></span>  | <span data-ttu-id="744a0-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="744a0-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="744a0-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="744a0-114">Request body</span></span>
<span data-ttu-id="744a0-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="744a0-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="744a0-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="744a0-116">Parameter</span></span>    | <span data-ttu-id="744a0-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="744a0-117">Type</span></span>   |<span data-ttu-id="744a0-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="744a0-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="744a0-119">name</span><span class="sxs-lookup"><span data-stu-id="744a0-119">name</span></span>|<span data-ttu-id="744a0-120">string</span><span class="sxs-lookup"><span data-stu-id="744a0-120">string</span></span>|<span data-ttu-id="744a0-121">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="744a0-121">The name of the named item.</span></span>|
|<span data-ttu-id="744a0-122">reference</span><span class="sxs-lookup"><span data-stu-id="744a0-122">reference</span></span>|<span data-ttu-id="744a0-123">string</span><span class="sxs-lookup"><span data-stu-id="744a0-123">string</span></span>|<span data-ttu-id="744a0-124">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="744a0-124">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="744a0-125">comment</span><span class="sxs-lookup"><span data-stu-id="744a0-125">comment</span></span>|<span data-ttu-id="744a0-126">string</span><span class="sxs-lookup"><span data-stu-id="744a0-126">string</span></span>|<span data-ttu-id="744a0-127">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="744a0-127">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="744a0-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="744a0-128">Response</span></span>

<span data-ttu-id="744a0-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [NamedItem](../resources/NamedItem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="744a0-129">If successful, this method returns `200, OK` response code and [NamedItem](../resources/NamedItem.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="744a0-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="744a0-130">Example</span></span>
<span data-ttu-id="744a0-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="744a0-131">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="744a0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="744a0-132">Request</span></span>
<span data-ttu-id="744a0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="744a0-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/add
Content-type: application/json
Content-length: 54

{
  "name": "test5",
  "reference": "=Sheet1!$F$15:$N$27",
  "comment": "Comment for the named item"
}


```

##### <a name="response"></a><span data-ttu-id="744a0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="744a0-134">Response</span></span>
<span data-ttu-id="744a0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="744a0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.namedItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 109

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#workbookNamedItem",
    "@odata.type": "#microsoft.graph.workbookNamedItem",
    "@odata.id": "/users('ca41eb6e-5828-486b-ab52-c3bd1f7a4047')/drive/root/workbook/names(%27test5%27)",
    "comment": "Comment for the named item",
    "name": "test5",
    "scope": "Workbook",
    "type": "Range",
    "value": "Sheet1!$F$15:$N$27",
    "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItemCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
