# <a name="range-clear"></a><span data-ttu-id="26b19-101">Range: clear</span><span class="sxs-lookup"><span data-stu-id="26b19-101">Range: clear</span></span>

<span data-ttu-id="26b19-102">Borrar valores de rango, formato, relleno, borde, etc.</span><span class="sxs-lookup"><span data-stu-id="26b19-102">Clear range values, format, fill, border, etc.</span></span>
## <a name="permissions"></a><span data-ttu-id="26b19-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="26b19-103">Permissions</span></span>
<span data-ttu-id="26b19-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="26b19-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="26b19-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="26b19-106">Permission type</span></span>      | <span data-ttu-id="26b19-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="26b19-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="26b19-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="26b19-108">Delegated (work or school account)</span></span> | <span data-ttu-id="26b19-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="26b19-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="26b19-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="26b19-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="26b19-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26b19-111">Not supported.</span></span>    |
|<span data-ttu-id="26b19-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="26b19-112">Application</span></span> | <span data-ttu-id="26b19-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="26b19-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="26b19-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="26b19-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/clear
GET /workbook/worksheets/{id|name}/range(<address>)/clear
GET /workbook/tables/{id|name}/columns/{id|name}/range/clear

```
## <a name="request-headers"></a><span data-ttu-id="26b19-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="26b19-115">Request headers</span></span>
| <span data-ttu-id="26b19-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="26b19-116">Name</span></span>       | <span data-ttu-id="26b19-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="26b19-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="26b19-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="26b19-118">Authorization</span></span>  | <span data-ttu-id="26b19-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="26b19-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="26b19-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="26b19-121">Request body</span></span>
<span data-ttu-id="26b19-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="26b19-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="26b19-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="26b19-123">Parameter</span></span>    | <span data-ttu-id="26b19-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="26b19-124">Type</span></span>   |<span data-ttu-id="26b19-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="26b19-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26b19-126">applyTo</span><span class="sxs-lookup"><span data-stu-id="26b19-126">applyTo</span></span>|<span data-ttu-id="26b19-127">string</span><span class="sxs-lookup"><span data-stu-id="26b19-127">string</span></span>|<span data-ttu-id="26b19-p103">Opcional. Determina el tipo de acción de borrado.  Valores posibles: `All`, `Formats`, `Contents`.</span><span class="sxs-lookup"><span data-stu-id="26b19-p103">Optional. Determines the type of clear action.  Possible values are: `All`, `Formats`, `Contents`.</span></span>|

## <a name="response"></a><span data-ttu-id="26b19-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26b19-131">Response</span></span>

<span data-ttu-id="26b19-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26b19-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="26b19-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="26b19-134">Example</span></span>
<span data-ttu-id="26b19-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="26b19-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="26b19-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="26b19-136">Request</span></span>
<span data-ttu-id="26b19-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="26b19-137">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="26b19-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="26b19-138">Response</span></span>
<span data-ttu-id="26b19-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="26b19-139">Here is an example of the response.</span></span> 
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