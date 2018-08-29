# <a name="rangeformat-autofitrows"></a><span data-ttu-id="f4d0c-101">RangeFormat: autofitRows</span><span class="sxs-lookup"><span data-stu-id="f4d0c-101">RangeFormat: autofitRows</span></span>

<span data-ttu-id="f4d0c-102">Cambia el alto de las filas del rango actual para obtener el ajuste perfecto (según los datos actuales de las columnas).</span><span class="sxs-lookup"><span data-stu-id="f4d0c-102">Changes the height of the rows of the current range to achieve the best fit, based on the current data in the columns.</span></span>
## <a name="permissions"></a><span data-ttu-id="f4d0c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f4d0c-103">Permissions</span></span>
<span data-ttu-id="f4d0c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f4d0c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f4d0c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4d0c-106">Permission type</span></span>      | <span data-ttu-id="f4d0c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4d0c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f4d0c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4d0c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f4d0c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f4d0c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f4d0c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4d0c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f4d0c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-111">Not supported.</span></span>    |
|<span data-ttu-id="f4d0c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4d0c-112">Application</span></span> | <span data-ttu-id="f4d0c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f4d0c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4d0c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/{name}/range/format/autofitRows
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/autofitRows
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/autofitRows

```
## <a name="request-headers"></a><span data-ttu-id="f4d0c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4d0c-115">Request headers</span></span>
| <span data-ttu-id="f4d0c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4d0c-116">Name</span></span>       | <span data-ttu-id="f4d0c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4d0c-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f4d0c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="f4d0c-118">Authorization</span></span>  | <span data-ttu-id="f4d0c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f4d0c-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="f4d0c-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="f4d0c-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4d0c-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4d0c-124">Request body</span></span>

## <a name="response"></a><span data-ttu-id="f4d0c-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4d0c-125">Response</span></span>

<span data-ttu-id="f4d0c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4d0c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4d0c-128">Example</span></span>
<span data-ttu-id="f4d0c-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f4d0c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4d0c-130">Request</span></span>
<span data-ttu-id="f4d0c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangeformat_autofitrows"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/format/autofitRows
```

##### <a name="response"></a><span data-ttu-id="f4d0c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4d0c-132">Response</span></span>
<span data-ttu-id="f4d0c-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4d0c-133">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat: autofitRows",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->