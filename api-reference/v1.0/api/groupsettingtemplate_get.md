# <a name="get-a-group-setting-template"></a><span data-ttu-id="71c1c-101">Obtener una plantilla de configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="71c1c-101">Get a group setting template</span></span>

<span data-ttu-id="71c1c-p101">Una plantilla de configuración de grupo representa una plantilla de configuración desde la que puede crearse la configuración para un arrendatario. Esta operación permite la recuperación de las propiedades del objeto [groupSettingTemplate](../resources/groupsettingtemplate.md), incluyendo las configuraciones disponibles y sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="71c1c-p101">A group setting template represents a template of settings from which settings may be created within a tenant. This operation allows retrieval of the properties of the [groupSettingTemplate](../resources/groupsettingtemplate.md) object, including the available settings and their defaults.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71c1c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71c1c-104">Prerequisites</span></span>

<span data-ttu-id="71c1c-105">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="71c1c-105">The following **scopes** are required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="71c1c-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71c1c-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupSettingTemplates/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="71c1c-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71c1c-107">Optional query parameters</span></span>
<span data-ttu-id="71c1c-108">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71c1c-108">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="71c1c-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71c1c-109">Request headers</span></span>
| <span data-ttu-id="71c1c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="71c1c-110">Name</span></span> | <span data-ttu-id="71c1c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="71c1c-111">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="71c1c-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="71c1c-112">Authorization</span></span> | <span data-ttu-id="71c1c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71c1c-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="71c1c-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71c1c-115">Request body</span></span>
<span data-ttu-id="71c1c-116">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71c1c-116">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71c1c-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71c1c-117">Response</span></span>

<span data-ttu-id="71c1c-118">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [groupSettingTemplate](../resources/groupsettingtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71c1c-118">If successful, this method returns a `200 OK` response code and [groupSettingTemplate](../resources/groupsettingtemplate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71c1c-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71c1c-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71c1c-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71c1c-120">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groupsettingtemplate"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettingTemplates/{id}
```
##### <a name="response"></a><span data-ttu-id="71c1c-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71c1c-121">Response</span></span>

<span data-ttu-id="71c1c-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71c1c-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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