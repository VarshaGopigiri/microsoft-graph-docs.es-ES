# <a name="create-a-group-setting"></a><span data-ttu-id="3acd5-101">Crear una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="3acd5-101">Create a group setting</span></span>

<span data-ttu-id="3acd5-p101">Use esta API para crear una nueva configuración basada en las plantillas disponibles en [groupSettingTemplates](../resources/groupsettingtemplate.md). Esta configuración puede establecerse a nivel de arrendatario o de grupo. La solicitud de creación debe proporcionar [settingValues](../resources/settingvalue.md) para toda la configuración establecida en la plantilla. Para configuraciones específicas de grupos, solo se puede establecer la configuración que indique si los miembros de un grupo pueden invitar a otros usuarios como invitados o no. Esto establecerá este comportamiento una vez que esté disponible de forma general la posibilidad de agregar usuarios como invitados.</span><span class="sxs-lookup"><span data-stu-id="3acd5-p101">Use this API to create a new setting, based on the templates available in [groupSettingTemplates](../resources/groupsettingtemplate.md). These settings can be at the tenant-level or at the group level. The creation request must provide [settingValues](../resources/settingvalue.md) for all the settings defined in the template. For group-specific settings, only the setting governing whether members of a group can invite guest users can be set. This will govern this behavior once the ability to add guest users to a group is generally available.</span></span>

## <a name="permissions"></a><span data-ttu-id="3acd5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3acd5-107">Permissions</span></span>

<span data-ttu-id="3acd5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3acd5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="3acd5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3acd5-110">Permission type</span></span>      | <span data-ttu-id="3acd5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3acd5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3acd5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3acd5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3acd5-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="3acd5-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="3acd5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3acd5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3acd5-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3acd5-115">Not supported.</span></span>    |
|<span data-ttu-id="3acd5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3acd5-116">Application</span></span> | <span data-ttu-id="3acd5-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3acd5-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3acd5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3acd5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupSettings
POST /groups/{id}/settings
```

## <a name="request-headers"></a><span data-ttu-id="3acd5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3acd5-119">Request headers</span></span>

| <span data-ttu-id="3acd5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="3acd5-120">Name</span></span> | <span data-ttu-id="3acd5-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3acd5-121">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="3acd5-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3acd5-122">Authorization</span></span> | <span data-ttu-id="3acd5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3acd5-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="3acd5-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3acd5-125">Content-Type</span></span> | <span data-ttu-id="3acd5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="3acd5-126">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="3acd5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3acd5-127">Request body</span></span>
<span data-ttu-id="3acd5-p104">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupSetting](../resources/groupsetting.md). Sin embargo, el nombre para mostrar de la configuración se establecerá según el nombre de la plantilla de configuración a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="3acd5-p104">In the request body, supply a JSON representation of [groupSetting](../resources/groupsetting.md) object. However, the display name for the setting will be set based on the referenced settings template name.</span></span>

## <a name="response"></a><span data-ttu-id="3acd5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3acd5-130">Response</span></span>

<span data-ttu-id="3acd5-131">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3acd5-131">If successful, this method returns `201 Created` response code and [groupSetting](../resources/groupsetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3acd5-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3acd5-132">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3acd5-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3acd5-133">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_groupsetting_from_groupsettings"
}-->
```http
POST https://graph.microsoft.com/v1.0/groupSettings
Content-type: application/json
Content-length: 215

{
  "groupSetting": {
    "displayName": "displayName-value",
    "templateId": "templateId-value",
    "values": [
      {
        "name": "name-value",
        "value": "value-value"
      }
    ]
  }
}
```
<span data-ttu-id="3acd5-134">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [groupSetting](../resources/groupsetting.md).</span><span class="sxs-lookup"><span data-stu-id="3acd5-134">In the request body, supply a JSON representation of [groupSetting](../resources/groupsetting.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="3acd5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3acd5-135">Response</span></span>

<span data-ttu-id="3acd5-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3acd5-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 238

{
  "groupSetting": {
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
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create groupsetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->