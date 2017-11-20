# <a name="worksheetprotection-protect"></a><span data-ttu-id="5283a-101">WorksheetProtection: protect</span><span class="sxs-lookup"><span data-stu-id="5283a-101">WorksheetProtection: protect</span></span>

<span data-ttu-id="5283a-p101">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5283a-p101">Protect a worksheet. It throws if the worksheet has been protected.</span></span>
## <a name="permissions"></a><span data-ttu-id="5283a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="5283a-104">Permissions</span></span>
<span data-ttu-id="5283a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5283a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5283a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5283a-107">Permission type</span></span>      | <span data-ttu-id="5283a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5283a-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5283a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5283a-109">Delegated (work or school account)</span></span> | <span data-ttu-id="5283a-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5283a-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5283a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5283a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5283a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5283a-112">Not supported.</span></span>    |
|<span data-ttu-id="5283a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5283a-113">Application</span></span> | <span data-ttu-id="5283a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5283a-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5283a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5283a-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/protect

```
## <a name="request-headers"></a><span data-ttu-id="5283a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5283a-116">Request headers</span></span>
| <span data-ttu-id="5283a-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="5283a-117">Name</span></span>       | <span data-ttu-id="5283a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5283a-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5283a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5283a-119">Authorization</span></span>  | <span data-ttu-id="5283a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5283a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5283a-122">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="5283a-122">Workbook-Session-Id</span></span>  | <span data-ttu-id="5283a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="5283a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="5283a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5283a-125">Request body</span></span>
<span data-ttu-id="5283a-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5283a-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5283a-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5283a-127">Parameter</span></span>    | <span data-ttu-id="5283a-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="5283a-128">Type</span></span>   |<span data-ttu-id="5283a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="5283a-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5283a-130">opciones</span><span class="sxs-lookup"><span data-stu-id="5283a-130">options</span></span>|<span data-ttu-id="5283a-131">WorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="5283a-131">WorksheetProtectionOptions</span></span>|<span data-ttu-id="5283a-p105">Opcional. Opciones de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="5283a-p105">Optional. sheet protection options.</span></span>|

## <a name="response"></a><span data-ttu-id="5283a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5283a-134">Response</span></span>

<span data-ttu-id="5283a-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5283a-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5283a-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5283a-137">Example</span></span>
<span data-ttu-id="5283a-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5283a-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5283a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5283a-139">Request</span></span>
<span data-ttu-id="5283a-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5283a-140">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="5283a-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5283a-141">Response</span></span>
<span data-ttu-id="5283a-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5283a-142">Here is an example of the response.</span></span> 
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
