---
title: 'reportRoot: getOneDriveUsageAccountCounts'
description: Obtiene la tendencia sobre el número de sitios activos de OneDrive para la Empresa. Cualquier sitio en que los usuarios vieron, modificaron, cargaron, descargaron, compartieron o sincronizaron archivos se considera un sitio activo.
ms.openlocfilehash: e467fac8d6836df002e6c8f13cd3a9fab207b8c8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032681"
---
# <a name="reportroot-getonedriveusageaccountcounts"></a><span data-ttu-id="1e673-104">reportRoot: getOneDriveUsageAccountCounts</span><span class="sxs-lookup"><span data-stu-id="1e673-104">reportRoot: getOneDriveUsageAccountCounts</span></span>

<span data-ttu-id="1e673-105">Obtiene la tendencia sobre el número de sitios activos de OneDrive para la Empresa.</span><span class="sxs-lookup"><span data-stu-id="1e673-105">Get the trend in the number of active OneDrive for Business sites.</span></span> <span data-ttu-id="1e673-106">Cualquier sitio en que los usuarios vieron, modificaron, cargaron, descargaron, compartieron o sincronizaron archivos se considera un sitio activo.</span><span class="sxs-lookup"><span data-stu-id="1e673-106">Any site on which users viewed, modified, uploaded, downloaded, shared, or synced files is considered an active site.</span></span>

> <span data-ttu-id="1e673-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="1e673-107">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="1e673-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1e673-108">Permissions</span></span>

<span data-ttu-id="1e673-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1e673-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="1e673-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1e673-111">Permission type</span></span>                        | <span data-ttu-id="1e673-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1e673-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="1e673-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1e673-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="1e673-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="1e673-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="1e673-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1e673-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1e673-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1e673-116">Not supported.</span></span>                           |
| <span data-ttu-id="1e673-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1e673-117">Application</span></span>                            | <span data-ttu-id="1e673-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="1e673-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="1e673-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1e673-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageAccountCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="1e673-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="1e673-120">Function parameters</span></span>

<span data-ttu-id="1e673-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="1e673-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="1e673-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1e673-122">Parameter</span></span> | <span data-ttu-id="1e673-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e673-123">Type</span></span>   | <span data-ttu-id="1e673-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e673-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="1e673-125">period</span><span class="sxs-lookup"><span data-stu-id="1e673-125">period</span></span>    | <span data-ttu-id="1e673-126">cadena</span><span class="sxs-lookup"><span data-stu-id="1e673-126">string</span></span> | <span data-ttu-id="1e673-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1e673-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="1e673-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="1e673-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="1e673-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="1e673-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="1e673-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="1e673-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="1e673-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1e673-131">Request headers</span></span>

| <span data-ttu-id="1e673-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e673-132">Name</span></span>          | <span data-ttu-id="1e673-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e673-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="1e673-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="1e673-134">Authorization</span></span> | <span data-ttu-id="1e673-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1e673-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="1e673-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="1e673-137">If-None-Match</span></span> | <span data-ttu-id="1e673-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="1e673-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="1e673-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1e673-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="1e673-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e673-140">Response</span></span>

<span data-ttu-id="1e673-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="1e673-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="1e673-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e673-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="1e673-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="1e673-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="1e673-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="1e673-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="1e673-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="1e673-145">Report Refresh Date</span></span>
- <span data-ttu-id="1e673-146">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="1e673-146">Site Type</span></span>
- <span data-ttu-id="1e673-147">Total</span><span class="sxs-lookup"><span data-stu-id="1e673-147">Total</span></span>
- <span data-ttu-id="1e673-148">Activo</span><span class="sxs-lookup"><span data-stu-id="1e673-148">Active</span></span>
- <span data-ttu-id="1e673-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="1e673-149">Report Date</span></span>
- <span data-ttu-id="1e673-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="1e673-150">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="1e673-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e673-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="1e673-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1e673-152">Request</span></span>

<span data-ttu-id="1e673-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1e673-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveusageaccountcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveUsageAccountCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="1e673-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1e673-154">Response</span></span>

<span data-ttu-id="1e673-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1e673-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="1e673-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="1e673-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Total,Active,Report Date,Report Period
```