# <a name="get-team"></a><span data-ttu-id="7e232-101">Obtener el equipo</span><span class="sxs-lookup"><span data-stu-id="7e232-101">Get team</span></span>



<span data-ttu-id="7e232-102">Recuperar las propiedades y relaciones del [equipo](../resources/team.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="7e232-102">Retrieve the properties and relationships of the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="7e232-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7e232-103">Permissions</span></span>
<span data-ttu-id="7e232-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7e232-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7e232-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7e232-106">Permission type</span></span>      | <span data-ttu-id="7e232-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7e232-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7e232-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7e232-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7e232-109">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e232-109">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="7e232-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7e232-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7e232-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7e232-111">Not supported.</span></span>    |
|<span data-ttu-id="7e232-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7e232-112">Application</span></span> | <span data-ttu-id="7e232-113">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7e232-113">Group.Read.All, Group.ReadWrite.All</span></span>    |

## <a name="http-request"></a><span data-ttu-id="7e232-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7e232-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /teams/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7e232-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7e232-115">Optional query parameters</span></span>
<span data-ttu-id="7e232-116">Este método admite la $select y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e232-116">This method supports the $select and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7e232-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7e232-117">Request headers</span></span>
| <span data-ttu-id="7e232-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e232-118">Header</span></span>       | <span data-ttu-id="7e232-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7e232-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="7e232-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="7e232-120">Authorization</span></span>  | <span data-ttu-id="7e232-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7e232-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7e232-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7e232-123">Request body</span></span>
<span data-ttu-id="7e232-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7e232-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7e232-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e232-125">Response</span></span>

<span data-ttu-id="7e232-126">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e232-126">If successful, this method returns a `200 OK` response code and a [team](../resources/team.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="7e232-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7e232-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="7e232-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7e232-128">Request</span></span>
<span data-ttu-id="7e232-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7e232-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "get_team"
}-->
```http
GET https://graph.microsoft.com/beta/teams/{id}
```
#### <a name="response"></a><span data-ttu-id="7e232-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7e232-130">Response</span></span>
<span data-ttu-id="7e232-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7e232-131">The following is an example of the response.</span></span> 

><span data-ttu-id="7e232-p103">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7e232-p103">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 401

{
  "isArchived" : false,
  "memberSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true,
    "allowAddRemoveApps": true,
    "allowCreateUpdateRemoveTabs": true,
    "allowCreateUpdateRemoveConnectors": true    
  },
  "guestSettings": {
    "allowCreateUpdateChannels": true,
    "allowDeleteChannels": true 
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true,
    "allowOwnerDeleteMessages": true,
    "allowTeamMentions": true,
    "allowChannelMentions": true    
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict",
    "allowStickersAndMemes": true,
    "allowCustomMemes": true
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
