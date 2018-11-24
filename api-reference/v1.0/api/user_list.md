# <a name="list-users"></a><span data-ttu-id="115db-101">List users</span><span class="sxs-lookup"><span data-stu-id="115db-101">List users</span></span>

<span data-ttu-id="115db-102">Recupera una lista de objetos de usuario.</span><span class="sxs-lookup"><span data-stu-id="115db-102">Retrieve a list of user objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="115db-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="115db-103">Permissions</span></span>

<span data-ttu-id="115db-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="115db-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="115db-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="115db-106">Permission type</span></span>      | <span data-ttu-id="115db-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="115db-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="115db-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="115db-108">Delegated (work or school account)</span></span> | <span data-ttu-id="115db-109">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="115db-109">User.ReadBasic.All, User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="115db-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="115db-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="115db-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="115db-111">Not supported.</span></span>    |
|<span data-ttu-id="115db-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="115db-112">Application</span></span> | <span data-ttu-id="115db-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="115db-113">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="115db-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="115db-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users
```

## <a name="optional-query-parameters"></a><span data-ttu-id="115db-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="115db-115">Optional query parameters</span></span>

<span data-ttu-id="115db-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="115db-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="115db-117">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_).</span><span class="sxs-lookup"><span data-stu-id="115db-117">By default, only a limited set of properties are returned ( _businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_ ).</span></span> 

<span data-ttu-id="115db-p102">Para devolver un conjunto de propiedades alternativo, tiene que especificar el conjunto de propiedades de [usuario](../resources/user.md) que prefiera con el parámetro de consulta `$select` de OData. Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="115db-p102">To return an alternative property set, you must specify the desired set of [user](../resources/user.md) properties using the OData `$select` query parameter. For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

> <span data-ttu-id="115db-p103">Nota: Algunas propiedades no se pueden devolver dentro de una colección de usuario. Las propiedades siguientes solo se admiten al [recuperar un único usuario](./user_get.md): _aboutMe, birthday, hireDate, interests, mySite, pastProjects, preferredName, responsibilities, schools, skills, mailboxSettings_</span><span class="sxs-lookup"><span data-stu-id="115db-p103">Note: Certain properties cannot be returned within a user collection. The following properties are only supported when [retrieving an single user](./user_get.md): _aboutMe, birthday, hireDate, interests, mySite, pastProjects, preferredName, responsibilities, schools, skills, mailboxSettings_</span></span>

## <a name="request-headers"></a><span data-ttu-id="115db-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="115db-122">Request headers</span></span>

| <span data-ttu-id="115db-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="115db-123">Header</span></span>        | <span data-ttu-id="115db-124">Valor</span><span class="sxs-lookup"><span data-stu-id="115db-124">Value</span></span>                      |
|:--------------|:---------------------------|
| <span data-ttu-id="115db-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="115db-125">Authorization</span></span> | <span data-ttu-id="115db-126">{token} de portador (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="115db-126">Bearer {token} (required)</span></span>  |
| <span data-ttu-id="115db-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="115db-127">Content-Type</span></span>  | <span data-ttu-id="115db-128">application/json</span><span class="sxs-lookup"><span data-stu-id="115db-128">application/json</span></span>           |

## <a name="request-body"></a><span data-ttu-id="115db-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="115db-129">Request body</span></span>

<span data-ttu-id="115db-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="115db-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="115db-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="115db-131">Response</span></span>

<span data-ttu-id="115db-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="115db-132">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="115db-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="115db-133">Examples</span></span>

### <a name="example-1-standard-users-request"></a><span data-ttu-id="115db-134">Ejemplo 1: Solicitud de usuarios estándar</span><span class="sxs-lookup"><span data-stu-id="115db-134">Example 1: Standard users request</span></span>

<span data-ttu-id="115db-p104">De forma predeterminada, solo se devuelve un conjunto limitado de propiedades. (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_). Este ejemplo ilustra las solicitudes y respuestas predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="115db-p104">By default, only a limited set of properties are returned (_businessPhones, displayName, givenName, id, jobTitle, mail, mobilePhone, officeLocation, preferredLanguage, surname, userPrincipalName_). This example illustrates the default request and response.</span></span> 

##### <a name="request"></a><span data-ttu-id="115db-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="115db-137">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/users
```

##### <a name="response"></a><span data-ttu-id="115db-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="115db-138">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 608

{
  "value": [
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
  ]
}
```

### <a name="example-2-users-request-using-select"></a><span data-ttu-id="115db-139">Ejemplo 2: Solicitud de los usuarios mediante $select</span><span class="sxs-lookup"><span data-stu-id="115db-139">Example 2: Users request using $select</span></span>

<span data-ttu-id="115db-p105">Si necesita otro conjunto de propiedades, puede usar el parámetro de consulta `$select` de OData. Por ejemplo, para devolver _displayName_, _givenName_ y _postalCode_, tendría que agregar lo siguiente a la consulta: `$select=displayName,givenName,postalCode`</span><span class="sxs-lookup"><span data-stu-id="115db-p105">If you need a different property set, you can use the OData `$select` query parameter. For example, to return _displayName_, _givenName_, and _postalCode_, you would use the add the following to your query `$select=displayName,givenName,postalCode`</span></span>

##### <a name="request"></a><span data-ttu-id="115db-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="115db-142">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_users"
}-->
```http
GET https://graph.microsoft.com/v1.0/users?$select=displayName,givenName,postalCode
```

##### <a name="response"></a><span data-ttu-id="115db-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="115db-143">Response</span></span>

<span data-ttu-id="115db-144">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="115db-144">Note: The response object shown here may be truncated for brevity.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 159

{
  "value": [
    {
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "postalCode": "postalCode-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List users",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
