# <a name="create-inferenceclassificationoverride"></a><span data-ttu-id="2c00a-101">Crear inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="2c00a-101">Create inferenceClassificationOverride</span></span>

<span data-ttu-id="2c00a-p101">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="2c00a-p101">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>

<span data-ttu-id="2c00a-104">**Nota**</span><span class="sxs-lookup"><span data-stu-id="2c00a-104">**Note**</span></span>

- <span data-ttu-id="2c00a-105">Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="2c00a-105">If an override already exists with the same STMP address, then the **classifyAs** and **name** fields of that override are updated with the provided values.</span></span>
- <span data-ttu-id="2c00a-106">El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.</span><span class="sxs-lookup"><span data-stu-id="2c00a-106">The maximum number of overrides supported for a mailbox is 1000, based on unique sender SMTP addresses.</span></span>
- <span data-ttu-id="2c00a-107">La operación POST solo admite la creación de invalidaciones de una en una.</span><span class="sxs-lookup"><span data-stu-id="2c00a-107">The POST operation supports creating only one override at a time.</span></span>

## <a name="permissions"></a><span data-ttu-id="2c00a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c00a-108">Permissions</span></span>
<span data-ttu-id="2c00a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2c00a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2c00a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c00a-111">Permission type</span></span>      | <span data-ttu-id="2c00a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c00a-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2c00a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c00a-113">Delegated (work or school account)</span></span> | <span data-ttu-id="2c00a-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c00a-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2c00a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c00a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c00a-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c00a-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2c00a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c00a-117">Application</span></span> | <span data-ttu-id="2c00a-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2c00a-118">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="2c00a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c00a-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a><span data-ttu-id="2c00a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c00a-120">Request headers</span></span>
| <span data-ttu-id="2c00a-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c00a-121">Name</span></span>       | <span data-ttu-id="2c00a-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c00a-122">Type</span></span> | <span data-ttu-id="2c00a-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c00a-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2c00a-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c00a-124">Authorization</span></span>  | <span data-ttu-id="2c00a-125">string</span><span class="sxs-lookup"><span data-stu-id="2c00a-125">string</span></span>  | <span data-ttu-id="2c00a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c00a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2c00a-128">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2c00a-128">Content-Type</span></span> | <span data-ttu-id="2c00a-129">string</span><span class="sxs-lookup"><span data-stu-id="2c00a-129">string</span></span>  | <span data-ttu-id="2c00a-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c00a-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2c00a-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2c00a-132">Request body</span></span>
<span data-ttu-id="2c00a-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).</span><span class="sxs-lookup"><span data-stu-id="2c00a-133">In the request body, supply a JSON representation of [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="2c00a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c00a-134">Response</span></span>

<span data-ttu-id="2c00a-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c00a-135">If successful, this method returns `201, Created` response code and an [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c00a-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c00a-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2c00a-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c00a-137">Request</span></span>
<span data-ttu-id="2c00a-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c00a-138">Here is an example of the request.</span></span>
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
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  }
}
```

##### <a name="response"></a><span data-ttu-id="2c00a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c00a-139">Response</span></span>
<span data-ttu-id="2c00a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c00a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
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