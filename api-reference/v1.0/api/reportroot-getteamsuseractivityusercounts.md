---
title: 'reportRoot: getTeamsUserActivityUserCounts'
description: Obtener el número de usuarios de Microsoft Teams por tipo de actividad. Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos.
localization_priority: Normal
ms.openlocfilehash: 5db9ccb20d79e487b564487f528c7f90289123e0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831300"
---
# <a name="reportroot-getteamsuseractivityusercounts"></a><span data-ttu-id="5f006-104">reportRoot: getTeamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="5f006-104">reportRoot: getTeamsUserActivityUserCounts</span></span>

<span data-ttu-id="5f006-105">Obtener el número de usuarios de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="5f006-105">Get the number of Microsoft Teams users by activity type.</span></span> <span data-ttu-id="5f006-106">Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos.</span><span class="sxs-lookup"><span data-stu-id="5f006-106">The activity types are number of teams chat messages, private chat messages, calls, or meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="5f006-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="5f006-107">Permissions</span></span>

<span data-ttu-id="5f006-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5f006-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5f006-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5f006-110">Permission type</span></span>                        | <span data-ttu-id="5f006-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5f006-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5f006-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5f006-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="5f006-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5f006-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="5f006-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5f006-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5f006-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5f006-115">Not supported.</span></span>                           |
| <span data-ttu-id="5f006-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5f006-116">Application</span></span>                            | <span data-ttu-id="5f006-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5f006-117">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="5f006-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5f006-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="5f006-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="5f006-119">Function parameters</span></span>

<span data-ttu-id="5f006-120">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="5f006-120">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="5f006-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5f006-121">Parameter</span></span> | <span data-ttu-id="5f006-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f006-122">Type</span></span>   | <span data-ttu-id="5f006-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f006-123">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5f006-124">period</span><span class="sxs-lookup"><span data-stu-id="5f006-124">period</span></span>    | <span data-ttu-id="5f006-125">cadena</span><span class="sxs-lookup"><span data-stu-id="5f006-125">string</span></span> | <span data-ttu-id="5f006-126">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5f006-126">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5f006-127">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="5f006-127">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5f006-128">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5f006-128">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="5f006-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="5f006-129">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="5f006-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5f006-130">Request headers</span></span>

| <span data-ttu-id="5f006-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f006-131">Name</span></span>          | <span data-ttu-id="5f006-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f006-132">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5f006-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f006-133">Authorization</span></span> | <span data-ttu-id="5f006-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f006-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="5f006-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f006-136">Response</span></span>

<span data-ttu-id="5f006-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="5f006-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5f006-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f006-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5f006-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="5f006-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5f006-140">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="5f006-140">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="5f006-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="5f006-141">Report Refresh Date</span></span>
- <span data-ttu-id="5f006-142">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="5f006-142">Report Date</span></span>
- <span data-ttu-id="5f006-143">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="5f006-143">Team Chat Messages</span></span>
- <span data-ttu-id="5f006-144">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="5f006-144">Private Chat Messages</span></span>
- <span data-ttu-id="5f006-145">Llamadas</span><span class="sxs-lookup"><span data-stu-id="5f006-145">Calls</span></span>
- <span data-ttu-id="5f006-146">Reuniones</span><span class="sxs-lookup"><span data-stu-id="5f006-146">Meetings</span></span>
- <span data-ttu-id="5f006-147">Otras acciones</span><span class="sxs-lookup"><span data-stu-id="5f006-147">Other Actions</span></span>
- <span data-ttu-id="5f006-148">Período del informe</span><span class="sxs-lookup"><span data-stu-id="5f006-148">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="5f006-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5f006-149">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5f006-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5f006-150">Request</span></span>

<span data-ttu-id="5f006-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5f006-151">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="5f006-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5f006-152">Response</span></span>

<span data-ttu-id="5f006-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5f006-153">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="5f006-154">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="5f006-154">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Other Actions,Report Period
```
