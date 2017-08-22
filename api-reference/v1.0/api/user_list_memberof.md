# <a name="list-memberof"></a><span data-ttu-id="4ab76-101">Enumerar memberOf</span><span class="sxs-lookup"><span data-stu-id="4ab76-101">List memberOf</span></span>

<span data-ttu-id="4ab76-102">Obtiene todos los [grupos](../resources/group.md) y [roles de directorio](../resources/directoryrole.md) de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="4ab76-102">Get [groups](../resources/group.md) and [directory roles](../resources/directoryrole.md) that the user is a direct member of.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="4ab76-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4ab76-103">Prerequisites</span></span>
<span data-ttu-id="4ab76-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="4ab76-104">One of the following **scopes** is required to execute this API: *Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="4ab76-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ab76-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="4ab76-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="4ab76-106">Optional query parameters</span></span>
<span data-ttu-id="4ab76-p101">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta. No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="4ab76-p101">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response. $filter is not supported.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="4ab76-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4ab76-109">Request headers</span></span>
| <span data-ttu-id="4ab76-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4ab76-110">Header</span></span>       | <span data-ttu-id="4ab76-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4ab76-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4ab76-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="4ab76-112">Authorization</span></span>  | <span data-ttu-id="4ab76-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4ab76-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="4ab76-115">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4ab76-115">Accept</span></span>  | <span data-ttu-id="4ab76-116">application/json</span><span class="sxs-lookup"><span data-stu-id="4ab76-116">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4ab76-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ab76-117">Request body</span></span>
<span data-ttu-id="4ab76-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4ab76-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4ab76-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ab76-119">Response</span></span>

<span data-ttu-id="4ab76-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ab76-120">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="4ab76-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ab76-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4ab76-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4ab76-122">Request</span></span>
<span data-ttu-id="4ab76-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4ab76-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/memberOf
```
##### <a name="response"></a><span data-ttu-id="4ab76-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ab76-124">Response</span></span>
<span data-ttu-id="4ab76-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4ab76-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
