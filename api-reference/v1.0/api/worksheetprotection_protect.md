# <a name="worksheetprotection-protect"></a><span data-ttu-id="88113-101">WorksheetProtection: protect</span><span class="sxs-lookup"><span data-stu-id="88113-101">WorksheetProtection: protect</span></span>

<span data-ttu-id="88113-p101">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="88113-p101">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="permissions"></a><span data-ttu-id="88113-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="88113-104">Permissions</span></span>
<span data-ttu-id="88113-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="88113-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="88113-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88113-107">Permission type</span></span>      | <span data-ttu-id="88113-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88113-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88113-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88113-109">Delegated (work or school account)</span></span> | <span data-ttu-id="88113-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88113-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="88113-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88113-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88113-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88113-112">Not supported.</span></span>    |
|<span data-ttu-id="88113-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88113-113">Application</span></span> | <span data-ttu-id="88113-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88113-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="88113-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88113-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="88113-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88113-116">Request headers</span></span>
| <span data-ttu-id="88113-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="88113-117">Name</span></span>       | <span data-ttu-id="88113-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="88113-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="88113-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="88113-119">Authorization</span></span>  | <span data-ttu-id="88113-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88113-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88113-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88113-122">Request body</span></span>
<span data-ttu-id="88113-123">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="88113-123">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="88113-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="88113-124">Parameter</span></span>    | <span data-ttu-id="88113-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="88113-125">Type</span></span>   |<span data-ttu-id="88113-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="88113-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="88113-127">opciones</span><span class="sxs-lookup"><span data-stu-id="88113-127">options</span></span>|<span data-ttu-id="88113-128">WorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="88113-128">WorksheetProtectionOptions</span></span>|<span data-ttu-id="88113-p104">Opcional. Opciones de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="88113-p104">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="88113-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88113-131">Response</span></span>

<span data-ttu-id="88113-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88113-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="88113-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88113-134">Example</span></span>
<span data-ttu-id="88113-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="88113-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="88113-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88113-136">Request</span></span>
<span data-ttu-id="88113-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88113-137">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="88113-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88113-138">Response</span></span>
<span data-ttu-id="88113-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88113-139">Here is an example of the response.</span></span> 
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
