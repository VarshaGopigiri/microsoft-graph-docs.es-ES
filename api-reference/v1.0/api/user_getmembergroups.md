# <a name="user-getmembergroups"></a><span data-ttu-id="6f7b8-101">usuario: getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="6f7b8-101">user: getMemberGroups</span></span>

<span data-ttu-id="6f7b8-p101">Devuelva todos los grupos de los que el usuario es miembro. La comprobación es transitiva, a diferencia de la lectura de la propiedad de navegación [memberOf](../api/user_list_memberof.md), que devuelve solo los grupos de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p101">Return all the groups that the user is a member of. The check is transitive, unlike reading the [memberOf](../api/user_list_memberof.md) navigation property, which returns only the groups that the user is a direct member of.</span></span>

<span data-ttu-id="6f7b8-p102">Esta función es compatible con Office 365 y otros tipos de grupos aprovisionados en Azure AD. El número máximo de grupos que puede devolver cada solicitud es de 2046. Tenga en cuenta que los grupos de Office 365 no pueden contener grupos. Por tanto, la pertenencia a un grupo de Office 365 es siempre directa.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p102">This function supports Office 365 and other types of groups provisioned in Azure AD. The maximum number of groups each request can return is 2046. Note that Office 365 Groups cannot contain groups. So membership in an Office 365 Group is always direct.</span></span>

## <a name="permissions"></a><span data-ttu-id="6f7b8-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f7b8-108">Permissions</span></span>

<span data-ttu-id="6f7b8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="6f7b8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f7b8-111">Permission type</span></span>                        | <span data-ttu-id="6f7b8-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f7b8-112">Permissions (from least to most privileged)</span></span>                                                                                                          |
| :------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="6f7b8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f7b8-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="6f7b8-114">~~User.Read y Group.Read.All~~, ~~User.ReadBasic.All y Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="6f7b8-114">~~User.Read and Group.Read.All~~, ~~User.ReadBasic.All and Group.Read.All~~, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
| <span data-ttu-id="6f7b8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f7b8-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f7b8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-116">Not supported.</span></span>                                                                                                                                       |
| <span data-ttu-id="6f7b8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f7b8-117">Application</span></span>                            | <span data-ttu-id="6f7b8-118">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f7b8-118">_Group.Read.All_, Directory.Read.All, Directory.ReadWrite.All</span></span>                                                                                        |

> <span data-ttu-id="6f7b8-119">**Nota:** En este momento, esta API requiere el permiso `Directory.Read.All` o superior.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-119">Note: This API currently requires the Directory.Read.All permission or higher.</span></span> <span data-ttu-id="6f7b8-120">El uso del permiso Group.Read.All, bien sea de forma independiente o junto con el permiso `User.`, devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-120">Using the Group.Read.All permission, either alone or in combination with a User permission, will return an error.</span></span> <span data-ttu-id="6f7b8-121">Se trata de un problema conocido.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-121">This is a known bug.</span></span>

## <a name="http-request"></a><span data-ttu-id="6f7b8-122">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f7b8-122">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /users/{id | userPrincipalName}/getMemberGroups
```

## <a name="request-headers"></a><span data-ttu-id="6f7b8-123">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f7b8-123">Request headers</span></span>

| <span data-ttu-id="6f7b8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f7b8-124">Header</span></span>        | <span data-ttu-id="6f7b8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6f7b8-125">Value</span></span>                     |
| :------------ | :------------------------ |
| <span data-ttu-id="6f7b8-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="6f7b8-126">Authorization</span></span> | <span data-ttu-id="6f7b8-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6f7b8-129">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6f7b8-129">Content-Type</span></span>  | <span data-ttu-id="6f7b8-130">application/json</span><span class="sxs-lookup"><span data-stu-id="6f7b8-130">application/json</span></span>          |

## <a name="request-body"></a><span data-ttu-id="6f7b8-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f7b8-131">Request body</span></span>

<span data-ttu-id="6f7b8-132">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-132">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6f7b8-133">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6f7b8-133">Parameter</span></span>           | <span data-ttu-id="6f7b8-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f7b8-134">Type</span></span>    | <span data-ttu-id="6f7b8-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f7b8-135">Description</span></span>                                                                                                                                                                                                                                                                         |
| :------------------ | :------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="6f7b8-136">securityEnabledOnly</span><span class="sxs-lookup"><span data-stu-id="6f7b8-136">securityEnabledOnly</span></span> | <span data-ttu-id="6f7b8-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="6f7b8-137">Boolean</span></span> | <span data-ttu-id="6f7b8-p106">**true** para especificar que solo se deben devolver los grupos de seguridad de los que el usuario es miembro; **false** para especificar que se deben devolver todos los grupos de los que el usuario es miembro. Nota: Establecer este parámetro en **verdadero** solo es posible al llamar este método en un usuario.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p106">**true** to specify that only security groups that the user is a member of should be returned; **false** to specify that all groups that the user is a member of should be returned. Note: Setting this parameter to **true** is only supported when calling this method on a user.</span></span> |

## <a name="response"></a><span data-ttu-id="6f7b8-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f7b8-140">Response</span></span>

<span data-ttu-id="6f7b8-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y la colección String en el cuerpo de la respuesta que contiene los identificadores de los grupos de los que el usuario sea miembro.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-141">If successful, this method returns `200 OK` response code and String collection in the response body that contains the IDs of the groups that the user is a member of.</span></span>

## <a name="example"></a><span data-ttu-id="6f7b8-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f7b8-142">Example</span></span>

<span data-ttu-id="6f7b8-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-143">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="6f7b8-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f7b8-144">Request</span></span>

<span data-ttu-id="6f7b8-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-145">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "user_getmembergroups"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/getMemberGroups
Content-type: application/json
Content-length: 33

{
  "securityEnabledOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="6f7b8-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f7b8-146">Response</span></span>

<span data-ttu-id="6f7b8-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f7b8-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "string",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "value": [
    "string-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "user: getMemberGroups",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
