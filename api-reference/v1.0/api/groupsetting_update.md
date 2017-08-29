# <a name="update-a-group-setting"></a><span data-ttu-id="05536-101">Actualizar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="05536-101">Update a group setting</span></span>

<span data-ttu-id="05536-102">Actualiza las propiedades de un objeto de configuración de grupo específico.</span><span class="sxs-lookup"><span data-stu-id="05536-102">Update the properties of a specific group setting object.</span></span>

## <a name="permissions"></a><span data-ttu-id="05536-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="05536-103">Permissions</span></span>

<span data-ttu-id="05536-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="05536-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="05536-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="05536-106">Permission type</span></span>      | <span data-ttu-id="05536-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="05536-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="05536-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="05536-108">Delegated (work or school account)</span></span> | <span data-ttu-id="05536-109">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="05536-109">Directory.ReadWrite.All or Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="05536-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="05536-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="05536-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="05536-111">Not supported.</span></span>    | 
|<span data-ttu-id="05536-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="05536-112">Application</span></span> | <span data-ttu-id="05536-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="05536-113">Directory.ReadWrite.All</span></span> | 


## <a name="http-request"></a><span data-ttu-id="05536-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="05536-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="05536-115">Actualiza una configuración para todo el inquilino o para un grupo específico.</span><span class="sxs-lookup"><span data-stu-id="05536-115">Update a tenant-wide or group specific setting.</span></span>

```http
PATCH /groupSettings/{id}
PATCH /groups/{id}/settings/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="05536-116">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="05536-116">Optional request headers</span></span>
| <span data-ttu-id="05536-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="05536-117">Name</span></span> | <span data-ttu-id="05536-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="05536-118">Description</span></span> |
|:-----------|:-----------|
| <span data-ttu-id="05536-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="05536-119">Authorization</span></span>  | <span data-ttu-id="05536-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="05536-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="05536-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="05536-122">Content-Type</span></span>  | <span data-ttu-id="05536-123">application/json</span><span class="sxs-lookup"><span data-stu-id="05536-123">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="05536-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="05536-124">Request body</span></span>
<span data-ttu-id="05536-125">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="05536-125">In the request body, supply the values for relevant fields that should be updated.</span></span> 

| <span data-ttu-id="05536-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="05536-126">Property</span></span> | <span data-ttu-id="05536-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="05536-127">Type</span></span> | <span data-ttu-id="05536-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="05536-128">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="05536-129">values</span><span class="sxs-lookup"><span data-stu-id="05536-129">values</span></span> | <span data-ttu-id="05536-130">settingValue</span><span class="sxs-lookup"><span data-stu-id="05536-130">settingValue</span></span> | <span data-ttu-id="05536-p103">Conjunto actualizado de valores.  NOTA: Debe proporcionar el conjunto de toda la colección. No puede actualizar un único conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="05536-p103">The updated set of values.  NOTE: You must supply the entire collection set. You cannot update a single set of values.</span></span> |

## <a name="response"></a><span data-ttu-id="05536-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05536-134">Response</span></span>

<span data-ttu-id="05536-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 OK` y el objeto [groupSetting](../resources/groupsetting.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="05536-135">If successful, this method returns a `204 OK` response code and updated [groupSetting](../resources/groupsetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="05536-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="05536-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="05536-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="05536-137">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "update_groupsetting"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groupSettings/{id}
Content-type: application/json
Content-length: 173

{
  "displayName": "displayName-value",
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
##### <a name="response"></a><span data-ttu-id="05536-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="05536-138">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupSetting"
} -->
```http
HTTP/1.1 204 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update groupSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->