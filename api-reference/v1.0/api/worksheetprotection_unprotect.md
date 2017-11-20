# <a name="worksheetprotection-unprotect"></a><span data-ttu-id="eaa66-101">WorksheetProtection: unprotect</span><span class="sxs-lookup"><span data-stu-id="eaa66-101">WorksheetProtection: unprotect</span></span>

<span data-ttu-id="eaa66-102">Desproteger una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="eaa66-102">Unprotect a worksheet</span></span>
## <a name="permissions"></a><span data-ttu-id="eaa66-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="eaa66-103">Permissions</span></span>
<span data-ttu-id="eaa66-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eaa66-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eaa66-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eaa66-106">Permission type</span></span>      | <span data-ttu-id="eaa66-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eaa66-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eaa66-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eaa66-108">Delegated (work or school account)</span></span> | <span data-ttu-id="eaa66-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eaa66-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eaa66-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eaa66-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eaa66-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaa66-111">Not supported.</span></span>    |
|<span data-ttu-id="eaa66-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eaa66-112">Application</span></span> | <span data-ttu-id="eaa66-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaa66-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eaa66-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eaa66-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/protection/unprotect

```
## <a name="request-headers"></a><span data-ttu-id="eaa66-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa66-115">Request headers</span></span>
| <span data-ttu-id="eaa66-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="eaa66-116">Name</span></span>       | <span data-ttu-id="eaa66-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaa66-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eaa66-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="eaa66-118">Authorization</span></span>  | <span data-ttu-id="eaa66-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eaa66-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eaa66-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="eaa66-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="eaa66-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="eaa66-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="eaa66-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa66-124">Request body</span></span>
<span data-ttu-id="eaa66-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="eaa66-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="eaa66-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="eaa66-126">Parameter</span></span>    | <span data-ttu-id="eaa66-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="eaa66-127">Type</span></span>   |<span data-ttu-id="eaa66-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaa66-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eaa66-129">password</span><span class="sxs-lookup"><span data-stu-id="eaa66-129">password</span></span>|<span data-ttu-id="eaa66-130">string</span><span class="sxs-lookup"><span data-stu-id="eaa66-130">string</span></span>|<span data-ttu-id="eaa66-p104">Opcional. Contraseña de protección de la hoja.</span><span class="sxs-lookup"><span data-stu-id="eaa66-p104">Optional. sheet protection password.</span></span>|

## <a name="response"></a><span data-ttu-id="eaa66-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaa66-133">Response</span></span>

<span data-ttu-id="eaa66-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaa66-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eaa66-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eaa66-136">Example</span></span>
<span data-ttu-id="eaa66-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eaa66-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eaa66-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eaa66-138">Request</span></span>
<span data-ttu-id="eaa66-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaa66-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="eaa66-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaa66-140">Response</span></span>
<span data-ttu-id="eaa66-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaa66-141">Here is an example of the response.</span></span> 
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