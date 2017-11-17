# <a name="list-memberof"></a><span data-ttu-id="ebbc2-101">Enumerar memberOf</span><span class="sxs-lookup"><span data-stu-id="ebbc2-101">List memberOf</span></span>

<span data-ttu-id="ebbc2-102">Obtiene todos los [grupos](../resources/group.md) y [roles de directorio](../resources/directoryrole.md) de los que el usuario es miembro directo.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-102">Get [groups](../resources/group.md) and [directory roles](../resources/directoryrole.md) that the user is a direct member of.</span></span> 

## <a name="permissions"></a><span data-ttu-id="ebbc2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ebbc2-103">Permissions</span></span>
<span data-ttu-id="ebbc2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ebbc2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ebbc2-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ebbc2-106">Permission type</span></span>      | <span data-ttu-id="ebbc2-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ebbc2-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ebbc2-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ebbc2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ebbc2-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ebbc2-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ebbc2-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ebbc2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ebbc2-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-111">Not supported.</span></span>    |
|<span data-ttu-id="ebbc2-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ebbc2-112">Application</span></span> | <span data-ttu-id="ebbc2-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ebbc2-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ebbc2-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ebbc2-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /users/{id | userPrincipalName}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ebbc2-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ebbc2-115">Optional query parameters</span></span>
<span data-ttu-id="ebbc2-p102">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta. No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-p102">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response. $filter is not supported.</span></span> 

## <a name="request-headers"></a><span data-ttu-id="ebbc2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbc2-118">Request headers</span></span>
| <span data-ttu-id="ebbc2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ebbc2-119">Header</span></span>       | <span data-ttu-id="ebbc2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ebbc2-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="ebbc2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ebbc2-121">Authorization</span></span>  | <span data-ttu-id="ebbc2-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="ebbc2-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ebbc2-124">Accept</span></span>  | <span data-ttu-id="ebbc2-125">application/json</span><span class="sxs-lookup"><span data-stu-id="ebbc2-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ebbc2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbc2-126">Request body</span></span>
<span data-ttu-id="ebbc2-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ebbc2-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebbc2-128">Response</span></span>

<span data-ttu-id="ebbc2-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-129">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ebbc2-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebbc2-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ebbc2-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ebbc2-131">Request</span></span>
<span data-ttu-id="ebbc2-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/memberOf
```
##### <a name="response"></a><span data-ttu-id="ebbc2-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ebbc2-133">Response</span></span>
<span data-ttu-id="ebbc2-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ebbc2-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.group",
      "id": "id-value",
      "createdDateTime": null,
      "description": "All users at the company",
      "displayName": "All Users",
      "groupTypes": [],
      "mailEnabled": false,
      "securityEnabled": true,
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
