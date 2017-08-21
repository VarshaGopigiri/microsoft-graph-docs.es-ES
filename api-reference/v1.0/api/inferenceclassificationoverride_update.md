# <a name="update-inferenceclassificationoverride"></a><span data-ttu-id="5dde1-101">Actualizar inferenceclassificationoverride</span><span class="sxs-lookup"><span data-stu-id="5dde1-101">Update inferenceclassificationoverride</span></span>

<span data-ttu-id="5dde1-102">Cambie el campo **classifyAs** de una invalidación tal y como se especifica.</span><span class="sxs-lookup"><span data-stu-id="5dde1-102">Change the **classifyAs** field of an override as specified.</span></span> 

<span data-ttu-id="5dde1-103">No puede usar PATCH para cambiar ningún otro campo de una instancia [inferenceClassificationOverride](../resources/inferenceClassificationOverride.md).</span><span class="sxs-lookup"><span data-stu-id="5dde1-103">You cannot use PATCH to change any other fields in an [inferenceClassificationOverride](../resources/inferenceClassificationOverride.md) instance.</span></span> 

<span data-ttu-id="5dde1-104">Si hay una invalidación para un remitente y este cambia su nombre para mostrar, puede usar [POST](inferenceclassification_post_overrides.md) para forzar una actualización en el campo de nombre de la invalidación existente.</span><span class="sxs-lookup"><span data-stu-id="5dde1-104">If an override exists for a sender and the sender changes his/her display name, you can use [POST](inferenceclassification_post_overrides.md) to force an update to the name field in the existing override.</span></span>

<span data-ttu-id="5dde1-105">Si hay una invalidación para un remitente y este cambia su dirección SMTP, la única forma de "actualizar" la invalidación de este remitente es [eliminar](inferenceclassificationoverride_delete.md) la invalidación existente y [crear](inferenceclassification_post_overrides.md) una nueva con la nueva dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="5dde1-105">If an override exists for a sender and the sender changes his/her SMTP address, [deleting](inferenceclassificationoverride_delete.md) the existing override and [creating](inferenceclassification_post_overrides.md) a new one with the new SMTP address is the only way to "update" the override for this sender.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5dde1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5dde1-106">Prerequisites</span></span>
<span data-ttu-id="5dde1-107">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="5dde1-107">The following **scopes** are required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="5dde1-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5dde1-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/inferenceClassification/overrides/{id}
PATCH /users/{id}/inferenceClassification/overrides/{id}
```

## <a name="request-headers"></a><span data-ttu-id="5dde1-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5dde1-109">Request headers</span></span>
| <span data-ttu-id="5dde1-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="5dde1-110">Name</span></span>       | <span data-ttu-id="5dde1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dde1-111">Type</span></span> | <span data-ttu-id="5dde1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dde1-112">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5dde1-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="5dde1-113">Authorization</span></span>  | <span data-ttu-id="5dde1-114">string</span><span class="sxs-lookup"><span data-stu-id="5dde1-114">string</span></span>  | <span data-ttu-id="5dde1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5dde1-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5dde1-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5dde1-117">Content-Type</span></span> | <span data-ttu-id="5dde1-118">string</span><span class="sxs-lookup"><span data-stu-id="5dde1-118">string</span></span>  | <span data-ttu-id="5dde1-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5dde1-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5dde1-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5dde1-121">Request body</span></span>
<span data-ttu-id="5dde1-p103">En el cuerpo de la solicitud, proporcione el nuevo valor de **classifyAs**. Para obtener el mejor rendimiento, no debe incluir valores existentes que no cambien.</span><span class="sxs-lookup"><span data-stu-id="5dde1-p103">In the request body, supply the new value for **classifyAs**. For best performance you shouldn't include existing values that are not changing.</span></span>

| <span data-ttu-id="5dde1-124">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5dde1-124">Property</span></span>     | <span data-ttu-id="5dde1-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dde1-125">Type</span></span>   |<span data-ttu-id="5dde1-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dde1-126">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5dde1-127">classifyAs</span><span class="sxs-lookup"><span data-stu-id="5dde1-127">classifyAs</span></span>|<span data-ttu-id="5dde1-128">string</span><span class="sxs-lookup"><span data-stu-id="5dde1-128">string</span></span>| <span data-ttu-id="5dde1-p104">Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="5dde1-p104">Specifies how incoming messages from a specific sender should always be classified as. Possible values are: `focused`, `other`.</span></span>|

## <a name="response"></a><span data-ttu-id="5dde1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5dde1-131">Response</span></span>

<span data-ttu-id="5dde1-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5dde1-132">If successful, this method returns a `200 OK` response code and updated [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5dde1-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dde1-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5dde1-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5dde1-134">Request</span></span>
<span data-ttu-id="5dde1-135">En el ejemplo siguiente, se cambia la invalidación de la dirección SMTP randiw@adatum.onmicrosoft.com de `other` a `focused`.</span><span class="sxs-lookup"><span data-stu-id="5dde1-135">The following example changes the override for the SMTP address randiw@adatum.onmicrosoft.com from `other` to `focused`.</span></span>

<!-- {
  "blockType": "request",
  "name": "update_inferenceclassificationoverride"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides/{id}
Content-type: application/json

{
  "classifyAs": "focused"
}
```
##### <a name="response"></a><span data-ttu-id="5dde1-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5dde1-136">Response</span></span>
<span data-ttu-id="5dde1-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5dde1-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Randi Welch",
    "address": "randiw@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update inferenceclassificationoverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->