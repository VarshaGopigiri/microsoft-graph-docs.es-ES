# <a name="list-groupsettingtemplates"></a><span data-ttu-id="28122-101">List groupSettingTemplates</span><span class="sxs-lookup"><span data-stu-id="28122-101">List groupSettingTemplates</span></span>

<span data-ttu-id="28122-p101">Las plantillas de configuración de grupo representan un conjunto de plantillas desde las que se pueden crear configuraciones de grupos para usarlas en un inquilino.  Con esta operación se recupera la lista de objetos groupSettingTemplates disponibles.</span><span class="sxs-lookup"><span data-stu-id="28122-p101">Group setting templates represents a set of templates  from which group settings may be created and used within a tenant.  This operation retrieves the list of available groupSettingTemplates objects.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="28122-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="28122-104">Prerequisites</span></span>

<span data-ttu-id="28122-105">Se requieren los siguientes **ámbitos** para ejecutar esta API: *Directory.Read.All*, *Directory.ReadWrite.All* o *Directory.AccessAsUser.All*</span><span class="sxs-lookup"><span data-stu-id="28122-105">The following **scopes** are required to execute this API: *Directory.Read.All* or *Directory.ReadWrite.All* or *Directory.AccessAsUser.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="28122-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="28122-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupSettingTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="28122-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="28122-107">Optional query parameters</span></span>
<span data-ttu-id="28122-108">Este método admite los [parámetros de consulta de OData](http://graph.microsoft.io/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28122-108">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="28122-109">**Nota:** No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="28122-109">**Note:** $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="28122-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="28122-110">Request headers</span></span>
| <span data-ttu-id="28122-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="28122-111">Name</span></span> | <span data-ttu-id="28122-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="28122-112">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="28122-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="28122-113">Authorization</span></span>  | <span data-ttu-id="28122-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="28122-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="28122-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="28122-116">Request body</span></span>
<span data-ttu-id="28122-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="28122-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="28122-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28122-118">Response</span></span>

<span data-ttu-id="28122-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [groupSettingTemplate](../resources/groupsettingtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="28122-119">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/groupsettingtemplate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="28122-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="28122-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="28122-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="28122-121">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groupsettingtemplates"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettingTemplates
```
##### <a name="response"></a><span data-ttu-id="28122-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="28122-122">Response</span></span>

<span data-ttu-id="28122-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="28122-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSettingTemplate",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1770

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#groupSettingTemplates",
    "value": [
                {
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
            ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupSettingTemplates",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->