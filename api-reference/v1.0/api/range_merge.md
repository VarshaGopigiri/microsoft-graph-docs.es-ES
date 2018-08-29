# <a name="range-merge"></a><span data-ttu-id="b7ff3-101">Range: merge</span><span class="sxs-lookup"><span data-stu-id="b7ff3-101">Range: merge</span></span>

<span data-ttu-id="b7ff3-102">Combinar las celdas del rango en una región de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-102">Merge the range cells into one region in the worksheet.</span></span>
## <a name="permissions"></a><span data-ttu-id="b7ff3-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b7ff3-103">Permissions</span></span>
<span data-ttu-id="b7ff3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b7ff3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b7ff3-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b7ff3-106">Permission type</span></span>      | <span data-ttu-id="b7ff3-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b7ff3-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b7ff3-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b7ff3-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b7ff3-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b7ff3-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b7ff3-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7ff3-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b7ff3-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-111">Not supported.</span></span>    |
|<span data-ttu-id="b7ff3-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b7ff3-112">Application</span></span> | <span data-ttu-id="b7ff3-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b7ff3-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b7ff3-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/merge
POST /workbook/worksheets/{id|name}/range(address='<address>')/merge
POST /workbook/tables/{id|name}/columns/{id|name}/range/merge

```
## <a name="request-headers"></a><span data-ttu-id="b7ff3-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ff3-115">Request headers</span></span>
| <span data-ttu-id="b7ff3-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b7ff3-116">Name</span></span>       | <span data-ttu-id="b7ff3-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ff3-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b7ff3-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b7ff3-118">Authorization</span></span>  | <span data-ttu-id="b7ff3-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="b7ff3-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b7ff3-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="b7ff3-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="b7ff3-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ff3-124">Request body</span></span>
<span data-ttu-id="b7ff3-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b7ff3-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b7ff3-126">Parameter</span></span>    | <span data-ttu-id="b7ff3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="b7ff3-127">Type</span></span>   |<span data-ttu-id="b7ff3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ff3-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b7ff3-129">across</span><span class="sxs-lookup"><span data-stu-id="b7ff3-129">across</span></span>|<span data-ttu-id="b7ff3-130">boolean</span><span class="sxs-lookup"><span data-stu-id="b7ff3-130">boolean</span></span>|<span data-ttu-id="b7ff3-p104">Opcional. Verdadero para que se combinen las celdas de cada fila del rango especificado como celdas combinadas distintas. El valor predeterminado es falso.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-p104">Optional. Set true to merge cells in each row of the specified range as separate merged cells. The default value is false.</span></span>|

## <a name="response"></a><span data-ttu-id="b7ff3-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ff3-134">Response</span></span>

<span data-ttu-id="b7ff3-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b7ff3-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b7ff3-137">Example</span></span>
<span data-ttu-id="b7ff3-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b7ff3-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b7ff3-139">Request</span></span>
<span data-ttu-id="b7ff3-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_merge"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/merge
Content-type: application/json
Content-length: 20

{
  "across": true
}
```

##### <a name="response"></a><span data-ttu-id="b7ff3-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b7ff3-141">Response</span></span>
<span data-ttu-id="b7ff3-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b7ff3-142">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: merge",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->