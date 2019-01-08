---
author: daspek
ms.author: dspektor
ms.date: 10/06/2017
title: Obtener estadísticas de actividad de elemento por intervalo
ms.openlocfilehash: 3b3c7139678715a11365f2551c318dcf66e68e7a
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748195"
---
# <a name="get-item-activity-stats-by-interval"></a><span data-ttu-id="8c5f4-102">Obtener estadísticas de actividad de elemento por intervalo</span><span class="sxs-lookup"><span data-stu-id="8c5f4-102">Get item activity stats by interval</span></span>

> <span data-ttu-id="8c5f4-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c5f4-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8c5f4-105">Obtener [itemActivityStats][] para las actividades que tuvieron lugar en este recurso dentro del intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-105">Get [itemActivityStats][] for the activities that took place under this resource within the specified time interval.</span></span>

><span data-ttu-id="8c5f4-106">**Nota:** El recurso **itemAnalytics** aún no está disponible en todas las [implementaciones nacionales](/graph/deployments).</span><span class="sxs-lookup"><span data-stu-id="8c5f4-106">**Note:** The **itemAnalytics** resource is not yet available in all [national deployments](/graph/deployments).</span></span>

<span data-ttu-id="8c5f4-107">Agregados de análisis no es posible que esté disponibles para todos los tipos de acción.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-107">Analytics aggregates might not be available for all action types.</span></span>

[itemActivityStats]: ../resources/itemactivitystat.md

## <a name="permissions"></a><span data-ttu-id="8c5f4-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="8c5f4-109">Permissions</span></span>

<span data-ttu-id="8c5f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c5f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8c5f4-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c5f4-112">Permission type</span></span>                        | <span data-ttu-id="8c5f4-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c5f4-113">Permissions (from least to most privileged)</span></span>
|:--------------------------------------|:-------------------------------------
|<span data-ttu-id="8c5f4-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c5f4-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="8c5f4-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c5f4-115">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>
|<span data-ttu-id="8c5f4-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c5f4-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8c5f4-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-117">Not supported.</span></span>
|<span data-ttu-id="8c5f4-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c5f4-118">Application</span></span>                            | <span data-ttu-id="8c5f4-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c5f4-119">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="8c5f4-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c5f4-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/getActivitiesByInterval(startDateTime='2017-01-01',endDateTime='2017-01-10',interval='day')
GET /sites/{site-id}/getActivitiesByInterval(startDateTime='2016',endDateTime='2017',interval='month')
GET /sites/{site-id}/lists/{list-id}/items/{item-id}/getActivitiesByInterval(startDateTime='2017-05-01',interval='week')
```

## <a name="function-parameters"></a><span data-ttu-id="8c5f4-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="8c5f4-121">Function parameters</span></span>

| <span data-ttu-id="8c5f4-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8c5f4-122">Parameter</span></span>      | <span data-ttu-id="8c5f4-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c5f4-123">Type</span></span>               | <span data-ttu-id="8c5f4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c5f4-124">Description</span></span>
|:---------------|:-------------------|:---------------------------------------
| <span data-ttu-id="8c5f4-125">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8c5f4-125">startDateTime</span></span>  | <span data-ttu-id="8c5f4-126">cadena (marca de tiempo)</span><span class="sxs-lookup"><span data-stu-id="8c5f4-126">string (timestamp)</span></span> | <span data-ttu-id="8c5f4-127">La hora de inicio a través del cual a las actividades de agregado.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-127">The start time over which to aggregate activities.</span></span>
| <span data-ttu-id="8c5f4-128">endDateTime</span><span class="sxs-lookup"><span data-stu-id="8c5f4-128">endDateTime</span></span>    | <span data-ttu-id="8c5f4-129">cadena (marca de tiempo)</span><span class="sxs-lookup"><span data-stu-id="8c5f4-129">string (timestamp)</span></span> | <span data-ttu-id="8c5f4-130">La hora de finalización a través del cual a las actividades de agregado.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-130">The end time over which to aggregate activities.</span></span>
| <span data-ttu-id="8c5f4-131">interval</span><span class="sxs-lookup"><span data-stu-id="8c5f4-131">interval</span></span>       | <span data-ttu-id="8c5f4-132">string</span><span class="sxs-lookup"><span data-stu-id="8c5f4-132">string</span></span>             | <span data-ttu-id="8c5f4-133">El intervalo de agregación.</span><span class="sxs-lookup"><span data-stu-id="8c5f4-133">The aggregation interval.</span></span>

## <a name="example"></a><span data-ttu-id="8c5f4-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c5f4-134">Example</span></span>

#### <a name="request"></a><span data-ttu-id="8c5f4-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c5f4-135">Request</span></span>

<!-- { "blockType": "request", "name": "get-activities-by-interval" } -->

```http
GET /drives/{drive-id}/items/{item-id}/getActivitiesByInterval(startDateTime='2017-01-01',endDateTime='2017-01-3',interval='day')
```

#### <a name="response"></a><span data-ttu-id="8c5f4-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c5f4-136">Response</span></span>

<!-- { "blockType": "response", "@type": "Collection(microsoft.graph.itemActivityStat)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "startDateTime": "2017-01-01T00:00:00.000Z",
            "endDateTime": "2017-01-02T00:00:00.000Z",
            "delete": {
                "actionCount": 1,
                "actorCount": 1
            },
            "access": {
                "actionCount": 5,
                "actorCount": 3
            }
        },
        {
            "startDateTime": "2017-01-02T00:00:00.000Z",
            "endDateTime": "2017-01-03T00:00:00.000Z",
            "edit": {
                "actionCount": 3,
                "actorCount": 1
            },
            "access": {
                "actionCount": 7,
                "actorCount": 6
            }
        }
    ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "BaseItem/Get activities by interval"
} -->
