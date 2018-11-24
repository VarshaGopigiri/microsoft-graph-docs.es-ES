# <a name="create-team"></a><span data-ttu-id="8f4a0-101">Crear equipo</span><span class="sxs-lookup"><span data-stu-id="8f4a0-101">Create team</span></span>



<span data-ttu-id="8f4a0-102">Crear un nuevo [equipo](../resources/team.md) en un [grupo](../resources/group.md).</span><span class="sxs-lookup"><span data-stu-id="8f4a0-102">Create a new [team](../resources/team.md) under a [group](../resources/group.md).</span></span>

<span data-ttu-id="8f4a0-103">Para poder crear un equipo, el grupo debe tener un propietario menos uno.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-103">In order to create a team, the group must have a least one owner.</span></span>

<span data-ttu-id="8f4a0-104">Si el grupo se ha creado desde hace menos de 15 minutos, es posible que la llamada de equipo de creación se lleve a cabo con un código de 404 error debido a retrasos en la replicación.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-104">If the group was created less than 15 minutes ago, it's possible for the Create team call to fail with a 404 error code due to replication delays.</span></span> <span data-ttu-id="8f4a0-105">El modelo recomendado es volver a intentar la llamada de equipo crear tres veces, con un retraso de segundo 10 entre llamadas.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-105">The recommended pattern is to retry the Create team call three times, with a 10 second delay between calls.</span></span>

## <a name="permissions"></a><span data-ttu-id="8f4a0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="8f4a0-106">Permissions</span></span>

<span data-ttu-id="8f4a0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f4a0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8f4a0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f4a0-109">Permission type</span></span>      | <span data-ttu-id="8f4a0-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f4a0-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8f4a0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f4a0-111">Delegated (work or school account)</span></span> | <span data-ttu-id="8f4a0-112">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f4a0-112">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8f4a0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f4a0-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8f4a0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-114">Not supported.</span></span>    |
|<span data-ttu-id="8f4a0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f4a0-115">Application</span></span> | <span data-ttu-id="8f4a0-116">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f4a0-116">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8f4a0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f4a0-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
PUT /groups/{id}/team
```

## <a name="request-headers"></a><span data-ttu-id="8f4a0-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f4a0-118">Request headers</span></span>

| <span data-ttu-id="8f4a0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f4a0-119">Header</span></span>       | <span data-ttu-id="8f4a0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8f4a0-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8f4a0-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f4a0-121">Authorization</span></span>  | <span data-ttu-id="8f4a0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8f4a0-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8f4a0-124">Content-Type</span></span>  | <span data-ttu-id="8f4a0-125">application/json</span><span class="sxs-lookup"><span data-stu-id="8f4a0-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8f4a0-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f4a0-126">Request body</span></span>

<span data-ttu-id="8f4a0-127">En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [equipo](../resources/team.md) .</span><span class="sxs-lookup"><span data-stu-id="8f4a0-127">In the request body, supply a JSON representation of a [team](../resources/team.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="8f4a0-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f4a0-128">Response</span></span>

<span data-ttu-id="8f4a0-129">Si es correcta, este método debe devolver un `201 Created` código de respuesta y un objeto de [equipo](../resources/team.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-129">If successful, this method should return a `201 Created` response code and a [team](../resources/team.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f4a0-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f4a0-130">Example</span></span>

#### <a name="request"></a><span data-ttu-id="8f4a0-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f4a0-131">Request</span></span>

<span data-ttu-id="8f4a0-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "ignored",
  "name": "create_team"
}-->
```http
PUT https://graph.microsoft.com/v1.0/groups/{id}/team
Content-type: application/json

{  
  "memberSettings": {
    "allowCreateUpdateChannels": true
  },
  "messagingSettings": {
    "allowUserEditMessages": true,
    "allowUserDeleteMessages": true
  },
  "funSettings": {
    "allowGiphy": true,
    "giphyContentRating": "strict"
  }
}
```

#### <a name="response"></a><span data-ttu-id="8f4a0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f4a0-133">Response</span></span>

<span data-ttu-id="8f4a0-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-134">The following is an example of the response.</span></span> 

><span data-ttu-id="8f4a0-p104">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f4a0-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "microsoft.graph.team"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 401

{
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
  "description": "Create Team",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a><span data-ttu-id="8f4a0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f4a0-137">See also</span></span>

- [<span data-ttu-id="8f4a0-138">Creación de un grupo con un equipo</span><span class="sxs-lookup"><span data-stu-id="8f4a0-138">Creating a group with a team</span></span>](../../../concepts/teams-create-group-and-team.md)
