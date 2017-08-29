# <a name="create-contactfolder"></a><span data-ttu-id="c60c2-101">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="c60c2-101">Create ContactFolder</span></span>

<span data-ttu-id="c60c2-102">Crea una contactFolder en la carpeta predeterminada de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="c60c2-102">Create a new contactFolder under the user's default contacts folder.</span></span>

<span data-ttu-id="c60c2-103">También se puede [crear una contactfolder como elemento secundario de cualquier carpeta de contacto especificada](contactfolder_post_childfolders.md).</span><span class="sxs-lookup"><span data-stu-id="c60c2-103">You can also [create a new contactfolder as a child of any specified contact folder](contactfolder_post_childfolders.md).</span></span>
## <a name="permissions"></a><span data-ttu-id="c60c2-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="c60c2-104">Permissions</span></span>
<span data-ttu-id="c60c2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c60c2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c60c2-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c60c2-107">Permission type</span></span>      | <span data-ttu-id="c60c2-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c60c2-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c60c2-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c60c2-109">Delegated (work or school account)</span></span> | <span data-ttu-id="c60c2-110">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c60c2-110">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="c60c2-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c60c2-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c60c2-112">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c60c2-112">Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="c60c2-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c60c2-113">Application</span></span> | <span data-ttu-id="c60c2-114">Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c60c2-114">Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c60c2-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c60c2-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/contactFolders
```
## <a name="request-headers"></a><span data-ttu-id="c60c2-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c60c2-116">Request headers</span></span>
| <span data-ttu-id="c60c2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c60c2-117">Header</span></span>       | <span data-ttu-id="c60c2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c60c2-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c60c2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c60c2-119">Authorization</span></span>  | <span data-ttu-id="c60c2-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c60c2-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="c60c2-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c60c2-122">Content-Type</span></span>  | <span data-ttu-id="c60c2-123">application/json</span><span class="sxs-lookup"><span data-stu-id="c60c2-123">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c60c2-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c60c2-124">Request body</span></span>
<span data-ttu-id="c60c2-125">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c60c2-125">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="c60c2-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c60c2-126">Response</span></span>

<span data-ttu-id="c60c2-127">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c60c2-127">If successful, this method returns `201, Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c60c2-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c60c2-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c60c2-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c60c2-129">Request</span></span>
<span data-ttu-id="c60c2-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c60c2-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
<span data-ttu-id="c60c2-131">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="c60c2-131">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="c60c2-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c60c2-132">Response</span></span>
<span data-ttu-id="c60c2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c60c2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 104

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ContactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
