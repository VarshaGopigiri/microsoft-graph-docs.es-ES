---
title: 'reportRoot: getOneDriveUsageFileCounts'
description: Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos. Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 76a9b0bf7fccde5ac93f45c0f47248fd99faabd6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921027"
---
# <a name="reportroot-getonedriveusagefilecounts"></a><span data-ttu-id="349cd-104">reportRoot: getOneDriveUsageFileCounts</span><span class="sxs-lookup"><span data-stu-id="349cd-104">reportRoot: getOneDriveUsageFileCounts</span></span>

<span data-ttu-id="349cd-105">Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos.</span><span class="sxs-lookup"><span data-stu-id="349cd-105">Get the total number of files across all sites and how many are active files.</span></span> <span data-ttu-id="349cd-106">Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="349cd-106">A file is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span>

> <span data-ttu-id="349cd-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="349cd-107">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="349cd-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="349cd-108">Permissions</span></span>

<span data-ttu-id="349cd-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="349cd-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="349cd-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="349cd-111">Permission type</span></span>                        | <span data-ttu-id="349cd-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="349cd-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="349cd-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="349cd-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="349cd-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="349cd-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="349cd-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="349cd-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="349cd-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="349cd-116">Not supported.</span></span>                           |
| <span data-ttu-id="349cd-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="349cd-117">Application</span></span>                            | <span data-ttu-id="349cd-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="349cd-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="349cd-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="349cd-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="349cd-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="349cd-120">Function parameters</span></span>

<span data-ttu-id="349cd-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="349cd-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="349cd-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="349cd-122">Parameter</span></span> | <span data-ttu-id="349cd-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="349cd-123">Type</span></span>   | <span data-ttu-id="349cd-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="349cd-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="349cd-125">period</span><span class="sxs-lookup"><span data-stu-id="349cd-125">period</span></span>    | <span data-ttu-id="349cd-126">cadena</span><span class="sxs-lookup"><span data-stu-id="349cd-126">string</span></span> | <span data-ttu-id="349cd-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="349cd-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="349cd-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="349cd-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="349cd-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="349cd-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="349cd-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="349cd-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="349cd-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="349cd-131">Request headers</span></span>

| <span data-ttu-id="349cd-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="349cd-132">Name</span></span>          | <span data-ttu-id="349cd-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="349cd-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="349cd-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="349cd-134">Authorization</span></span> | <span data-ttu-id="349cd-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="349cd-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="349cd-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="349cd-137">If-None-Match</span></span> | <span data-ttu-id="349cd-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="349cd-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="349cd-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="349cd-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="349cd-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="349cd-140">Response</span></span>

<span data-ttu-id="349cd-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="349cd-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="349cd-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="349cd-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="349cd-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="349cd-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="349cd-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="349cd-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="349cd-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="349cd-145">Report Refresh Date</span></span>
- <span data-ttu-id="349cd-146">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="349cd-146">Site Type</span></span>
- <span data-ttu-id="349cd-147">Total</span><span class="sxs-lookup"><span data-stu-id="349cd-147">Total</span></span>
- <span data-ttu-id="349cd-148">Activo</span><span class="sxs-lookup"><span data-stu-id="349cd-148">Active</span></span>
- <span data-ttu-id="349cd-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="349cd-149">Report Date</span></span>
- <span data-ttu-id="349cd-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="349cd-150">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="349cd-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="349cd-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="349cd-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="349cd-152">Request</span></span>

<span data-ttu-id="349cd-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="349cd-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveusagefilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="349cd-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="349cd-154">Response</span></span>

<span data-ttu-id="349cd-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="349cd-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="349cd-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="349cd-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Total,Active,Report Date,Report Period
```
