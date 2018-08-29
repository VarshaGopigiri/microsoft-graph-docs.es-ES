# <a name="get-group"></a><span data-ttu-id="3e4fc-101">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="3e4fc-101">Get group</span></span>

<span data-ttu-id="3e4fc-102">Recupere el **group** de Office 365 correspondiente a este objeto **educationClass**.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-102">Retrieve the Office 365 **group** that corresponds to this **educationClass**.</span></span>

><span data-ttu-id="3e4fc-103">**Nota:** Si se usa el token delegado, los miembros solo pueden ver información sobre sus propios centros educativos.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-103">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="3e4fc-104">Use el recurso `...beta/education/me/schools` en este caso.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-104">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="3e4fc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3e4fc-105">Permissions</span></span>
<span data-ttu-id="3e4fc-106">Se requiere una combinación de permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-106">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="3e4fc-107">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3e4fc-107">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3e4fc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3e4fc-108">Permission type</span></span>      | <span data-ttu-id="3e4fc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3e4fc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3e4fc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3e4fc-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="3e4fc-111">Uno de los permisos EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="3e4fc-111">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus Directory.Read.All</span></span>|
|<span data-ttu-id="3e4fc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3e4fc-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="3e4fc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-113">Not supported.</span></span>  |
|<span data-ttu-id="3e4fc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3e4fc-114">Application</span></span> | <span data-ttu-id="3e4fc-115">EduRoster.Read.All, EduRoster.ReadWrite.All y Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="3e4fc-115">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="3e4fc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3e4fc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/classes/{id}/group
```
## <a name="request-headers"></a><span data-ttu-id="3e4fc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3e4fc-117">Request headers</span></span>
| <span data-ttu-id="3e4fc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3e4fc-118">Header</span></span>       | <span data-ttu-id="3e4fc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3e4fc-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3e4fc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="3e4fc-120">Authorization</span></span>  | <span data-ttu-id="3e4fc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3e4fc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3e4fc-123">Request body</span></span>
<span data-ttu-id="3e4fc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="3e4fc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e4fc-125">Response</span></span>
<span data-ttu-id="3e4fc-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-126">If successful, this method returns a `200 OK` response code and a [group](../resources/group.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3e4fc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3e4fc-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3e4fc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3e4fc-128">Request</span></span>
<span data-ttu-id="3e4fc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/group
```
##### <a name="response"></a><span data-ttu-id="3e4fc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3e4fc-130">Response</span></span>
<span data-ttu-id="3e4fc-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-131">The following is an example of the response.</span></span> 

><span data-ttu-id="3e4fc-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3e4fc-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
  "id": "id-value",
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value",
  "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
  "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": [
    "proxyAddresses-value"
   ],
   "securityEnabled": true,
   "visibility": "visibility-value"
}
```

<!-- uuid: 0087D9B3-1418-4C87-91C9-A18C6D93706B
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->