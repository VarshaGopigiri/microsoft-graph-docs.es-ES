# <a name="delete-inferenceclassificationoverride"></a><span data-ttu-id="104cb-101">Delete inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="104cb-101">Delete inferenceClassificationOverride</span></span>

<span data-ttu-id="104cb-102">Elimina un reemplazo especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="104cb-102">Delete an override specified by its ID.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="104cb-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="104cb-103">Prerequisites</span></span>
<span data-ttu-id="104cb-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="104cb-104">The following **scopes** are required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="104cb-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="104cb-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/inferenceClassification/overrides/{id}
DELETE /users/{id}/inferenceClassification/overrides/{id}
```
## <a name="request-headers"></a><span data-ttu-id="104cb-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="104cb-106">Request headers</span></span>
| <span data-ttu-id="104cb-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="104cb-107">Name</span></span>       | <span data-ttu-id="104cb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="104cb-108">Type</span></span> | <span data-ttu-id="104cb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="104cb-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="104cb-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="104cb-110">Authorization</span></span>  | <span data-ttu-id="104cb-111">string</span><span class="sxs-lookup"><span data-stu-id="104cb-111">string</span></span>  | <span data-ttu-id="104cb-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="104cb-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="104cb-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="104cb-114">Request body</span></span>
<span data-ttu-id="104cb-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="104cb-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="104cb-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="104cb-116">Response</span></span>

<span data-ttu-id="104cb-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="104cb-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="104cb-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="104cb-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="104cb-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="104cb-120">Request</span></span>
<span data-ttu-id="104cb-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="104cb-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_inferenceclassificationoverride"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides/98f5bdef-576a-404d-a2ea-07a3cf34af4r
```
##### <a name="response"></a><span data-ttu-id="104cb-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="104cb-122">Response</span></span>
<span data-ttu-id="104cb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="104cb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->