# <a name="update-tab"></a><span data-ttu-id="34bb8-101">Ficha de actualización</span><span class="sxs-lookup"><span data-stu-id="34bb8-101">Update tab</span></span>



<span data-ttu-id="34bb8-102">Actualizar las propiedades de la [ficha](../resources/teamstab.md)de especificado. Esto se puede usar para configurar el contenido de la ficha.</span><span class="sxs-lookup"><span data-stu-id="34bb8-102">Update the properties of the specified [tab](../resources/teamstab.md). This can be used to configure the content of the tab.</span></span>

## <a name="permissions"></a><span data-ttu-id="34bb8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="34bb8-103">Permissions</span></span>
<span data-ttu-id="34bb8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="34bb8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="34bb8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="34bb8-106">Permission type</span></span>      | <span data-ttu-id="34bb8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="34bb8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="34bb8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="34bb8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="34bb8-109">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34bb8-109">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="34bb8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="34bb8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="34bb8-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="34bb8-111">Not supported.</span></span>    |
|<span data-ttu-id="34bb8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="34bb8-112">Application</span></span>                            | <span data-ttu-id="34bb8-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="34bb8-113">Group.ReadWrite.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="34bb8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="34bb8-114">HTTP request</span></span>
```http
PATCH /teams/{id}/channels/{id}/tabs/{id}
```
## <a name="request-headers"></a><span data-ttu-id="34bb8-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="34bb8-115">Request headers</span></span>
| <span data-ttu-id="34bb8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34bb8-116">Header</span></span>       | <span data-ttu-id="34bb8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="34bb8-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="34bb8-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="34bb8-118">Authorization</span></span>  | <span data-ttu-id="34bb8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="34bb8-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="34bb8-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="34bb8-121">Content-Type</span></span>  | <span data-ttu-id="34bb8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="34bb8-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="34bb8-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="34bb8-123">Request body</span></span>
<span data-ttu-id="34bb8-124">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [tab](../resources/teamstab.md) .</span><span class="sxs-lookup"><span data-stu-id="34bb8-124">In the request body, supply a JSON representation of [tab](../resources/teamstab.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="34bb8-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34bb8-125">Response</span></span>

<span data-ttu-id="34bb8-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="34bb8-126">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="34bb8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="34bb8-127">Example</span></span>
#### <a name="request"></a><span data-ttu-id="34bb8-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="34bb8-128">Request</span></span>
<span data-ttu-id="34bb8-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="34bb8-129">The following is an example of the request.</span></span>
```http
PATCH https://graph.microsoft.com/beta/teams/{id}/channels/{id}/tabs/{id}
Content-type: application/json
Content-length: 211

{
  "name": "My Contoso Tab - updated"
}
```
#### <a name="response"></a><span data-ttu-id="34bb8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="34bb8-130">Response</span></span>
```http
HTTP/1.1 200 Success
Content-type: application/json

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

## <a name="see-also"></a><span data-ttu-id="34bb8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="34bb8-131">See also</span></span>

[<span data-ttu-id="34bb8-132">Configuración de los tipos de ficha integrada</span><span class="sxs-lookup"><span data-stu-id="34bb8-132">Configuring the built-in tab types</span></span>](../../../concepts/teams-configuring-builtin-tabs.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tab in channel",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
