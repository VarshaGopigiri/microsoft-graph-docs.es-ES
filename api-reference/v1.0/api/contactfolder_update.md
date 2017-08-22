# <a name="update-contactfolder"></a><span data-ttu-id="b5c5d-101">Actualizar contactfolder</span><span class="sxs-lookup"><span data-stu-id="b5c5d-101">Update contactfolder</span></span>

<span data-ttu-id="b5c5d-102">Actualiza las propiedades del objeto contactfolder.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-102">Update the properties of contactfolder object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b5c5d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b5c5d-103">Prerequisites</span></span>
<span data-ttu-id="b5c5d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="b5c5d-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="b5c5d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b5c5d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/contactFolders/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b5c5d-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b5c5d-106">Request headers</span></span>
| <span data-ttu-id="b5c5d-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5c5d-107">Header</span></span>       | <span data-ttu-id="b5c5d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b5c5d-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b5c5d-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="b5c5d-109">Authorization</span></span>  | <span data-ttu-id="b5c5d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b5c5d-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b5c5d-112">Content-Type</span></span>  | <span data-ttu-id="b5c5d-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b5c5d-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b5c5d-115">Request body</span></span>
<span data-ttu-id="b5c5d-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b5c5d-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5c5d-119">Property</span></span>     | <span data-ttu-id="b5c5d-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5c5d-120">Type</span></span>   |<span data-ttu-id="b5c5d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5c5d-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5c5d-122">displayName</span><span class="sxs-lookup"><span data-stu-id="b5c5d-122">displayName</span></span>|<span data-ttu-id="b5c5d-123">String</span><span class="sxs-lookup"><span data-stu-id="b5c5d-123">String</span></span>|<span data-ttu-id="b5c5d-124">Nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-124">The folder's display name.</span></span>|
|<span data-ttu-id="b5c5d-125">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="b5c5d-125">parentFolderId</span></span>|<span data-ttu-id="b5c5d-126">String</span><span class="sxs-lookup"><span data-stu-id="b5c5d-126">String</span></span>|<span data-ttu-id="b5c5d-127">Identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-127">The ID of the folder's parent folder.</span></span>|

## <a name="response"></a><span data-ttu-id="b5c5d-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5c5d-128">Response</span></span>

<span data-ttu-id="b5c5d-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-129">If successful, this method returns a `200 OK` response code and updated [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b5c5d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5c5d-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b5c5d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b5c5d-131">Request</span></span>
<span data-ttu-id="b5c5d-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_contactfolder"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/contactFolders/{id}
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
##### <a name="response"></a><span data-ttu-id="b5c5d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b5c5d-133">Response</span></span>
<span data-ttu-id="b5c5d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b5c5d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
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
  "description": "Update contactfolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
