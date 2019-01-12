---
title: 'reportRoot: getSkypeForBusinessActivityUserDetail'
description: Obtiene información sobre la actividad de Skype Empresarial por usuario.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: c7439cf6eaff88e61379fbbb10cee2b4fb9b3efd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27954172"
---
# <a name="reportroot-getskypeforbusinessactivityuserdetail"></a><span data-ttu-id="994fa-103">reportRoot: getSkypeForBusinessActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="994fa-103">reportRoot: getSkypeForBusinessActivityUserDetail</span></span>

<span data-ttu-id="994fa-104">Obtiene información sobre la actividad de Skype Empresarial por usuario.</span><span class="sxs-lookup"><span data-stu-id="994fa-104">Get details about Skype for Business activity by user.</span></span>

> <span data-ttu-id="994fa-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="994fa-105">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="994fa-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="994fa-106">Permissions</span></span>

<span data-ttu-id="994fa-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="994fa-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="994fa-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="994fa-109">Permission type</span></span>                        | <span data-ttu-id="994fa-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="994fa-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="994fa-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="994fa-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="994fa-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="994fa-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="994fa-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="994fa-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="994fa-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="994fa-114">Not supported.</span></span>                           |
| <span data-ttu-id="994fa-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="994fa-115">Application</span></span>                            | <span data-ttu-id="994fa-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="994fa-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="994fa-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="994fa-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserDetail(period='{period_value}')
GET /reports/getSkypeForBusinessActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="994fa-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="994fa-118">Function parameters</span></span>

<span data-ttu-id="994fa-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="994fa-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="994fa-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="994fa-120">Parameter</span></span> | <span data-ttu-id="994fa-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="994fa-121">Type</span></span>   | <span data-ttu-id="994fa-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="994fa-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="994fa-123">period</span><span class="sxs-lookup"><span data-stu-id="994fa-123">period</span></span>    | <span data-ttu-id="994fa-124">cadena</span><span class="sxs-lookup"><span data-stu-id="994fa-124">string</span></span> | <span data-ttu-id="994fa-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="994fa-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="994fa-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="994fa-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="994fa-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="994fa-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="994fa-128">date</span><span class="sxs-lookup"><span data-stu-id="994fa-128">date</span></span>      | <span data-ttu-id="994fa-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="994fa-129">Date</span></span>   | <span data-ttu-id="994fa-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="994fa-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="994fa-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="994fa-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="994fa-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="994fa-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="994fa-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="994fa-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="994fa-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="994fa-134">Request headers</span></span>

| <span data-ttu-id="994fa-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="994fa-135">Name</span></span>          | <span data-ttu-id="994fa-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="994fa-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="994fa-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="994fa-137">Authorization</span></span> | <span data-ttu-id="994fa-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="994fa-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="994fa-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="994fa-140">If-None-Match</span></span> | <span data-ttu-id="994fa-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="994fa-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="994fa-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="994fa-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="994fa-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="994fa-143">Response</span></span>

<span data-ttu-id="994fa-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="994fa-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="994fa-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="994fa-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="994fa-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="994fa-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="994fa-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="994fa-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="994fa-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="994fa-148">Report Refresh Date</span></span>
- <span data-ttu-id="994fa-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="994fa-149">User Principal Name</span></span>
- <span data-ttu-id="994fa-150">Eliminado</span><span class="sxs-lookup"><span data-stu-id="994fa-150">Is Deleted</span></span>
- <span data-ttu-id="994fa-151">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="994fa-151">Deleted Date</span></span>
- <span data-ttu-id="994fa-152">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="994fa-152">Last Activity Date</span></span>
- <span data-ttu-id="994fa-153">Número total de sesiones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-153">Total Peer-to-peer Session Count</span></span>
- <span data-ttu-id="994fa-154">Número total de conferencias organizadas</span><span class="sxs-lookup"><span data-stu-id="994fa-154">Total Organized Conference Count</span></span>
- <span data-ttu-id="994fa-155">Número total de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-155">Total Participated Conference Count</span></span>
- <span data-ttu-id="994fa-156">Fecha de la última actividad de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-156">Peer-to-peer Last Activity Date</span></span>
- <span data-ttu-id="994fa-157">Fecha de la última actividad de una conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-157">Organized Conference Last Activity Date</span></span>
- <span data-ttu-id="994fa-158">Fecha de la última actividad de una conferencia en la que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-158">Participated Conference Last Activity Date</span></span>
- <span data-ttu-id="994fa-159">Números de mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-159">Peer-to-peer IM Count</span></span>
- <span data-ttu-id="994fa-160">Número de sesiones de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-160">Peer-to-peer Audio Count</span></span>
- <span data-ttu-id="994fa-161">Minutos de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-161">Peer-to-peer Audio Minutes</span></span>
- <span data-ttu-id="994fa-162">Número de sesiones de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-162">Peer-to-peer Video Count</span></span>
- <span data-ttu-id="994fa-163">Minutos de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-163">Peer-to-peer Video Minutes</span></span>
- <span data-ttu-id="994fa-164">Número de sesiones de uso compartido de aplicaciones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-164">Peer-to-peer App Sharing Count</span></span>
- <span data-ttu-id="994fa-165">Número de transferencias de archivos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="994fa-165">Peer-to-peer File Transfer Count</span></span>
- <span data-ttu-id="994fa-166">Número de mensajes instantáneos de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-166">Organized Conference IM Count</span></span>
- <span data-ttu-id="994fa-167">Número de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-167">Organized Conference Audio/Video Count</span></span>
- <span data-ttu-id="994fa-168">Minutos de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-168">Organized Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="994fa-169">Número de sesiones de uso compartido de aplicaciones se conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-169">Organized Conference App Sharing Count</span></span>
- <span data-ttu-id="994fa-170">Número de sesiones web de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="994fa-170">Organized Conference Web Count</span></span>
- <span data-ttu-id="994fa-171">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por terceros</span><span class="sxs-lookup"><span data-stu-id="994fa-171">Organized Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="994fa-172">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="994fa-172">Organized Conference Dial-in/out Microsoft Count</span></span>
- <span data-ttu-id="994fa-173">Minutos de conferencias de acceso telefónico local organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="994fa-173">Organized Conference Dial-in Microsoft Minutes</span></span>
- <span data-ttu-id="994fa-174">Minutos de conferencias por aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="994fa-174">Organized Conference Dial-out Microsoft Minutes</span></span>
- <span data-ttu-id="994fa-175">Número de mensajes instantáneos de conferencias en la que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-175">Paricipated Conference IM Count</span></span>
- <span data-ttu-id="994fa-176">Número de sesiones de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-176">Participated Conference Audio/Video Count</span></span>
- <span data-ttu-id="994fa-177">Minutos de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-177">Participated Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="994fa-178">Número de sesiones de uso compartido de aplicaciones de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-178">Participated Conference App Sharing Count</span></span>
- <span data-ttu-id="994fa-179">Número de sesiones web de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-179">Participated Conference Web Count</span></span>
- <span data-ttu-id="994fa-180">Número de conferencias de acceso telefónico local o aceptación de llamada de terceros en las que participó</span><span class="sxs-lookup"><span data-stu-id="994fa-180">Participated Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="994fa-181">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="994fa-181">Assigned Products</span></span>
- <span data-ttu-id="994fa-182">Período del informe</span><span class="sxs-lookup"><span data-stu-id="994fa-182">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="994fa-183">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="994fa-183">Example</span></span>

#### <a name="request"></a><span data-ttu-id="994fa-184">Solicitud</span><span class="sxs-lookup"><span data-stu-id="994fa-184">Request</span></span>

<span data-ttu-id="994fa-185">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="994fa-185">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="994fa-186">Respuesta</span><span class="sxs-lookup"><span data-stu-id="994fa-186">Response</span></span>

<span data-ttu-id="994fa-187">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="994fa-187">The following is an example of the response.</span></span>

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

<span data-ttu-id="994fa-188">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="994fa-188">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Total Peer-to-peer Session Count,Total Organized Conference Count,Total Participated Conference Count,Peer-to-peer Last Activity Date,Organized Conference Last Activity Date,Participated Conference Last Activity Date,Peer-to-peer IM Count,Peer-to-peer Audio Count,Peer-to-peer Audio Minutes,Peer-to-peer Video Count,Peer-to-peer Video Minutes,Peer-to-peer App Sharing Count,Peer-to-peer File Transfer Count,Organized Conference IM Count,Organized Conference Audio/Video Count,Organized Conference Audio/Video Minutes,Organized Conference App Sharing Count,Organized Conference Web Count,Organized Conference Dial-in/out 3rd Party Count,Organized Conference Dial-in/out Microsoft Count,Organized Conference Dial-in Microsoft Minutes,Organized Conference Dial-out Microsoft Minutes,Paricipated Conference IM Count,Participated Conference Audio/Video Count,Participated Conference Audio/Video Minutes,Participated Conference App Sharing Count,Participated Conference Web Count,Participated Conference Dial-in/out 3rd Party Count,Assigned Products,Report Period
```
