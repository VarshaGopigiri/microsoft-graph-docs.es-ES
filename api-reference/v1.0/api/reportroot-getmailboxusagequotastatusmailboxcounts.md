---
title: 'reportRoot: getMailboxUsageQuotaStatusMailboxCounts'
description: Obtiene el número de buzones de usuario en cada categoría de cuota.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: d440dc4e7c3077424eb657ac49071eff7791e388
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977979"
---
# <a name="reportroot-getmailboxusagequotastatusmailboxcounts"></a><span data-ttu-id="07376-103">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="07376-103">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span></span>

<span data-ttu-id="07376-104">Obtiene el número de buzones de usuario en cada categoría de cuota.</span><span class="sxs-lookup"><span data-stu-id="07376-104">Get the count of user mailboxes in each quota category.</span></span>

> <span data-ttu-id="07376-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="07376-105">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="07376-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="07376-106">Permissions</span></span>

<span data-ttu-id="07376-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07376-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="07376-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07376-109">Permission type</span></span>                        | <span data-ttu-id="07376-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07376-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="07376-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07376-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="07376-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="07376-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="07376-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07376-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="07376-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07376-114">Not supported.</span></span>                           |
| <span data-ttu-id="07376-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07376-115">Application</span></span>                            | <span data-ttu-id="07376-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="07376-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="07376-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07376-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageQuotaStatusMailboxCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="07376-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="07376-118">Function parameters</span></span>

<span data-ttu-id="07376-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="07376-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="07376-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="07376-120">Parameter</span></span> | <span data-ttu-id="07376-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="07376-121">Type</span></span>   | <span data-ttu-id="07376-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="07376-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="07376-123">period</span><span class="sxs-lookup"><span data-stu-id="07376-123">period</span></span>    | <span data-ttu-id="07376-124">cadena</span><span class="sxs-lookup"><span data-stu-id="07376-124">string</span></span> | <span data-ttu-id="07376-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="07376-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="07376-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="07376-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="07376-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="07376-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="07376-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="07376-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="07376-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07376-129">Request headers</span></span>

| <span data-ttu-id="07376-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="07376-130">Name</span></span>          | <span data-ttu-id="07376-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="07376-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="07376-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="07376-132">Authorization</span></span> | <span data-ttu-id="07376-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="07376-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="07376-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="07376-135">If-None-Match</span></span> | <span data-ttu-id="07376-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="07376-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="07376-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="07376-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="07376-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07376-138">Response</span></span>

<span data-ttu-id="07376-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="07376-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="07376-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07376-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="07376-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="07376-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="07376-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="07376-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="07376-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="07376-143">Report Refresh Date</span></span>
- <span data-ttu-id="07376-144">Por debajo del límite</span><span class="sxs-lookup"><span data-stu-id="07376-144">Under Limit</span></span>
- <span data-ttu-id="07376-145">Advertencia emitida</span><span class="sxs-lookup"><span data-stu-id="07376-145">Warning Issued</span></span>
- <span data-ttu-id="07376-146">Envío prohibido</span><span class="sxs-lookup"><span data-stu-id="07376-146">Send Prohibited</span></span>
- <span data-ttu-id="07376-147">Envío o recepción prohibidos</span><span class="sxs-lookup"><span data-stu-id="07376-147">Send/Receive Prohibited</span></span>
- <span data-ttu-id="07376-148">Indeterminado</span><span class="sxs-lookup"><span data-stu-id="07376-148">Indeterminate</span></span>
- <span data-ttu-id="07376-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="07376-149">Report Date</span></span>
- <span data-ttu-id="07376-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="07376-150">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="07376-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07376-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="07376-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07376-152">Request</span></span>

<span data-ttu-id="07376-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07376-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusagequotastatusmailboxcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageQuotaStatusMailboxCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="07376-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07376-154">Response</span></span>

<span data-ttu-id="07376-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07376-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="07376-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="07376-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Under Limit,Warning Issued,Send Prohibited,Send/Receive Prohibited,Indeterminate,Report Date,Report Period
```
