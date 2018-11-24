# <a name="delete-outlook-category"></a><span data-ttu-id="04f55-101">Eliminar categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="04f55-101">Delete Outlook category</span></span>


<span data-ttu-id="04f55-102">Eliminar el objeto [outlookCategory](../resources/outlookCategory.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="04f55-102">Delete the specified [outlookCategory](../resources/outlookCategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="04f55-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="04f55-103">Permissions</span></span>
<span data-ttu-id="04f55-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="04f55-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="04f55-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="04f55-106">Permission type</span></span>      | <span data-ttu-id="04f55-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="04f55-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="04f55-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="04f55-108">Delegated (work or school account)</span></span> | <span data-ttu-id="04f55-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04f55-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="04f55-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="04f55-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="04f55-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04f55-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="04f55-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="04f55-112">Application</span></span> | <span data-ttu-id="04f55-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="04f55-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="04f55-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="04f55-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="04f55-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="04f55-115">Optional query parameters</span></span>
<span data-ttu-id="04f55-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04f55-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="04f55-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="04f55-117">Request headers</span></span>
| <span data-ttu-id="04f55-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="04f55-118">Name</span></span>      |<span data-ttu-id="04f55-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="04f55-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="04f55-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="04f55-120">Authorization</span></span>  | <span data-ttu-id="04f55-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="04f55-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="04f55-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="04f55-123">Request body</span></span>
<span data-ttu-id="04f55-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="04f55-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="04f55-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04f55-125">Response</span></span>

<span data-ttu-id="04f55-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04f55-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="04f55-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="04f55-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="04f55-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="04f55-129">Request</span></span>
<span data-ttu-id="04f55-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="04f55-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["4b1c2495-54c9-4a5e-90a2-0ab0b31987d8"],
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/outlook/masterCategories/4b1c2495-54c9-4a5e-90a2-0ab0b31987d8
```
##### <a name="response"></a><span data-ttu-id="04f55-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="04f55-131">Response</span></span>
<span data-ttu-id="04f55-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="04f55-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "name": "delete_outlookcategory",
  "isEmpty": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->