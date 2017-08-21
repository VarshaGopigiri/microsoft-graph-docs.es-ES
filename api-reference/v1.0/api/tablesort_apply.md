# <a name="tablesort-apply"></a><span data-ttu-id="f9fa0-101">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="f9fa0-101">TableSort: apply</span></span>

<span data-ttu-id="f9fa0-102">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-102">Perform a sort operation.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9fa0-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9fa0-103">Prerequisites</span></span>
<span data-ttu-id="f9fa0-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="f9fa0-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="f9fa0-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9fa0-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="f9fa0-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9fa0-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="f9fa0-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9fa0-107">Request headers</span></span>
| <span data-ttu-id="f9fa0-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9fa0-108">Name</span></span>       | <span data-ttu-id="f9fa0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9fa0-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f9fa0-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9fa0-110">Authorization</span></span>  | <span data-ttu-id="f9fa0-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="f9fa0-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9fa0-113">Request body</span></span>
<span data-ttu-id="f9fa0-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f9fa0-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f9fa0-115">Parameter</span></span>    | <span data-ttu-id="f9fa0-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9fa0-116">Type</span></span>   |<span data-ttu-id="f9fa0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9fa0-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f9fa0-118">fields</span><span class="sxs-lookup"><span data-stu-id="f9fa0-118">fields</span></span>|<span data-ttu-id="f9fa0-119">SortField</span><span class="sxs-lookup"><span data-stu-id="f9fa0-119">SortField</span></span>|<span data-ttu-id="f9fa0-120">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-120">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="f9fa0-121">matchCase</span><span class="sxs-lookup"><span data-stu-id="f9fa0-121">matchCase</span></span>|<span data-ttu-id="f9fa0-122">boolean</span><span class="sxs-lookup"><span data-stu-id="f9fa0-122">boolean</span></span>|<span data-ttu-id="f9fa0-p102">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-p102">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="f9fa0-125">method</span><span class="sxs-lookup"><span data-stu-id="f9fa0-125">method</span></span>|<span data-ttu-id="f9fa0-126">string</span><span class="sxs-lookup"><span data-stu-id="f9fa0-126">string</span></span>|<span data-ttu-id="f9fa0-p103">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-p103">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="f9fa0-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9fa0-130">Response</span></span>

<span data-ttu-id="f9fa0-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9fa0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9fa0-133">Example</span></span>
<span data-ttu-id="f9fa0-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f9fa0-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9fa0-135">Request</span></span>
<span data-ttu-id="f9fa0-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply
Content-type: application/json
Content-length: 298

{
  "fields": [
    {
      "key": 99,
      "sortOn": "sortOn-value",
      "ascending": true,
      "color": "color-value",
      "dataOption": "dataOption-value",
      "icon": {
        "set": "set-value",
        "index": 99
      }
    }
  ],
  "matchCase": true,
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="f9fa0-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9fa0-137">Response</span></span>
<span data-ttu-id="f9fa0-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9fa0-138">Here is an example of the response.</span></span> 
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
  "description": "TableSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->