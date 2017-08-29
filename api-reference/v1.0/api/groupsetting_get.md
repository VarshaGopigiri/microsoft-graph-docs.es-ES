# <a name="get-a-group-setting"></a><span data-ttu-id="32234-101">Obtener una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="32234-101">Get a group setting</span></span>

<span data-ttu-id="32234-102">Recupera las propiedades de un objeto de configuración de grupo específico.</span><span class="sxs-lookup"><span data-stu-id="32234-102">Retrieve the properties of a specific of group setting object.</span></span>

## <a name="permissions"></a><span data-ttu-id="32234-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="32234-103">Permissions</span></span>

<span data-ttu-id="32234-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="32234-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="32234-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32234-106">Permission type</span></span>      | <span data-ttu-id="32234-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32234-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="32234-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32234-108">Delegated (work or school account)</span></span> | <span data-ttu-id="32234-109">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="32234-109">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="32234-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32234-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="32234-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32234-111">Not supported.</span></span>    |
|<span data-ttu-id="32234-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32234-112">Application</span></span> | <span data-ttu-id="32234-113">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="32234-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="32234-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32234-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="32234-115">Obtiene una configuración para todo el inquilino o para un grupo.</span><span class="sxs-lookup"><span data-stu-id="32234-115">Get a specific tenant-wide or group setting.</span></span>

```http
GET /groupSettings/{id}
GET /groups/{id}/settings/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="32234-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="32234-116">Optional query parameters</span></span>
<span data-ttu-id="32234-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32234-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="32234-118">Nota: No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="32234-118">Note: $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="32234-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32234-119">Request headers</span></span>
| <span data-ttu-id="32234-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="32234-120">Name</span></span> | <span data-ttu-id="32234-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="32234-121">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="32234-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="32234-122">Authorization</span></span> | <span data-ttu-id="32234-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32234-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="32234-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32234-125">Request body</span></span>

<span data-ttu-id="32234-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="32234-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="32234-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32234-127">Response</span></span>

<span data-ttu-id="32234-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32234-128">If successful, this method returns a `200 OK` response code and [groupSetting](../resources/groupsetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="32234-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32234-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="32234-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32234-130">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groupsetting"
}-->

```http
GET https://graph.microsoft.com/v1.0/groupSettings/{id}
```
##### <a name="response"></a><span data-ttu-id="32234-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32234-131">Response</span></span>

<span data-ttu-id="32234-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32234-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 194

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
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get groupSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->