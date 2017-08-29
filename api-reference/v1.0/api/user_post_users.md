# <a name="create-user"></a><span data-ttu-id="9a7ce-101">Crear usuario</span><span class="sxs-lookup"><span data-stu-id="9a7ce-101">Create User</span></span>

<span data-ttu-id="9a7ce-p101">Use esta API para crear un nuevo usuario. El cuerpo de la solicitud contiene el usuario que se creará. Como mínimo, debe especificar las propiedades necesarias para el usuario. De forma opcional, puede especificar cualquier otra propiedad modificable.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-p101">Use this API to create a new User. The request body contains the user to create. At a minimum, you must specify the required properties for the user. You can optionally specify any other writable properties.</span></span>
## <a name="permissions"></a><span data-ttu-id="9a7ce-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="9a7ce-106">Permissions</span></span>
<span data-ttu-id="9a7ce-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9a7ce-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9a7ce-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a7ce-109">Permission type</span></span>      | <span data-ttu-id="9a7ce-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a7ce-110">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="9a7ce-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a7ce-111">Delegated (work or school account)</span></span> | <span data-ttu-id="9a7ce-112">User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="9a7ce-112">One of the following scopes is required to execute this API: User.ReadWrite.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="9a7ce-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a7ce-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9a7ce-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-114">Not supported.</span></span>    | 
|<span data-ttu-id="9a7ce-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a7ce-115">Application</span></span> | <span data-ttu-id="9a7ce-116">User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9a7ce-116">User.ReadWrite.All, Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9a7ce-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a7ce-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users
```
## <a name="request-headers"></a><span data-ttu-id="9a7ce-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7ce-118">Request headers</span></span>
| <span data-ttu-id="9a7ce-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a7ce-119">Header</span></span>       | <span data-ttu-id="9a7ce-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9a7ce-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9a7ce-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9a7ce-121">Authorization</span></span>  | <span data-ttu-id="9a7ce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9a7ce-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9a7ce-124">Content-Type</span></span>  | <span data-ttu-id="9a7ce-125">application/json</span><span class="sxs-lookup"><span data-stu-id="9a7ce-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9a7ce-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7ce-126">Request body</span></span>
<span data-ttu-id="9a7ce-127">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="9a7ce-127">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>

<span data-ttu-id="9a7ce-128">En la tabla siguiente, se muestran las propiedades necesarias al crear un usuario.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-128">The following table shows the properties that are required when you create a user.</span></span>

| <span data-ttu-id="9a7ce-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9a7ce-129">Parameter</span></span> | <span data-ttu-id="9a7ce-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a7ce-130">Type</span></span> | <span data-ttu-id="9a7ce-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a7ce-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a7ce-132">accountEnabled</span><span class="sxs-lookup"><span data-stu-id="9a7ce-132">accountEnabled</span></span> |<span data-ttu-id="9a7ce-133">boolean</span><span class="sxs-lookup"><span data-stu-id="9a7ce-133">boolean</span></span> |<span data-ttu-id="9a7ce-134">true si la cuenta está habilitada; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-134">true if the account is enabled; otherwise, false.</span></span>|
|<span data-ttu-id="9a7ce-135">displayName</span><span class="sxs-lookup"><span data-stu-id="9a7ce-135">displayName</span></span> |<span data-ttu-id="9a7ce-136">string</span><span class="sxs-lookup"><span data-stu-id="9a7ce-136">string</span></span> |<span data-ttu-id="9a7ce-137">El nombre para mostrar en la libreta de direcciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-137">The name to display in the address book for the user.</span></span>|
|<span data-ttu-id="9a7ce-138">onPremisesImmutableId</span><span class="sxs-lookup"><span data-stu-id="9a7ce-138">onPremisesImmutableId</span></span> |<span data-ttu-id="9a7ce-139">string</span><span class="sxs-lookup"><span data-stu-id="9a7ce-139">string</span></span> |<span data-ttu-id="9a7ce-140">Solo se debe especificar al crear una nueva cuenta de usuario si usa un dominio federado para la propiedad userPrincipalName (UPN) del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-140">Only needs to be specified when creating a new user account if you are using a federated domain for the user's userPrincipalName (UPN) property.</span></span>|
|<span data-ttu-id="9a7ce-141">mailNickname</span><span class="sxs-lookup"><span data-stu-id="9a7ce-141">mailNickname</span></span> |<span data-ttu-id="9a7ce-142">string</span><span class="sxs-lookup"><span data-stu-id="9a7ce-142">string</span></span> |<span data-ttu-id="9a7ce-143">El alias de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-143">The mail alias for the user.</span></span>|
|<span data-ttu-id="9a7ce-144">passwordProfile</span><span class="sxs-lookup"><span data-stu-id="9a7ce-144">passwordProfile</span></span>|[<span data-ttu-id="9a7ce-145">PasswordProfile</span><span class="sxs-lookup"><span data-stu-id="9a7ce-145">PasswordProfile</span></span>](../resources/passwordprofile.md) |<span data-ttu-id="9a7ce-146">El perfil de contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-146">The password profile for the user.</span></span>|
|<span data-ttu-id="9a7ce-147">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9a7ce-147">userPrincipalName</span></span> |<span data-ttu-id="9a7ce-148">string</span><span class="sxs-lookup"><span data-stu-id="9a7ce-148">string</span></span> |<span data-ttu-id="9a7ce-149">El nombre principal de usuario (usuario@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="9a7ce-149">The user principal name (someuser@contoso.com).</span></span>|

## <a name="response"></a><span data-ttu-id="9a7ce-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a7ce-150">Response</span></span>

<span data-ttu-id="9a7ce-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-151">If successful, this method returns `201, Created` response code and [user](../resources/user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a7ce-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a7ce-152">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9a7ce-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a7ce-153">Request</span></span>
<span data-ttu-id="9a7ce-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-154">Here is an example of the request.</span></span>
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
<span data-ttu-id="9a7ce-155">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="9a7ce-155">In the request body, supply a JSON representation of [user](../resources/user.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="9a7ce-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a7ce-156">Response</span></span>
<span data-ttu-id="9a7ce-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a7ce-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
