# <a name="range-clear"></a><span data-ttu-id="85fdc-101">Range: clear</span><span class="sxs-lookup"><span data-stu-id="85fdc-101">Range: clear</span></span>

<span data-ttu-id="85fdc-102">Borrar valores de rango, formato, relleno, borde, etc.</span><span class="sxs-lookup"><span data-stu-id="85fdc-102">Clear range values, format, fill, border, etc.</span></span>
## <a name="permissions"></a><span data-ttu-id="85fdc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="85fdc-103">Permissions</span></span>
<span data-ttu-id="85fdc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="85fdc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="85fdc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="85fdc-106">Permission type</span></span>      | <span data-ttu-id="85fdc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="85fdc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="85fdc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="85fdc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="85fdc-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="85fdc-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="85fdc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="85fdc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="85fdc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85fdc-111">Not supported.</span></span>    |
|<span data-ttu-id="85fdc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="85fdc-112">Application</span></span> | <span data-ttu-id="85fdc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85fdc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="85fdc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85fdc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/clear
POST /workbook/worksheets/{id|name}/range(address='<address>')/clear
POST /workbook/tables/{id|name}/columns/{id|name}/range/clear

```
## <a name="request-headers"></a><span data-ttu-id="85fdc-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85fdc-115">Request headers</span></span>
| <span data-ttu-id="85fdc-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="85fdc-116">Name</span></span>       | <span data-ttu-id="85fdc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="85fdc-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="85fdc-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="85fdc-118">Authorization</span></span>  | <span data-ttu-id="85fdc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="85fdc-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="85fdc-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="85fdc-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="85fdc-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="85fdc-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="85fdc-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="85fdc-124">Request body</span></span>
<span data-ttu-id="85fdc-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="85fdc-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="85fdc-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="85fdc-126">Parameter</span></span>    | <span data-ttu-id="85fdc-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="85fdc-127">Type</span></span>   |<span data-ttu-id="85fdc-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="85fdc-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="85fdc-129">applyTo</span><span class="sxs-lookup"><span data-stu-id="85fdc-129">applyTo</span></span>|<span data-ttu-id="85fdc-130">cadena</span><span class="sxs-lookup"><span data-stu-id="85fdc-130">string</span></span>|<span data-ttu-id="85fdc-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="85fdc-131">Optional.</span></span> <span data-ttu-id="85fdc-132">Determina el tipo de acción Borrar.</span><span class="sxs-lookup"><span data-stu-id="85fdc-132">Optional. Determines the type of clear action.  Possible values are: , , .</span></span>  <span data-ttu-id="85fdc-133">Los valores posibles son: `All`, `Formats`, `Contents`.</span><span class="sxs-lookup"><span data-stu-id="85fdc-133">The possible values are `All`, `Formats`, `Contents`, , , , , , , , , or .</span></span>|

## <a name="response"></a><span data-ttu-id="85fdc-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85fdc-134">Response</span></span>

<span data-ttu-id="85fdc-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85fdc-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="85fdc-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85fdc-137">Example</span></span>
<span data-ttu-id="85fdc-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="85fdc-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="85fdc-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85fdc-139">Request</span></span>
<span data-ttu-id="85fdc-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85fdc-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/clear
Content-type: application/json
Content-length: 32

{
  "applyTo": "applyTo-value"
}
```

##### <a name="response"></a><span data-ttu-id="85fdc-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85fdc-141">Response</span></span>
<span data-ttu-id="85fdc-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85fdc-142">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 204 No Content
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