# <a name="get-tab"></a><span data-ttu-id="ad760-101">Obtener la ficha</span><span class="sxs-lookup"><span data-stu-id="ad760-101">Get tab</span></span>



<span data-ttu-id="ad760-102">Recuperar las propiedades y relaciones de la [ficha](../resources/teamstab.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="ad760-102">Retrieve the properties and relationships of the specified [tab](../resources/teamstab.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="ad760-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ad760-103">Permissions</span></span>
<span data-ttu-id="ad760-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ad760-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ad760-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ad760-106">Permission type</span></span>      | <span data-ttu-id="ad760-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ad760-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ad760-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ad760-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ad760-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad760-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="ad760-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ad760-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ad760-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ad760-111">Not supported.</span></span>    |
|<span data-ttu-id="ad760-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ad760-112">Application</span></span> | <span data-ttu-id="ad760-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ad760-113">Group.Read.All, Group.ReadWrite.All</span></span> |

> <span data-ttu-id="ad760-114">Actualmente, se admiten sólo [delegar permisos](../../../concepts/permissions_reference.md) para esta operación.</span><span class="sxs-lookup"><span data-stu-id="ad760-114">Currently, only [delegated permissions](../../../concepts/permissions_reference.md) are supported for this operation.</span></span>

## <a name="http-request"></a><span data-ttu-id="ad760-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ad760-115">HTTP request</span></span>
```http
GET /teams/{id}/channels/{id}/tabs/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ad760-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ad760-116">Optional query parameters</span></span>

<span data-ttu-id="ad760-117">Este método admite la $select y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad760-117">This method supports the $select, and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ad760-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ad760-118">Request headers</span></span>
| <span data-ttu-id="ad760-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad760-119">Header</span></span>       | <span data-ttu-id="ad760-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ad760-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ad760-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ad760-121">Authorization</span></span>  | <span data-ttu-id="ad760-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad760-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ad760-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ad760-124">Request body</span></span>
<span data-ttu-id="ad760-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ad760-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ad760-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad760-126">Response</span></span>

<span data-ttu-id="ad760-127">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [tab](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad760-127">If successful, this method returns a `200 OK` response code and a [tab](../resources/teamstab.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ad760-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ad760-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ad760-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ad760-129">Request</span></span>
<span data-ttu-id="ad760-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ad760-130">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
```
#### <a name="response"></a><span data-ttu-id="ad760-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ad760-131">Response</span></span>
<span data-ttu-id="ad760-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ad760-132">The following is an example of the response.</span></span> 

><span data-ttu-id="ad760-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ad760-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "id": "tabId",
  "name": "My Contoso Tab - updated",
  "teamsAppId": "06805b9e-77e3-4b93-ac81-525eb87513b8",
  "configuration": {
    "entityId": "2DCA2E6C7A10415CAF6B8AB6661B3154",
    "contentUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/tabView",
    "websiteUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154",
    "removeUrl": "https://www.contoso.com/Orders/2DCA2E6C7A10415CAF6B8AB6661B3154/uninstallTab"
  },
  "sortOrderIndex": 20,
  "webUrl": "https://teams.microsoft.com/l/channel/19%3ac2e36757ee744c569e70b385e6dd79b6%40thread.skype/tab%3a%3afd736d46-51ed-4c0b-9b23-e67ca354bb24?label=my%20%contoso%to%tab"
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get a channel tab",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
