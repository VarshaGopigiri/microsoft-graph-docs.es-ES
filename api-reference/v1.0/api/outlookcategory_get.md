# <a name="get-outlook-category"></a><span data-ttu-id="98229-101">Obtener categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="98229-101">Get Outlook category</span></span>


<span data-ttu-id="98229-102">Obtener las propiedades y relaciones del objeto [outlookCategory](../resources/outlookCategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="98229-102">Get the properties and relationships of the specified [outlookCategory](../resources/outlookCategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="98229-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="98229-103">Permissions</span></span>
<span data-ttu-id="98229-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="98229-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="98229-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98229-106">Permission type</span></span>      | <span data-ttu-id="98229-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98229-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="98229-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98229-108">Delegated (work or school account)</span></span> | <span data-ttu-id="98229-109">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="98229-109">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="98229-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98229-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="98229-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="98229-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="98229-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98229-112">Application</span></span> | <span data-ttu-id="98229-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="98229-113">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="98229-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98229-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories/{id}
GET /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="98229-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="98229-115">Optional query parameters</span></span>
<span data-ttu-id="98229-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98229-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="98229-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98229-117">Request headers</span></span>
| <span data-ttu-id="98229-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="98229-118">Name</span></span>      |<span data-ttu-id="98229-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="98229-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="98229-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="98229-120">Authorization</span></span>  | <span data-ttu-id="98229-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="98229-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="98229-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98229-123">Request body</span></span>
<span data-ttu-id="98229-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="98229-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="98229-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98229-125">Response</span></span>

<span data-ttu-id="98229-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [outlookCategory](../resources/outlookCategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98229-126">If successful, this method returns a `200 OK` response code and [outlookCategory](../resources/outlookCategory.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="98229-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98229-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="98229-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98229-128">Request</span></span>
<span data-ttu-id="98229-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98229-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["de912e4d-c790-4da9-949c-ccd933aaa0f7"],
  "name": "get_outlookcategory"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/masterCategories/de912e4d-c790-4da9-949c-ccd933aaa0f7
```
##### <a name="response"></a><span data-ttu-id="98229-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98229-130">Response</span></span>
<span data-ttu-id="98229-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98229-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 249

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"de912e4d-c790-4da9-949c-ccd933aaa0f7",
  "displayName":"Yellow category",
  "color":"preset3"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->