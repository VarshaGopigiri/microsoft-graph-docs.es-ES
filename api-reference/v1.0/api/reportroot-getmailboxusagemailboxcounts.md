---
title: 'reportRoot: getMailboxUsageMailboxCounts'
description: Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe. Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 621c3897b7e97043d93852f14909713309164a58
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27968872"
---
# <a name="reportroot-getmailboxusagemailboxcounts"></a><span data-ttu-id="ade3b-104">reportRoot: getMailboxUsageMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="ade3b-104">reportRoot: getMailboxUsageMailboxCounts</span></span>

<span data-ttu-id="ade3b-105">Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe.</span><span class="sxs-lookup"><span data-stu-id="ade3b-105">Get the total number of user mailboxes in your organization and how many are active each day of the reporting period.</span></span> <span data-ttu-id="ade3b-106">Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ade3b-106">A mailbox is considered active if the user sent or read any email.</span></span>

> <span data-ttu-id="ade3b-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="ade3b-107">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="ade3b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ade3b-108">Permissions</span></span>

<span data-ttu-id="ade3b-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ade3b-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ade3b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ade3b-111">Permission type</span></span>                        | <span data-ttu-id="ade3b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ade3b-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ade3b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ade3b-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="ade3b-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ade3b-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ade3b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ade3b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ade3b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ade3b-116">Not supported.</span></span>                           |
| <span data-ttu-id="ade3b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ade3b-117">Application</span></span>                            | <span data-ttu-id="ade3b-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ade3b-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ade3b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ade3b-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageMailboxCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ade3b-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ade3b-120">Function parameters</span></span>

<span data-ttu-id="ade3b-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ade3b-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ade3b-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ade3b-122">Parameter</span></span> | <span data-ttu-id="ade3b-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ade3b-123">Type</span></span>   | <span data-ttu-id="ade3b-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ade3b-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ade3b-125">period</span><span class="sxs-lookup"><span data-stu-id="ade3b-125">period</span></span>    | <span data-ttu-id="ade3b-126">cadena</span><span class="sxs-lookup"><span data-stu-id="ade3b-126">string</span></span> | <span data-ttu-id="ade3b-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ade3b-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ade3b-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ade3b-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ade3b-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ade3b-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ade3b-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ade3b-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="ade3b-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ade3b-131">Request headers</span></span>

| <span data-ttu-id="ade3b-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="ade3b-132">Name</span></span>          | <span data-ttu-id="ade3b-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ade3b-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ade3b-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="ade3b-134">Authorization</span></span> | <span data-ttu-id="ade3b-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ade3b-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ade3b-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ade3b-137">If-None-Match</span></span> | <span data-ttu-id="ade3b-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ade3b-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ade3b-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ade3b-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ade3b-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ade3b-140">Response</span></span>

<span data-ttu-id="ade3b-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ade3b-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ade3b-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ade3b-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ade3b-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ade3b-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ade3b-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ade3b-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ade3b-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ade3b-145">Report Refresh Date</span></span>
- <span data-ttu-id="ade3b-146">Total</span><span class="sxs-lookup"><span data-stu-id="ade3b-146">Total</span></span>
- <span data-ttu-id="ade3b-147">Activo</span><span class="sxs-lookup"><span data-stu-id="ade3b-147">Active</span></span>
- <span data-ttu-id="ade3b-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ade3b-148">Report Date</span></span>
- <span data-ttu-id="ade3b-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ade3b-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="ade3b-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ade3b-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ade3b-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ade3b-151">Request</span></span>

<span data-ttu-id="ade3b-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ade3b-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusagemailboxcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageMailboxCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ade3b-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ade3b-153">Response</span></span>

<span data-ttu-id="ade3b-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ade3b-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="ade3b-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ade3b-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```
