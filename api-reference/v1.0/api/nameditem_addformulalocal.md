# <a name="add-named-item-formulalocal"></a><span data-ttu-id="59b81-101">Agregar FormulaLocal del elemento con nombre </span><span class="sxs-lookup"><span data-stu-id="59b81-101">Add Named Item FormulaLocal</span></span>
<span data-ttu-id="59b81-102">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="59b81-102">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="59b81-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59b81-103">Prerequisites</span></span>
<span data-ttu-id="59b81-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="59b81-104">One of the following **scopes** is required to execute this API:</span></span>

  * <span data-ttu-id="59b81-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="59b81-105">Files.ReadWrite</span></span>
  * <span data-ttu-id="59b81-106">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="59b81-106">Sites.Read.All</span></span>
  
## <a name="http-request"></a><span data-ttu-id="59b81-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59b81-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="59b81-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59b81-108">Request headers</span></span>
| <span data-ttu-id="59b81-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="59b81-109">Name</span></span>       | <span data-ttu-id="59b81-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="59b81-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="59b81-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="59b81-111">Authorization</span></span>  | <span data-ttu-id="59b81-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59b81-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="59b81-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59b81-114">Request body</span></span>
<span data-ttu-id="59b81-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="59b81-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="59b81-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="59b81-116">Parameter</span></span>    | <span data-ttu-id="59b81-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="59b81-117">Type</span></span>   |<span data-ttu-id="59b81-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="59b81-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="59b81-119">name</span><span class="sxs-lookup"><span data-stu-id="59b81-119">name</span></span>|<span data-ttu-id="59b81-120">string</span><span class="sxs-lookup"><span data-stu-id="59b81-120">string</span></span>|<span data-ttu-id="59b81-121">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="59b81-121">The name of the named item.</span></span>|
|<span data-ttu-id="59b81-122">formula</span><span class="sxs-lookup"><span data-stu-id="59b81-122">formula</span></span>|<span data-ttu-id="59b81-123">string</span><span class="sxs-lookup"><span data-stu-id="59b81-123">string</span></span>|<span data-ttu-id="59b81-124">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="59b81-124">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="59b81-125">comment</span><span class="sxs-lookup"><span data-stu-id="59b81-125">comment</span></span>|<span data-ttu-id="59b81-126">string</span><span class="sxs-lookup"><span data-stu-id="59b81-126">string</span></span>|<span data-ttu-id="59b81-127">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="59b81-127">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="59b81-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59b81-128">Response</span></span>

<span data-ttu-id="59b81-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [NamedItem](../resources/NamedItem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59b81-129">If successful, this method returns `200, OK` response code and [NamedItem](../resources/NamedItem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59b81-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59b81-130">Example</span></span>
<span data-ttu-id="59b81-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="59b81-131">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="59b81-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59b81-132">Request</span></span>
<span data-ttu-id="59b81-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59b81-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "NamedItemcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/addFormulaLocal
Content-type: application/json
Content-length: 54

{
  "name": "test7",
  "formula": "=SUM(Sheet2!$A$1+Sheet2!$A$2)",
  "comment": "Comment for the named item"
}
```

##### <a name="response"></a><span data-ttu-id="59b81-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59b81-134">Response</span></span>
<span data-ttu-id="59b81-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59b81-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "@odata.id": "/users('ca41eb6e-5828-486b-ab52-c3bd1f7a4047')/drive/root/workbook/names(%27test7%27)",
    "comment": "Comment for the named item",
    "name": "test7",
    "scope": "Workbook",
    "type": "Double",
    "value": 0,
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
