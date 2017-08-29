# <a name="get-a-group-setting-template"></a><span data-ttu-id="aa0b5-101">Obtener una plantilla de configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="aa0b5-101">Get a group setting template</span></span>

<span data-ttu-id="aa0b5-p101">Una plantilla de configuración de grupo representa una plantilla de configuración desde la que puede crearse la configuración para un arrendatario. Esta operación permite la recuperación de las propiedades del objeto [groupSettingTemplate](../resources/groupsettingtemplate.md), incluyendo las configuraciones disponibles y sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-p101">A group setting template represents a template of settings from which settings may be created within a tenant. This operation allows retrieval of the properties of the [groupSettingTemplate](../resources/groupsettingtemplate.md) object, including the available settings and their defaults.</span></span>

## <a name="permissions"></a><span data-ttu-id="aa0b5-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="aa0b5-104">Permissions</span></span>

<span data-ttu-id="aa0b5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="aa0b5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="aa0b5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa0b5-107">Permission type</span></span>      | <span data-ttu-id="aa0b5-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa0b5-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="aa0b5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa0b5-109">Delegated (work or school account)</span></span> | <span data-ttu-id="aa0b5-110">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="aa0b5-110">One of the following scopes is required to execute this API: Directory.Read.All; Directory.ReadWrite.All; Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="aa0b5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa0b5-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="aa0b5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-112">Not supported.</span></span>    |
|<span data-ttu-id="aa0b5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa0b5-113">Application</span></span> | <span data-ttu-id="aa0b5-114">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa0b5-114">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="aa0b5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa0b5-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupSettingTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="aa0b5-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="aa0b5-116">Optional query parameters</span></span>
<span data-ttu-id="aa0b5-117">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-117">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="aa0b5-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0b5-118">Request headers</span></span>
| <span data-ttu-id="aa0b5-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="aa0b5-119">Name</span></span> | <span data-ttu-id="aa0b5-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa0b5-120">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="aa0b5-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa0b5-121">Authorization</span></span> | <span data-ttu-id="aa0b5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="aa0b5-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0b5-124">Request body</span></span>
<span data-ttu-id="aa0b5-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="aa0b5-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa0b5-126">Response</span></span>

<span data-ttu-id="aa0b5-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [groupSettingTemplate](../resources/groupsettingtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-127">If successful, this method returns a `200 OK` response code and [groupSettingTemplate](../resources/groupsettingtemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa0b5-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa0b5-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="aa0b5-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa0b5-129">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groupsettingtemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettingTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="aa0b5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa0b5-130">Response</span></span>

<span data-ttu-id="aa0b5-p104">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa0b5-p104">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSettingTemplate"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1341

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groupSettingTemplates/$entity",
    "id": "62375ab9-6b52-47ed-826b-58e47e0e304b",
    "deletedDateTime": null,
    "displayName": "Group.Unified",
    "description": "Setting templates define the different settings that can be used for the associated ObjectSettings. This template defines settings that can be used for Unified Groups.",
    "values": [
        {
            "name": "CustomBlockedWordsList",
            "type": "System.String",
            "defaultValue": "",
            "description": "A comma-delimited list of blocked words for Unified Group displayName and mailNickName."
        },
        {
            "name": "EnableMSStandardBlockedWords",
            "type": "System.Boolean",
            "defaultValue": "false",
            "description": "A flag indicating whether or not to enable the Microsoft Standard list of blocked words for Unified Group displayName and mailNickName."
        },
        {
            "name": "ClassificationDescriptions",
            "type": "System.String",
            "defaultValue": "",
            "description": "A comma-delimited list of structured strings describing the classification values in the ClassificationList. The structure of the string is: Value: Description"
        }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get groupSettingTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->