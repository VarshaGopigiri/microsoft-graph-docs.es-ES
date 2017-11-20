# <a name="nameditem-range"></a><span data-ttu-id="47de2-101">NamedItem: Range</span><span class="sxs-lookup"><span data-stu-id="47de2-101">NamedItem: Range</span></span>

<span data-ttu-id="47de2-p101">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="47de2-p101">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>
## <a name="permissions"></a><span data-ttu-id="47de2-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="47de2-104">Permissions</span></span>
<span data-ttu-id="47de2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="47de2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="47de2-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47de2-107">Permission type</span></span>      | <span data-ttu-id="47de2-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47de2-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="47de2-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47de2-109">Delegated (work or school account)</span></span> | <span data-ttu-id="47de2-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="47de2-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="47de2-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47de2-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="47de2-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47de2-112">Not supported.</span></span>    |
|<span data-ttu-id="47de2-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47de2-113">Application</span></span> | <span data-ttu-id="47de2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47de2-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="47de2-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47de2-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/Range

```
## <a name="request-headers"></a><span data-ttu-id="47de2-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47de2-116">Request headers</span></span>
| <span data-ttu-id="47de2-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="47de2-117">Name</span></span>       | <span data-ttu-id="47de2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="47de2-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="47de2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="47de2-119">Authorization</span></span>  | <span data-ttu-id="47de2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="47de2-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="47de2-122">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="47de2-122">Workbook-Session-Id</span></span>  | <span data-ttu-id="47de2-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="47de2-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="47de2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47de2-125">Request body</span></span>

## <a name="response"></a><span data-ttu-id="47de2-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47de2-126">Response</span></span>

<span data-ttu-id="47de2-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47de2-127">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47de2-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47de2-128">Example</span></span>
<span data-ttu-id="47de2-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="47de2-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="47de2-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47de2-130">Request</span></span>
<span data-ttu-id="47de2-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47de2-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "nameditem_range"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/Range
```

##### <a name="response"></a><span data-ttu-id="47de2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47de2-132">Response</span></span>
<span data-ttu-id="47de2-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47de2-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem: Range",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->