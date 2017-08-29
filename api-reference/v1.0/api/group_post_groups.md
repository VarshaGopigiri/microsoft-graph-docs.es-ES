# <a name="create-group"></a><span data-ttu-id="9dac7-101">Crear grupo</span><span class="sxs-lookup"><span data-stu-id="9dac7-101">Create group</span></span>

<span data-ttu-id="9dac7-p101">Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:</span><span class="sxs-lookup"><span data-stu-id="9dac7-p101">Use this API to create a new group as specified in the request body. You can create one of three types of groups:</span></span>

* <span data-ttu-id="9dac7-104">Grupo de Office 365 (grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="9dac7-104">Office 365 group (unified group)</span></span>
* <span data-ttu-id="9dac7-105">Grupo dinámico</span><span class="sxs-lookup"><span data-stu-id="9dac7-105">Dynamic group</span></span>
* <span data-ttu-id="9dac7-106">Grupo de seguridad</span><span class="sxs-lookup"><span data-stu-id="9dac7-106">Security group</span></span>

> <span data-ttu-id="9dac7-p102">**Nota**: Aunque Microsoft Teams se basa en grupos de Office 365, actualmente no puede crear un equipo mediante esta API. Puede usar las otras API de grupo para administrar un equipo que se ha creado en la interfaz de usuario de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="9dac7-p102">**Note**: Although Microsoft Teams is built on Office 365 groups, you can't currently create a team via this API. You can use the other group APIs to manage a team that has been created in the Microsoft Teams UI.</span></span>

## <a name="permissions"></a><span data-ttu-id="9dac7-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="9dac7-109">Permissions</span></span>
<span data-ttu-id="9dac7-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9dac7-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9dac7-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9dac7-112">Permission type</span></span>      | <span data-ttu-id="9dac7-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9dac7-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9dac7-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9dac7-114">Delegated (work or school account)</span></span> | <span data-ttu-id="9dac7-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9dac7-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="9dac7-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9dac7-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9dac7-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9dac7-117">Not supported.</span></span>    |
|<span data-ttu-id="9dac7-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9dac7-118">Application</span></span> | <span data-ttu-id="9dac7-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9dac7-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9dac7-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9dac7-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```
## <a name="request-headers"></a><span data-ttu-id="9dac7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac7-121">Request headers</span></span>
| <span data-ttu-id="9dac7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9dac7-122">Name</span></span>       | <span data-ttu-id="9dac7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="9dac7-123">Type</span></span> | <span data-ttu-id="9dac7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dac7-124">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9dac7-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="9dac7-125">Authorization</span></span>  | <span data-ttu-id="9dac7-126">string</span><span class="sxs-lookup"><span data-stu-id="9dac7-126">string</span></span>  | <span data-ttu-id="9dac7-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9dac7-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9dac7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac7-129">Request body</span></span>
<span data-ttu-id="9dac7-130">La tabla siguiente muestra las propiedades del recurso [grupo](../resources/group.md) que debe especificar al mínimo al crear un grupo.</span><span class="sxs-lookup"><span data-stu-id="9dac7-130">The following table shows the properties of the [group](../resources/group.md) resource that you must specify at a minimum when you create a group.</span></span> 

| <span data-ttu-id="9dac7-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9dac7-131">Property</span></span> | <span data-ttu-id="9dac7-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="9dac7-132">Type</span></span> | <span data-ttu-id="9dac7-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dac7-133">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9dac7-134">displayName</span><span class="sxs-lookup"><span data-stu-id="9dac7-134">displayName</span></span> | <span data-ttu-id="9dac7-135">string</span><span class="sxs-lookup"><span data-stu-id="9dac7-135">string</span></span> | <span data-ttu-id="9dac7-136">El nombre para mostrar en la libreta de direcciones del grupo.</span><span class="sxs-lookup"><span data-stu-id="9dac7-136">The name to display in the address book for the group.</span></span> |
| <span data-ttu-id="9dac7-137">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="9dac7-137">mailEnabled</span></span> | <span data-ttu-id="9dac7-138">boolean</span><span class="sxs-lookup"><span data-stu-id="9dac7-138">boolean</span></span> | <span data-ttu-id="9dac7-p105">Establézcalo en **true** para grupos habilitados para correo. Establézcalo en **true** si está creando un grupo de Office 365. Establézcalo en **false** si está creando un grupo dinámico o de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9dac7-p105">Set to **true** for mail-enabled groups. Set this to **true** if creating an Office 365 group. Set this to **false** if creating dynamic or security group.</span></span>|
| <span data-ttu-id="9dac7-142">mailNickname</span><span class="sxs-lookup"><span data-stu-id="9dac7-142">mailNickname</span></span> | <span data-ttu-id="9dac7-143">string</span><span class="sxs-lookup"><span data-stu-id="9dac7-143">string</span></span> | <span data-ttu-id="9dac7-144">El alias de correo del grupo.</span><span class="sxs-lookup"><span data-stu-id="9dac7-144">The mail alias for the group.</span></span> |
| <span data-ttu-id="9dac7-145">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="9dac7-145">securityEnabled</span></span> | <span data-ttu-id="9dac7-146">boolean</span><span class="sxs-lookup"><span data-stu-id="9dac7-146">boolean</span></span> | <span data-ttu-id="9dac7-p106">Establézcalo en **true** para grupos con seguridad habilitada. Establézcalo en **true** si está creando un grupo dinámico o de seguridad. Establézcalo en **false** si está creando un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="9dac7-p106">Set to **true** for security-enabled groups. Set this to **true** if creating a dynamic or security group. Set this to **false** if creating an Office 365 group.</span></span> |

<span data-ttu-id="9dac7-150">Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="9dac7-150">Specify the **groupTypes** property if you're creating an Office 365 or dynamic group, as stated below.</span></span>

| <span data-ttu-id="9dac7-151">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="9dac7-151">Type of group</span></span> | <span data-ttu-id="9dac7-152">Propiedad **groupTypes**</span><span class="sxs-lookup"><span data-stu-id="9dac7-152">**groupTypes** property</span></span> |
|:--------------|:------------------------|
| <span data-ttu-id="9dac7-153">Office 365 (también conocido como grupo unificado)</span><span class="sxs-lookup"><span data-stu-id="9dac7-153">Office 365 (aka unified group)</span></span>| <span data-ttu-id="9dac7-154">"Unificado"</span><span class="sxs-lookup"><span data-stu-id="9dac7-154">"Unified"</span></span> |
| <span data-ttu-id="9dac7-155">Dinámico</span><span class="sxs-lookup"><span data-stu-id="9dac7-155">Dynamic</span></span> | <span data-ttu-id="9dac7-156">"DynamicMembership"</span><span class="sxs-lookup"><span data-stu-id="9dac7-156">"DynamicMembership"</span></span> |
| <span data-ttu-id="9dac7-157">Seguridad</span><span class="sxs-lookup"><span data-stu-id="9dac7-157">Security</span></span> | <span data-ttu-id="9dac7-158">Sin establecer.</span><span class="sxs-lookup"><span data-stu-id="9dac7-158">Do not set.</span></span> |

<span data-ttu-id="9dac7-p107">Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="9dac7-p107">Specify other writable properties as necessary for your group. For more information, see the properties of the [group](../resources/group.md) resource.</span></span>

## <a name="response"></a><span data-ttu-id="9dac7-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dac7-161">Response</span></span>

<span data-ttu-id="9dac7-162">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9dac7-162">If successful, this method returns `201, Created` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9dac7-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9dac7-163">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9dac7-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9dac7-164">Request</span></span>
<span data-ttu-id="9dac7-165">Este es un ejemplo de una solicitud que crea un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="9dac7-165">Here is an example of a request that creates an Office 365 group.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_group_from_groups"
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

##### <a name="response"></a><span data-ttu-id="9dac7-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dac7-166">Response</span></span>
<span data-ttu-id="9dac7-p108">Aquí tiene un ejemplo de la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán más propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9dac7-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. More properties will be returned from an actual call.</span></span>
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
