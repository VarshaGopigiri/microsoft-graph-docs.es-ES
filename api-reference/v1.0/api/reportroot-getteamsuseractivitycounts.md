---
title: 'reportRoot: getTeamsUserActivityCounts'
description: Obtener el número de actividades de Microsoft Teams por tipo de actividad. Los tipos de actividad son mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipo.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: e854e02525c32d03550f604c3802ded3ca5dd559
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940508"
---
# <a name="reportroot-getteamsuseractivitycounts"></a><span data-ttu-id="3d318-104">reportRoot: getTeamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="3d318-104">reportRoot: getTeamsUserActivityCounts</span></span>

<span data-ttu-id="3d318-105">Obtener el número de actividades de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="3d318-105">Get the number of Microsoft Teams activities by activity type.</span></span> <span data-ttu-id="3d318-106">Los tipos de actividad son mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipo.</span><span class="sxs-lookup"><span data-stu-id="3d318-106">The activity types are team chat messages, private chat messages, calls, and meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="3d318-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d318-107">Permissions</span></span>

<span data-ttu-id="3d318-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d318-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3d318-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d318-110">Permission type</span></span>                        | <span data-ttu-id="3d318-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d318-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3d318-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d318-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="3d318-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d318-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="3d318-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d318-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d318-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d318-115">Not supported.</span></span>                           |
| <span data-ttu-id="3d318-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d318-116">Application</span></span>                            | <span data-ttu-id="3d318-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d318-117">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3d318-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d318-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="3d318-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3d318-119">Function parameters</span></span>

<span data-ttu-id="3d318-120">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3d318-120">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="3d318-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3d318-121">Parameter</span></span> | <span data-ttu-id="3d318-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d318-122">Type</span></span>   | <span data-ttu-id="3d318-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d318-123">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3d318-124">period</span><span class="sxs-lookup"><span data-stu-id="3d318-124">period</span></span>    | <span data-ttu-id="3d318-125">cadena</span><span class="sxs-lookup"><span data-stu-id="3d318-125">string</span></span> | <span data-ttu-id="3d318-126">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d318-126">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3d318-127">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3d318-127">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3d318-128">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d318-128">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="3d318-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3d318-129">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="3d318-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d318-130">Request headers</span></span>

| <span data-ttu-id="3d318-131">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d318-131">Name</span></span>          | <span data-ttu-id="3d318-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d318-132">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="3d318-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d318-133">Authorization</span></span> | <span data-ttu-id="3d318-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d318-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="3d318-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d318-136">Response</span></span>

<span data-ttu-id="3d318-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3d318-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3d318-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d318-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3d318-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3d318-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3d318-140">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="3d318-140">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="3d318-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3d318-141">Report Refresh Date</span></span>
- <span data-ttu-id="3d318-142">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="3d318-142">Report Date</span></span>
- <span data-ttu-id="3d318-143">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="3d318-143">Team Chat Messages</span></span>
- <span data-ttu-id="3d318-144">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="3d318-144">Private Chat Messages</span></span>
- <span data-ttu-id="3d318-145">Llamadas</span><span class="sxs-lookup"><span data-stu-id="3d318-145">Calls</span></span>
- <span data-ttu-id="3d318-146">Reuniones</span><span class="sxs-lookup"><span data-stu-id="3d318-146">Meetings</span></span>
- <span data-ttu-id="3d318-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3d318-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="3d318-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d318-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3d318-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d318-149">Request</span></span>

<span data-ttu-id="3d318-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d318-150">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="3d318-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d318-151">Response</span></span>

<span data-ttu-id="3d318-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d318-152">The following is an example of the response.</span></span>

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
<span data-ttu-id="3d318-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d318-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Report Period
```
