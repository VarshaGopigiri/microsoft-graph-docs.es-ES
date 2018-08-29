# <a name="create-rule"></a><span data-ttu-id="0dc9b-101">Crear regla</span><span class="sxs-lookup"><span data-stu-id="0dc9b-101">Create rule</span></span>


<span data-ttu-id="0dc9b-102">Crear un objeto [messageRule](../resources/messagerule.md) especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-102">Create a [messageRule](../resources/messagerule.md) object by specifying a set of conditions and actions.</span></span> 

<span data-ttu-id="0dc9b-103">Outlook lleva a cabo esas acciones si un mensaje entrante en la Bandeja de entrada del usuario cumple las condiciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-103">Outlook carries out those actions if an incoming message in the user's Inbox meets the specified conditions.</span></span>

## <a name="permissions"></a><span data-ttu-id="0dc9b-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="0dc9b-104">Permissions</span></span>
<span data-ttu-id="0dc9b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0dc9b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0dc9b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0dc9b-107">Permission type</span></span>      | <span data-ttu-id="0dc9b-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0dc9b-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0dc9b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0dc9b-109">Delegated (work or school account)</span></span> | <span data-ttu-id="0dc9b-110">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0dc9b-110">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="0dc9b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0dc9b-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0dc9b-112">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0dc9b-112">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="0dc9b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0dc9b-113">Application</span></span> | <span data-ttu-id="0dc9b-114">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0dc9b-114">MailboxSettings.ReadWrite</span></span> |


## <a name="http-request"></a><span data-ttu-id="0dc9b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0dc9b-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/inbox/messageRules
POST /users/{id | userPrincipalName}/mailFolders/inbox/messageRules
```
## <a name="request-headers"></a><span data-ttu-id="0dc9b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0dc9b-116">Request headers</span></span>
| <span data-ttu-id="0dc9b-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="0dc9b-117">Name</span></span>       | <span data-ttu-id="0dc9b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc9b-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0dc9b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0dc9b-119">Authorization</span></span>  | <span data-ttu-id="0dc9b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="0dc9b-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0dc9b-122">Request body</span></span>
<span data-ttu-id="0dc9b-123">En el cuerpo de la solicitud, proporcione los parámetros que se aplican a la regla.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-123">In the request body, supply the parameters that are applicable to your rule.</span></span> <span data-ttu-id="0dc9b-124">Estos son los parámetros de cuerpo que suelen usarse al crear reglas.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-124">The following are body parameters that are typically used when creating rules.</span></span> <span data-ttu-id="0dc9b-125">Puede especificar cualquier otra propiedad **messageRule** modificable que corresponda en el cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-125">You can specify any other writable **messageRule** properties as appropriate in the request body.</span></span>

### <a name="request-parameters"></a><span data-ttu-id="0dc9b-126">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0dc9b-126">Request parameters</span></span>
| <span data-ttu-id="0dc9b-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="0dc9b-127">Name</span></span>       | <span data-ttu-id="0dc9b-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="0dc9b-128">Type</span></span>|<span data-ttu-id="0dc9b-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc9b-129">Description</span></span>|
|:--------|:-------|:----------|
|<span data-ttu-id="0dc9b-130">actions</span><span class="sxs-lookup"><span data-stu-id="0dc9b-130">actions</span></span>|[<span data-ttu-id="0dc9b-131">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="0dc9b-131">messageRuleActions</span></span>](../resources/messageruleactions.md)|<span data-ttu-id="0dc9b-132">Acciones que se van a realizar en un mensaje cuando las condiciones correspondientes, si las hubiera, se cumplan.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-132">Actions to be taken on a message when the corresponding conditions, if any, are fulfilled.</span></span> <span data-ttu-id="0dc9b-133">Necesario.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-133">Required.</span></span>|
|<span data-ttu-id="0dc9b-134">conditions</span><span class="sxs-lookup"><span data-stu-id="0dc9b-134">conditions</span></span>|[<span data-ttu-id="0dc9b-135">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="0dc9b-135">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)|<span data-ttu-id="0dc9b-136">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-136">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> <span data-ttu-id="0dc9b-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-137">Optional.</span></span>|
|<span data-ttu-id="0dc9b-138">displayName</span><span class="sxs-lookup"><span data-stu-id="0dc9b-138">displayName</span></span>| <span data-ttu-id="0dc9b-139">String</span><span class="sxs-lookup"><span data-stu-id="0dc9b-139">String</span></span>  | <span data-ttu-id="0dc9b-140">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-140">The display name of the rule.</span></span> <span data-ttu-id="0dc9b-141">Necesario.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-141">Required.</span></span>|
|<span data-ttu-id="0dc9b-142">exceptions</span><span class="sxs-lookup"><span data-stu-id="0dc9b-142">exceptions</span></span>| [<span data-ttu-id="0dc9b-143">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="0dc9b-143">messageRulePredicates</span></span>](../resources/messagerulepredicates.md)| <span data-ttu-id="0dc9b-144">Representa las condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-144">Represents exception conditions for the rule.</span></span> <span data-ttu-id="0dc9b-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-145">Optional.</span></span> |
|<span data-ttu-id="0dc9b-146">isEnabled</span><span class="sxs-lookup"><span data-stu-id="0dc9b-146">isEnabled</span></span> | <span data-ttu-id="0dc9b-147">Boolean</span><span class="sxs-lookup"><span data-stu-id="0dc9b-147">Boolean</span></span> | <span data-ttu-id="0dc9b-148">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-148">Indicates whether the rule is enabled to be applied to messages.</span></span> <span data-ttu-id="0dc9b-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-149">Optional.</span></span> |
|<span data-ttu-id="0dc9b-150">sequence</span><span class="sxs-lookup"><span data-stu-id="0dc9b-150">sequence</span></span>| <span data-ttu-id="0dc9b-151">Int32</span><span class="sxs-lookup"><span data-stu-id="0dc9b-151">Int32</span></span> | <span data-ttu-id="0dc9b-152">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-152">Indicates the order in which the rule is executed, among other rules.</span></span> <span data-ttu-id="0dc9b-153">Necesario.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-153">Required.</span></span>|

## <a name="response"></a><span data-ttu-id="0dc9b-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dc9b-154">Response</span></span>
<span data-ttu-id="0dc9b-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto **messageRule** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-155">If successful, this method returns `201 Created` response code and a **messageRule** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0dc9b-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dc9b-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0dc9b-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0dc9b-157">Request</span></span>
<span data-ttu-id="0dc9b-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "sampleKeys": ["inbox"],
  "name": "create_messagerule_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/inbox/messageRules
Content-type: application/json

{      
    "displayName": "From partner",      
    "sequence": 2,      
    "isEnabled": true,          
    "conditions": {
        "senderContains": [
          "adele"       
        ]
     },
     "actions": {
        "forwardTo": [
          {
             "emailAddress": {
                "name": "Alex Wilbur",
                "address": "AlexW@contoso.onmicrosoft.com"
              }
           }
        ],
        "stopProcessingRules": true
     }    
}

```
##### <a name="response"></a><span data-ttu-id="0dc9b-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0dc9b-159">Response</span></span>
<span data-ttu-id="0dc9b-p110">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-p110">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id":"AQAAAJ5dZqA=",
  "displayName":"From partner",
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
      "stopProcessingRules":true,
      "forwardTo":[
        {
          "emailAddress":{
            "name":"Alex Wilbur",
            "address":"AlexW@contoso.onmicrosoft.com"
          }
        }
      ]
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->