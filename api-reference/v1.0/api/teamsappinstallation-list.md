---
title: Lista de aplicaciones en el equipo
description: Recuperar la lista de aplicaciones que se instalan en el equipo especificado.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 3289f7abc80e20a11d38c9ab35a9961981b81dd1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985735"
---
# <a name="list-apps-in-team"></a><span data-ttu-id="2280f-103">Lista de aplicaciones en el equipo</span><span class="sxs-lookup"><span data-stu-id="2280f-103">List apps in team</span></span>



<span data-ttu-id="2280f-104">Recuperar la lista de [aplicaciones instalado](../resources/teamsappinstallation.md) en el [equipo](../resources/team.md)de especificado.</span><span class="sxs-lookup"><span data-stu-id="2280f-104">Retrieve the list of [apps installed](../resources/teamsappinstallation.md) in the specified [team](../resources/team.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="2280f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2280f-105">Permissions</span></span>

<span data-ttu-id="2280f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2280f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2280f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2280f-108">Permission type</span></span>      | <span data-ttu-id="2280f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2280f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2280f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2280f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2280f-111">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2280f-111">Group.Read.All, Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="2280f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2280f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2280f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2280f-113">Not supported.</span></span>    |
|<span data-ttu-id="2280f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2280f-114">Application</span></span> | <span data-ttu-id="2280f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2280f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2280f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2280f-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /teams/{id}/installedApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="2280f-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2280f-117">Optional query parameters</span></span>

<span data-ttu-id="2280f-118">Este método admite la $filter, $select, y $expanda [Parámetros de consulta de OData](/graph/query-parameters) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2280f-118">This method supports the $filter, $select, and $expand [OData Query Parameters](/graph/query-parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2280f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2280f-119">Request headers</span></span>

| <span data-ttu-id="2280f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2280f-120">Header</span></span>       | <span data-ttu-id="2280f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2280f-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2280f-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2280f-122">Authorization</span></span>  | <span data-ttu-id="2280f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2280f-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2280f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2280f-125">Request body</span></span>

<span data-ttu-id="2280f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2280f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2280f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2280f-127">Response</span></span>

<span data-ttu-id="2280f-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y la colección de objetos de [teamsApp](../resources/teamsapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2280f-128">If successful, this method returns a `200 OK` response code and collection of [teamsApp](../resources/teamsapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2280f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2280f-129">Example</span></span>

### <a name="request"></a><span data-ttu-id="2280f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2280f-130">Request</span></span>

<span data-ttu-id="2280f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2280f-131">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->

```http
GET /teams/{id}/installedApps
```

### <a name="response"></a><span data-ttu-id="2280f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2280f-132">Response</span></span>

<span data-ttu-id="2280f-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2280f-133">The following is an example of the response.</span></span>
><span data-ttu-id="2280f-134">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2280f-134">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2280f-135">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2280f-135">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

## <a name="example----getting-the-names-of-the-installed-apps"></a><span data-ttu-id="2280f-136">Ejemplo: obtener los nombres de las aplicaciones instaladas</span><span class="sxs-lookup"><span data-stu-id="2280f-136">Example -- getting the names of the installed apps</span></span>

### <a name="request"></a><span data-ttu-id="2280f-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2280f-137">Request</span></span>

<span data-ttu-id="2280f-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2280f-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->

```http
GET https://graph.microsoft.com/v1.0/teams/{id}/installedApps?$expand=teamsAppDefinition
```

### <a name="response"></a><span data-ttu-id="2280f-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2280f-139">Response</span></span>

<span data-ttu-id="2280f-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2280f-140">The following is an example of the response.</span></span>

><span data-ttu-id="2280f-141">**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="2280f-141">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="2280f-142">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2280f-142">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
    "value": [
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZDgyMGVjZC1kZWYyLTQyOTctYWRhZC03ODA1NmNkZTdjNzg=",
            "teamsAppDefinition": {
                "id": "MGQ4MjBlY2QtZGVmMi00Mjk3LWFkYWQtNzgwNTZjZGU3Yzc4IyMxLjAuMA==",
                "teamsAppId": "0d820ecd-def2-4297-adad-78056cde7c78",
                "displayName": "OneNote",
                "version": "1.0.0"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMwZmQ5MjVhMC0zNTdmLTRkMjUtODQ1Ni1iMzAyMmFhYTQxYTk=",
            "teamsAppDefinition": {
                "id": "MGZkOTI1YTAtMzU3Zi00ZDI1LTg0NTYtYjMwMjJhYWE0MWE5IyMxLjc=",
                "teamsAppId": "0fd925a0-357f-4d25-8456-b3022aaa41a9",
                "displayName": "SurveyMonkey",
                "version": "1.7"
            }
        },
        {
            "id": "NjRiOWM3NDYtYjE1NS00MDQyLThkNDctOTQxYmQzODE2ODFiIyMyYTUyNzcwMy0xZjZmLTQ1NTktYTMzMi1kOGE3ZDI4OGNkODg=",
            "teamsAppDefinition": {
                "id": "MmE1Mjc3MDMtMWY2Zi00NTU5LWEzMzItZDhhN2QyODhjZDg4IyMxLjA=",
                "teamsAppId": "2a527703-1f6f-4559-a332-d8a7d288cd88",
                "displayName": "SharePoint",
                "version": "1.0"
            }
        }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
