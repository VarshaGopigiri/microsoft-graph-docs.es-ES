# <a name="update-group"></a><span data-ttu-id="c9688-101">Actualizar grupo</span><span class="sxs-lookup"><span data-stu-id="c9688-101">Update group</span></span>
<span data-ttu-id="c9688-102">Actualiza las propiedades de un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="c9688-102">Update the properties of a group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="c9688-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9688-103">Permissions</span></span>
<span data-ttu-id="c9688-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c9688-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c9688-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9688-106">Permission type</span></span>      | <span data-ttu-id="c9688-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9688-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c9688-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9688-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c9688-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c9688-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="c9688-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9688-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9688-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9688-111">Not supported.</span></span>    |
|<span data-ttu-id="c9688-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9688-112">Application</span></span> | <span data-ttu-id="c9688-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c9688-113">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c9688-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9688-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="c9688-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9688-115">Request headers</span></span>

| <span data-ttu-id="c9688-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9688-116">Name</span></span>       | <span data-ttu-id="c9688-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9688-117">Type</span></span> | <span data-ttu-id="c9688-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9688-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c9688-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9688-119">Authorization</span></span>  | <span data-ttu-id="c9688-120">string</span><span class="sxs-lookup"><span data-stu-id="c9688-120">string</span></span>  | <span data-ttu-id="c9688-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9688-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c9688-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c9688-123">Request body</span></span>

<span data-ttu-id="c9688-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="c9688-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="c9688-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9688-127">Property</span></span>     | <span data-ttu-id="c9688-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9688-128">Type</span></span>   |<span data-ttu-id="c9688-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9688-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c9688-130">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="c9688-130">autoSubscribeNewMembers</span></span>|<span data-ttu-id="c9688-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9688-131">Boolean</span></span>|<span data-ttu-id="c9688-p104">El valor predeterminado es **false**. Indica si los miembros agregados al grupo se suscribirán de forma automática para recibir notificaciones por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c9688-p104">Default is **false**. Indicates if new members added to the group will be auto-subscribed to receive email notifications.</span></span>|
|<span data-ttu-id="c9688-134">descripción</span><span class="sxs-lookup"><span data-stu-id="c9688-134">description</span></span>|<span data-ttu-id="c9688-135">String</span><span class="sxs-lookup"><span data-stu-id="c9688-135">String</span></span>|<span data-ttu-id="c9688-136">Una descripción opcional del grupo.</span><span class="sxs-lookup"><span data-stu-id="c9688-136">An optional description for the group.</span></span> |
|<span data-ttu-id="c9688-137">displayName</span><span class="sxs-lookup"><span data-stu-id="c9688-137">displayName</span></span>|<span data-ttu-id="c9688-138">String</span><span class="sxs-lookup"><span data-stu-id="c9688-138">String</span></span>|<span data-ttu-id="c9688-p105">El nombre para mostrar del grupo. Esta propiedad es necesaria cuando se crea un grupo y no se puede borrar durante las actualizaciones. Es compatible con $filter y $orderby.</span><span class="sxs-lookup"><span data-stu-id="c9688-p105">The display name for the group. This property is required when a group is created and it cannot be cleared during updates. Supports $filter and $orderby.</span></span>|
|<span data-ttu-id="c9688-142">groupTypes</span><span class="sxs-lookup"><span data-stu-id="c9688-142">groupTypes</span></span>|<span data-ttu-id="c9688-143">Colección string</span><span class="sxs-lookup"><span data-stu-id="c9688-143">String collection</span></span>|<span data-ttu-id="c9688-p106">Especifica el tipo de grupo que se va a crear. Los valores posibles son **Unified** para crear un grupo de Office 365 o **DynamicMembership** para grupos dinámicos.  Para los demás tipos de grupos, como los grupos con seguridad habilitada y los grupos de seguridad habilitados para correo electrónico, no establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c9688-p106">Specifies the type of group to create. Possible values are **Unified** to create an Office 365 group, or **DynamicMembership** for dynamic groups.  For all other group types, like security-enabled groups and email-enabled security groups, do not set this property.</span></span>|
|<span data-ttu-id="c9688-147">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="c9688-147">mailEnabled</span></span>|<span data-ttu-id="c9688-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9688-148">Boolean</span></span>|<span data-ttu-id="c9688-p107">Especifica si el grupo está habilitado para correo. Si la propiedad **securityEnabled** también es **true**, el grupo es un grupo de seguridad habilitado para correo electrónico; en caso contrario, el grupo es un grupo de distribución de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9688-p107">Specifies whether the group is mail-enabled. If the **securityEnabled** property is also **true**, the group is a mail-enabled security group; otherwise, the group is a Microsoft Exchange distribution group.</span></span>|
|<span data-ttu-id="c9688-151">mailNickname</span><span class="sxs-lookup"><span data-stu-id="c9688-151">mailNickname</span></span>|<span data-ttu-id="c9688-152">String</span><span class="sxs-lookup"><span data-stu-id="c9688-152">String</span></span>|<span data-ttu-id="c9688-p108">El alias de correo del grupo. Esta propiedad debe especificarse al crear un grupo. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="c9688-p108">The mail alias for the group. This property must be specified when a group is created. Supports $filter.</span></span>|
|<span data-ttu-id="c9688-156">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="c9688-156">securityEnabled</span></span>|<span data-ttu-id="c9688-157">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9688-157">Boolean</span></span>|<span data-ttu-id="c9688-p109">Especifica si el grupo es un grupo de seguridad. Si la propiedad **mailEnabled** también es true, el grupo es un grupo de seguridad habilitado para correo electrónico; de lo contrario, es un grupo de seguridad. Debe ser **false** para grupos de Office 365. Es compatible con $filter.</span><span class="sxs-lookup"><span data-stu-id="c9688-p109">Specifies whether the group is a security group. If the **mailEnabled** property is also true, the group is a mail-enabled security group; otherwise it is a security group. Must be **false** for Office 365 groups. Supports $filter..</span></span>|
|<span data-ttu-id="c9688-162">visibility</span><span class="sxs-lookup"><span data-stu-id="c9688-162">visibility</span></span>|<span data-ttu-id="c9688-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="c9688-163">Boolean</span></span>|<span data-ttu-id="c9688-p110">Especifica la visibilidad de un grupo de Office 365. Los valores posibles son: **Private**, **Public** o vacío (que se interpreta como **Public**).</span><span class="sxs-lookup"><span data-stu-id="c9688-p110">Specifies the visibility of an Office 365 group. Possible values are: **Private**, **Public**, or empty (which is interpreted as **Public**).</span></span>|

<span data-ttu-id="c9688-166">**Nota**</span><span class="sxs-lookup"><span data-stu-id="c9688-166">**Note**</span></span>

- <span data-ttu-id="c9688-167">Puede actualizar **autoSubscribeNewMembers** especificándolo en su propia solicitud PATCH sin incluir el resto de propiedades de la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="c9688-167">You can update **autoSubscribeNewMembers** by specifying it in its own PATCH request, without including the other properties in the table above.</span></span>
- <span data-ttu-id="c9688-p111">Solo un subconjunto de la API de grupo relativa a la administración de grupos básicos admite permisos delegados y de aplicación. Todos los demás miembros de la API de grupo, incluida la actualización **autoSubscribeNewMembers**, son compatible solo con los permisos delegados. Vea [problemas conocidos](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c9688-p111">Only a subset of the group API pertaining to core group administration and management support application and delegated permissions. All other members of the group API, including updating  **autoSubscribeNewMembers**, support only delegated permissions. See [known issues](https://developer.microsoft.com/graph/docs/overview/release_notes#group-permission-scopes) for examples.</span></span>

## <a name="response"></a><span data-ttu-id="c9688-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9688-171">Response</span></span>
<span data-ttu-id="c9688-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="c9688-172">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="c9688-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9688-173">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c9688-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9688-174">Request</span></span>
<span data-ttu-id="c9688-175">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c9688-175">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "update_group"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}
Content-type: application/json
Content-length: 211

{
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value"
}
```

#### <a name="response"></a><span data-ttu-id="c9688-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9688-176">Response</span></span>
<span data-ttu-id="c9688-177">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9688-177">Here is an example of the response.</span></span>
><span data-ttu-id="c9688-178">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="c9688-178">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="c9688-179">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c9688-179">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->