# <a name="range-clear"></a><span data-ttu-id="632b8-101">Range: clear</span><span class="sxs-lookup"><span data-stu-id="632b8-101">Range: clear</span></span>

<span data-ttu-id="632b8-102">Borra valores de rango, formato, relleno, borde, etc.</span><span class="sxs-lookup"><span data-stu-id="632b8-102">Clear range values, format, fill, border, etc.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="632b8-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="632b8-103">Prerequisites</span></span>
<span data-ttu-id="632b8-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="632b8-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="632b8-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="632b8-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="632b8-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="632b8-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/clear
GET /workbook/worksheets/{id|name}/range(<address>)/clear
GET /workbook/tables/{id|name}/columns/{id|name}/range/clear

```
## <a name="request-headers"></a><span data-ttu-id="632b8-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="632b8-107">Request headers</span></span>
| <span data-ttu-id="632b8-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="632b8-108">Name</span></span>       | <span data-ttu-id="632b8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="632b8-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="632b8-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="632b8-110">Authorization</span></span>  | <span data-ttu-id="632b8-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="632b8-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="632b8-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="632b8-113">Request body</span></span>
<span data-ttu-id="632b8-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="632b8-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="632b8-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="632b8-115">Parameter</span></span>    | <span data-ttu-id="632b8-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="632b8-116">Type</span></span>   |<span data-ttu-id="632b8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="632b8-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="632b8-118">applyTo</span><span class="sxs-lookup"><span data-stu-id="632b8-118">applyTo</span></span>|<span data-ttu-id="632b8-119">string</span><span class="sxs-lookup"><span data-stu-id="632b8-119">string</span></span>|<span data-ttu-id="632b8-p102">Opcional. Determina el tipo de acción de borrado.  Valores posibles: `All`, `Formats`, `Contents`.</span><span class="sxs-lookup"><span data-stu-id="632b8-p102">Optional. Determines the type of clear action.  Possible values are: `All`, `Formats`, `Contents`.</span></span>|

## <a name="response"></a><span data-ttu-id="632b8-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="632b8-123">Response</span></span>

<span data-ttu-id="632b8-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="632b8-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="632b8-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="632b8-126">Example</span></span>
<span data-ttu-id="632b8-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="632b8-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="632b8-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="632b8-128">Request</span></span>
<span data-ttu-id="632b8-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="632b8-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_clear"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/clear
Content-type: application/json
Content-length: 32

{
  "applyTo": "applyTo-value"
}
```

##### <a name="response"></a><span data-ttu-id="632b8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="632b8-130">Response</span></span>
<span data-ttu-id="632b8-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="632b8-131">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->