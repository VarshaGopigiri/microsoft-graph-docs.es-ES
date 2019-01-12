---
title: Actualizar una configuración de grupo
description: Actualiza las propiedades de un objeto de configuración de grupo específico.
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 1ebea83f26bd3fcf54e530e80173c830fbde7ba8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941691"
---
# <a name="update-a-group-setting"></a><span data-ttu-id="33663-103">Actualizar una configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="33663-103">Update a group setting</span></span>

<span data-ttu-id="33663-104">Actualiza las propiedades de un objeto de configuración de grupo específico.</span><span class="sxs-lookup"><span data-stu-id="33663-104">Update the properties of a specific group setting object.</span></span>

## <a name="permissions"></a><span data-ttu-id="33663-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="33663-105">Permissions</span></span>

<span data-ttu-id="33663-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33663-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="33663-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33663-108">Permission type</span></span>      | <span data-ttu-id="33663-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33663-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="33663-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33663-110">Delegated (work or school account)</span></span> | <span data-ttu-id="33663-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="33663-111">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="33663-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33663-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="33663-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33663-113">Not supported.</span></span>    |
|<span data-ttu-id="33663-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33663-114">Application</span></span> | <span data-ttu-id="33663-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="33663-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="33663-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33663-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="33663-117">Actualiza una configuración para todo el inquilino o para un grupo específico.</span><span class="sxs-lookup"><span data-stu-id="33663-117">Update a tenant-wide or group specific setting.</span></span>

```http
PATCH /groupSettings/{id}
PATCH /groups/{id}/settings/{id}
```
## <a name="optional-request-headers"></a><span data-ttu-id="33663-118">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="33663-118">Optional request headers</span></span>
| <span data-ttu-id="33663-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="33663-119">Name</span></span> | <span data-ttu-id="33663-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="33663-120">Description</span></span> |
|:-----------|:-----------|
| <span data-ttu-id="33663-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="33663-121">Authorization</span></span>  | <span data-ttu-id="33663-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="33663-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="33663-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="33663-124">Content-Type</span></span>  | <span data-ttu-id="33663-125">application/json</span><span class="sxs-lookup"><span data-stu-id="33663-125">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="33663-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33663-126">Request body</span></span>
<span data-ttu-id="33663-127">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="33663-127">In the request body, supply the values for relevant fields that should be updated.</span></span> 

| <span data-ttu-id="33663-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33663-128">Property</span></span> | <span data-ttu-id="33663-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="33663-129">Type</span></span> | <span data-ttu-id="33663-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="33663-130">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="33663-131">values</span><span class="sxs-lookup"><span data-stu-id="33663-131">values</span></span> | <span data-ttu-id="33663-132">Colección de settingValue</span><span class="sxs-lookup"><span data-stu-id="33663-132">settingValue collection</span></span> | <span data-ttu-id="33663-p103">Conjunto actualizado de valores.  NOTA: Debe proporcionar el conjunto de toda la colección. No puede actualizar un único conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="33663-p103">The updated set of values.  NOTE: You must supply the entire collection set. You cannot update a single set of values.</span></span> |

## <a name="response"></a><span data-ttu-id="33663-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33663-136">Response</span></span>

<span data-ttu-id="33663-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="33663-137">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="33663-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33663-138">Example</span></span>
#### <a name="request"></a><span data-ttu-id="33663-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33663-139">Request</span></span>
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
      "name": "CustomBlockedWordsList",
      "value": ""
    },
    {
      "name": "EnableMSStandardBlockedWords",
      "value": "False"
    },
    {
      "name": "ClassificationDescriptions",
      "value": ""
    },
    {
      "name": "DefaultClassification",
      "value": ""
    },
    {
      "name": "PrefixSuffixNamingRequirement",
      "value": ""
    },
    {
      "name": "AllowGuestsToBeGroupOwner",
      "value": "False"
    },
    {
      "name": "AllowGuestsToAccessGroups",
      "value": "True"
    },
    {
      "name": "GuestUsageGuidelinesUrl",
      "value": ""
    },
    {
      "name": "GroupCreationAllowedGroupId",
      "value": "62e90394-69f5-4237-9190-012177145e10"
    },
    {
      "name": "AllowToAddGuests",
      "value": "True"
    },
    {
      "name": "UsageGuidelinesUrl",
      "value": ""
    },
    {
      "name": "ClassificationList",
      "value": ""
    },
    {
      "name": "EnableGroupCreation",
      "value": "True"
    }
  ]
}
```

#### <a name="response"></a><span data-ttu-id="33663-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33663-140">Response</span></span>

<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
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
