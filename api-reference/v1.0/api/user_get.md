# <a name="get-a-user"></a><span data-ttu-id="79de2-101">Obtener un usuario</span><span class="sxs-lookup"><span data-stu-id="79de2-101">Get a user</span></span>

<span data-ttu-id="79de2-102">Recupere las propiedades y las relaciones del objeto de usuario.</span><span class="sxs-lookup"><span data-stu-id="79de2-102">Retrieve the properties and relationships of user object.</span></span>

> <span data-ttu-id="79de2-p101">Nota: La obtención de un usuario solo devuelve un conjunto predeterminado de propiedades (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` para obtener otras propiedades y relaciones del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="79de2-p101">Note: Getting a user returns a default set of properties only (*businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName*). Use `$select` to get the other properties and relationships for the [user](../resources/user.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="79de2-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="79de2-105">Permissions</span></span>
<span data-ttu-id="79de2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79de2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="79de2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79de2-108">Permission type</span></span>      | <span data-ttu-id="79de2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79de2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79de2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79de2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="79de2-111">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="79de2-111">User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="79de2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79de2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79de2-113">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="79de2-113">User.Read, User.ReadWrite</span></span>    |
|<span data-ttu-id="79de2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79de2-114">Application</span></span> | <span data-ttu-id="79de2-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79de2-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="79de2-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79de2-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="79de2-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="79de2-117">Optional query parameters</span></span>
<span data-ttu-id="79de2-118">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79de2-118">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="79de2-119">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="79de2-119">By default, only a limited set of properties are returned (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span></span> 

<span data-ttu-id="79de2-120">Para devolver un conjunto de propiedades alternativo, tiene que especificar el conjunto de propiedades de [usuario](../resources/user.md) que prefiera con el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="79de2-120">To return an alternative property set, you must specify the desired set of [user](../resources/user.md) properties using the ODATA `$select` query parameter. For example, to return displayName, givenName, id and postalCode, you would use the add the following to your query </span></span> <span data-ttu-id="79de2-121">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="79de2-121">To return an alternative property set, you must specify the desired set of user properties using the ODATA  query parameter. For example, to return _displayName_, _givenName, id_ and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

## <a name="request-headers"></a><span data-ttu-id="79de2-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79de2-122">Request headers</span></span>
| <span data-ttu-id="79de2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79de2-123">Header</span></span>       | <span data-ttu-id="79de2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="79de2-124">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="79de2-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="79de2-125">Authorization</span></span>  | <span data-ttu-id="79de2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="79de2-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="79de2-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="79de2-128">Content-Type</span></span>   | <span data-ttu-id="79de2-129">application/json</span><span class="sxs-lookup"><span data-stu-id="79de2-129">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="79de2-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="79de2-130">Request body</span></span>
<span data-ttu-id="79de2-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79de2-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="79de2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79de2-132">Response</span></span>

<span data-ttu-id="79de2-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79de2-133">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="79de2-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="79de2-134">Examples</span></span>

### <a name="example-1-standard-users-request"></a><span data-ttu-id="79de2-135">Ejemplo 1: Solicitud de usuarios estándar</span><span class="sxs-lookup"><span data-stu-id="79de2-135">Example 1: Standard users request</span></span>

<span data-ttu-id="79de2-136">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="79de2-136">By default, only a limited set of properties are returned (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span></span> <span data-ttu-id="79de2-137">Este ejemplo ilustra las solicitudes y respuestas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="79de2-137">This example illustrates the default request and response.</span></span> 

##### <a name="request"></a><span data-ttu-id="79de2-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79de2-138">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/me
```
##### <a name="response"></a><span data-ttu-id="79de2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79de2-139">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```

### <a name="example-2-users-request-using-select"></a><span data-ttu-id="79de2-140">Ejemplo 2: Solicitud de los usuarios mediante $select</span><span class="sxs-lookup"><span data-stu-id="79de2-140">Example 2: Users request using $select</span></span>

<span data-ttu-id="79de2-141">Si necesita otro conjunto de propiedades, puede usar el parámetro de consulta `$select` de OData.</span><span class="sxs-lookup"><span data-stu-id="79de2-141">If you need a different property set, you can use the OData `$select` query parameter.</span></span> <span data-ttu-id="79de2-142">Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="79de2-142">To return an alternative property set, you must specify the desired set of user properties using the ODATA  query parameter. For example, to return _displayName_, _givenName, id_ and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

##### <a name="request"></a><span data-ttu-id="79de2-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79de2-143">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/me?$select=displayName,givenName,postalCode
```
##### <a name="response"></a><span data-ttu-id="79de2-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79de2-144">Response</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "postalCode": "postalCode-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
