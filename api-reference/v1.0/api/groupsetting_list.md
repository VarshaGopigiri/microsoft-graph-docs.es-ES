# <a name="list-group-settings"></a><span data-ttu-id="3a9f7-101">Enumerar configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="3a9f7-101">List group settings</span></span>

<span data-ttu-id="3a9f7-102">Recupera una lista de objetos de configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-102">Retrieve a list of group setting objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="3a9f7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="3a9f7-103">Permissions</span></span>

<span data-ttu-id="3a9f7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3a9f7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="3a9f7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3a9f7-106">Permission type</span></span>      | <span data-ttu-id="3a9f7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3a9f7-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="3a9f7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3a9f7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="3a9f7-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3a9f7-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="3a9f7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3a9f7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3a9f7-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-111">Not supported.</span></span>    | 
|<span data-ttu-id="3a9f7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3a9f7-112">Application</span></span> | <span data-ttu-id="3a9f7-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3a9f7-113">Directory.Read.All, Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="3a9f7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a9f7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="3a9f7-115">Enumera la configuración de todo el inquilino o de un grupo.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-115">List tenant-wide or group settings.</span></span>

```http
GET /groupSettings
GET group/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3a9f7-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3a9f7-116">Optional query parameters</span></span>
<span data-ttu-id="3a9f7-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="3a9f7-118">Nota: No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-118">Note: $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3a9f7-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9f7-119">Request headers</span></span>
| <span data-ttu-id="3a9f7-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3a9f7-120">Name</span></span> | <span data-ttu-id="3a9f7-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a9f7-121">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="3a9f7-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a9f7-122">Authorization</span></span>  | <span data-ttu-id="3a9f7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3a9f7-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9f7-125">Request body</span></span>
<span data-ttu-id="3a9f7-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3a9f7-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a9f7-127">Response</span></span>

<span data-ttu-id="3a9f7-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-128">If successful, this method returns a `200 OK` response code and collection of [groupSetting](../resources/groupsetting.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3a9f7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a9f7-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3a9f7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a9f7-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_groupsettings"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettings
```
##### <a name="response"></a><span data-ttu-id="3a9f7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a9f7-131">Response</span></span>

<span data-ttu-id="3a9f7-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a9f7-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 263

{
  "value": [
    {
      "displayName": "displayName-value",
      "templateId": "templateId-value",
      "values": [
        {
          "name": "name-value",
          "value": "value-value"
        }
      ],
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupSettings",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->