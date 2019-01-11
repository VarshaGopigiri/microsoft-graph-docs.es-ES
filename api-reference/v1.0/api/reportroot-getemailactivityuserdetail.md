---
title: 'reportRoot: getEmailActivityUserDetail'
description: Obtiene información sobre las actividades de correo electrónico que realizaron los usuarios.
localization_priority: Priority
ms.openlocfilehash: 4919f6ab0ea9bccb895b8c325f96d2da92488416
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875155"
---
# <a name="reportroot-getemailactivityuserdetail"></a><span data-ttu-id="ef18e-103">reportRoot: getEmailActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="ef18e-103">reportRoot: getEmailActivityUserDetail</span></span>

<span data-ttu-id="ef18e-104">Obtiene información sobre las actividades de correo electrónico que realizaron los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ef18e-104">Get details about email activity users have performed.</span></span>

> <span data-ttu-id="ef18e-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividades de correo electrónico](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).</span><span class="sxs-lookup"><span data-stu-id="ef18e-105">**Note:** For details about different report views and names, see [Office 365 Reports - Email Activity](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).</span></span>

## <a name="permissions"></a><span data-ttu-id="ef18e-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ef18e-106">Permissions</span></span>

<span data-ttu-id="ef18e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ef18e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ef18e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ef18e-109">Permission type</span></span>                        | <span data-ttu-id="ef18e-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ef18e-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ef18e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ef18e-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="ef18e-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ef18e-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ef18e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ef18e-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ef18e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ef18e-114">Not supported.</span></span>                           |
| <span data-ttu-id="ef18e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ef18e-115">Application</span></span>                            | <span data-ttu-id="ef18e-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ef18e-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ef18e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ef18e-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getEmailActivityUserDetail(period='{period_value}')
GET /reports/getEmailActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="ef18e-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ef18e-118">Function parameters</span></span>

<span data-ttu-id="ef18e-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ef18e-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="ef18e-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ef18e-120">Parameter</span></span> | <span data-ttu-id="ef18e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ef18e-121">Type</span></span>   | <span data-ttu-id="ef18e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef18e-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ef18e-123">period</span><span class="sxs-lookup"><span data-stu-id="ef18e-123">period</span></span>    | <span data-ttu-id="ef18e-124">cadena</span><span class="sxs-lookup"><span data-stu-id="ef18e-124">string</span></span> | <span data-ttu-id="ef18e-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ef18e-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ef18e-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ef18e-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ef18e-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ef18e-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="ef18e-128">date</span><span class="sxs-lookup"><span data-stu-id="ef18e-128">date</span></span>      | <span data-ttu-id="ef18e-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="ef18e-129">Date</span></span>   | <span data-ttu-id="ef18e-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="ef18e-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="ef18e-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="ef18e-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="ef18e-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="ef18e-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="ef18e-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="ef18e-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ef18e-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ef18e-134">Request headers</span></span>

| <span data-ttu-id="ef18e-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ef18e-135">Name</span></span>          | <span data-ttu-id="ef18e-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef18e-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ef18e-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="ef18e-137">Authorization</span></span> | <span data-ttu-id="ef18e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ef18e-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ef18e-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ef18e-140">If-None-Match</span></span> | <span data-ttu-id="ef18e-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ef18e-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ef18e-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ef18e-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ef18e-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef18e-143">Response</span></span>

<span data-ttu-id="ef18e-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ef18e-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ef18e-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef18e-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ef18e-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ef18e-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ef18e-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ef18e-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ef18e-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ef18e-148">Report Refresh Date</span></span>
- <span data-ttu-id="ef18e-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="ef18e-149">User Principal Name</span></span>
- <span data-ttu-id="ef18e-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="ef18e-150">Display Name</span></span>
- <span data-ttu-id="ef18e-151">Eliminado</span><span class="sxs-lookup"><span data-stu-id="ef18e-151">Is Deleted</span></span>
- <span data-ttu-id="ef18e-152">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="ef18e-152">Deleted Date</span></span>
- <span data-ttu-id="ef18e-153">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="ef18e-153">Last Activity Date</span></span>
- <span data-ttu-id="ef18e-154">Número de envíos</span><span class="sxs-lookup"><span data-stu-id="ef18e-154">Send Count</span></span>
- <span data-ttu-id="ef18e-155">Número de recepciones</span><span class="sxs-lookup"><span data-stu-id="ef18e-155">Receive Count</span></span>
- <span data-ttu-id="ef18e-156">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="ef18e-156">Read Count</span></span>
- <span data-ttu-id="ef18e-157">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="ef18e-157">Assigned Products</span></span>
- <span data-ttu-id="ef18e-158">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ef18e-158">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="ef18e-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ef18e-159">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ef18e-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ef18e-160">Request</span></span>

<span data-ttu-id="ef18e-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ef18e-161">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ef18e-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ef18e-162">Response</span></span>

<span data-ttu-id="ef18e-163">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ef18e-163">The following is an example of the response.</span></span>

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

<span data-ttu-id="ef18e-164">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef18e-164">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Last Activity Date,Send Count,Receive Count,Read Count,Assigned Products,Report Period
```
