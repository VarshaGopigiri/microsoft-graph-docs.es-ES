# <a name="update-rule"></a><span data-ttu-id="a343a-101">Actualizar regla</span><span class="sxs-lookup"><span data-stu-id="a343a-101">Update rule</span></span>


<span data-ttu-id="a343a-102">Cambie las propiedades modificables en un objeto [messageRule](../resources/messagerule.md) y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="a343a-102">Change writable properties on a [messageRule](../resources/messagerule.md) object and save the changes.</span></span>

## <a name="permissions"></a><span data-ttu-id="a343a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a343a-103">Permissions</span></span>
<span data-ttu-id="a343a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a343a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a343a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a343a-106">Permission type</span></span>      | <span data-ttu-id="a343a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a343a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a343a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a343a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="a343a-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a343a-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a343a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a343a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a343a-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a343a-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="a343a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a343a-112">Application</span></span> | <span data-ttu-id="a343a-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a343a-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a343a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a343a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/inbox/messagerules/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="a343a-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="a343a-115">Optional request headers</span></span>
| <span data-ttu-id="a343a-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="a343a-116">Name</span></span>       | <span data-ttu-id="a343a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a343a-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="a343a-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="a343a-118">Authorization</span></span>  | <span data-ttu-id="a343a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a343a-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="a343a-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a343a-121">Request body</span></span>
<span data-ttu-id="a343a-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="a343a-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="a343a-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a343a-125">Property</span></span>     | <span data-ttu-id="a343a-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="a343a-126">Type</span></span>   |<span data-ttu-id="a343a-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a343a-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a343a-128">actions</span><span class="sxs-lookup"><span data-stu-id="a343a-128">Actions</span></span> | [<span data-ttu-id="a343a-129">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="a343a-129">messageRuleActions</span></span>](../resources/messageruleactions.md) | <span data-ttu-id="a343a-130">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="a343a-130">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="a343a-131">conditions</span><span class="sxs-lookup"><span data-stu-id="a343a-131">Conditions</span></span> | [<span data-ttu-id="a343a-132">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="a343a-132">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="a343a-133">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="a343a-133">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="a343a-134">displayName</span><span class="sxs-lookup"><span data-stu-id="a343a-134">displayName</span></span> | <span data-ttu-id="a343a-135">String</span><span class="sxs-lookup"><span data-stu-id="a343a-135">String</span></span> | <span data-ttu-id="a343a-136">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="a343a-136">The name of the new formatting rule.</span></span> |
| <span data-ttu-id="a343a-137">exceptions</span><span class="sxs-lookup"><span data-stu-id="a343a-137">exceptions</span></span> | [<span data-ttu-id="a343a-138">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="a343a-138">messageRulePredicates</span></span>](../resources/messagerulepredicates.md) | <span data-ttu-id="a343a-139">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="a343a-139">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="a343a-140">isEnabled</span><span class="sxs-lookup"><span data-stu-id="a343a-140">isEnabled</span></span> | <span data-ttu-id="a343a-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="a343a-141">Boolean</span></span> | <span data-ttu-id="a343a-142">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a343a-142">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="a343a-143">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="a343a-143">isReadOnly</span></span> | <span data-ttu-id="a343a-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="a343a-144">Boolean</span></span> | <span data-ttu-id="a343a-145">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="a343a-145">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="a343a-146">sequence</span><span class="sxs-lookup"><span data-stu-id="a343a-146">Sequence</span></span> | <span data-ttu-id="a343a-147">Int32</span><span class="sxs-lookup"><span data-stu-id="a343a-147">Int32</span></span> | <span data-ttu-id="a343a-148">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="a343a-148">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="response"></a><span data-ttu-id="a343a-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a343a-149">Response</span></span>
<span data-ttu-id="a343a-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a343a-150">If successful, this method returns a `200 OK` response code and updated [ChartSeries](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="a343a-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a343a-151">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a343a-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a343a-152">Request</span></span>
<span data-ttu-id="a343a-153">En el ejemplo siguiente se cambia el nombre de la regla y las acciones que se realizan para esa regla en el [ejemplo](messagerule_get.md#example) de [Obtener regla](messagerule_get.md), desde reenviarla a una dirección hasta marcar su importancia como alta.</span><span class="sxs-lookup"><span data-stu-id="a343a-153">The following example changes the name of the rule, and the actions to be taken for that rule in the [example](messagerule_get.md#example) in [Get rule](messagerule_get.md), from forwarding to an address to marking its importance as high.</span></span> 
<!-- {
  "blockType": "request",
  "name": "update_messagerule"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')

Content-type: application/json

{
    "displayName": "Important from partner",
    "actions": {
        "markImportance": "high"
     }
} 
```
##### <a name="response"></a><span data-ttu-id="a343a-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a343a-154">Response</span></span>
<span data-ttu-id="a343a-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a343a-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
  "id":"AQAAAJ5dZqA=",
  "displayName":"Important from partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
    "markImportance": "high"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->