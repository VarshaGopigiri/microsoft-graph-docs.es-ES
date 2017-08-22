# <a name="worksheetprotection-protect"></a><span data-ttu-id="ae68a-101">WorksheetProtection: protect</span><span class="sxs-lookup"><span data-stu-id="ae68a-101">WorksheetProtection: protect</span></span>

<span data-ttu-id="ae68a-p101">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ae68a-p101">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ae68a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ae68a-104">Prerequisites</span></span>
<span data-ttu-id="ae68a-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="ae68a-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="ae68a-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ae68a-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="ae68a-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae68a-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="ae68a-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae68a-108">Request headers</span></span>
| <span data-ttu-id="ae68a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae68a-109">Name</span></span>       | <span data-ttu-id="ae68a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae68a-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ae68a-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae68a-111">Authorization</span></span>  | <span data-ttu-id="ae68a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae68a-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ae68a-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ae68a-114">Request body</span></span>
<span data-ttu-id="ae68a-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="ae68a-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="ae68a-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ae68a-116">Parameter</span></span>    | <span data-ttu-id="ae68a-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae68a-117">Type</span></span>   |<span data-ttu-id="ae68a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae68a-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ae68a-119">opciones</span><span class="sxs-lookup"><span data-stu-id="ae68a-119">options</span></span>|<span data-ttu-id="ae68a-120">WorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="ae68a-120">WorksheetProtectionOptions</span></span>|<span data-ttu-id="ae68a-p103">Opcional. Opciones de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="ae68a-p103">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="ae68a-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae68a-123">Response</span></span>

<span data-ttu-id="ae68a-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae68a-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ae68a-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae68a-126">Example</span></span>
<span data-ttu-id="ae68a-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="ae68a-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="ae68a-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae68a-128">Request</span></span>
<span data-ttu-id="ae68a-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae68a-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetprotection_protect"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/protection/protect
Content-type: application/json
Content-length: 383

{
  "options": {
    "allowFormatCells": true,
    "allowFormatColumns": true,
    "allowFormatRows": true,
    "allowInsertColumns": true,
    "allowInsertRows": true,
    "allowInsertHyperlinks": true,
    "allowDeleteColumns": true,
    "allowDeleteRows": true,
    "allowSort": true,
    "allowAutoFilter": true,
    "allowPivotTables": true
  }
}
```

##### <a name="response"></a><span data-ttu-id="ae68a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae68a-130">Response</span></span>
<span data-ttu-id="ae68a-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae68a-131">Here is an example of the response.</span></span> 
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
  "description": "WorksheetProtection: protect",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
