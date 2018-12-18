---
title: List groupSettingTemplates
description: Las plantillas de configuración de grupo representan un conjunto de plantillas desde las que se pueden crear configuraciones de grupos para usarlas en un inquilino.  Con esta operación se recupera la lista de objetos groupSettingTemplates disponibles.
author: dkershaw10
ms.openlocfilehash: b47613093d8efa7fac99a313fff45d846d7a5073
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359363"
---
# <a name="list-groupsettingtemplates"></a><span data-ttu-id="64db8-104">List groupSettingTemplates</span><span class="sxs-lookup"><span data-stu-id="64db8-104">List groupSettingTemplates</span></span>

<span data-ttu-id="64db8-p102">Las plantillas de configuración de grupo representan un conjunto de plantillas desde las que se pueden crear configuraciones de grupos para usarlas en un inquilino.  Con esta operación se recupera la lista de objetos groupSettingTemplates disponibles.</span><span class="sxs-lookup"><span data-stu-id="64db8-p102">Group setting templates represents a set of templates  from which group settings may be created and used within a tenant.  This operation retrieves the list of available groupSettingTemplates objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="64db8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="64db8-107">Permissions</span></span>

<span data-ttu-id="64db8-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64db8-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="64db8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64db8-110">Permission type</span></span>      | <span data-ttu-id="64db8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64db8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64db8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64db8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="64db8-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="64db8-113">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="64db8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64db8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="64db8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="64db8-115">Not supported.</span></span>    |
|<span data-ttu-id="64db8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64db8-116">Application</span></span> | <span data-ttu-id="64db8-117">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="64db8-117">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="64db8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64db8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupSettingTemplates
```
## <a name="optional-query-parameters"></a><span data-ttu-id="64db8-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="64db8-119">Optional query parameters</span></span>
<span data-ttu-id="64db8-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64db8-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="64db8-121">**Nota:** No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="64db8-121">**Note:** $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="64db8-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64db8-122">Request headers</span></span>
| <span data-ttu-id="64db8-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="64db8-123">Name</span></span> | <span data-ttu-id="64db8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="64db8-124">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="64db8-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="64db8-125">Authorization</span></span>  | <span data-ttu-id="64db8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64db8-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="64db8-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64db8-128">Request body</span></span>
<span data-ttu-id="64db8-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="64db8-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="64db8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64db8-130">Response</span></span>

<span data-ttu-id="64db8-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [groupSettingTemplate](../resources/groupsettingtemplate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64db8-131">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/groupsettingtemplate.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="64db8-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64db8-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="64db8-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64db8-133">Request</span></span>
<!-- {
  "blockType": "request",
  "name": "get_groupsettingtemplates"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettingTemplates
```
##### <a name="response"></a><span data-ttu-id="64db8-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64db8-134">Response</span></span>

<span data-ttu-id="64db8-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64db8-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
                    ]
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