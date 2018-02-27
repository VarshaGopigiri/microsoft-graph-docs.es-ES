# <a name="get-user"></a><span data-ttu-id="b72ce-101">Obtener usuario</span><span class="sxs-lookup"><span data-stu-id="b72ce-101">Get user</span></span>

<span data-ttu-id="b72ce-102">Recupere el directorio simple **user** correspondiente a este objeto **educationUser**.</span><span class="sxs-lookup"><span data-stu-id="b72ce-102">Retrieve the simple directory **user** that corresponds to this **educationUser**.</span></span>

><span data-ttu-id="b72ce-103">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="b72ce-103">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="b72ce-104">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="b72ce-104">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="b72ce-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b72ce-105">Permissions</span></span>
<span data-ttu-id="b72ce-106">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b72ce-106">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="b72ce-107">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b72ce-107">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b72ce-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b72ce-108">Permission type</span></span>      | <span data-ttu-id="b72ce-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b72ce-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b72ce-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b72ce-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="b72ce-111">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All o User.Read</span><span class="sxs-lookup"><span data-stu-id="b72ce-111">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus either Directory.Read.All or User.Read</span></span>|
|<span data-ttu-id="b72ce-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b72ce-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="b72ce-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b72ce-113">Not supported.</span></span>  |
|<span data-ttu-id="b72ce-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b72ce-114">Application</span></span> | <span data-ttu-id="b72ce-115">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="b72ce-115">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="b72ce-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b72ce-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/user
GET /education/users/{id}/user
```
## <a name="request-headers"></a><span data-ttu-id="b72ce-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b72ce-117">Request headers</span></span>
| <span data-ttu-id="b72ce-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b72ce-118">Header</span></span>       | <span data-ttu-id="b72ce-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b72ce-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b72ce-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b72ce-120">Authorization</span></span>  | <span data-ttu-id="b72ce-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b72ce-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b72ce-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b72ce-123">Request body</span></span>
<span data-ttu-id="b72ce-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b72ce-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="b72ce-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b72ce-125">Response</span></span>
<span data-ttu-id="b72ce-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b72ce-126">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b72ce-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b72ce-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b72ce-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b72ce-128">Request</span></span>
<span data-ttu-id="b72ce-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b72ce-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/user
```
##### <a name="response"></a><span data-ttu-id="b72ce-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b72ce-130">Response</span></span>
<span data-ttu-id="b72ce-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b72ce-131">The following is an example of the response.</span></span> 

><span data-ttu-id="b72ce-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b72ce-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
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

<!-- uuid: FC4AAF57-A0ED-4899-B104-A8B89B72AD5A
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->