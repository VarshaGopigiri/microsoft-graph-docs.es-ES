# <a name="get-rule"></a><span data-ttu-id="43e4e-101">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="43e4e-101">Get rule</span></span>


<span data-ttu-id="43e4e-102">Obtener las propiedades y relaciones de un objeto [messageRule](../resources/messagerule.md).</span><span class="sxs-lookup"><span data-stu-id="43e4e-102">Get the properties and relationships of a [calendar](../resources/messagerule.md) object.</span></span>


## <a name="permissions"></a><span data-ttu-id="43e4e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="43e4e-103">Permissions</span></span>
<span data-ttu-id="43e4e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="43e4e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="43e4e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="43e4e-106">Permission type</span></span>      | <span data-ttu-id="43e4e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="43e4e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="43e4e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="43e4e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="43e4e-109">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="43e4e-109">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="43e4e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="43e4e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43e4e-111">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="43e4e-111">MailboxSettings.Read</span></span>    |
|<span data-ttu-id="43e4e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="43e4e-112">Application</span></span> | <span data-ttu-id="43e4e-113">MailboxSettings.Read</span><span class="sxs-lookup"><span data-stu-id="43e4e-113">MailboxSettings.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="43e4e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="43e4e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/inbox/messagerules/{id}
GET /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="43e4e-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="43e4e-115">Optional query parameters</span></span>
<span data-ttu-id="43e4e-116">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43e4e-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="43e4e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4e-117">Request headers</span></span>
| <span data-ttu-id="43e4e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="43e4e-118">Name</span></span>      |<span data-ttu-id="43e4e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="43e4e-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="43e4e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="43e4e-120">Authorization</span></span>  | <span data-ttu-id="43e4e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43e4e-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="43e4e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4e-123">Request body</span></span>
<span data-ttu-id="43e4e-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="43e4e-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="43e4e-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43e4e-125">Response</span></span>
<span data-ttu-id="43e4e-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43e4e-126">If successful, this method returns a `200 OK` response code and a [deviceManagementExchangeConnector](../resources/messagerule.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="43e4e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="43e4e-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="43e4e-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="43e4e-128">Request</span></span>
<span data-ttu-id="43e4e-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="43e4e-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_messagerule"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')
```
##### <a name="response"></a><span data-ttu-id="43e4e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="43e4e-130">Response</span></span>
<span data-ttu-id="43e4e-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="43e4e-131">Here is an example of the response.</span></span> <span data-ttu-id="43e4e-132">De forma predeterminada, las propiedades de fecha y hora de la respuesta están en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="43e4e-132">By default, the date-time properties in the response are in UTC.</span></span> 

<span data-ttu-id="43e4e-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="43e4e-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
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
  "description": "Get rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->