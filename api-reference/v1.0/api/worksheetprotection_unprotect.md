# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="187e3-101">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="187e3-101">WorksheetProtection: unprotect</span></span>

<span data-ttu-id="187e3-102">Desprotege una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="187e3-102">Unprotect a worksheet</span></span>
## <a name="prerequisites"></a><span data-ttu-id="187e3-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="187e3-103">Prerequisites</span></span>
<span data-ttu-id="187e3-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="187e3-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="187e3-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="187e3-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="187e3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="187e3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="187e3-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="187e3-107">Request headers</span></span>
| <span data-ttu-id="187e3-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="187e3-108">Name</span></span>       | <span data-ttu-id="187e3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="187e3-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="187e3-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="187e3-110">Authorization</span></span>  | <span data-ttu-id="187e3-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="187e3-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="187e3-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="187e3-113">Request body</span></span>
<span data-ttu-id="187e3-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="187e3-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="187e3-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="187e3-115">Parameter</span></span>    | <span data-ttu-id="187e3-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="187e3-116">Type</span></span>   |<span data-ttu-id="187e3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="187e3-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="187e3-118">password</span><span class="sxs-lookup"><span data-stu-id="187e3-118">password</span></span>|<span data-ttu-id="187e3-119">string</span><span class="sxs-lookup"><span data-stu-id="187e3-119">string</span></span>|<span data-ttu-id="187e3-p102">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="187e3-p102">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="187e3-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="187e3-122">Response</span></span>

<span data-ttu-id="187e3-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="187e3-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="187e3-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="187e3-125">Example</span></span>
<span data-ttu-id="187e3-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="187e3-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="187e3-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="187e3-127">Request</span></span>
<span data-ttu-id="187e3-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="187e3-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_unprotect"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/unprotect
Content-type: application/json
Content-length: 34

{
  "password": "password-value"
}
```

##### <a name="response"></a><span data-ttu-id="187e3-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="187e3-129">Response</span></span>
<span data-ttu-id="187e3-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="187e3-130">Here is an example of the response.</span></span> 
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
  "description": "WorksheetProtection: unprotect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->