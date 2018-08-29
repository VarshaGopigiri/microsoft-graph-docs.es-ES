# <a name="rangeformat-autofitcolumns"></a><span data-ttu-id="7956d-101">RangeFormat: autofitColumns</span><span class="sxs-lookup"><span data-stu-id="7956d-101">RangeFormat: autofitColumns</span></span>

<span data-ttu-id="7956d-102">Cambia el ancho de las columnas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="7956d-102">Changes the width of the columns of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="permissions"></a><span data-ttu-id="7956d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7956d-103">Permissions</span></span>
<span data-ttu-id="7956d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7956d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7956d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7956d-106">Permission type</span></span>      | <span data-ttu-id="7956d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7956d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7956d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7956d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7956d-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7956d-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7956d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7956d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7956d-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7956d-111">Not supported.</span></span>    |
|<span data-ttu-id="7956d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7956d-112">Application</span></span> | <span data-ttu-id="7956d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7956d-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7956d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7956d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/format/autofitColumns
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/autofitColumns
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitColumns

```
## <a name="request-headers"></a><span data-ttu-id="7956d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7956d-115">Request headers</span></span>
| <span data-ttu-id="7956d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7956d-116">Name</span></span>       | <span data-ttu-id="7956d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="7956d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="7956d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="7956d-118">Authorization</span></span>  | <span data-ttu-id="7956d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7956d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7956d-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="7956d-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="7956d-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="7956d-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="7956d-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7956d-124">Request body</span></span>

## <a name="response"></a><span data-ttu-id="7956d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7956d-125">Response</span></span>

<span data-ttu-id="7956d-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7956d-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7956d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7956d-128">Example</span></span>
<span data-ttu-id="7956d-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="7956d-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="7956d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7956d-130">Request</span></span>
<span data-ttu-id="7956d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7956d-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitcolumns"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/autofitColumns
```

##### <a name="response"></a><span data-ttu-id="7956d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7956d-132">Response</span></span>
<span data-ttu-id="7956d-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7956d-133">Here is an example of the response.</span></span> 
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
  "description": "RangeFormat: autofitColumns",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->