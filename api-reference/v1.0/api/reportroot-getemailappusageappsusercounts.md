---
title: 'reportRoot: getEmailAppUsageAppsUserCounts'
description: Obtiene el número de usuarios únicos por aplicación de correo electrónico.
localization_priority: Normal
ms.openlocfilehash: c9a05532f1dcbe3db4718ac2b551278af9691011
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875855"
---
# <a name="reportroot-getemailappusageappsusercounts"></a><span data-ttu-id="dd949-103">reportRoot: getEmailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="dd949-103">reportRoot: getEmailAppUsageAppsUserCounts</span></span>

<span data-ttu-id="dd949-104">Obtiene el número de usuarios únicos por aplicación de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="dd949-104">Get the count of unique users per email app.</span></span>

> <span data-ttu-id="dd949-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="dd949-105">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="dd949-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="dd949-106">Permissions</span></span>

<span data-ttu-id="dd949-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dd949-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="dd949-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dd949-109">Permission type</span></span>                        | <span data-ttu-id="dd949-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dd949-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="dd949-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dd949-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="dd949-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dd949-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="dd949-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dd949-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dd949-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dd949-114">Not supported.</span></span>                           |
| <span data-ttu-id="dd949-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dd949-115">Application</span></span>                            | <span data-ttu-id="dd949-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dd949-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="dd949-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dd949-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageAppsUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="dd949-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="dd949-118">Function parameters</span></span>

<span data-ttu-id="dd949-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="dd949-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="dd949-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dd949-120">Parameter</span></span> | <span data-ttu-id="dd949-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="dd949-121">Type</span></span>   | <span data-ttu-id="dd949-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd949-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="dd949-123">period</span><span class="sxs-lookup"><span data-stu-id="dd949-123">period</span></span>    | <span data-ttu-id="dd949-124">cadena</span><span class="sxs-lookup"><span data-stu-id="dd949-124">string</span></span> | <span data-ttu-id="dd949-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dd949-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="dd949-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="dd949-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="dd949-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dd949-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="dd949-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="dd949-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="dd949-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dd949-129">Request headers</span></span>

| <span data-ttu-id="dd949-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="dd949-130">Name</span></span>          | <span data-ttu-id="dd949-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="dd949-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="dd949-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="dd949-132">Authorization</span></span> | <span data-ttu-id="dd949-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dd949-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="dd949-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="dd949-135">If-None-Match</span></span> | <span data-ttu-id="dd949-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="dd949-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="dd949-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dd949-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="dd949-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd949-138">Response</span></span>

<span data-ttu-id="dd949-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="dd949-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="dd949-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd949-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="dd949-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="dd949-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="dd949-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="dd949-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="dd949-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="dd949-143">Report Refresh Date</span></span>
- <span data-ttu-id="dd949-144">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="dd949-144">Mail For Mac</span></span>
- <span data-ttu-id="dd949-145">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="dd949-145">Outlook For Mac</span></span>
- <span data-ttu-id="dd949-146">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="dd949-146">Outlook For Windows</span></span>
- <span data-ttu-id="dd949-147">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="dd949-147">Outlook For Mobile</span></span>
- <span data-ttu-id="dd949-148">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="dd949-148">Other For Mobile</span></span>
- <span data-ttu-id="dd949-149">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="dd949-149">Outlook For Web</span></span>
- <span data-ttu-id="dd949-150">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="dd949-150">POP3 App</span></span>
- <span data-ttu-id="dd949-151">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="dd949-151">IMAP4 App</span></span>
- <span data-ttu-id="dd949-152">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="dd949-152">SMTP App</span></span>
- <span data-ttu-id="dd949-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="dd949-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="dd949-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dd949-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="dd949-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dd949-155">Request</span></span>

<span data-ttu-id="dd949-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dd949-156">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailappusageappsusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailAppUsageAppsUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="dd949-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dd949-157">Response</span></span>

<span data-ttu-id="dd949-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dd949-158">The following is an example of the response.</span></span>

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

<span data-ttu-id="dd949-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="dd949-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```
