# <a name="nameditem-range"></a><span data-ttu-id="0b310-101">NamedItem: Range</span><span class="sxs-lookup"><span data-stu-id="0b310-101">NamedItem: Range</span></span>

<span data-ttu-id="0b310-p101">Devuelve el objeto de intervalo asociado al nombre. Produce una excepción si el tipo del elemento con nombre no es un intervalo.</span><span class="sxs-lookup"><span data-stu-id="0b310-p101">Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0b310-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0b310-104">Prerequisites</span></span>
<span data-ttu-id="0b310-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="0b310-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="0b310-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b310-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="0b310-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0b310-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/Range

```
## <a name="request-headers"></a><span data-ttu-id="0b310-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0b310-108">Request headers</span></span>
| <span data-ttu-id="0b310-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="0b310-109">Name</span></span>       | <span data-ttu-id="0b310-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b310-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0b310-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="0b310-111">Authorization</span></span>  | <span data-ttu-id="0b310-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b310-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="0b310-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0b310-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="0b310-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b310-115">Response</span></span>

<span data-ttu-id="0b310-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0b310-116">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0b310-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0b310-117">Example</span></span>
<span data-ttu-id="0b310-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0b310-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0b310-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0b310-119">Request</span></span>
<span data-ttu-id="0b310-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0b310-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "nameditem_range"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/Range
```

##### <a name="response"></a><span data-ttu-id="0b310-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0b310-121">Response</span></span>
<span data-ttu-id="0b310-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0b310-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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