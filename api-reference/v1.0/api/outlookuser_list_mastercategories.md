# <a name="list-outlook-categories"></a><span data-ttu-id="b528e-101">Enumerar categorías de Outlook</span><span class="sxs-lookup"><span data-stu-id="b528e-101">List Outlook categories</span></span>


<span data-ttu-id="b528e-102">Obtener todas las categorías que han sido definidas por el usuario.</span><span class="sxs-lookup"><span data-stu-id="b528e-102">Get all the categories that have been defined for the user.</span></span>

## <a name="permissions"></a><span data-ttu-id="b528e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b528e-103">Permissions</span></span>
<span data-ttu-id="b528e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b528e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b528e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b528e-106">Permission type</span></span>      | <span data-ttu-id="b528e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b528e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b528e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b528e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b528e-109">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b528e-109">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="b528e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b528e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b528e-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b528e-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="b528e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b528e-112">Application</span></span> | <span data-ttu-id="b528e-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="b528e-113">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="b528e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b528e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/masterCategories
GET /users/{id|userPrincipalName}/outlook/masterCategories
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b528e-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b528e-115">Optional query parameters</span></span>
<span data-ttu-id="b528e-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b528e-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b528e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b528e-117">Request headers</span></span>
| <span data-ttu-id="b528e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b528e-118">Name</span></span>      |<span data-ttu-id="b528e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="b528e-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="b528e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b528e-120">Authorization</span></span>  | <span data-ttu-id="b528e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b528e-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b528e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b528e-123">Request body</span></span>
<span data-ttu-id="b528e-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b528e-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b528e-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b528e-125">Response</span></span>

<span data-ttu-id="b528e-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [outlookCategory](../resources/outlookCategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b528e-126">If successful, this method returns a `200 OK` response code and collection of [outlookCategory](../resources/outlookCategory.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b528e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b528e-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b528e-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b528e-128">Request</span></span>
<span data-ttu-id="b528e-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b528e-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mastercategories"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/masterCategories
```
##### <a name="response"></a><span data-ttu-id="b528e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b528e-130">Response</span></span>
<span data-ttu-id="b528e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b528e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 727

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories",
  "value":[
    {
      "id":"5a9a6aa8-b65f-4357-b1f9-60c6bf6330d8",
      "displayName":"Red category",
      "color":"preset0"
    },
    {
      "id":"4b1c2495-54c9-4a5e-90a2-0ab0b31987d8",
      "displayName":"Orange category",
      "color":"preset1"
    },
    {
      "id":"de912e4d-c790-4da9-949c-ccd933aaa0f7",
      "displayName":"Yellow category",
      "color":"preset3"
    },
    {
      "id":"79c8d8f8-9db1-49ec-99ce-ae25793e7232",
      "displayName":"Green category",
      "color":"preset4"
    },
    {
      "id":"626e696c-6a10-48b8-89b9-12de3160cfb9",
      "displayName":"Blue category",
      "color":"preset7"
    },
    {
      "id":"453d06d0-447d-41f7-91cd-aa0f6b190b5b",
      "displayName":"Purple category",
      "color":"preset8"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List categories",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->