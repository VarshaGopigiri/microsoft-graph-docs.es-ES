---
title: Enumerar configuración de grupo
description: Recupera una lista de objetos de configuración de grupo.
author: dkershaw10
ms.openlocfilehash: 834e843ee470d559427775370ed723fe6dafaf5e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359643"
---
# <a name="list-group-settings"></a><span data-ttu-id="86205-103">Enumerar configuración de grupo</span><span class="sxs-lookup"><span data-stu-id="86205-103">List group settings</span></span>

<span data-ttu-id="86205-104">Recupera una lista de objetos de configuración de grupo.</span><span class="sxs-lookup"><span data-stu-id="86205-104">Retrieve a list of group setting objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="86205-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="86205-105">Permissions</span></span>

<span data-ttu-id="86205-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="86205-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="86205-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86205-108">Permission type</span></span>      | <span data-ttu-id="86205-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="86205-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="86205-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86205-110">Delegated (work or school account)</span></span> | <span data-ttu-id="86205-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="86205-111">Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="86205-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86205-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="86205-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86205-113">Not supported.</span></span>    |
|<span data-ttu-id="86205-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86205-114">Application</span></span> | <span data-ttu-id="86205-115">Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86205-115">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="86205-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86205-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="86205-117">Enumera la configuración de todo el inquilino o de un grupo.</span><span class="sxs-lookup"><span data-stu-id="86205-117">List tenant-wide or group settings.</span></span>

```http
GET /groupSettings
GET group/{id}/settings
```
## <a name="optional-query-parameters"></a><span data-ttu-id="86205-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="86205-118">Optional query parameters</span></span>
<span data-ttu-id="86205-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86205-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

> <span data-ttu-id="86205-120">Nota: No se admite $filter.</span><span class="sxs-lookup"><span data-stu-id="86205-120">Note: $filter is not supported.</span></span>

## <a name="request-headers"></a><span data-ttu-id="86205-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86205-121">Request headers</span></span>
| <span data-ttu-id="86205-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="86205-122">Name</span></span> | <span data-ttu-id="86205-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="86205-123">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="86205-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="86205-124">Authorization</span></span>  | <span data-ttu-id="86205-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="86205-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="86205-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86205-127">Request body</span></span>
<span data-ttu-id="86205-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="86205-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="86205-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86205-129">Response</span></span>

<span data-ttu-id="86205-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [groupSetting](../resources/groupsetting.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86205-130">If successful, this method returns a `200 OK` response code and collection of [groupSetting](../resources/groupsetting.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="86205-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86205-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="86205-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86205-132">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_groupsettings"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupSettings
```
##### <a name="response"></a><span data-ttu-id="86205-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86205-133">Response</span></span>

<span data-ttu-id="86205-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="86205-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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