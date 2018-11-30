---
title: 'reportRoot: getSharePointSiteUsageStorage'
description: Obtiene la tendencia del almacenamiento asignado y usado durante el período del informe.
ms.openlocfilehash: f9d30ee353271d3266bc50d97622272e0540d29f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030136"
---
# <a name="reportroot-getsharepointsiteusagestorage"></a><span data-ttu-id="f5ca9-103">reportRoot: getSharePointSiteUsageStorage</span><span class="sxs-lookup"><span data-stu-id="f5ca9-103">reportRoot: getSharePointSiteUsageStorage</span></span>

<span data-ttu-id="f5ca9-104">Obtiene la tendencia del almacenamiento asignado y usado durante el período del informe.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-104">Get the trend of storage allocated and consumed during the reporting period.</span></span>

> <span data-ttu-id="f5ca9-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span><span class="sxs-lookup"><span data-stu-id="f5ca9-105">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint site usage](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span></span>

## <a name="permissions"></a><span data-ttu-id="f5ca9-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5ca9-106">Permissions</span></span>

<span data-ttu-id="f5ca9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f5ca9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f5ca9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5ca9-109">Permission type</span></span>                        | <span data-ttu-id="f5ca9-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5ca9-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f5ca9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5ca9-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="f5ca9-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5ca9-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="f5ca9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5ca9-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5ca9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-114">Not supported.</span></span>                           |
| <span data-ttu-id="f5ca9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5ca9-115">Application</span></span>                            | <span data-ttu-id="f5ca9-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5ca9-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f5ca9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5ca9-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointSiteUsageStorage(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="f5ca9-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="f5ca9-118">Function parameters</span></span>

<span data-ttu-id="f5ca9-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="f5ca9-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f5ca9-120">Parameter</span></span> | <span data-ttu-id="f5ca9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5ca9-121">Type</span></span>   | <span data-ttu-id="f5ca9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5ca9-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f5ca9-123">period</span><span class="sxs-lookup"><span data-stu-id="f5ca9-123">period</span></span>    | <span data-ttu-id="f5ca9-124">cadena</span><span class="sxs-lookup"><span data-stu-id="f5ca9-124">string</span></span> | <span data-ttu-id="f5ca9-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f5ca9-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f5ca9-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="f5ca9-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="f5ca9-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5ca9-129">Request headers</span></span>

| <span data-ttu-id="f5ca9-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5ca9-130">Name</span></span>          | <span data-ttu-id="f5ca9-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5ca9-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="f5ca9-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5ca9-132">Authorization</span></span> | <span data-ttu-id="f5ca9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="f5ca9-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="f5ca9-135">If-None-Match</span></span> | <span data-ttu-id="f5ca9-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="f5ca9-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="f5ca9-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5ca9-138">Response</span></span>

<span data-ttu-id="f5ca9-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f5ca9-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f5ca9-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f5ca9-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f5ca9-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="f5ca9-143">Report Refresh Date</span></span>
- <span data-ttu-id="f5ca9-144">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="f5ca9-144">Site Type</span></span>
- <span data-ttu-id="f5ca9-145">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="f5ca9-145">Storage Used (Byte)</span></span>
- <span data-ttu-id="f5ca9-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="f5ca9-146">Report Date</span></span>
- <span data-ttu-id="f5ca9-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="f5ca9-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="f5ca9-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5ca9-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f5ca9-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5ca9-149">Request</span></span>

<span data-ttu-id="f5ca9-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getsharepointsiteusagestorage"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSharePointSiteUsageStorage(period='D7')
```

#### <a name="response"></a><span data-ttu-id="f5ca9-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5ca9-151">Response</span></span>

<span data-ttu-id="f5ca9-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-152">The following is an example of the response.</span></span>

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

<span data-ttu-id="f5ca9-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5ca9-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Storage Used (Byte),Report Date,Report Period
```
