# <a name="create-user"></a><span data-ttu-id="0f9e7-101">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="0f9e7-101">Create User</span></span>

<span data-ttu-id="0f9e7-p101">Use esta API para crear un nuevo usuario. El cuerpo de la solicitud contiene el usuario que se creará. Como mínimo, debe especificar las propiedades necesarias para el usuario. De forma opcional, puede especificar cualquier otra propiedad modificable.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-p101">Use this API to create a new User. The request body contains the user to create. At a minimum, you must specify the required properties for the user. You can optionally specify any other writable properties.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0f9e7-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0f9e7-106">Prerequisites</span></span>
<span data-ttu-id="0f9e7-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="0f9e7-107">One of the following **scopes** is required to execute this API: *User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="0f9e7-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f9e7-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users
```
## <a name="request-headers"></a><span data-ttu-id="0f9e7-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f9e7-109">Request headers</span></span>
| <span data-ttu-id="0f9e7-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f9e7-110">Header</span></span>       | <span data-ttu-id="0f9e7-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0f9e7-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0f9e7-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="0f9e7-112">Authorization</span></span>  | <span data-ttu-id="0f9e7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="0f9e7-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0f9e7-115">Content-Type</span></span>  | <span data-ttu-id="0f9e7-116">application/json</span><span class="sxs-lookup"><span data-stu-id="0f9e7-116">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0f9e7-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f9e7-117">Request body</span></span>
<span data-ttu-id="0f9e7-118">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="0f9e7-118">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>

<span data-ttu-id="0f9e7-119">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-119">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="0f9e7-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0f9e7-120">Parameter</span></span> | <span data-ttu-id="0f9e7-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f9e7-121">Type</span></span> | <span data-ttu-id="0f9e7-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f9e7-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0f9e7-123">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="0f9e7-123">accountEnabled</span></span> |<span data-ttu-id="0f9e7-124">boolean</span><span class="sxs-lookup"><span data-stu-id="0f9e7-124">boolean</span></span> |<span data-ttu-id="0f9e7-125">true si la cuenta está habilitada; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-125">true if the account is enabled; otherwise, false.</span></span>|
|<span data-ttu-id="0f9e7-126">displayName</span><span class="sxs-lookup"><span data-stu-id="0f9e7-126">displayName</span></span> |<span data-ttu-id="0f9e7-127">string</span><span class="sxs-lookup"><span data-stu-id="0f9e7-127">string</span></span> |<span data-ttu-id="0f9e7-128">El nombre para mostrar en la libreta de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-128">The name to display in the address book for the user.</span></span>|
|<span data-ttu-id="0f9e7-129">onPremisesImmutableId</span><span class="sxs-lookup"><span data-stu-id="0f9e7-129">onPremisesImmutableId</span></span> |<span data-ttu-id="0f9e7-130">string</span><span class="sxs-lookup"><span data-stu-id="0f9e7-130">string</span></span> |<span data-ttu-id="0f9e7-131">Solo se debe especificar al crear una nueva cuenta de usuario si usa un dominio federado para la propiedad userPrincipalName (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-131">Only needs to be specified when creating a new user account if you are using a federated domain for the user's userPrincipalName (UPN) property.</span></span>|
|<span data-ttu-id="0f9e7-132">mailNickname</span><span class="sxs-lookup"><span data-stu-id="0f9e7-132">mailNickname</span></span> |<span data-ttu-id="0f9e7-133">string</span><span class="sxs-lookup"><span data-stu-id="0f9e7-133">string</span></span> |<span data-ttu-id="0f9e7-134">El alias de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-134">The mail alias for the user.</span></span>|
|<span data-ttu-id="0f9e7-135">passwordProfile</span><span class="sxs-lookup"><span data-stu-id="0f9e7-135">passwordProfile</span></span>|[<span data-ttu-id="0f9e7-136">PasswordProfile</span><span class="sxs-lookup"><span data-stu-id="0f9e7-136">PasswordProfile</span></span>](../resources/passwordprofile.md) |<span data-ttu-id="0f9e7-137">El perfil de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-137">The password profile for the user.</span></span>|
|<span data-ttu-id="0f9e7-138">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0f9e7-138">userPrincipalName</span></span> |<span data-ttu-id="0f9e7-139">string</span><span class="sxs-lookup"><span data-stu-id="0f9e7-139">string</span></span> |<span data-ttu-id="0f9e7-140">El nombre principal de usuario (usuario@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="0f9e7-140">The user principal name (someuser@contoso.com).</span></span>|

## <a name="response"></a><span data-ttu-id="0f9e7-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f9e7-141">Response</span></span>

<span data-ttu-id="0f9e7-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-142">If successful, this method returns `201, Created` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f9e7-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f9e7-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0f9e7-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f9e7-144">Request</span></span>
<span data-ttu-id="0f9e7-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_user_from_users"
}-->
```http
POST https://graph.microsoft.com/v1.0/users
Content-type: application/json

{
  "accountEnabled": true,
  "displayName": "displayName-value",
  "mailNickname": "mailNickname-value",
  "userPrincipalName": "upn-value@tenant-value.onmicrosoft.com",
  "passwordProfile" : {
    "forceChangePasswordNextSignIn": true,
    "password": "password-value"
  }
}
```
<span data-ttu-id="0f9e7-146">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="0f9e7-146">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="0f9e7-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f9e7-147">Response</span></span>
<span data-ttu-id="0f9e7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0f9e7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users/$entity",
    "id": "id-value",
    "businessPhones": [],
    "displayName": "displayName-value",
    "givenName": null,
    "jobTitle": null,
    "mail": null,
    "mobilePhone": null,
    "officeLocation": null,
    "preferredLanguage": null,
    "surname": null,
    "userPrincipalName": "upn-value@tenant-value.onmicrosoft.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create User",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
