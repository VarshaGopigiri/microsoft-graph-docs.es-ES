---
title: 'reportRoot: getTeamsUserActivityUserDetail'
description: Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.
ms.openlocfilehash: 6905f9a18627a9ebf3c63ca92c111d1518564a3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030572"
---
# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="21646-103">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="21646-103">reportRoot: getTeamsUserActivityUserDetail</span></span>

<span data-ttu-id="21646-104">Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="21646-104">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="21646-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="21646-105">Permissions</span></span>

<span data-ttu-id="21646-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="21646-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="21646-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="21646-108">Permission type</span></span>                        | <span data-ttu-id="21646-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="21646-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="21646-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="21646-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="21646-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="21646-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="21646-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="21646-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="21646-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="21646-113">Not supported.</span></span>                           |
| <span data-ttu-id="21646-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="21646-114">Application</span></span>                            | <span data-ttu-id="21646-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="21646-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="21646-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="21646-116">HTTP request</span></span>

<!-- { "blockType": "samples" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='{period_value}')
GET /reports/getTeamsUserActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="21646-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="21646-117">Function parameters</span></span>

<span data-ttu-id="21646-118">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="21646-118">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="21646-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="21646-119">Parameter</span></span> | <span data-ttu-id="21646-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="21646-120">Type</span></span>   | <span data-ttu-id="21646-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="21646-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="21646-122">period</span><span class="sxs-lookup"><span data-stu-id="21646-122">period</span></span>    | <span data-ttu-id="21646-123">cadena</span><span class="sxs-lookup"><span data-stu-id="21646-123">string</span></span> | <span data-ttu-id="21646-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="21646-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="21646-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="21646-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="21646-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="21646-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="21646-127">date</span><span class="sxs-lookup"><span data-stu-id="21646-127">date</span></span>      | <span data-ttu-id="21646-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="21646-128">Date</span></span>   | <span data-ttu-id="21646-129">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="21646-129">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="21646-130">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="21646-130">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="21646-131">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="21646-131">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="21646-132">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="21646-132">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="21646-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="21646-133">Request headers</span></span>

| <span data-ttu-id="21646-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="21646-134">Name</span></span>          | <span data-ttu-id="21646-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="21646-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="21646-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="21646-136">Authorization</span></span> | <span data-ttu-id="21646-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="21646-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="21646-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21646-139">Response</span></span>

<span data-ttu-id="21646-140">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="21646-140">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="21646-141">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21646-141">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="21646-142">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="21646-142">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="21646-143">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="21646-143">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="21646-144">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="21646-144">Report Refresh Date</span></span>
- <span data-ttu-id="21646-145">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="21646-145">User Principal Name</span></span>
- <span data-ttu-id="21646-146">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="21646-146">Last Activity Date</span></span>
- <span data-ttu-id="21646-147">Eliminado</span><span class="sxs-lookup"><span data-stu-id="21646-147">Is Deleted</span></span>
- <span data-ttu-id="21646-148">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="21646-148">Deleted Date</span></span>
- <span data-ttu-id="21646-149">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="21646-149">Assigned Products</span></span>
- <span data-ttu-id="21646-150">Recuento de mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="21646-150">Team Chat Message Count</span></span>
- <span data-ttu-id="21646-151">Recuento de mensajes de chat privado</span><span class="sxs-lookup"><span data-stu-id="21646-151">Private Chat Message Count</span></span>
- <span data-ttu-id="21646-152">Recuento de llamadas</span><span class="sxs-lookup"><span data-stu-id="21646-152">Call Count</span></span>
- <span data-ttu-id="21646-153">Recuento de reuniones</span><span class="sxs-lookup"><span data-stu-id="21646-153">Meeting Count</span></span>
- <span data-ttu-id="21646-154">Tiene otra acción</span><span class="sxs-lookup"><span data-stu-id="21646-154">Has Other Action</span></span>
- <span data-ttu-id="21646-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="21646-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="21646-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21646-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="21646-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="21646-157">Request</span></span>

<span data-ttu-id="21646-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="21646-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="21646-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="21646-159">Response</span></span>

<span data-ttu-id="21646-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="21646-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="21646-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="21646-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```