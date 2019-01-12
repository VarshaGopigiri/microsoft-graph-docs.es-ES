---
title: Crear una configuración de Active directory
description: Utilice esta API para crear una nueva configuración, en función de las plantillas disponibles en directorySettingTemplates. Esta configuración puede ser en el nivel de inquilino o en un nivel de objeto (actualmente únicamente para los grupos). La solicitud de creación debe proporcionar settingValues para toda la configuración definida en la plantilla. Para la configuración específica de grupo, se puede establecer sólo la configuración que rigen si los miembros de un grupo pueden invitar a los usuarios invitados. Una vez que esté disponible la capacidad de agregar los usuarios invitados a un grupo que rige este comportamiento.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6754e8e4210da0161a6f0cd790dc355e4788e121
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921769"
---
# <a name="create-a-directory-setting"></a><span data-ttu-id="1cad7-107">Crear una configuración de Active directory</span><span class="sxs-lookup"><span data-stu-id="1cad7-107">Create a directory setting</span></span>

> <span data-ttu-id="1cad7-108">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1cad7-108">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1cad7-109">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1cad7-109">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1cad7-110">Utilice esta API para crear una nueva configuración, en función de las plantillas disponibles en directorySettingTemplates.</span><span class="sxs-lookup"><span data-stu-id="1cad7-110">Use this API to create a new setting, based on the templates available in directorySettingTemplates.</span></span> <span data-ttu-id="1cad7-111">Esta configuración puede ser en el nivel de inquilino o en un nivel de objeto (actualmente únicamente para los grupos).</span><span class="sxs-lookup"><span data-stu-id="1cad7-111">These settings can be at the tenant-level or at an object level (currently only for groups).</span></span> <span data-ttu-id="1cad7-112">La solicitud de creación debe proporcionar settingValues para toda la configuración definida en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="1cad7-112">The creation request must provide settingValues for all the settings defined in the template.</span></span> <span data-ttu-id="1cad7-113">Para la configuración específica de grupo, se puede establecer sólo la configuración que rigen si los miembros de un grupo pueden invitar a los usuarios invitados.</span><span class="sxs-lookup"><span data-stu-id="1cad7-113">For group-specific settings, only the setting governing whether members of a group can invite guest users can be set.</span></span> <span data-ttu-id="1cad7-114">Una vez que esté disponible la capacidad de agregar los usuarios invitados a un grupo que rige este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="1cad7-114">This will govern this behavior once the ability to add guest users to a group is generally available.</span></span>

> <span data-ttu-id="1cad7-115">**Nota**: la versión de /beta de esta API es sólo se aplica a los grupos.</span><span class="sxs-lookup"><span data-stu-id="1cad7-115">**Note**: The /beta version of this API is only applies to groups.</span></span> <span data-ttu-id="1cad7-116">Se ha cambiado la versión /v1.0 de esta API para *crear groupSettings*.</span><span class="sxs-lookup"><span data-stu-id="1cad7-116">The /v1.0 version of this API has been renamed to *Create groupSettings*.</span></span>

<span data-ttu-id="1cad7-117">Para obtener una lista de plantillas y las propiedades que se admiten en la versión beta, utilice una [consulta de directorySettingTemplate](https://developer.microsoft.com/graph/graph-explorer?request=directorySettingTemplates&version=beta).</span><span class="sxs-lookup"><span data-stu-id="1cad7-117">For a list of templates and the properties they support in beta, use a [directorySettingTemplate query](https://developer.microsoft.com/graph/graph-explorer?request=directorySettingTemplates&version=beta).</span></span> <span data-ttu-id="1cad7-118">(Para los extremos de v1.0, llamada [groupSettingTemplates](https://developer.microsoft.com/graph/graph-explorer?request=groupSettingTemplates&version=v1.0)).</span><span class="sxs-lookup"><span data-stu-id="1cad7-118">(For v1.0 endpoints, call [groupSettingTemplates](https://developer.microsoft.com/graph/graph-explorer?request=groupSettingTemplates&version=v1.0).)</span></span>


## <a name="permissions"></a><span data-ttu-id="1cad7-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="1cad7-119">Permissions</span></span>
<span data-ttu-id="1cad7-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1cad7-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1cad7-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1cad7-122">Permission type</span></span>      | <span data-ttu-id="1cad7-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1cad7-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1cad7-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1cad7-124">Delegated (work or school account)</span></span> | <span data-ttu-id="1cad7-125">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="1cad7-125">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="1cad7-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1cad7-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1cad7-127">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1cad7-127">Not supported.</span></span>    |
|<span data-ttu-id="1cad7-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1cad7-128">Application</span></span> | <span data-ttu-id="1cad7-129">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1cad7-129">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1cad7-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1cad7-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /settings
POST /groups/{id}/settings
```
## <a name="request-headers"></a><span data-ttu-id="1cad7-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1cad7-131">Request headers</span></span>
| <span data-ttu-id="1cad7-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="1cad7-132">Name</span></span>       | <span data-ttu-id="1cad7-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cad7-133">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1cad7-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="1cad7-134">Authorization</span></span>  | <span data-ttu-id="1cad7-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1cad7-p107">Bearer {token}. Required.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1cad7-137">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1cad7-137">Request body</span></span>
<span data-ttu-id="1cad7-138">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="1cad7-138">In the request body, supply a JSON representation of [directorySetting](../resources/directorysetting.md) object.</span></span>  <span data-ttu-id="1cad7-139">Sin embargo, el nombre para mostrar para la configuración se establecerá en función en el nombre de la plantilla de configuración que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="1cad7-139">However, the display name for the setting will be set based on the referenced settings template name.</span></span>

## <a name="response"></a><span data-ttu-id="1cad7-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cad7-140">Response</span></span>

<span data-ttu-id="1cad7-141">Si tiene éxito, este método devuelve `201 Created` objeto de código y [establecer](../resources/directorysetting.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1cad7-141">If successful, this method returns `201 Created` response code and [directorySetting](../resources/directorysetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1cad7-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1cad7-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1cad7-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1cad7-143">Request</span></span>
<span data-ttu-id="1cad7-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1cad7-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directorysetting_from_settings"
}-->
```http
POST https://graph.microsoft.com/beta/settings
Content-type: application/json
Content-length: 222

{
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
<span data-ttu-id="1cad7-145">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="1cad7-145">In the request body, supply a JSON representation of [directorySetting](../resources/directorysetting.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="1cad7-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1cad7-146">Response</span></span>
<span data-ttu-id="1cad7-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1cad7-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySetting"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
    "@odata.context": "https://graph.microsoft.com/stagingbeta/$metadata#settings/$entity",
    "id": "id-value",
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

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directorySetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
