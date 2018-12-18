---
title: Crear una configuración de Active directory en grupos
description: Utilice esta API para crear una nueva configuración de Active directory para el grupo.
author: dkershaw10
ms.openlocfilehash: 2e400babc809bdc8d9277cad1bd41b8b714e4e92
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27358999"
---
# <a name="create-a-directory-setting-on-groups"></a><span data-ttu-id="33971-103">Crear una configuración de Active directory en grupos</span><span class="sxs-lookup"><span data-stu-id="33971-103">Create a directory setting on groups</span></span>

> <span data-ttu-id="33971-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33971-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33971-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33971-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="33971-106">Utilice esta API para crear una nueva configuración de Active directory para el grupo.</span><span class="sxs-lookup"><span data-stu-id="33971-106">Use this API to create a new directory setting for the group.</span></span>
## <a name="permissions"></a><span data-ttu-id="33971-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="33971-107">Permissions</span></span>
<span data-ttu-id="33971-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33971-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33971-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33971-110">Permission type</span></span>      | <span data-ttu-id="33971-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33971-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="33971-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33971-112">Delegated (work or school account)</span></span> | <span data-ttu-id="33971-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="33971-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="33971-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33971-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="33971-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="33971-115">Not supported.</span></span>    |
|<span data-ttu-id="33971-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33971-116">Application</span></span> | <span data-ttu-id="33971-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="33971-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="33971-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33971-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/settings
```
## <a name="request-headers"></a><span data-ttu-id="33971-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33971-119">Request headers</span></span>
| <span data-ttu-id="33971-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="33971-120">Name</span></span>       | <span data-ttu-id="33971-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="33971-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="33971-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="33971-122">Authorization</span></span>  | <span data-ttu-id="33971-123">Bearer <token>.</span><span class="sxs-lookup"><span data-stu-id="33971-123">Bearer <token>.</span></span> <span data-ttu-id="33971-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="33971-124">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="33971-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33971-125">Request body</span></span>
<span data-ttu-id="33971-126">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="33971-126">In the request body, supply a JSON representation of [directorySetting](../resources/directorysetting.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="33971-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33971-127">Response</span></span>

<span data-ttu-id="33971-128">Si tiene éxito, este método devuelve `201 Created` objeto de código y [establecer](../resources/directorysetting.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33971-128">If successful, this method returns `201 Created` response code and [directorySetting](../resources/directorysetting.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33971-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33971-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="33971-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33971-130">Request</span></span>
<span data-ttu-id="33971-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33971-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_directorysetting_from_group"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/settings
Content-type: application/json
Content-length: 222

{
  "directorySetting": {
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
<span data-ttu-id="33971-132">En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [establecer](../resources/directorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="33971-132">In the request body, supply a JSON representation of [directorySetting](../resources/directorysetting.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="33971-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33971-133">Response</span></span>
<span data-ttu-id="33971-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="33971-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "directorySetting": {
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