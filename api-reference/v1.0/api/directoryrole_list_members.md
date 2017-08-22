# <a name="list-members"></a><span data-ttu-id="3249f-101">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="3249f-101">List members</span></span>

<span data-ttu-id="3249f-p101">Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="3249f-p101">Retrieve a list of the users that are assigned to the directory role.  Only users can be assigned to a directory role.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3249f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3249f-104">Prerequisites</span></span>
<span data-ttu-id="3249f-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="3249f-105">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="3249f-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3249f-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3249f-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3249f-107">Optional query parameters</span></span>
<span data-ttu-id="3249f-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3249f-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3249f-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3249f-109">Request headers</span></span>
| <span data-ttu-id="3249f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="3249f-110">Name</span></span>       | <span data-ttu-id="3249f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3249f-111">Type</span></span> | <span data-ttu-id="3249f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3249f-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3249f-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="3249f-113">Authorization</span></span>  | <span data-ttu-id="3249f-114">string</span><span class="sxs-lookup"><span data-stu-id="3249f-114">string</span></span>  | <span data-ttu-id="3249f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3249f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3249f-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3249f-117">Request body</span></span>
<span data-ttu-id="3249f-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3249f-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3249f-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3249f-119">Response</span></span>

<span data-ttu-id="3249f-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3249f-120">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3249f-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3249f-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3249f-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3249f-122">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
```
##### <a name="response"></a><span data-ttu-id="3249f-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3249f-123">Response</span></span>
<span data-ttu-id="3249f-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3249f-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "businessPhones":["000-000-0000"],
      "displayName":"First Last",
      "givenName":"First",
      "jobTitle":null,
      "mail":"first@example.com",
      "officeLocation":null,
      "preferredLanguage":"en-US",
      "surname":"Last",
      "userPrincipalName":"first@example.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->