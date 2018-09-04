# <a name="add-named-item-formulalocal"></a><span data-ttu-id="d325f-101">Agregar FormulaLocal del elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="d325f-101">Add Named Item FormulaLocal</span></span>
<span data-ttu-id="d325f-102">Agrega un nuevo nombre a la colección del ámbito especificado, empleando la configuración regional del usuario para la fórmula.</span><span class="sxs-lookup"><span data-stu-id="d325f-102">Adds a new name to the collection of the given scope using the user's locale for the formula.</span></span>

## <a name="permissions"></a><span data-ttu-id="d325f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d325f-103">Permissions</span></span>
<span data-ttu-id="d325f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d325f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d325f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d325f-106">Permission type</span></span>      | <span data-ttu-id="d325f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d325f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d325f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d325f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d325f-109">Files.ReadWrite, Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="d325f-109">Files.ReadWrite, Sites.Read.All</span></span>    |
|<span data-ttu-id="d325f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d325f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d325f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d325f-111">Not supported.</span></span>    |
|<span data-ttu-id="d325f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d325f-112">Application</span></span> | <span data-ttu-id="d325f-113">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="d325f-113">Sites.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d325f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d325f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/add
POST /workbook/worksheets({id|name})/names/add

```
## <a name="request-headers"></a><span data-ttu-id="d325f-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d325f-115">Request headers</span></span>
| <span data-ttu-id="d325f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d325f-116">Name</span></span>       | <span data-ttu-id="d325f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d325f-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d325f-118">Autorización</span><span class="sxs-lookup"><span data-stu-id="d325f-118">Authorization</span></span>  | <span data-ttu-id="d325f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d325f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d325f-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d325f-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="d325f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d325f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d325f-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d325f-124">Request body</span></span>
<span data-ttu-id="d325f-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d325f-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d325f-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d325f-126">Parameter</span></span>    | <span data-ttu-id="d325f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d325f-127">Type</span></span>   |<span data-ttu-id="d325f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d325f-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d325f-129">name</span><span class="sxs-lookup"><span data-stu-id="d325f-129">name</span></span>|<span data-ttu-id="d325f-130">cadena</span><span class="sxs-lookup"><span data-stu-id="d325f-130">string</span></span>|<span data-ttu-id="d325f-131">Nombre del elemento con nombre.</span><span class="sxs-lookup"><span data-stu-id="d325f-131">The name of the named item.</span></span>|
|<span data-ttu-id="d325f-132">formula</span><span class="sxs-lookup"><span data-stu-id="d325f-132">formula</span></span>|<span data-ttu-id="d325f-133">cadena</span><span class="sxs-lookup"><span data-stu-id="d325f-133">string</span></span>|<span data-ttu-id="d325f-134">Fórmula o rango a los que se refiere el nombre.</span><span class="sxs-lookup"><span data-stu-id="d325f-134">The formula or the range that the name will refer to.</span></span>|
|<span data-ttu-id="d325f-135">comment</span><span class="sxs-lookup"><span data-stu-id="d325f-135">comment</span></span>|<span data-ttu-id="d325f-136">cadena</span><span class="sxs-lookup"><span data-stu-id="d325f-136">string</span></span>|<span data-ttu-id="d325f-137">Comentario asociado al elemento con nombre</span><span class="sxs-lookup"><span data-stu-id="d325f-137">The comment associated with the named item</span></span>|

## <a name="response"></a><span data-ttu-id="d325f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d325f-138">Response</span></span>

<span data-ttu-id="d325f-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [WorkbookNamedItem](../resources/NamedItem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d325f-139">If successful, this method returns `200 OK` response code and [groupSetting](../resources/NamedItem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d325f-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d325f-140">Example</span></span>
<span data-ttu-id="d325f-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d325f-141">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="d325f-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d325f-142">Request</span></span>
<span data-ttu-id="d325f-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d325f-143">Here is an example of the request.</span></span>

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

##### <a name="response"></a><span data-ttu-id="d325f-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d325f-144">Response</span></span>
<span data-ttu-id="d325f-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d325f-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookNamedItem"
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
    "type": "String",
    "value": "0",
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
