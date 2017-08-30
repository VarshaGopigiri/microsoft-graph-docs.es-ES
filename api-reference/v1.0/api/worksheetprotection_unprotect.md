# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="08f61-101">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="08f61-101">WorksheetProtection: unprotect</span></span>

<span data-ttu-id="08f61-102">Desproteger una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="08f61-102">Unprotect a worksheet</span></span>
## <a name="permissions"></a><span data-ttu-id="08f61-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="08f61-103">Permissions</span></span>
<span data-ttu-id="08f61-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="08f61-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="08f61-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08f61-106">Permission type</span></span>      | <span data-ttu-id="08f61-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08f61-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08f61-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08f61-108">Delegated (work or school account)</span></span> | <span data-ttu-id="08f61-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="08f61-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="08f61-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08f61-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="08f61-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08f61-111">Not supported.</span></span>    |
|<span data-ttu-id="08f61-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08f61-112">Application</span></span> | <span data-ttu-id="08f61-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08f61-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="08f61-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08f61-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="08f61-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08f61-115">Request headers</span></span>
| <span data-ttu-id="08f61-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="08f61-116">Name</span></span>       | <span data-ttu-id="08f61-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="08f61-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="08f61-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="08f61-118">Authorization</span></span>  | <span data-ttu-id="08f61-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08f61-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="08f61-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08f61-121">Request body</span></span>
<span data-ttu-id="08f61-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="08f61-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="08f61-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="08f61-123">Parameter</span></span>    | <span data-ttu-id="08f61-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="08f61-124">Type</span></span>   |<span data-ttu-id="08f61-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="08f61-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08f61-126">password</span><span class="sxs-lookup"><span data-stu-id="08f61-126">password</span></span>|<span data-ttu-id="08f61-127">string</span><span class="sxs-lookup"><span data-stu-id="08f61-127">string</span></span>|<span data-ttu-id="08f61-p103">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="08f61-p103">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="08f61-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08f61-130">Response</span></span>

<span data-ttu-id="08f61-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08f61-p104">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08f61-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08f61-133">Example</span></span>
<span data-ttu-id="08f61-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="08f61-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="08f61-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08f61-135">Request</span></span>
<span data-ttu-id="08f61-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08f61-136">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="08f61-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08f61-137">Response</span></span>
<span data-ttu-id="08f61-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08f61-138">Here is an example of the response.</span></span> 
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