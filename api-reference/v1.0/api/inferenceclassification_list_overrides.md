# <a name="list-overrides"></a><span data-ttu-id="40e5b-101">List overrides</span><span class="sxs-lookup"><span data-stu-id="40e5b-101">List overrides</span></span>

<span data-ttu-id="40e5b-102">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="40e5b-102">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>

<span data-ttu-id="40e5b-p101">Cada reemplazo corresponde a una dirección SMTP de un remitente. Inicialmente, un usuario no tiene ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="40e5b-p101">Each override corresponds to an SMTP address of a sender. Initially, a user does not have any overrides.</span></span>
## <a name="permissions"></a><span data-ttu-id="40e5b-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="40e5b-105">Permissions</span></span>
<span data-ttu-id="40e5b-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="40e5b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="40e5b-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40e5b-108">Permission type</span></span>      | <span data-ttu-id="40e5b-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40e5b-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="40e5b-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40e5b-110">Delegated (work or school account)</span></span> | <span data-ttu-id="40e5b-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="40e5b-111">Mail.Read</span></span>    | 
|<span data-ttu-id="40e5b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40e5b-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="40e5b-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="40e5b-113">Mail.Read</span></span>    | 
|<span data-ttu-id="40e5b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40e5b-114">Application</span></span> | <span data-ttu-id="40e5b-115">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="40e5b-115">Mail.Read</span></span> | 

## <a name="http-request"></a><span data-ttu-id="40e5b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40e5b-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/inferenceClassification/overrides
GET /users/{id}/inferenceClassification/overrides
```

## <a name="request-headers"></a><span data-ttu-id="40e5b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40e5b-117">Request headers</span></span>
| <span data-ttu-id="40e5b-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="40e5b-118">Name</span></span>       | <span data-ttu-id="40e5b-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="40e5b-119">Type</span></span> | <span data-ttu-id="40e5b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="40e5b-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="40e5b-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="40e5b-121">Authorization</span></span>  | <span data-ttu-id="40e5b-122">string</span><span class="sxs-lookup"><span data-stu-id="40e5b-122">string</span></span>  | <span data-ttu-id="40e5b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="40e5b-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="40e5b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40e5b-125">Request body</span></span>
<span data-ttu-id="40e5b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="40e5b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="40e5b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40e5b-127">Response</span></span>

<span data-ttu-id="40e5b-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta. Se devuelve una colección vacía si el usuario no ha configurado ningún reemplazo.</span><span class="sxs-lookup"><span data-stu-id="40e5b-p104">If successful, this method returns a `200 OK` response code and a collection of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) objects in the response body. An empty collection is returned if the user doesn't have any overrides set up.</span></span>
## <a name="example"></a><span data-ttu-id="40e5b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40e5b-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="40e5b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40e5b-131">Request</span></span>
<span data-ttu-id="40e5b-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40e5b-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_overrides"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
```
##### <a name="response"></a><span data-ttu-id="40e5b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40e5b-133">Response</span></span>
<span data-ttu-id="40e5b-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40e5b-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "classifyAs": "focused",
      "senderEmailAddress": {
        "name": "Fanny Downs",
        "address": "fannyd@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
    },
    {
      "classifyAs": "other",
      "senderEmailAddress": {
        "name": "Randi Welch",
        "address": "randiw@adatum.onmicrosoft.com"
      },
      "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List overrides",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->