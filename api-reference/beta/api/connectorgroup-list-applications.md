---
title: Aplicaciones de lista
description: Recuperar una lista de objetos de la aplicación asociada con la connectorGroup.
ms.openlocfilehash: 11d81454677b60e2402c4d1fe32aae5c974c1afc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086938"
---
# <a name="list-applications"></a><span data-ttu-id="775b7-103">Aplicaciones de lista</span><span class="sxs-lookup"><span data-stu-id="775b7-103">List applications</span></span>

> <span data-ttu-id="775b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="775b7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="775b7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="775b7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="775b7-106">Recuperar una lista de objetos de la aplicación asociada con la connectorGroup.</span><span class="sxs-lookup"><span data-stu-id="775b7-106">Retrieve a list of application objects associated with the connectorGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="775b7-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="775b7-107">Permissions</span></span>
<span data-ttu-id="775b7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="775b7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="775b7-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="775b7-110">Permission type</span></span>      | <span data-ttu-id="775b7-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="775b7-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="775b7-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="775b7-112">Delegated (work or school account)</span></span> | <span data-ttu-id="775b7-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="775b7-113">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="775b7-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="775b7-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="775b7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="775b7-115">Not supported.</span></span>    |
|<span data-ttu-id="775b7-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="775b7-116">Application</span></span> | <span data-ttu-id="775b7-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="775b7-117">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="775b7-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="775b7-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /connectorGroups/{id}/applications
```
## <a name="optional-query-parameters"></a><span data-ttu-id="775b7-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="775b7-119">Optional query parameters</span></span>
<span data-ttu-id="775b7-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="775b7-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="775b7-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="775b7-121">Request headers</span></span>
| <span data-ttu-id="775b7-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="775b7-122">Name</span></span>      |<span data-ttu-id="775b7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="775b7-123">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="775b7-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="775b7-124">Authorization</span></span>  | <span data-ttu-id="775b7-125">Bearer.</span><span class="sxs-lookup"><span data-stu-id="775b7-125">Bearer.</span></span> <span data-ttu-id="775b7-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="775b7-126">Required</span></span>|

## <a name="request-body"></a><span data-ttu-id="775b7-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="775b7-127">Request body</span></span>
<span data-ttu-id="775b7-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="775b7-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="775b7-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="775b7-129">Response</span></span>

<span data-ttu-id="775b7-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [aplicación](../resources/application.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="775b7-130">If successful, this method returns a `200 OK` response code and collection of [application](../resources/application.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="775b7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="775b7-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="775b7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="775b7-132">Request</span></span>
<span data-ttu-id="775b7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="775b7-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_applications"
}-->
```http
GET https://graph.microsoft.com/{ver}/connectorGroups/{id}/applications
```
##### <a name="response"></a><span data-ttu-id="775b7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="775b7-134">Response</span></span>
<span data-ttu-id="775b7-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="775b7-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 420

{
  "value": [
    {
      "appId": "appId-value",
      "onPremisesPublishing": {
        "externalUrl": "externalUrl-value",
        "internalUrl": "internalUrl-value",
        "externalAuthenticationType": "externalAuthenticationType-value",
        "customDomainCertificate": "customDomainCertificate-value",
        "isTranslateHostHeaderEnabled": true,
        "isOnPremPublishingEnabled": true
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List applications",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->