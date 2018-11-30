---
title: 'reportRoot: getTeamsDeviceUsageUserDetail'
description: Obtenga información sobre el uso de los dispositivos de Microsoft Teams por usuario.
ms.openlocfilehash: 28b39c0bc93645e64d0de5b7131f1f4ea2a3f9c3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031660"
---
# <a name="reportroot-getteamsdeviceusageuserdetail"></a><span data-ttu-id="10007-103">reportRoot: getTeamsDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="10007-103">reportRoot: getTeamsDeviceUsageUserDetail</span></span>

<span data-ttu-id="10007-104">Obtenga información sobre el uso de los dispositivos de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="10007-104">Get details about Microsoft Teams device usage by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="10007-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="10007-105">Permissions</span></span>

<span data-ttu-id="10007-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="10007-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="10007-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="10007-108">Permission type</span></span>                        | <span data-ttu-id="10007-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="10007-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="10007-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="10007-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="10007-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="10007-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="10007-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="10007-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="10007-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="10007-113">Not supported.</span></span>                           |
| <span data-ttu-id="10007-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="10007-114">Application</span></span>                            | <span data-ttu-id="10007-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="10007-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="10007-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10007-116">HTTP request</span></span>

<!-- { "blockType": "samples" } -->

```http
GET /reports/getTeamsDeviceUsageUserDetail(period='{period_value}')
GET /reports/getTeamsDeviceUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="10007-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="10007-117">Function parameters</span></span>

<span data-ttu-id="10007-118">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="10007-118">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="10007-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="10007-119">Parameter</span></span> | <span data-ttu-id="10007-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="10007-120">Type</span></span>   | <span data-ttu-id="10007-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="10007-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="10007-122">period</span><span class="sxs-lookup"><span data-stu-id="10007-122">period</span></span>    | <span data-ttu-id="10007-123">cadena</span><span class="sxs-lookup"><span data-stu-id="10007-123">string</span></span> | <span data-ttu-id="10007-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="10007-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="10007-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="10007-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="10007-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="10007-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="10007-127">date</span><span class="sxs-lookup"><span data-stu-id="10007-127">date</span></span>      | <span data-ttu-id="10007-128">Fecha</span><span class="sxs-lookup"><span data-stu-id="10007-128">Date</span></span>   | <span data-ttu-id="10007-129">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="10007-129">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="10007-130">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="10007-130">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="10007-131">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="10007-131">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="10007-132">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="10007-132">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="10007-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10007-133">Request headers</span></span>

| <span data-ttu-id="10007-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="10007-134">Name</span></span>          | <span data-ttu-id="10007-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="10007-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="10007-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="10007-136">Authorization</span></span> | <span data-ttu-id="10007-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="10007-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="10007-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10007-139">Response</span></span>

<span data-ttu-id="10007-140">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="10007-140">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="10007-141">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10007-141">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="10007-142">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="10007-142">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="10007-143">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="10007-143">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="10007-144">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="10007-144">Report Refresh Date</span></span>
- <span data-ttu-id="10007-145">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="10007-145">User Principal Name</span></span>
- <span data-ttu-id="10007-146">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="10007-146">Last Activity Date</span></span>
- <span data-ttu-id="10007-147">Eliminado</span><span class="sxs-lookup"><span data-stu-id="10007-147">Is Deleted</span></span>
- <span data-ttu-id="10007-148">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="10007-148">Deleted Date</span></span>
- <span data-ttu-id="10007-149">Web usada</span><span class="sxs-lookup"><span data-stu-id="10007-149">Used Web</span></span>
- <span data-ttu-id="10007-150">Windows Phone usado</span><span class="sxs-lookup"><span data-stu-id="10007-150">Used Windows Phone</span></span>
- <span data-ttu-id="10007-151">iOS usado</span><span class="sxs-lookup"><span data-stu-id="10007-151">Used iOS</span></span>
- <span data-ttu-id="10007-152">Mac usado</span><span class="sxs-lookup"><span data-stu-id="10007-152">Used Mac</span></span>
- <span data-ttu-id="10007-153">Teléfono Android usado</span><span class="sxs-lookup"><span data-stu-id="10007-153">Used Android Phone</span></span>
- <span data-ttu-id="10007-154">Windows usado</span><span class="sxs-lookup"><span data-stu-id="10007-154">Used Windows</span></span>
- <span data-ttu-id="10007-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="10007-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="10007-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10007-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="10007-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10007-157">Request</span></span>

<span data-ttu-id="10007-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10007-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="10007-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10007-159">Response</span></span>

<span data-ttu-id="10007-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10007-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="10007-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="10007-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Used Web,Used Windows Phone,Used iOS,Used Mac,Used Android Phone,Used Windows,Report Period
```
