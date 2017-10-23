# <a name="rangefill-clear"></a><span data-ttu-id="b29ba-101">RangeFill: clear</span><span class="sxs-lookup"><span data-stu-id="b29ba-101">RangeFill: clear</span></span>

<span data-ttu-id="b29ba-102">Restablece el fondo del rango.</span><span class="sxs-lookup"><span data-stu-id="b29ba-102">Resets the range background.</span></span>
## <a name="permissions"></a><span data-ttu-id="b29ba-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b29ba-103">Permissions</span></span>
<span data-ttu-id="b29ba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b29ba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b29ba-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b29ba-106">Permission type</span></span>      | <span data-ttu-id="b29ba-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b29ba-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b29ba-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b29ba-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b29ba-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b29ba-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b29ba-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b29ba-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b29ba-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29ba-111">Not supported.</span></span>    |
|<span data-ttu-id="b29ba-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b29ba-112">Application</span></span> | <span data-ttu-id="b29ba-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b29ba-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b29ba-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b29ba-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/fill/clear
POST /workbook/worksheets/{id|name}/range(<address>)/format/fill/clear
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/fill/clear

```
## <a name="request-headers"></a><span data-ttu-id="b29ba-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ba-115">Request headers</span></span>
| <span data-ttu-id="b29ba-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b29ba-116">Name</span></span>       | <span data-ttu-id="b29ba-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b29ba-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b29ba-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b29ba-118">Authorization</span></span>  | <span data-ttu-id="b29ba-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b29ba-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b29ba-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ba-121">Request body</span></span>

## <a name="response"></a><span data-ttu-id="b29ba-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29ba-122">Response</span></span>

<span data-ttu-id="b29ba-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b29ba-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b29ba-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b29ba-125">Example</span></span>
<span data-ttu-id="b29ba-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b29ba-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b29ba-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b29ba-127">Request</span></span>
<span data-ttu-id="b29ba-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b29ba-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangefill_clear"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/fill/clear
```

##### <a name="response"></a><span data-ttu-id="b29ba-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b29ba-129">Response</span></span>
<span data-ttu-id="b29ba-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b29ba-130">Here is an example of the response.</span></span> 
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
  "description": "RangeFill: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->