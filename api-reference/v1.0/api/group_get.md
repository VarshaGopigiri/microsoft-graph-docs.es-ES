# <a name="get-group"></a><span data-ttu-id="b6375-101">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="b6375-101">Get group</span></span>

<span data-ttu-id="b6375-102">Obtiene las propiedades y relaciones de un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="b6375-102">Get the properties and relationships of a group object.</span></span>

##### <a name="default-properties"></a><span data-ttu-id="b6375-103">Propiedades predeterminadas</span><span class="sxs-lookup"><span data-stu-id="b6375-103">Default properties</span></span>

<span data-ttu-id="b6375-p101">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="b6375-p101">The following represent the default set of properties that are returned when getting or listing groups. These are a subset of all available properties.</span></span> 

* <span data-ttu-id="b6375-106">descripción</span><span class="sxs-lookup"><span data-stu-id="b6375-106">description</span></span>
* <span data-ttu-id="b6375-107">displayName</span><span class="sxs-lookup"><span data-stu-id="b6375-107">displayName</span></span>
* <span data-ttu-id="b6375-108">groupTypes</span><span class="sxs-lookup"><span data-stu-id="b6375-108">groupTypes</span></span>
* <span data-ttu-id="b6375-109">id</span><span class="sxs-lookup"><span data-stu-id="b6375-109">id</span></span>
* <span data-ttu-id="b6375-110">mail</span><span class="sxs-lookup"><span data-stu-id="b6375-110">mail</span></span>
* <span data-ttu-id="b6375-111">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="b6375-111">mailEnabled</span></span>
* <span data-ttu-id="b6375-112">mailNickname</span><span class="sxs-lookup"><span data-stu-id="b6375-112">mailNickname</span></span>
* <span data-ttu-id="b6375-113">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="b6375-113">onPremisesLastSyncDateTime</span></span>
* <span data-ttu-id="b6375-114">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="b6375-114">onPremisesSecurityIdentifier</span></span>
* <span data-ttu-id="b6375-115">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="b6375-115">onPremisesSyncEnabled</span></span>
* <span data-ttu-id="b6375-116">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="b6375-116">proxyAddresses</span></span>
* <span data-ttu-id="b6375-117">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="b6375-117">securityEnabled</span></span>
* <span data-ttu-id="b6375-118">visibility</span><span class="sxs-lookup"><span data-stu-id="b6375-118">visibility</span></span>

<span data-ttu-id="b6375-119">De forma predeterminada, no se devuelven las siguientes propiedades de grupo:</span><span class="sxs-lookup"><span data-stu-id="b6375-119">The following group properties are not returned by default:</span></span>

* <span data-ttu-id="b6375-120">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="b6375-120">allowExternalSenders</span></span>
* <span data-ttu-id="b6375-121">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="b6375-121">autoSubscribeNewMembers</span></span>
* <span data-ttu-id="b6375-122">isSubscribedByMail</span><span class="sxs-lookup"><span data-stu-id="b6375-122">isSubscribedByMail</span></span>
* <span data-ttu-id="b6375-123">unseenCount</span><span class="sxs-lookup"><span data-stu-id="b6375-123">unseenCount</span></span>

<span data-ttu-id="b6375-p102">Para obtener estas propiedades, use el parámetro de consulta **$select**. A continuación puede ver algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="b6375-p102">To get these properties, use the **$select** query parameter. The following are examples:</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```


## <a name="prerequisites"></a><span data-ttu-id="b6375-126">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6375-126">Prerequisites</span></span>
<span data-ttu-id="b6375-127">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="b6375-127">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="b6375-128">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6375-128">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b6375-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b6375-129">Optional query parameters</span></span>
<span data-ttu-id="b6375-130">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6375-130">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b6375-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6375-131">Request headers</span></span>
| <span data-ttu-id="b6375-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="b6375-132">Name</span></span>       | <span data-ttu-id="b6375-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6375-133">Type</span></span> | <span data-ttu-id="b6375-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6375-134">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="b6375-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6375-135">Authorization</span></span>  | <span data-ttu-id="b6375-136">string</span><span class="sxs-lookup"><span data-stu-id="b6375-136">string</span></span>  | <span data-ttu-id="b6375-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6375-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b6375-139">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6375-139">Request body</span></span>
<span data-ttu-id="b6375-140">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6375-140">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6375-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6375-141">Response</span></span>

<span data-ttu-id="b6375-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6375-142">If successful, this method returns a `200 OK` response code and [group](../resources/group.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b6375-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6375-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6375-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6375-144">Request</span></span>
<span data-ttu-id="b6375-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6375-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}
```
##### <a name="response"></a><span data-ttu-id="b6375-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6375-146">Response</span></span>
<span data-ttu-id="b6375-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6375-147">Here is an example of the response.</span></span>

<span data-ttu-id="b6375-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b6375-p104">Note: The response object shown here may be truncated for brevity. The default properties will be returned from an actual call, as described above.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: xxx

{
  "id": "id-value",
  "description": "description-value",
  "displayName": "displayName-value",
  "groupTypes": [
    "groupTypes-value"
  ],
  "mail": "mail-value",
  "mailEnabled": true,
  "mailNickname": "mailNickname-value",
  "onPremisesLastSyncDateTime": "onPremisesLastSyncDateTime-value",
  "onPremisesSecurityIdentifier": "onPremisesSecurityIdentifier-value",
  "onPremisesSyncEnabled": true,
  "proxyAddresses": [
    "proxyAddresses-value"
   ],
   "securityEnabled": true,
   "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
