---
title: 'reportRoot: getEmailAppUsageUserDetail'
description: Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico.
ms.openlocfilehash: 6ea60e5729c17d25a36ad0651da4eb55dbe61560
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032244"
---
# <a name="reportroot-getemailappusageuserdetail"></a><span data-ttu-id="418a4-103">reportRoot: getEmailAppUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="418a4-103">reportRoot: getEmailAppUsageUserDetail</span></span>

<span data-ttu-id="418a4-104">Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="418a4-104">Get details about which activities users performed on the various email apps.</span></span>

> <span data-ttu-id="418a4-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="418a4-105">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="418a4-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="418a4-106">Permissions</span></span>

<span data-ttu-id="418a4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="418a4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="418a4-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="418a4-109">Permission type</span></span>                        | <span data-ttu-id="418a4-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="418a4-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="418a4-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="418a4-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="418a4-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="418a4-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="418a4-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="418a4-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="418a4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="418a4-114">Not supported.</span></span>                           |
| <span data-ttu-id="418a4-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="418a4-115">Application</span></span>                            | <span data-ttu-id="418a4-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="418a4-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="418a4-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="418a4-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getEmailAppUsageUserDetail(period='{period_value}')
GET /reports/getEmailAppUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="418a4-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="418a4-118">Function parameters</span></span>

<span data-ttu-id="418a4-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="418a4-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="418a4-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="418a4-120">Parameter</span></span> | <span data-ttu-id="418a4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="418a4-121">Type</span></span>   | <span data-ttu-id="418a4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="418a4-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="418a4-123">period</span><span class="sxs-lookup"><span data-stu-id="418a4-123">period</span></span>    | <span data-ttu-id="418a4-124">cadena</span><span class="sxs-lookup"><span data-stu-id="418a4-124">string</span></span> | <span data-ttu-id="418a4-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="418a4-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="418a4-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="418a4-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="418a4-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="418a4-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="418a4-128">date</span><span class="sxs-lookup"><span data-stu-id="418a4-128">date</span></span>      | <span data-ttu-id="418a4-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="418a4-129">Date</span></span>   | <span data-ttu-id="418a4-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="418a4-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="418a4-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="418a4-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="418a4-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="418a4-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="418a4-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="418a4-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="418a4-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="418a4-134">Request headers</span></span>

| <span data-ttu-id="418a4-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="418a4-135">Name</span></span>          | <span data-ttu-id="418a4-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="418a4-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="418a4-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="418a4-137">Authorization</span></span> | <span data-ttu-id="418a4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="418a4-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="418a4-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="418a4-140">If-None-Match</span></span> | <span data-ttu-id="418a4-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="418a4-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="418a4-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="418a4-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="418a4-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="418a4-143">Response</span></span>

<span data-ttu-id="418a4-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="418a4-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="418a4-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="418a4-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="418a4-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="418a4-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="418a4-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="418a4-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="418a4-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="418a4-148">Report Refresh Date</span></span>
- <span data-ttu-id="418a4-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="418a4-149">User Principal Name</span></span>
- <span data-ttu-id="418a4-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="418a4-150">Display Name</span></span>
- <span data-ttu-id="418a4-151">Eliminado</span><span class="sxs-lookup"><span data-stu-id="418a4-151">Is Deleted</span></span>
- <span data-ttu-id="418a4-152">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="418a4-152">Deleted Date</span></span>
- <span data-ttu-id="418a4-153">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="418a4-153">Last Activity Date</span></span>
- <span data-ttu-id="418a4-154">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="418a4-154">Mail For Mac</span></span>
- <span data-ttu-id="418a4-155">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="418a4-155">Outlook For Mac</span></span>
- <span data-ttu-id="418a4-156">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="418a4-156">Outlook For Windows</span></span>
- <span data-ttu-id="418a4-157">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="418a4-157">Outlook For Mobile</span></span>
- <span data-ttu-id="418a4-158">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="418a4-158">Other For Mobile</span></span>
- <span data-ttu-id="418a4-159">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="418a4-159">Outlook For Web</span></span>
- <span data-ttu-id="418a4-160">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="418a4-160">POP3 App</span></span>
- <span data-ttu-id="418a4-161">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="418a4-161">IMAP4 App</span></span>
- <span data-ttu-id="418a4-162">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="418a4-162">SMTP App</span></span>
- <span data-ttu-id="418a4-163">Período del informe</span><span class="sxs-lookup"><span data-stu-id="418a4-163">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="418a4-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="418a4-164">Example</span></span>

#### <a name="request"></a><span data-ttu-id="418a4-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="418a4-165">Request</span></span>

<span data-ttu-id="418a4-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="418a4-166">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailappusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailAppUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="418a4-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="418a4-167">Response</span></span>

<span data-ttu-id="418a4-168">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="418a4-168">The following is an example of the response.</span></span>

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

<span data-ttu-id="418a4-169">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="418a4-169">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Last Activity Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```
