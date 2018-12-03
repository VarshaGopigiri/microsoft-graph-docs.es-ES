---
title: 'reportRoot: getEmailActivityCounts'
description: Le permite comprender las tendencias de las actividades de correo electrónico (por ejemplo, cuántos se enviaron, leyeron y recibieron) en la organización.
ms.openlocfilehash: 1cd15a10959c3ec4da11b879acf5c617b8cb22dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029283"
---
# <a name="reportroot-getemailactivitycounts"></a><span data-ttu-id="ccb49-103">reportRoot: getEmailActivityCounts</span><span class="sxs-lookup"><span data-stu-id="ccb49-103">reportRoot: getEmailActivityCounts</span></span>

<span data-ttu-id="ccb49-104">Le permite comprender las tendencias de las actividades de correo electrónico (por ejemplo, cuántos se enviaron, leyeron y recibieron) en la organización.</span><span class="sxs-lookup"><span data-stu-id="ccb49-104">Enables you to understand the trends of email activity (like how many were sent, read, and received) in your organization.</span></span>

> <span data-ttu-id="ccb49-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividades de correo electrónico](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).</span><span class="sxs-lookup"><span data-stu-id="ccb49-105">**Note:** For details about different report views and names, see [Office 365 Reports - Email Activity](https://support.office.com/client/Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44).</span></span>

## <a name="permissions"></a><span data-ttu-id="ccb49-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ccb49-106">Permissions</span></span>

<span data-ttu-id="ccb49-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ccb49-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ccb49-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ccb49-109">Permission type</span></span>                        | <span data-ttu-id="ccb49-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ccb49-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ccb49-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ccb49-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="ccb49-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ccb49-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ccb49-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ccb49-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ccb49-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ccb49-114">Not supported.</span></span>                           |
| <span data-ttu-id="ccb49-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ccb49-115">Application</span></span>                            | <span data-ttu-id="ccb49-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ccb49-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ccb49-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ccb49-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ccb49-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ccb49-118">Function parameters</span></span>

<span data-ttu-id="ccb49-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ccb49-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ccb49-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ccb49-120">Parameter</span></span> | <span data-ttu-id="ccb49-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccb49-121">Type</span></span>   | <span data-ttu-id="ccb49-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccb49-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ccb49-123">period</span><span class="sxs-lookup"><span data-stu-id="ccb49-123">period</span></span>    | <span data-ttu-id="ccb49-124">cadena</span><span class="sxs-lookup"><span data-stu-id="ccb49-124">string</span></span> | <span data-ttu-id="ccb49-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ccb49-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ccb49-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ccb49-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ccb49-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ccb49-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ccb49-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ccb49-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="ccb49-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccb49-129">Request headers</span></span>

| <span data-ttu-id="ccb49-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccb49-130">Name</span></span>          | <span data-ttu-id="ccb49-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccb49-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ccb49-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="ccb49-132">Authorization</span></span> | <span data-ttu-id="ccb49-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ccb49-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ccb49-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ccb49-135">If-None-Match</span></span> | <span data-ttu-id="ccb49-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ccb49-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ccb49-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ccb49-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ccb49-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ccb49-138">Response</span></span>

<span data-ttu-id="ccb49-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ccb49-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ccb49-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb49-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ccb49-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ccb49-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ccb49-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ccb49-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ccb49-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ccb49-143">Report Refresh Date</span></span>
- <span data-ttu-id="ccb49-144">Envío</span><span class="sxs-lookup"><span data-stu-id="ccb49-144">Send</span></span>
- <span data-ttu-id="ccb49-145">Recepción</span><span class="sxs-lookup"><span data-stu-id="ccb49-145">Receive</span></span>
- <span data-ttu-id="ccb49-146">Leído</span><span class="sxs-lookup"><span data-stu-id="ccb49-146">Read</span></span>
- <span data-ttu-id="ccb49-147">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ccb49-147">Report Date</span></span>
- <span data-ttu-id="ccb49-148">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ccb49-148">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="ccb49-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccb49-149">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ccb49-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ccb49-150">Request</span></span>

<span data-ttu-id="ccb49-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ccb49-151">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailactivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ccb49-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ccb49-152">Response</span></span>

<span data-ttu-id="ccb49-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb49-153">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="ccb49-154">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ccb49-154">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "ignored"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Send,Receive,Read,Report Date,Report Period
```