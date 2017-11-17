# <a name="table-reapplyfilters"></a><span data-ttu-id="a1657-101">Table: reapplyFilters</span><span class="sxs-lookup"><span data-stu-id="a1657-101">Table: reapplyFilters</span></span>

<span data-ttu-id="a1657-102">Vuelve a aplicar todos los filtros aplicados actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="a1657-102">Reapplies all the filters currently on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="a1657-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1657-103">Permissions</span></span>
<span data-ttu-id="a1657-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1657-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a1657-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1657-106">Permission type</span></span>      | <span data-ttu-id="a1657-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1657-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1657-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1657-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a1657-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a1657-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="a1657-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1657-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1657-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1657-111">Not supported.</span></span>    |
|<span data-ttu-id="a1657-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1657-112">Application</span></span> | <span data-ttu-id="a1657-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1657-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="a1657-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1657-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/reapplyFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/reapplyFilters

```
## <a name="request-headers"></a><span data-ttu-id="a1657-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1657-115">Request headers</span></span>
| <span data-ttu-id="a1657-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a1657-116">Name</span></span>       | <span data-ttu-id="a1657-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1657-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="a1657-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1657-118">Authorization</span></span>  | <span data-ttu-id="a1657-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1657-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a1657-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1657-121">Request body</span></span>

## <a name="response"></a><span data-ttu-id="a1657-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1657-122">Response</span></span>

<span data-ttu-id="a1657-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1657-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1657-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1657-125">Example</span></span>
<span data-ttu-id="a1657-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="a1657-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="a1657-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1657-127">Request</span></span>
<span data-ttu-id="a1657-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1657-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_reapplyfilters"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/reapplyFilters
```

##### <a name="response"></a><span data-ttu-id="a1657-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1657-129">Response</span></span>
<span data-ttu-id="a1657-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1657-130">Here is an example of the response.</span></span> 
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
  "description": "Table: reapplyFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->