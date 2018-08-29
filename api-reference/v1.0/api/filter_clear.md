# <a name="filter-clear"></a><span data-ttu-id="e8bcc-101">Filter: clear</span><span class="sxs-lookup"><span data-stu-id="e8bcc-101">Filter: clear</span></span>

<span data-ttu-id="e8bcc-102">Borrar el filtro de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-102">Clear the filter on the given column.</span></span>
## <a name="permissions"></a><span data-ttu-id="e8bcc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e8bcc-103">Permissions</span></span>
<span data-ttu-id="e8bcc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e8bcc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e8bcc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e8bcc-106">Permission type</span></span>      | <span data-ttu-id="e8bcc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e8bcc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e8bcc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e8bcc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e8bcc-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e8bcc-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e8bcc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e8bcc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e8bcc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-111">Not supported.</span></span>    |
|<span data-ttu-id="e8bcc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e8bcc-112">Application</span></span> | <span data-ttu-id="e8bcc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e8bcc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e8bcc-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/filter/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/filter/clear

```
## <a name="request-headers"></a><span data-ttu-id="e8bcc-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bcc-115">Request headers</span></span>
| <span data-ttu-id="e8bcc-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e8bcc-116">Name</span></span>       | <span data-ttu-id="e8bcc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8bcc-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e8bcc-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e8bcc-118">Authorization</span></span>  | <span data-ttu-id="e8bcc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e8bcc-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bcc-121">Request body</span></span>
<span data-ttu-id="e8bcc-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e8bcc-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8bcc-123">Response</span></span>

<span data-ttu-id="e8bcc-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e8bcc-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e8bcc-126">Example</span></span>
<span data-ttu-id="e8bcc-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e8bcc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e8bcc-128">Request</span></span>
<span data-ttu-id="e8bcc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "filter_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/filter/clear
```

##### <a name="response"></a><span data-ttu-id="e8bcc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e8bcc-130">Response</span></span>
<span data-ttu-id="e8bcc-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e8bcc-131">Here is an example of the response.</span></span> 
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
  "description": "Filter: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->