---
title: 'reportRoot: getSharePointSiteUsageSiteCounts'
description: Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.
localization_priority: Normal
ms.openlocfilehash: e16470419654f1c75b3c74b445a6677974ef20b7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27837193"
---
# <a name="reportroot-getsharepointsiteusagesitecounts"></a><span data-ttu-id="09435-104">reportRoot: getSharePointSiteUsageSiteCounts</span><span class="sxs-lookup"><span data-stu-id="09435-104">reportRoot: getSharePointSiteUsageSiteCounts</span></span>

<span data-ttu-id="09435-105">Obtiene el número total de archivos en todos los sitios y el número de archivos activos.</span><span class="sxs-lookup"><span data-stu-id="09435-105">Get the total number of files across all sites and the number of active files.</span></span> <span data-ttu-id="09435-106">Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="09435-106">A file (user or system) is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span>

> <span data-ttu-id="09435-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span><span class="sxs-lookup"><span data-stu-id="09435-107">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint site usage](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span></span>

## <a name="permissions"></a><span data-ttu-id="09435-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="09435-108">Permissions</span></span>

<span data-ttu-id="09435-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="09435-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="09435-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="09435-111">Permission type</span></span>                        | <span data-ttu-id="09435-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="09435-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="09435-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="09435-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="09435-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="09435-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="09435-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="09435-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="09435-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="09435-116">Not supported.</span></span>                           |
| <span data-ttu-id="09435-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="09435-117">Application</span></span>                            | <span data-ttu-id="09435-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="09435-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="09435-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="09435-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointSiteUsageSiteCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="09435-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="09435-120">Function parameters</span></span>

<span data-ttu-id="09435-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="09435-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="09435-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="09435-122">Parameter</span></span> | <span data-ttu-id="09435-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="09435-123">Type</span></span>   | <span data-ttu-id="09435-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="09435-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="09435-125">period</span><span class="sxs-lookup"><span data-stu-id="09435-125">period</span></span>    | <span data-ttu-id="09435-126">cadena</span><span class="sxs-lookup"><span data-stu-id="09435-126">string</span></span> | <span data-ttu-id="09435-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="09435-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="09435-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="09435-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="09435-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="09435-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="09435-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="09435-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="09435-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="09435-131">Request headers</span></span>

| <span data-ttu-id="09435-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="09435-132">Name</span></span>          | <span data-ttu-id="09435-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="09435-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="09435-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="09435-134">Authorization</span></span> | <span data-ttu-id="09435-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="09435-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="09435-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="09435-137">If-None-Match</span></span> | <span data-ttu-id="09435-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="09435-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="09435-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09435-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="09435-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09435-140">Response</span></span>

<span data-ttu-id="09435-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="09435-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="09435-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09435-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="09435-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="09435-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="09435-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="09435-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="09435-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="09435-145">Report Refresh Date</span></span>
- <span data-ttu-id="09435-146">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="09435-146">Site Type</span></span>
- <span data-ttu-id="09435-147">Total</span><span class="sxs-lookup"><span data-stu-id="09435-147">Total</span></span>
- <span data-ttu-id="09435-148">Activo</span><span class="sxs-lookup"><span data-stu-id="09435-148">Active</span></span>
- <span data-ttu-id="09435-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="09435-149">Report Date</span></span>
- <span data-ttu-id="09435-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="09435-150">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="09435-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="09435-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="09435-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="09435-152">Request</span></span>

<span data-ttu-id="09435-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="09435-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getsharepointsiteusagesitecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSharePointSiteUsageSiteCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="09435-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="09435-154">Response</span></span>

<span data-ttu-id="09435-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="09435-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="09435-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="09435-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Total,Active,Report Date,Report Period
```
