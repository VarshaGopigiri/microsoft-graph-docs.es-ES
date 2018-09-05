# <a name="create-group"></a><span data-ttu-id="69a68-101">Crear grupo</span><span class="sxs-lookup"><span data-stu-id="69a68-101">Create group</span></span>
<span data-ttu-id="69a68-p101">Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:</span><span class="sxs-lookup"><span data-stu-id="69a68-p101">Use this API to create a new group as specified in the request body. You can create one of three types of groups:</span></span>

* <span data-ttu-id="69a68-104">Grupo de Office 365 (grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="69a68-104">Office 365 Group (unified group)</span></span>
* <span data-ttu-id="69a68-105">Grupo dinámico</span><span class="sxs-lookup"><span data-stu-id="69a68-105">Dynamic group</span></span>
* <span data-ttu-id="69a68-106">Grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="69a68-106">Security group</span></span>

> <span data-ttu-id="69a68-p102">**Nota**: Aunque Microsoft Teams se basa en Grupos de Office 365, actualmente no puede crear un equipo mediante esta API. Puede usar las otras API de grupo para administrar un equipo que se ha creado en la interfaz de usuario de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="69a68-p102">**Note**: Although Microsoft Teams is built on Office 365 Groups, you can't currently create a team via this API. You can use the other group APIs to manage a team that has been created in the Microsoft Teams UI.</span></span>

## <a name="permissions"></a><span data-ttu-id="69a68-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="69a68-109">Permissions</span></span>
<span data-ttu-id="69a68-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="69a68-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="69a68-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="69a68-112">Permission type</span></span>      | <span data-ttu-id="69a68-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="69a68-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="69a68-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="69a68-114">Delegated (work or school account)</span></span> | <span data-ttu-id="69a68-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69a68-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="69a68-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="69a68-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="69a68-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="69a68-117">Not supported.</span></span>    |
|<span data-ttu-id="69a68-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="69a68-118">Application</span></span> | <span data-ttu-id="69a68-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="69a68-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="69a68-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="69a68-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```

## <a name="request-headers"></a><span data-ttu-id="69a68-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="69a68-121">Request headers</span></span>
| <span data-ttu-id="69a68-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="69a68-122">Name</span></span>       | <span data-ttu-id="69a68-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="69a68-123">Type</span></span> | <span data-ttu-id="69a68-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="69a68-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="69a68-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="69a68-125">Authorization</span></span>  | <span data-ttu-id="69a68-126">cadena</span><span class="sxs-lookup"><span data-stu-id="69a68-126">string</span></span>  | <span data-ttu-id="69a68-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="69a68-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="69a68-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="69a68-129">Request body</span></span>
<span data-ttu-id="69a68-130">La tabla siguiente muestra las propiedades del recurso [grupo](../resources/group.md) que debe especificar al crear un grupo.</span><span class="sxs-lookup"><span data-stu-id="69a68-130">The following table shows the properties of the [group](../resources/group.md) resource that you must specify at a minimum when you create a group.</span></span> 

| <span data-ttu-id="69a68-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="69a68-131">Property</span></span> | <span data-ttu-id="69a68-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="69a68-132">Type</span></span> | <span data-ttu-id="69a68-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="69a68-133">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="69a68-134">displayName</span><span class="sxs-lookup"><span data-stu-id="69a68-134">displayName</span></span> | <span data-ttu-id="69a68-135">cadena</span><span class="sxs-lookup"><span data-stu-id="69a68-135">string</span></span> | <span data-ttu-id="69a68-136">El nombre que se muestra en la libreta de direcciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="69a68-136">The name to display in the address book for the group.</span></span> <span data-ttu-id="69a68-137">Necesario.</span><span class="sxs-lookup"><span data-stu-id="69a68-137">Required.</span></span> |
| <span data-ttu-id="69a68-138">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="69a68-138">mailEnabled</span></span> | <span data-ttu-id="69a68-139">booleano</span><span class="sxs-lookup"><span data-stu-id="69a68-139">boolean</span></span> | <span data-ttu-id="69a68-140">Establézcalo en **true** para grupos habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="69a68-140">Set to **true** for mail-enabled groups.</span></span> <span data-ttu-id="69a68-141">Establézcalo en **true** si crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="69a68-141">Set this to **true** if creating an Office 365 Group.</span></span> <span data-ttu-id="69a68-142">Establézcalo en **false** si crea un grupo de seguridad o dinámico.</span><span class="sxs-lookup"><span data-stu-id="69a68-142">Set this to **false** if creating dynamic or security group.</span></span> <span data-ttu-id="69a68-143">Necesario.</span><span class="sxs-lookup"><span data-stu-id="69a68-143">Required.</span></span> |
| <span data-ttu-id="69a68-144">mailNickname</span><span class="sxs-lookup"><span data-stu-id="69a68-144">mailNickname</span></span> | <span data-ttu-id="69a68-145">cadena</span><span class="sxs-lookup"><span data-stu-id="69a68-145">string</span></span> | <span data-ttu-id="69a68-146">El alias de correo del grupo.</span><span class="sxs-lookup"><span data-stu-id="69a68-146">The mail alias for the group.</span></span> <span data-ttu-id="69a68-147">Necesario.</span><span class="sxs-lookup"><span data-stu-id="69a68-147">Required.</span></span> |
| <span data-ttu-id="69a68-148">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="69a68-148">securityEnabled</span></span> | <span data-ttu-id="69a68-149">booleano</span><span class="sxs-lookup"><span data-stu-id="69a68-149">boolean</span></span> | <span data-ttu-id="69a68-150">Establézcalo en **true** para los grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="69a68-150">Set to **true** for security-enabled groups.</span></span> <span data-ttu-id="69a68-151">Establézcalo en **true** si crea un grupo de seguridad o dinámico.</span><span class="sxs-lookup"><span data-stu-id="69a68-151">Set this to **true** if creating a dynamic or security group.</span></span> <span data-ttu-id="69a68-152">Establézcalo en **false** si crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="69a68-152">Set this to **false** if creating an Office 365 group.</span></span> <span data-ttu-id="69a68-153">Necesario.</span><span class="sxs-lookup"><span data-stu-id="69a68-153">Required.</span></span> |
| <span data-ttu-id="69a68-154">owners</span><span class="sxs-lookup"><span data-stu-id="69a68-154">owners</span></span> | <span data-ttu-id="69a68-155">string collection</span><span class="sxs-lookup"><span data-stu-id="69a68-155">string collection</span></span> | <span data-ttu-id="69a68-156">Esta propiedad representa los propietarios del grupo en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="69a68-156">This property represents the owners for the group at creation time.</span></span> <span data-ttu-id="69a68-157">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69a68-157">Optional.</span></span> |
| <span data-ttu-id="69a68-158">members</span><span class="sxs-lookup"><span data-stu-id="69a68-158">members</span></span> | <span data-ttu-id="69a68-159">string collection</span><span class="sxs-lookup"><span data-stu-id="69a68-159">string collection</span></span> | <span data-ttu-id="69a68-160">Esta propiedad representa a los miembros del grupo en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="69a68-160">This property represents the members for the group at creation time.</span></span> <span data-ttu-id="69a68-161">Opcional.</span><span class="sxs-lookup"><span data-stu-id="69a68-161">Optional.</span></span> |


<span data-ttu-id="69a68-162">Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="69a68-162">Specify the **groupTypes** property if you're creating an Office 365 or dynamic group, as stated below.</span></span>

### <a name="grouptypes-options"></a><span data-ttu-id="69a68-163">Opciones de groupTypes</span><span class="sxs-lookup"><span data-stu-id="69a68-163">groupTypes options</span></span>

| <span data-ttu-id="69a68-164">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="69a68-164">Type of group</span></span> | <span data-ttu-id="69a68-165">Propiedad **groupTypes**</span><span class="sxs-lookup"><span data-stu-id="69a68-165">**groupTypes** property</span></span> |
|:--------------|:------------------------|
| <span data-ttu-id="69a68-166">Office 365 (también conocido como grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="69a68-166">Office 365 (aka unified group)</span></span>| <span data-ttu-id="69a68-167">"Unificado"</span><span class="sxs-lookup"><span data-stu-id="69a68-167">"Unified"</span></span> |
| <span data-ttu-id="69a68-168">Dinámico</span><span class="sxs-lookup"><span data-stu-id="69a68-168">Dynamic</span></span> | <span data-ttu-id="69a68-169">"DynamicMembership"</span><span class="sxs-lookup"><span data-stu-id="69a68-169">"DynamicMembership"</span></span> |
| <span data-ttu-id="69a68-170">Seguridad</span><span class="sxs-lookup"><span data-stu-id="69a68-170">Security</span></span> | <span data-ttu-id="69a68-171">Sin establecer.</span><span class="sxs-lookup"><span data-stu-id="69a68-171">Do not set.</span></span> |


><span data-ttu-id="69a68-172">**Nota:** Si crea un grupo de Office 365 mediante programación sin un contexto de usuario y sin especificar los propietarios, se creará el grupo de forma anónima.</span><span class="sxs-lookup"><span data-stu-id="69a68-172">**Note:** Creating an Office 365 Group programmatically without a user context and  without specifying owners will create the group anonymously.</span></span>  <span data-ttu-id="69a68-173">Al hacerlo, es posible que el sitio de SharePoint Online no se cree automáticamente hasta que se lleve a cabo una acción manual.</span><span class="sxs-lookup"><span data-stu-id="69a68-173">Doing so can result in the associated SharePoint Online site not being created automatically until further manual action is taken.</span></span>  

<span data-ttu-id="69a68-p112">Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="69a68-p112">Specify other writable properties as necessary for your group. For more information, see the properties of the [group](../resources/group.md) resource.</span></span>

## <a name="response"></a><span data-ttu-id="69a68-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="69a68-176">Response</span></span>
<span data-ttu-id="69a68-177">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69a68-177">If successful, this method returns `201 Created` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="69a68-178">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="69a68-178">Example</span></span>
#### <a name="request-1"></a><span data-ttu-id="69a68-179">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="69a68-179">Request 1</span></span>
<span data-ttu-id="69a68-180">La primera solicitud de ejemplo crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="69a68-180">The following is an example of a request that creates an Office 365 Group.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="response-1"></a><span data-ttu-id="69a68-181">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="69a68-181">Response 1</span></span>
<span data-ttu-id="69a68-182">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="69a68-182">The following is an example of the response.</span></span>
><span data-ttu-id="69a68-p113">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69a68-p113">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mail": "library@contoso.onmicrosoft.com",
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="request-2"></a><span data-ttu-id="69a68-185">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="69a68-185">Request 2</span></span>
<span data-ttu-id="69a68-186">La segunda solicitud de ejemplo crea un grupo de Office 365 con los propietarios especificados.</span><span class="sxs-lookup"><span data-stu-id="69a68-186">The second example request creates an Office 365 Group with owners specified.</span></span>
<!-- {
  "blockType": "request"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-Type: application/json

{
  "description": "Group with owners",
  "displayName": "Group1",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "group1",
  "securityEnabled": false,
  "owners@odata.bind": [
    "https://graph.microsoft.com/v1.0/users/26be1845-4119-4801-a799-aea79d09f1a2"
  ]
}
```

#### <a name="response-2"></a><span data-ttu-id="69a68-187">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="69a68-187">Response 2</span></span>
<span data-ttu-id="69a68-188">Aquí tiene un ejemplo de respuesta adecuada.</span><span class="sxs-lookup"><span data-stu-id="69a68-188">The following is an example of the response.</span></span>
><span data-ttu-id="69a68-p114">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="69a68-p114">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "description": "Group with owners",
    "displayName": "Group1",
    "groupTypes": [
        "Unified"
    ],
    "mail": "group1@contoso.onmicrosoft.com",
    "mailEnabled": true,
    "mailNickname": "group1",
    "securityEnabled": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
