---
title: 'reportRoot: getTeamsUserActivityUserDetail'
description: Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.
localization_priority: Priority
ms.prod: reports
ms.openlocfilehash: b968a5cb17ad588ffea678b05a5752e226b5eb5d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960710"
---
# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="6e04d-103">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="6e04d-103">reportRoot: getTeamsUserActivityUserDetail</span></span>

<span data-ttu-id="6e04d-104">Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="6e04d-104">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="6e04d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="6e04d-105">Permissions</span></span>

<span data-ttu-id="6e04d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e04d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6e04d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e04d-108">Permission type</span></span>                        | <span data-ttu-id="6e04d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e04d-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="6e04d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e04d-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="6e04d-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6e04d-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="6e04d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e04d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6e04d-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6e04d-113">Not supported.</span></span>                           |
| <span data-ttu-id="6e04d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e04d-114">Application</span></span>                            | <span data-ttu-id="6e04d-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6e04d-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="6e04d-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e04d-116">HTTP request</span></span>

<!-- { "blockType": "samples" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='{period_value}')
GET /reports/getTeamsUserActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="6e04d-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="6e04d-117">Function parameters</span></span>

<span data-ttu-id="6e04d-118">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="6e04d-118">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="6e04d-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6e04d-119">Parameter</span></span> | <span data-ttu-id="6e04d-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e04d-120">Type</span></span>   | <span data-ttu-id="6e04d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e04d-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="6e04d-122">period</span><span class="sxs-lookup"><span data-stu-id="6e04d-122">period</span></span>    | <span data-ttu-id="6e04d-123">cadena</span><span class="sxs-lookup"><span data-stu-id="6e04d-123">string</span></span> | <span data-ttu-id="6e04d-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6e04d-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="6e04d-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="6e04d-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="6e04d-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6e04d-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="6e04d-127">date</span><span class="sxs-lookup"><span data-stu-id="6e04d-127">date</span></span>      | <span data-ttu-id="6e04d-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="6e04d-128">Date</span></span>   | <span data-ttu-id="6e04d-129">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="6e04d-129">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="6e04d-130">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="6e04d-130">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="6e04d-131">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="6e04d-131">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="6e04d-132">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="6e04d-132">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6e04d-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e04d-133">Request headers</span></span>

| <span data-ttu-id="6e04d-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e04d-134">Name</span></span>          | <span data-ttu-id="6e04d-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e04d-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="6e04d-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e04d-136">Authorization</span></span> | <span data-ttu-id="6e04d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e04d-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="6e04d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e04d-139">Response</span></span>

<span data-ttu-id="6e04d-140">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="6e04d-140">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="6e04d-141">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e04d-141">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="6e04d-142">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="6e04d-142">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="6e04d-143">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="6e04d-143">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="6e04d-144">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="6e04d-144">Report Refresh Date</span></span>
- <span data-ttu-id="6e04d-145">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="6e04d-145">User Principal Name</span></span>
- <span data-ttu-id="6e04d-146">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="6e04d-146">Last Activity Date</span></span>
- <span data-ttu-id="6e04d-147">Eliminado</span><span class="sxs-lookup"><span data-stu-id="6e04d-147">Is Deleted</span></span>
- <span data-ttu-id="6e04d-148">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="6e04d-148">Deleted Date</span></span>
- <span data-ttu-id="6e04d-149">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="6e04d-149">Assigned Products</span></span>
- <span data-ttu-id="6e04d-150">Recuento de mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="6e04d-150">Team Chat Message Count</span></span>
- <span data-ttu-id="6e04d-151">Recuento de mensajes de chat privado</span><span class="sxs-lookup"><span data-stu-id="6e04d-151">Private Chat Message Count</span></span>
- <span data-ttu-id="6e04d-152">Recuento de llamadas</span><span class="sxs-lookup"><span data-stu-id="6e04d-152">Call Count</span></span>
- <span data-ttu-id="6e04d-153">Recuento de reuniones</span><span class="sxs-lookup"><span data-stu-id="6e04d-153">Meeting Count</span></span>
- <span data-ttu-id="6e04d-154">Tiene otra acción</span><span class="sxs-lookup"><span data-stu-id="6e04d-154">Has Other Action</span></span>
- <span data-ttu-id="6e04d-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="6e04d-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="6e04d-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e04d-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="6e04d-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e04d-157">Request</span></span>

<span data-ttu-id="6e04d-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e04d-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="6e04d-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e04d-159">Response</span></span>

<span data-ttu-id="6e04d-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e04d-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="6e04d-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e04d-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```
