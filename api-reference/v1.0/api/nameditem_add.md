# <a name="add-named-item"></a><span data-ttu-id="6193d-101">Agregar un elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="6193d-101">Add Named Item</span></span>

<span data-ttu-id="6193d-102">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="6193d-102">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="6193d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6193d-103">Permissions</span></span>
<span data-ttu-id="6193d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6193d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6193d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6193d-106">Permission type</span></span>      | <span data-ttu-id="6193d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6193d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6193d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6193d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6193d-109">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="6193d-109">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="6193d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6193d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6193d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6193d-111">Not supported.</span></span>    |
|<span data-ttu-id="6193d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6193d-112">Application</span></span> | <span data-ttu-id="6193d-113">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="6193d-113">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="6193d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6193d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="6193d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6193d-115">Request headers</span></span>
| <span data-ttu-id="6193d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6193d-116">Name</span></span>       | <span data-ttu-id="6193d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6193d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6193d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6193d-118">Authorization</span></span>  | <span data-ttu-id="6193d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6193d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6193d-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6193d-121">Request body</span></span>
<span data-ttu-id="6193d-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6193d-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6193d-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6193d-123">Parameter</span></span>    | <span data-ttu-id="6193d-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="6193d-124">Type</span></span>   |<span data-ttu-id="6193d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="6193d-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6193d-126">name</span><span class="sxs-lookup"><span data-stu-id="6193d-126">name</span></span>|<span data-ttu-id="6193d-127">string</span><span class="sxs-lookup"><span data-stu-id="6193d-127">string</span></span>|<span data-ttu-id="6193d-128">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="6193d-128">The name of the named item.</span></span>|
|<span data-ttu-id="6193d-129">reference</span><span class="sxs-lookup"><span data-stu-id="6193d-129">reference</span></span>|<span data-ttu-id="6193d-130">string</span><span class="sxs-lookup"><span data-stu-id="6193d-130">string</span></span>|<span data-ttu-id="6193d-131">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="6193d-131">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="6193d-132">comment</span><span class="sxs-lookup"><span data-stu-id="6193d-132">comment</span></span>|<span data-ttu-id="6193d-133">string</span><span class="sxs-lookup"><span data-stu-id="6193d-133">string</span></span>|<span data-ttu-id="6193d-134">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="6193d-134">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="6193d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6193d-135">Response</span></span>

<span data-ttu-id="6193d-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [NamedItem](../resources/NamedItem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6193d-136">If successful, this method returns `200, OK` response code and [NamedItem](../resources/NamedItem.md) object in the response body.</span></span>


## <a name="example"></a><span data-ttu-id="6193d-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6193d-137">Example</span></span>
<span data-ttu-id="6193d-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6193d-138">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="6193d-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6193d-139">Request</span></span>
<span data-ttu-id="6193d-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6193d-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="6193d-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6193d-141">Response</span></span>
<span data-ttu-id="6193d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6193d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
