---
title: 'reportRoot: función getYammerDeviceUsageUserDetail'
description: Obtiene información sobre el uso de dispositivos de Yammer por usuario.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 6a5fe63ed48914e51961259d05aea5eda7b21bd5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975879"
---
# <a name="reportroot-getyammerdeviceusageuserdetail-function"></a><span data-ttu-id="b90a2-103">reportRoot: función getYammerDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="b90a2-103">reportRoot: getYammerDeviceUsageUserDetail function</span></span>

<span data-ttu-id="b90a2-104">Obtiene información sobre el uso de dispositivos de Yammer por usuario.</span><span class="sxs-lookup"><span data-stu-id="b90a2-104">Get details about Yammer device usage by user.</span></span>

> <span data-ttu-id="b90a2-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span><span class="sxs-lookup"><span data-stu-id="b90a2-105">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="b90a2-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="b90a2-106">Permissions</span></span>

<span data-ttu-id="b90a2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b90a2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b90a2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b90a2-109">Permission type</span></span>                        | <span data-ttu-id="b90a2-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b90a2-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b90a2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b90a2-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="b90a2-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b90a2-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b90a2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b90a2-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b90a2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b90a2-114">Not supported.</span></span>                           |
| <span data-ttu-id="b90a2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b90a2-115">Application</span></span>                            | <span data-ttu-id="b90a2-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b90a2-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b90a2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b90a2-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageUserDetail(period='{period_value}')
GET /reports/getYammerDeviceUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="b90a2-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="b90a2-118">Function parameters</span></span>

<span data-ttu-id="b90a2-119">En la URL de la solicitud, especifique el parámetro de consulta seleccionado con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="b90a2-119">In the request URL, provide the query parameter with a valid value.</span></span>

| <span data-ttu-id="b90a2-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b90a2-120">Parameter</span></span> | <span data-ttu-id="b90a2-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b90a2-121">Type</span></span>   | <span data-ttu-id="b90a2-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90a2-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="b90a2-123">period</span><span class="sxs-lookup"><span data-stu-id="b90a2-123">period</span></span>    | <span data-ttu-id="b90a2-124">cadena</span><span class="sxs-lookup"><span data-stu-id="b90a2-124">string</span></span> | <span data-ttu-id="b90a2-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b90a2-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="b90a2-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="b90a2-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="b90a2-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b90a2-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="b90a2-128">date</span><span class="sxs-lookup"><span data-stu-id="b90a2-128">date</span></span>      | <span data-ttu-id="b90a2-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="b90a2-129">Date</span></span>   | <span data-ttu-id="b90a2-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="b90a2-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="b90a2-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="b90a2-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="b90a2-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="b90a2-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="b90a2-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="b90a2-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b90a2-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b90a2-134">Request headers</span></span>

| <span data-ttu-id="b90a2-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="b90a2-135">Name</span></span>          | <span data-ttu-id="b90a2-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="b90a2-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="b90a2-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="b90a2-137">Authorization</span></span> | <span data-ttu-id="b90a2-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b90a2-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="b90a2-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="b90a2-140">If-None-Match</span></span> | <span data-ttu-id="b90a2-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="b90a2-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="b90a2-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b90a2-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="b90a2-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b90a2-143">Response</span></span>

<span data-ttu-id="b90a2-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b90a2-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b90a2-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b90a2-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b90a2-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b90a2-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b90a2-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="b90a2-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="b90a2-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b90a2-148">Report Refresh Date</span></span>
- <span data-ttu-id="b90a2-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="b90a2-149">User Principal Name</span></span>
- <span data-ttu-id="b90a2-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="b90a2-150">Display Name</span></span>
- <span data-ttu-id="b90a2-151">Estado del usuario</span><span class="sxs-lookup"><span data-stu-id="b90a2-151">User State</span></span>
- <span data-ttu-id="b90a2-152">Fecha de cambio de estado</span><span class="sxs-lookup"><span data-stu-id="b90a2-152">State Change Date</span></span>
- <span data-ttu-id="b90a2-153">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="b90a2-153">Last Activity Date</span></span>
- <span data-ttu-id="b90a2-154">Web usada</span><span class="sxs-lookup"><span data-stu-id="b90a2-154">Used Web</span></span>
- <span data-ttu-id="b90a2-155">Windows Phone usado</span><span class="sxs-lookup"><span data-stu-id="b90a2-155">Used Windows Phone</span></span>
- <span data-ttu-id="b90a2-156">Teléfono Android usado</span><span class="sxs-lookup"><span data-stu-id="b90a2-156">Used Android Phone</span></span>
- <span data-ttu-id="b90a2-157">iPhone usado</span><span class="sxs-lookup"><span data-stu-id="b90a2-157">Used iPhone</span></span>
- <span data-ttu-id="b90a2-158">iPad usado</span><span class="sxs-lookup"><span data-stu-id="b90a2-158">Used iPad</span></span>
- <span data-ttu-id="b90a2-159">Otros usados</span><span class="sxs-lookup"><span data-stu-id="b90a2-159">Used Others</span></span>
- <span data-ttu-id="b90a2-160">Período del informe</span><span class="sxs-lookup"><span data-stu-id="b90a2-160">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="b90a2-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b90a2-161">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b90a2-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b90a2-162">Request</span></span>

<span data-ttu-id="b90a2-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b90a2-163">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammerdeviceusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="b90a2-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b90a2-164">Response</span></span>

<span data-ttu-id="b90a2-165">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b90a2-165">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

#### <a name="request"></a><span data-ttu-id="b90a2-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b90a2-166">Request</span></span>

<span data-ttu-id="b90a2-167">Si se llama a con el `date` parámetro, el informe se limita al uso en la fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="b90a2-167">If called with the `date` parameter, the report is scoped to usage on the given date.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammerdeviceusageuserdetail_date"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserDetail(date='2018-03-05')
```

#### <a name="response"></a><span data-ttu-id="b90a2-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b90a2-168">Response</span></span>

<span data-ttu-id="b90a2-169">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b90a2-169">The following is an example of the response.</span></span>

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

<span data-ttu-id="b90a2-170">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b90a2-170">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,User State,State Change Date,Last Activity Date,Used Web,Used Windows Phone,Used Android Phone,Used iPhone,Used iPad,Used Others,Report Period
```
