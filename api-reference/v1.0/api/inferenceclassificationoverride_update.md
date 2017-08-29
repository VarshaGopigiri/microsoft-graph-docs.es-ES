# <a name="update-inferenceclassificationoverride"></a><span data-ttu-id="0c6ce-101">Actualizar inferenceclassificationoverride</span><span class="sxs-lookup"><span data-stu-id="0c6ce-101">Update inferenceclassificationoverride</span></span>

<span data-ttu-id="0c6ce-102">Cambie el campo **classifyAs** de una invalidación tal y como se especifica.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-102">Change the **classifyAs** field of an override as specified.</span></span> 

<span data-ttu-id="0c6ce-103">No puede usar PATCH para cambiar ningún otro campo de una instancia [inferenceClassificationOverride](../resources/inferenceClassificationOverride.md).</span><span class="sxs-lookup"><span data-stu-id="0c6ce-103">You cannot use PATCH to change any other fields in an [inferenceClassificationOverride](../resources/inferenceClassificationOverride.md) instance.</span></span> 

<span data-ttu-id="0c6ce-104">Si hay una invalidación para un remitente y este cambia su nombre para mostrar, puede usar [POST](inferenceclassification_post_overrides.md) para forzar una actualización en el campo de nombre de la invalidación existente.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-104">If an override exists for a sender and the sender changes his/her display name, you can use [POST](inferenceclassification_post_overrides.md) to force an update to the name field in the existing override.</span></span>

<span data-ttu-id="0c6ce-105">Si hay una invalidación para un remitente y este cambia su dirección SMTP, la única forma de "actualizar" la invalidación de este remitente es [eliminar](inferenceclassificationoverride_delete.md) la invalidación existente y [crear](inferenceclassification_post_overrides.md) una nueva con la nueva dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-105">If an override exists for a sender and the sender changes his/her SMTP address, [deleting](inferenceclassificationoverride_delete.md) the existing override and [creating](inferenceclassification_post_overrides.md) a new one with the new SMTP address is the only way to "update" the override for this sender.</span></span>

## <a name="permissions"></a><span data-ttu-id="0c6ce-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="0c6ce-106">Permissions</span></span>
<span data-ttu-id="0c6ce-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0c6ce-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0c6ce-109">Permission type</span></span>      | <span data-ttu-id="0c6ce-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0c6ce-110">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="0c6ce-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0c6ce-111">Delegated (work or school account)</span></span> | <span data-ttu-id="0c6ce-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c6ce-112">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="0c6ce-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0c6ce-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0c6ce-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c6ce-114">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="0c6ce-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0c6ce-115">Application</span></span> | <span data-ttu-id="0c6ce-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c6ce-116">Mail.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="0c6ce-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0c6ce-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/inferenceClassification/overrides/{id}
PATCH /users/{id}/inferenceClassification/overrides/{id}
```

## <a name="request-headers"></a><span data-ttu-id="0c6ce-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6ce-118">Request headers</span></span>
| <span data-ttu-id="0c6ce-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="0c6ce-119">Name</span></span>       | <span data-ttu-id="0c6ce-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c6ce-120">Type</span></span> | <span data-ttu-id="0c6ce-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c6ce-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0c6ce-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="0c6ce-122">Authorization</span></span>  | <span data-ttu-id="0c6ce-123">string</span><span class="sxs-lookup"><span data-stu-id="0c6ce-123">string</span></span>  | <span data-ttu-id="0c6ce-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0c6ce-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="0c6ce-126">Content-Type</span></span> | <span data-ttu-id="0c6ce-127">string</span><span class="sxs-lookup"><span data-stu-id="0c6ce-127">string</span></span>  | <span data-ttu-id="0c6ce-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0c6ce-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6ce-130">Request body</span></span>
<span data-ttu-id="0c6ce-p104">En el cuerpo de la solicitud, proporcione el nuevo valor de **classifyAs**. Para obtener el mejor rendimiento, no debe incluir valores existentes que no cambien.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p104">In the request body, supply the new value for **classifyAs**. For best performance you shouldn't include existing values that are not changing.</span></span>

| <span data-ttu-id="0c6ce-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c6ce-133">Property</span></span>     | <span data-ttu-id="0c6ce-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c6ce-134">Type</span></span>   |<span data-ttu-id="0c6ce-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c6ce-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0c6ce-136">classifyAs</span><span class="sxs-lookup"><span data-stu-id="0c6ce-136">classifyAs</span></span>|<span data-ttu-id="0c6ce-137">string</span><span class="sxs-lookup"><span data-stu-id="0c6ce-137">string</span></span>| <span data-ttu-id="0c6ce-p105">Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Los valores posibles son: `focused`, `other`.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p105">Specifies how incoming messages from a specific sender should always be classified as. Possible values are: `focused`, `other`.</span></span>|

## <a name="response"></a><span data-ttu-id="0c6ce-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6ce-140">Response</span></span>

<span data-ttu-id="0c6ce-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-141">If successful, this method returns a `200 OK` response code and updated [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0c6ce-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0c6ce-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0c6ce-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0c6ce-143">Request</span></span>
<span data-ttu-id="0c6ce-144">En el ejemplo siguiente, se cambia la invalidación de la dirección SMTP randiw@adatum.onmicrosoft.com de `other` a `focused`.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-144">The following example changes the override for the SMTP address randiw@adatum.onmicrosoft.com from `other` to `focused`.</span></span>

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
##### <a name="response"></a><span data-ttu-id="0c6ce-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0c6ce-145">Response</span></span>
<span data-ttu-id="0c6ce-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0c6ce-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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