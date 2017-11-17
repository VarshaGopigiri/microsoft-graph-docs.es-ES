# <a name="chart-delete"></a><span data-ttu-id="eaae0-101">Chart: delete</span><span class="sxs-lookup"><span data-stu-id="eaae0-101">Chart: delete</span></span>

<span data-ttu-id="eaae0-102">Elimina el objeto chart.</span><span class="sxs-lookup"><span data-stu-id="eaae0-102">Deletes the chart object.</span></span>
## <a name="permissions"></a><span data-ttu-id="eaae0-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="eaae0-103">Permissions</span></span>
<span data-ttu-id="eaae0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="eaae0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="eaae0-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="eaae0-106">Permission type</span></span>      | <span data-ttu-id="eaae0-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="eaae0-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="eaae0-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="eaae0-108">Delegated (work or school account)</span></span> | <span data-ttu-id="eaae0-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eaae0-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="eaae0-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="eaae0-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="eaae0-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaae0-111">Not supported.</span></span>    |
|<span data-ttu-id="eaae0-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="eaae0-112">Application</span></span> | <span data-ttu-id="eaae0-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="eaae0-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="eaae0-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eaae0-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/{id|name}/charts(<name>)/delete

```
## <a name="request-headers"></a><span data-ttu-id="eaae0-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eaae0-115">Request headers</span></span>
| <span data-ttu-id="eaae0-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="eaae0-116">Name</span></span>       | <span data-ttu-id="eaae0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaae0-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="eaae0-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="eaae0-118">Authorization</span></span>  | <span data-ttu-id="eaae0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eaae0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eaae0-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eaae0-121">Request body</span></span>

## <a name="response"></a><span data-ttu-id="eaae0-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaae0-122">Response</span></span>

<span data-ttu-id="eaae0-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaae0-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eaae0-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eaae0-125">Example</span></span>
<span data-ttu-id="eaae0-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eaae0-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eaae0-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eaae0-127">Request</span></span>
<span data-ttu-id="eaae0-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eaae0-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "chart_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/charts(<name>)/delete
```

##### <a name="response"></a><span data-ttu-id="eaae0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eaae0-129">Response</span></span>
<span data-ttu-id="eaae0-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eaae0-130">Here is an example of the response.</span></span> 
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
  "description": "Chart: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->