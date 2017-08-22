# <a name="list-group-settings"></a><span data-ttu-id="86f86-101">Enumerar configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="86f86-101">List group settings</span></span>

<span data-ttu-id="86f86-102">Recupera una lista de objetos de configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="86f86-102">Retrieve a list of group setting objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86f86-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="86f86-103">Prerequisites</span></span>

<span data-ttu-id="86f86-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="86f86-104">One of the following **scopes** is required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="86f86-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86f86-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="86f86-106">Enumera la configuración de todo el inquilino o de un grupo.</span><span class="sxs-lookup"><span data-stu-id="86f86-106">List tenant-wide or group settings.</span></span>

```http
GET /groupSettings
GET group/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="86f86-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="86f86-107">Optional query parameters</span></span>
<span data-ttu-id="86f86-108">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86f86-108">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="86f86-109">Nota: No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="86f86-109">Note: $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="86f86-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86f86-110">Request headers</span></span>
| <span data-ttu-id="86f86-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="86f86-111">Name</span></span> | <span data-ttu-id="86f86-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="86f86-112">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="86f86-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="86f86-113">Authorization</span></span>  | <span data-ttu-id="86f86-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="86f86-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="86f86-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86f86-116">Request body</span></span>
<span data-ttu-id="86f86-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="86f86-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="86f86-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86f86-118">Response</span></span>

<span data-ttu-id="86f86-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86f86-119">If successful, this method returns a `200 OK` response code and collection of [groupSetting](../resources/groupsetting.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="86f86-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86f86-120">Example</span></span>

##### <a name="request"></a><span data-ttu-id="86f86-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86f86-121">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_groupsettings"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettings
```
##### <a name="response"></a><span data-ttu-id="86f86-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86f86-122">Response</span></span>

<span data-ttu-id="86f86-p102">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="86f86-p102">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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