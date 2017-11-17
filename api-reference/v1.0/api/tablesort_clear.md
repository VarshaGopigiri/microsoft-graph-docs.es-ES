# <a name="tablesort-clear"></a><span data-ttu-id="e78b7-101">TableSort: clear</span><span class="sxs-lookup"><span data-stu-id="e78b7-101">TableSort: clear</span></span>

<span data-ttu-id="e78b7-p101">Borra la ordenación que se aplica actualmente en la tabla. Aunque esto no modifica la ordenación de la tabla, borra el estado de los botones de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e78b7-p101">Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.</span></span>
## <a name="permissions"></a><span data-ttu-id="e78b7-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="e78b7-104">Permissions</span></span>
<span data-ttu-id="e78b7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e78b7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e78b7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e78b7-107">Permission type</span></span>      | <span data-ttu-id="e78b7-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e78b7-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e78b7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e78b7-109">Delegated (work or school account)</span></span> | <span data-ttu-id="e78b7-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e78b7-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e78b7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e78b7-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e78b7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e78b7-112">Not supported.</span></span>    |
|<span data-ttu-id="e78b7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e78b7-113">Application</span></span> | <span data-ttu-id="e78b7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e78b7-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e78b7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e78b7-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/clear
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/clear

```
## <a name="request-headers"></a><span data-ttu-id="e78b7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e78b7-116">Request headers</span></span>
| <span data-ttu-id="e78b7-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="e78b7-117">Name</span></span>       | <span data-ttu-id="e78b7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e78b7-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e78b7-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e78b7-119">Authorization</span></span>  | <span data-ttu-id="e78b7-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e78b7-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e78b7-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e78b7-122">Request body</span></span>

## <a name="response"></a><span data-ttu-id="e78b7-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e78b7-123">Response</span></span>

<span data-ttu-id="e78b7-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e78b7-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e78b7-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e78b7-126">Example</span></span>
<span data-ttu-id="e78b7-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e78b7-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e78b7-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e78b7-128">Request</span></span>
<span data-ttu-id="e78b7-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e78b7-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/clear
```

##### <a name="response"></a><span data-ttu-id="e78b7-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e78b7-130">Response</span></span>
<span data-ttu-id="e78b7-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e78b7-131">Here is an example of the response.</span></span> 
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
  "description": "TableSort: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->