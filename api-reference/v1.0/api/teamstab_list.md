# <a name="list-tabs-in-channel"></a><span data-ttu-id="2dddc-101">Fichas de lista de canal</span><span class="sxs-lookup"><span data-stu-id="2dddc-101">List tabs in channel</span></span>



<span data-ttu-id="2dddc-102">Recuperar la lista de [fichas](../resources/teamstab.md) en el [canal](../resources/channel.md) especificado dentro de un [equipo](../resources/team.md).</span><span class="sxs-lookup"><span data-stu-id="2dddc-102">Retrieve the list of [tabs](../resources/teamstab.md) in the specified [channel](../resources/channel.md) within a [team](../resources/team.md).</span></span> 

## <a name="permissions"></a><span data-ttu-id="2dddc-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2dddc-103">Permissions</span></span>
<span data-ttu-id="2dddc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2dddc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2dddc-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2dddc-106">Permission type</span></span>      | <span data-ttu-id="2dddc-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2dddc-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2dddc-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2dddc-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2dddc-109">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="2dddc-109">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="2dddc-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2dddc-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2dddc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2dddc-111">Not supported.</span></span>    |
| <span data-ttu-id="2dddc-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2dddc-112">Application</span></span>                            | <span data-ttu-id="2dddc-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2dddc-113">Group.Read.All, Group.ReadWrite.All</span></span>         |

## <a name="http-request"></a><span data-ttu-id="2dddc-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2dddc-114">HTTP request</span></span>

```http
GET /teams/{id}/channels/{id}/tabs
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2dddc-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2dddc-115">Optional query parameters</span></span>

<span data-ttu-id="2dddc-116">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2dddc-116">This method supports the $filter, $select, and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2dddc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2dddc-117">Request headers</span></span>
| <span data-ttu-id="2dddc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dddc-118">Header</span></span>       | <span data-ttu-id="2dddc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2dddc-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2dddc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="2dddc-120">Authorization</span></span>  | <span data-ttu-id="2dddc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2dddc-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2dddc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2dddc-123">Request body</span></span>
<span data-ttu-id="2dddc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2dddc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2dddc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2dddc-125">Response</span></span>
<span data-ttu-id="2dddc-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [las fichas](../resources/teamstab.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2dddc-126">If successful, this method returns a `200 OK` response code and collection of [tabs](../resources/teamstab.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2dddc-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2dddc-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="2dddc-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2dddc-128">Request</span></span>
<span data-ttu-id="2dddc-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2dddc-129">The following is an example of the request.</span></span>
```http
GET https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs
```

#### <a name="response"></a><span data-ttu-id="2dddc-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2dddc-130">Response</span></span>
<span data-ttu-id="2dddc-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2dddc-131">The following is an example of the response.</span></span>
><span data-ttu-id="2dddc-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2dddc-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
```http
HTTP/1.1 200 Success
Content-type: application/json

{
  "value": [
    {
      "id": "794f0e4e-4d10-4bb5-9079-3a465a629eff",
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
    },
    {
      "id": "b5d5f001-0471-49a5-aac4-04ef96683be0",
      "name": "My Trello Tab",
      "teamsAppId": "23134c6b-5e4b-439c-8f70-3ded1df20805",
      "configuration": null,
      "sortOrderIndex": 21,
      "webUrl": "https://teams.microsoft.com/l/channel/19%3ac2e36757ee744c569e70b385e6dd79b6%40thread.skype/tab%3a%3a3709b35c-a0ba-467c-8001-0f66895fb9d3?label=My%20Trello%Tab"
    }
  ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List all tabs in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
