# <a name="chartfill-clear"></a><span data-ttu-id="fbb7c-101">ChartFill: clear</span><span class="sxs-lookup"><span data-stu-id="fbb7c-101">ChartFill: clear</span></span>

<span data-ttu-id="fbb7c-102">Borrar el color de relleno de un elemento de gráfico.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-102">Clear the fill color of a chart element.</span></span>
## <a name="permissions"></a><span data-ttu-id="fbb7c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="fbb7c-103">Permissions</span></span>
<span data-ttu-id="fbb7c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fbb7c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fbb7c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fbb7c-106">Permission type</span></span>      | <span data-ttu-id="fbb7c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fbb7c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fbb7c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fbb7c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="fbb7c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fbb7c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="fbb7c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fbb7c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fbb7c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-111">Not supported.</span></span>    |
|<span data-ttu-id="fbb7c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fbb7c-112">Application</span></span> | <span data-ttu-id="fbb7c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="fbb7c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fbb7c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/title/format/fill/clear
POST /workbook/worksheets/{id|name}/charts/{name}/legend/format/fill/clear

```
## <a name="request-headers"></a><span data-ttu-id="fbb7c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fbb7c-115">Request headers</span></span>
| <span data-ttu-id="fbb7c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="fbb7c-116">Name</span></span>       | <span data-ttu-id="fbb7c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbb7c-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="fbb7c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="fbb7c-118">Authorization</span></span>  | <span data-ttu-id="fbb7c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fbb7c-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="fbb7c-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="fbb7c-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fbb7c-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fbb7c-124">Request body</span></span>
<span data-ttu-id="fbb7c-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fbb7c-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbb7c-126">Response</span></span>

<span data-ttu-id="fbb7c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fbb7c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fbb7c-129">Example</span></span>
<span data-ttu-id="fbb7c-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fbb7c-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fbb7c-131">Request</span></span>
<span data-ttu-id="fbb7c-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chartfill_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts/{name}/format/fill/clear
```

##### <a name="response"></a><span data-ttu-id="fbb7c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fbb7c-133">Response</span></span>
<span data-ttu-id="fbb7c-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fbb7c-134">Here is an example of the response.</span></span> 
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
  "description": "ChartFill: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->