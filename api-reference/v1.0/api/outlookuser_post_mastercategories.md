# <a name="create-outlook-category"></a><span data-ttu-id="629d7-101">Crear categoría de Outlook</span><span class="sxs-lookup"><span data-stu-id="629d7-101">Create Outlook category</span></span>


<span data-ttu-id="629d7-102">Crear un objeto [outlookCategory](../resources/outlookCategory.md) en la lista principal de categorías del usuario.</span><span class="sxs-lookup"><span data-stu-id="629d7-102">Create an [outlookCategory](../resources/outlookCategory.md) object in the user's master list of categories.</span></span>

## <a name="permissions"></a><span data-ttu-id="629d7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="629d7-103">Permissions</span></span>
<span data-ttu-id="629d7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="629d7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="629d7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="629d7-106">Permission type</span></span>      | <span data-ttu-id="629d7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="629d7-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="629d7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="629d7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="629d7-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="629d7-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="629d7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="629d7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="629d7-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="629d7-111">MailboxSettings.ReadWrite</span></span>   |
|<span data-ttu-id="629d7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="629d7-112">Application</span></span> | <span data-ttu-id="629d7-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="629d7-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="629d7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="629d7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/outlook/masterCategories
POST /users/{id|userPrincipalName}/outlook/masterCategories
```
## <a name="request-headers"></a><span data-ttu-id="629d7-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="629d7-115">Request headers</span></span>
| <span data-ttu-id="629d7-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="629d7-116">Name</span></span>       | <span data-ttu-id="629d7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="629d7-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="629d7-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="629d7-118">Authorization</span></span>  | <span data-ttu-id="629d7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="629d7-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="629d7-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="629d7-121">Request body</span></span>
<span data-ttu-id="629d7-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [outlookCategory](../resources/outlookCategory.md).</span><span class="sxs-lookup"><span data-stu-id="629d7-122">In the request body, supply a JSON representation of [plannerTask](../resources/outlookCategory.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="629d7-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="629d7-123">Response</span></span>

<span data-ttu-id="629d7-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [outlookCategory](../resources/outlookCategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="629d7-124">If successful, this method returns `201 Created` response code and the new [page](../resources/outlookCategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="629d7-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="629d7-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="629d7-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="629d7-126">Request</span></span>
<span data-ttu-id="629d7-127">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="629d7-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlookcategory_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/outlook/masterCategories
Content-type: application/json
Content-Length: 70

{
      "displayName":"Project expenses",
      "color":"preset9"
}
```
<span data-ttu-id="629d7-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [outlookCategory](../resources/outlookCategory.md).</span><span class="sxs-lookup"><span data-stu-id="629d7-128">In the request body, supply a JSON representation of [plannerTask](../resources/outlookCategory.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="629d7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="629d7-129">Response</span></span>
<span data-ttu-id="629d7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="629d7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 250

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"bac262b7-485d-4739-b436-e31467d64fac",
  "displayName":"Project expenses",
  "color":"preset9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->