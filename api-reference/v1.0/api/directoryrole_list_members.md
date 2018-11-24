# <a name="list-members"></a><span data-ttu-id="a0c15-101">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="a0c15-101">List members</span></span>

<span data-ttu-id="a0c15-p101">Recupera una lista de los usuarios que están asignados al rol de directorio.  Solo los usuarios se pueden asignar a un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="a0c15-p101">Retrieve a list of the users that are assigned to the directory role.  Only users can be assigned to a directory role.</span></span>
## <a name="permissions"></a><span data-ttu-id="a0c15-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="a0c15-104">Permissions</span></span>
<span data-ttu-id="a0c15-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a0c15-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="a0c15-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a0c15-107">Permission type</span></span>      | <span data-ttu-id="a0c15-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a0c15-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a0c15-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a0c15-109">Delegated (work or school account)</span></span> | <span data-ttu-id="a0c15-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="a0c15-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="a0c15-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a0c15-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a0c15-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a0c15-112">Not supported.</span></span>    |
|<span data-ttu-id="a0c15-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a0c15-113">Application</span></span> | <span data-ttu-id="a0c15-114">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a0c15-114">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a0c15-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a0c15-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /directoryRoles/{id}/members
```
## <a name="optional-query-parameters"></a><span data-ttu-id="a0c15-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a0c15-116">Optional query parameters</span></span>
<span data-ttu-id="a0c15-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0c15-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="a0c15-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c15-118">Request headers</span></span>
| <span data-ttu-id="a0c15-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a0c15-119">Name</span></span>       | <span data-ttu-id="a0c15-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0c15-120">Type</span></span> | <span data-ttu-id="a0c15-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0c15-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a0c15-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a0c15-122">Authorization</span></span>  | <span data-ttu-id="a0c15-123">string</span><span class="sxs-lookup"><span data-stu-id="a0c15-123">string</span></span>  | <span data-ttu-id="a0c15-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a0c15-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a0c15-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c15-126">Request body</span></span>
<span data-ttu-id="a0c15-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a0c15-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a0c15-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0c15-128">Response</span></span>

<span data-ttu-id="a0c15-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a0c15-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a0c15-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0c15-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a0c15-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a0c15-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
```
##### <a name="response"></a><span data-ttu-id="a0c15-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a0c15-132">Response</span></span>
<span data-ttu-id="a0c15-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a0c15-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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