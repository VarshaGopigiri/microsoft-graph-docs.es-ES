---
title: 'reportRoot: getYammerActivityUserDetail'
description: Obtiene información sobre las actividades de Yammer por usuario.
ms.openlocfilehash: 8dc1fd6ae92ce1f71915ba836f0f0f0662a5cd4c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031414"
---
# <a name="reportroot-getyammeractivityuserdetail"></a><span data-ttu-id="5c860-103">reportRoot: getYammerActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="5c860-103">reportRoot: getYammerActivityUserDetail</span></span>

<span data-ttu-id="5c860-104">Obtiene información sobre las actividades de Yammer por usuario.</span><span class="sxs-lookup"><span data-stu-id="5c860-104">Get details about Yammer activity by user.</span></span>

> <span data-ttu-id="5c860-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Yammer](https://support.office.com/client/Yammer-activity-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a).</span><span class="sxs-lookup"><span data-stu-id="5c860-105">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer Activity](https://support.office.com/client/Yammer-activity-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a).</span></span>

## <a name="permissions"></a><span data-ttu-id="5c860-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="5c860-106">Permissions</span></span>

<span data-ttu-id="5c860-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5c860-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5c860-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c860-109">Permission type</span></span>                        | <span data-ttu-id="5c860-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c860-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5c860-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c860-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="5c860-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5c860-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="5c860-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c860-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5c860-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5c860-114">Not supported.</span></span>                           |
| <span data-ttu-id="5c860-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c860-115">Application</span></span>                            | <span data-ttu-id="5c860-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5c860-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="5c860-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c860-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerActivityUserDetail(period='{period_value}')
GET /reports/getYammerActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="5c860-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="5c860-118">Function parameters</span></span>

<span data-ttu-id="5c860-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="5c860-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="5c860-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5c860-120">Parameter</span></span> | <span data-ttu-id="5c860-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c860-121">Type</span></span>   | <span data-ttu-id="5c860-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c860-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5c860-123">period</span><span class="sxs-lookup"><span data-stu-id="5c860-123">period</span></span>    | <span data-ttu-id="5c860-124">cadena</span><span class="sxs-lookup"><span data-stu-id="5c860-124">string</span></span> | <span data-ttu-id="5c860-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5c860-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5c860-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="5c860-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5c860-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5c860-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="5c860-128">date</span><span class="sxs-lookup"><span data-stu-id="5c860-128">date</span></span>      | <span data-ttu-id="5c860-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="5c860-129">Date</span></span>   | <span data-ttu-id="5c860-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="5c860-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="5c860-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="5c860-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="5c860-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="5c860-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="5c860-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="5c860-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5c860-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c860-134">Request headers</span></span>

| <span data-ttu-id="5c860-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="5c860-135">Name</span></span>          | <span data-ttu-id="5c860-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c860-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="5c860-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c860-137">Authorization</span></span> | <span data-ttu-id="5c860-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c860-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="5c860-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="5c860-140">If-None-Match</span></span> | <span data-ttu-id="5c860-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="5c860-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="5c860-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5c860-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="5c860-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c860-143">Response</span></span>

<span data-ttu-id="5c860-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="5c860-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5c860-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c860-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5c860-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="5c860-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5c860-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="5c860-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="5c860-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="5c860-148">Report Refresh Date</span></span>
- <span data-ttu-id="5c860-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="5c860-149">User Principal Name</span></span>
- <span data-ttu-id="5c860-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="5c860-150">Display Name</span></span>
- <span data-ttu-id="5c860-151">Estado del usuario</span><span class="sxs-lookup"><span data-stu-id="5c860-151">User State</span></span>
- <span data-ttu-id="5c860-152">Fecha de cambio de estado</span><span class="sxs-lookup"><span data-stu-id="5c860-152">State Change Date</span></span>
- <span data-ttu-id="5c860-153">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="5c860-153">Last Activity Date</span></span>
- <span data-ttu-id="5c860-154">Número de publicaciones</span><span class="sxs-lookup"><span data-stu-id="5c860-154">Posted Count</span></span>
- <span data-ttu-id="5c860-155">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="5c860-155">Read Count</span></span>
- <span data-ttu-id="5c860-156">Número de etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="5c860-156">Liked Count</span></span>
- <span data-ttu-id="5c860-157">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="5c860-157">Assigned Products</span></span>
- <span data-ttu-id="5c860-158">Período del informe</span><span class="sxs-lookup"><span data-stu-id="5c860-158">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="5c860-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c860-159">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5c860-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c860-160">Request</span></span>

<span data-ttu-id="5c860-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c860-161">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammeractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="5c860-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c860-162">Response</span></span>

<span data-ttu-id="5c860-163">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c860-163">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

#### <a name="request"></a><span data-ttu-id="5c860-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c860-164">Request</span></span>

<span data-ttu-id="5c860-165">Si el `date` se especifica el parámetro, el informe se limita a las actividades que tuvieron lugar en la fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="5c860-165">If the `date` parameter is specified, the report is scoped to activities that took place on the given date.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammeractivityuserdetail_date"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerActivityUserDetail(date='2018-03-05')
```

#### <a name="response"></a><span data-ttu-id="5c860-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c860-166">Response</span></span>

<span data-ttu-id="5c860-167">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c860-167">The following is an example of the response.</span></span>

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


<span data-ttu-id="5c860-168">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="5c860-168">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,User State,State Change Date,Last Activity Date,Posted Count,Read Count,Liked Count,Assigned Products,Report Period
```