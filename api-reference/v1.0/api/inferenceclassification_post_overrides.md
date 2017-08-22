# <a name="create-inferenceclassificationoverride"></a><span data-ttu-id="6f6a8-101">Crear inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="6f6a8-101">Create inferenceClassificationOverride</span></span>

<span data-ttu-id="6f6a8-p101">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-p101">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>

<span data-ttu-id="6f6a8-104">**Nota**</span><span class="sxs-lookup"><span data-stu-id="6f6a8-104">**Note**</span></span>

- <span data-ttu-id="6f6a8-105">Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-105">If an override already exists with the same STMP address, then the **classifyAs** and **name** fields of that override are updated with the provided values.</span></span>
- <span data-ttu-id="6f6a8-106">El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-106">The maximum number of overrides supported for a mailbox is 1000, based on unique sender SMTP addresses.</span></span>
- <span data-ttu-id="6f6a8-107">La operación POST solo admite la creación de invalidaciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-107">The POST operation supports creating only one override at a time.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6f6a8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6f6a8-108">Prerequisites</span></span>
<span data-ttu-id="6f6a8-109">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="6f6a8-109">The following **scopes** are required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="6f6a8-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f6a8-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a><span data-ttu-id="6f6a8-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f6a8-111">Request headers</span></span>
| <span data-ttu-id="6f6a8-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f6a8-112">Name</span></span>       | <span data-ttu-id="6f6a8-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f6a8-113">Type</span></span> | <span data-ttu-id="6f6a8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f6a8-114">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6f6a8-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f6a8-115">Authorization</span></span>  | <span data-ttu-id="6f6a8-116">string</span><span class="sxs-lookup"><span data-stu-id="6f6a8-116">string</span></span>  | <span data-ttu-id="6f6a8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6f6a8-119">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6f6a8-119">Content-Type</span></span> | <span data-ttu-id="6f6a8-120">string</span><span class="sxs-lookup"><span data-stu-id="6f6a8-120">string</span></span>  | <span data-ttu-id="6f6a8-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f6a8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f6a8-123">Request body</span></span>
<span data-ttu-id="6f6a8-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="6f6a8-124">In the request body, supply a JSON representation of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="6f6a8-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f6a8-125">Response</span></span>

<span data-ttu-id="6f6a8-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-126">If successful, this method returns `201, Created` response code and an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f6a8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f6a8-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f6a8-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f6a8-128">Request</span></span>
<span data-ttu-id="6f6a8-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_inferenceclassificationoverride_from_inferenceclassification"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Fanny Downs",
    "address": "fannyd@adatum.onmicrosoft.com"
  }
}
```

##### <a name="response"></a><span data-ttu-id="6f6a8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f6a8-130">Response</span></span>
<span data-ttu-id="6f6a8-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f6a8-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Fanny Downs",
    "address": "fannyd@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->