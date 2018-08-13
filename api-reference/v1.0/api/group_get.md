# <a name="get-group"></a><span data-ttu-id="a1588-101">Obtener grupo</span><span class="sxs-lookup"><span data-stu-id="a1588-101">Get group</span></span>
<span data-ttu-id="a1588-102">Obtiene las propiedades y relaciones de un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="a1588-102">Get the properties and relationships of a group object.</span></span>

##### <a name="default-properties"></a><span data-ttu-id="a1588-103">Propiedades predeterminadas</span><span class="sxs-lookup"><span data-stu-id="a1588-103">Default properties</span></span>

<span data-ttu-id="a1588-p101">Las siguientes propiedades representan el conjunto predeterminado de propiedades que se devuelven al obtener o enumerar grupos. Son un subconjunto de todas las propiedades disponibles.</span><span class="sxs-lookup"><span data-stu-id="a1588-p101">The following represent the default set of properties that are returned when getting or listing groups. These are a subset of all available properties.</span></span>

* <span data-ttu-id="a1588-106">descripción</span><span class="sxs-lookup"><span data-stu-id="a1588-106">description</span></span>
* <span data-ttu-id="a1588-107">displayName</span><span class="sxs-lookup"><span data-stu-id="a1588-107">displayName</span></span>
* <span data-ttu-id="a1588-108">groupTypes</span><span class="sxs-lookup"><span data-stu-id="a1588-108">groupTypes</span></span>
* <span data-ttu-id="a1588-109">id</span><span class="sxs-lookup"><span data-stu-id="a1588-109">id</span></span>
* <span data-ttu-id="a1588-110">mail</span><span class="sxs-lookup"><span data-stu-id="a1588-110">mail</span></span>
* <span data-ttu-id="a1588-111">mailEnabled</span><span class="sxs-lookup"><span data-stu-id="a1588-111">mailEnabled</span></span>
* <span data-ttu-id="a1588-112">mailNickname</span><span class="sxs-lookup"><span data-stu-id="a1588-112">mailNickname</span></span>
* <span data-ttu-id="a1588-113">onPremisesLastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a1588-113">onPremisesLastSyncDateTime</span></span>
* <span data-ttu-id="a1588-114">onPremisesSecurityIdentifier</span><span class="sxs-lookup"><span data-stu-id="a1588-114">onPremisesSecurityIdentifier</span></span>
* <span data-ttu-id="a1588-115">onPremisesSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="a1588-115">onPremisesSyncEnabled</span></span>
* <span data-ttu-id="a1588-116">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="a1588-116">proxyAddresses</span></span>
* <span data-ttu-id="a1588-117">securityEnabled</span><span class="sxs-lookup"><span data-stu-id="a1588-117">securityEnabled</span></span>
* <span data-ttu-id="a1588-118">visibility</span><span class="sxs-lookup"><span data-stu-id="a1588-118">visibility</span></span>

<span data-ttu-id="a1588-119">De forma predeterminada, no se devuelven las siguientes propiedades de grupo:</span><span class="sxs-lookup"><span data-stu-id="a1588-119">The following group properties are not returned by default:</span></span>

* <span data-ttu-id="a1588-120">allowExternalSenders</span><span class="sxs-lookup"><span data-stu-id="a1588-120">allowExternalSenders</span></span>
* <span data-ttu-id="a1588-121">autoSubscribeNewMembers</span><span class="sxs-lookup"><span data-stu-id="a1588-121">autoSubscribeNewMembers</span></span>
* <span data-ttu-id="a1588-122">isSubscribedByMail</span><span class="sxs-lookup"><span data-stu-id="a1588-122">isSubscribedByMail</span></span>
* <span data-ttu-id="a1588-123">unseenCount</span><span class="sxs-lookup"><span data-stu-id="a1588-123">unseenCount</span></span>

<span data-ttu-id="a1588-p102">Para obtener estas propiedades, use el parámetro de consulta **$select**. A continuación puede ver algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="a1588-p102">To get these properties, use the **$select** query parameter. The following are examples:</span></span> 

<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=allowExternalSenders,autoSubscribeNewMembers,isSubscribedByMail,unseenCount

GET https://graph.microsoft.com/v1.0/groups/c28c1cc9-e1ab-4c4d-98d1-d8fdf128b60f?$select=description,allowExternalSenders
```


## <a name="permissions"></a><span data-ttu-id="a1588-126">Permisos</span><span class="sxs-lookup"><span data-stu-id="a1588-126">Permissions</span></span>
<span data-ttu-id="a1588-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a1588-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a1588-129">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a1588-129">Permission type</span></span>      | <span data-ttu-id="a1588-130">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a1588-130">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a1588-131">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a1588-131">Delegated (work or school account)</span></span> | <span data-ttu-id="a1588-132">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1588-132">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="a1588-133">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a1588-133">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a1588-134">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a1588-134">Not supported.</span></span>    |
|<span data-ttu-id="a1588-135">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a1588-135">Application</span></span> | <span data-ttu-id="a1588-136">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a1588-136">Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a1588-137">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a1588-137">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a1588-138">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a1588-138">Optional query parameters</span></span>
<span data-ttu-id="a1588-139">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1588-139">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a1588-140">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a1588-140">Request headers</span></span>
| <span data-ttu-id="a1588-141">Nombre</span><span class="sxs-lookup"><span data-stu-id="a1588-141">Name</span></span>       | <span data-ttu-id="a1588-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="a1588-142">Type</span></span> | <span data-ttu-id="a1588-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1588-143">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="a1588-144">Authorization</span><span class="sxs-lookup"><span data-stu-id="a1588-144">Authorization</span></span>  | <span data-ttu-id="a1588-145">string</span><span class="sxs-lookup"><span data-stu-id="a1588-145">string</span></span>  | <span data-ttu-id="a1588-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a1588-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a1588-148">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a1588-148">Request body</span></span>
<span data-ttu-id="a1588-149">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a1588-149">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a1588-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1588-150">Response</span></span>
<span data-ttu-id="a1588-151">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1588-151">If successful, this method returns a `200 OK` response code and [group](../resources/group.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a1588-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a1588-152">Example</span></span>
#### <a name="request"></a><span data-ttu-id="a1588-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a1588-153">Request</span></span>
<span data-ttu-id="a1588-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a1588-154">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_group"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="a1588-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a1588-155">Response</span></span>
<span data-ttu-id="a1588-156">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a1588-156">The following is an example of the response.</span></span>

><span data-ttu-id="a1588-157">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1588-157">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="a1588-158">Se devolverán todas las propiedades predeterminadas de una llamada real, como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a1588-158">The default properties will be returned from an actual call, as described before.</span></span>
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
