# <a name="list-domainnamereferences"></a><span data-ttu-id="c3cc3-101">Enumerar domainNameReferences</span><span class="sxs-lookup"><span data-stu-id="c3cc3-101">List domainNameReferences</span></span>

<span data-ttu-id="c3cc3-p101">Recupere una lista de [directoryObject](../resources/directoryobject.md) con una referencia al dominio. La lista devuelta contendrá todos los objetos del directorio que tengan una dependencia en el dominio.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-p101">Retrieve a list of [directoryObject](../resources/directoryobject.md) with a reference to the domain. The returned list will contain all directory objects that have a dependency on the domain.</span></span>

## <a name="permissions"></a><span data-ttu-id="c3cc3-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="c3cc3-104">Permissions</span></span>

<span data-ttu-id="c3cc3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c3cc3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="c3cc3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c3cc3-107">Permission type</span></span>      | <span data-ttu-id="c3cc3-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c3cc3-108">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="c3cc3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c3cc3-109">Delegated (work or school account)</span></span> | <span data-ttu-id="c3cc3-110">Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="c3cc3-110">Directory.Read.All</span></span>    | 
|<span data-ttu-id="c3cc3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c3cc3-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3cc3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-112">Not supported.</span></span>    | 
|<span data-ttu-id="c3cc3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c3cc3-113">Application</span></span> | <span data-ttu-id="c3cc3-114">Directory.Read.All, Domain.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3cc3-114">Directory.Read.All, Domain.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="c3cc3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3cc3-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /domains/{id}/domainNameReferences
```

> <span data-ttu-id="c3cc3-116">En {id}, especifique el dominio con su nombre completo.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-116">For {id}, specify the domain with its fully qualified domain name.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="c3cc3-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c3cc3-117">Optional query parameters</span></span>

<span data-ttu-id="c3cc3-118">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-118">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c3cc3-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3cc3-119">Request headers</span></span>

| <span data-ttu-id="c3cc3-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3cc3-120">Name</span></span>      |<span data-ttu-id="c3cc3-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3cc3-121">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="c3cc3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3cc3-122">Authorization</span></span>  | <span data-ttu-id="c3cc3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c3cc3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c3cc3-125">Request body</span></span>

<span data-ttu-id="c3cc3-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c3cc3-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3cc3-127">Response</span></span>

<span data-ttu-id="c3cc3-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-128">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c3cc3-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3cc3-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3cc3-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3cc3-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_domainnamereferences"
}-->
```http
GET https://graph.microsoft.com/V1.0/domains/contoso.com/domainNameReferences
```

##### <a name="response"></a><span data-ttu-id="c3cc3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3cc3-131">Response</span></span>
<span data-ttu-id="c3cc3-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c3cc3-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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