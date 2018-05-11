# <a name="outlookuser-supportedlanguages"></a><span data-ttu-id="8396a-101">outlookUser: supportedLanguages</span><span class="sxs-lookup"><span data-stu-id="8396a-101">outlookUser: supportedLanguages</span></span>

<span data-ttu-id="8396a-102">Obtener una lista de idiomas y configuraciones regionales compatibles con el usuario, según la configuración del servidor de buzones del usuario.</span><span class="sxs-lookup"><span data-stu-id="8396a-102">Get the list of locales and languages that are supported for the user, as configured on the user's mailbox server.</span></span>

<span data-ttu-id="8396a-103">Al configurar un cliente de Outlook, el usuario selecciona el idioma preferido de esta lista admitida.</span><span class="sxs-lookup"><span data-stu-id="8396a-103">When setting up an Outlook client, the user selects the preferred language from this supported list.</span></span> <span data-ttu-id="8396a-104">Posteriormente, puede obtener el idioma preferido [obteniendo la configuración del buzón del usuario](user_get_mailboxsettings.md).</span><span class="sxs-lookup"><span data-stu-id="8396a-104">You can subsequently get the preferred language by [getting the user's mailbox settings](user_get_mailboxsettings.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="8396a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8396a-105">Permissions</span></span>
<span data-ttu-id="8396a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8396a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8396a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8396a-108">Permission type</span></span>      | <span data-ttu-id="8396a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8396a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8396a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8396a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8396a-111">User.Read, User.ReadBasic.All</span><span class="sxs-lookup"><span data-stu-id="8396a-111">User.Read, User.ReadBasic.All</span></span>    |
|<span data-ttu-id="8396a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8396a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8396a-113">User.Read</span><span class="sxs-lookup"><span data-stu-id="8396a-113">User.Read</span></span>    |
|<span data-ttu-id="8396a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8396a-114">Application</span></span> | <span data-ttu-id="8396a-115">User.Read.All</span><span class="sxs-lookup"><span data-stu-id="8396a-115">User.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8396a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8396a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/outlook/supportedLanguages
GET /users/{id|userPrincipalName}/outlook/supportedLanguages
```
## <a name="request-headers"></a><span data-ttu-id="8396a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8396a-117">Request headers</span></span>
| <span data-ttu-id="8396a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="8396a-118">Name</span></span>       | <span data-ttu-id="8396a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8396a-119">Type</span></span> | <span data-ttu-id="8396a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8396a-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8396a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8396a-121">Authorization</span></span>  | <span data-ttu-id="8396a-122">string</span><span class="sxs-lookup"><span data-stu-id="8396a-122">string</span></span>  | <span data-ttu-id="8396a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8396a-p103">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="8396a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8396a-125">Request body</span></span>
<span data-ttu-id="8396a-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8396a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8396a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8396a-127">Response</span></span>
<span data-ttu-id="8396a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [localeInfo](../resources/localeinfo.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8396a-128">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/localeinfo.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8396a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8396a-129">Example</span></span>
<span data-ttu-id="8396a-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8396a-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8396a-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8396a-131">Request</span></span>
<span data-ttu-id="8396a-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8396a-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "user_supportedlanguages"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/outlook/supportedLanguages
```

##### <a name="response"></a><span data-ttu-id="8396a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8396a-133">Response</span></span>
<span data-ttu-id="8396a-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8396a-134">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.localeInfo",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#Collection(microsoft.graph.localeInfo)",
  "value":[
    {
      "locale":"af-ZA",
      "displayName":"Afrikaans (Suid-Afrika)"
    },
    {
      "locale":"en-US",
      "displayName":"English (United States)"
    },
    {
       "locale":"en-CA",
       "displayName":"English (Canada)"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "user: supportedLanguages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->