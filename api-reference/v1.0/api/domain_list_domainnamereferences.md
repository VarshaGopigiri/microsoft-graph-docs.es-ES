# <a name="list-domainnamereferences"></a><span data-ttu-id="93c20-101">Enumerar domainNameReferences</span><span class="sxs-lookup"><span data-stu-id="93c20-101">List domainNameReferences</span></span>

<span data-ttu-id="93c20-p101">Recupere una lista de [directoryObject](../resources/directoryobject.md) con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.</span><span class="sxs-lookup"><span data-stu-id="93c20-p101">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain. The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="93c20-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="93c20-104">Prerequisites</span></span>

<span data-ttu-id="93c20-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All* o *Domain.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="93c20-105">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Domain.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="93c20-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93c20-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="93c20-107">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="93c20-107">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="93c20-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="93c20-108">Optional query parameters</span></span>

<span data-ttu-id="93c20-109">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93c20-109">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="93c20-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="93c20-110">Request headers</span></span>

| <span data-ttu-id="93c20-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="93c20-111">Name</span></span>      |<span data-ttu-id="93c20-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="93c20-112">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="93c20-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="93c20-113">Authorization</span></span>  | <span data-ttu-id="93c20-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="93c20-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="93c20-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93c20-116">Request body</span></span>

<span data-ttu-id="93c20-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="93c20-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="93c20-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93c20-118">Response</span></span>

<span data-ttu-id="93c20-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93c20-119">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="93c20-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93c20-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="93c20-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93c20-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com/domainNameReferences
```

##### <a name="response"></a><span data-ttu-id="93c20-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93c20-122">Response</span></span>
<span data-ttu-id="93c20-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="93c20-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
        "odata.type": "Microsoft.DirectoryServices.User",
        "objectType": "User",
        "objectId": "567a0db6-289c-43f7-a650-2645c03cbbbb",
        "accountEnabled": true,
        "displayName": "TestUser1",
        "facsimileTelephoneNumber": null,
        "mailNickname": "testuser1",
        "mobile": null,
        "userPrincipalName": "testuser1@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List domainNameReferences",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->