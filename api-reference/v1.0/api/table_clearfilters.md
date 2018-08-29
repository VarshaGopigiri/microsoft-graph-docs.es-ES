# <a name="table-clearfilters"></a><span data-ttu-id="89d72-101">Table: clearFilters</span><span class="sxs-lookup"><span data-stu-id="89d72-101">Table: clearFilters</span></span>

<span data-ttu-id="89d72-102">Borra todos los filtros aplicados actualmente en la tabla.</span><span class="sxs-lookup"><span data-stu-id="89d72-102">Clears all the filters currently applied on the table.</span></span>
## <a name="permissions"></a><span data-ttu-id="89d72-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="89d72-103">Permissions</span></span>
<span data-ttu-id="89d72-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="89d72-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="89d72-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="89d72-106">Permission type</span></span>      | <span data-ttu-id="89d72-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="89d72-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="89d72-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="89d72-108">Delegated (work or school account)</span></span> | <span data-ttu-id="89d72-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="89d72-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="89d72-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="89d72-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="89d72-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89d72-111">Not supported.</span></span>    |
|<span data-ttu-id="89d72-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="89d72-112">Application</span></span> | <span data-ttu-id="89d72-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="89d72-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="89d72-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="89d72-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/clearFilters
POST /workbook/worksheets/{id|name}/tables/{id|name}/clearFilters

```
## <a name="request-headers"></a><span data-ttu-id="89d72-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="89d72-115">Request headers</span></span>
| <span data-ttu-id="89d72-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="89d72-116">Name</span></span>       | <span data-ttu-id="89d72-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="89d72-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="89d72-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="89d72-118">Authorization</span></span>  | <span data-ttu-id="89d72-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="89d72-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="89d72-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="89d72-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="89d72-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="89d72-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="89d72-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="89d72-124">Request body</span></span>

## <a name="response"></a><span data-ttu-id="89d72-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89d72-125">Response</span></span>

<span data-ttu-id="89d72-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89d72-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="89d72-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89d72-128">Example</span></span>
<span data-ttu-id="89d72-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="89d72-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="89d72-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="89d72-130">Request</span></span>
<span data-ttu-id="89d72-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="89d72-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_clearfilters"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/clearFilters
```

##### <a name="response"></a><span data-ttu-id="89d72-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="89d72-132">Response</span></span>
<span data-ttu-id="89d72-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="89d72-133">Here is an example of the response.</span></span> 
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
  "description": "Table: clearFilters",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->