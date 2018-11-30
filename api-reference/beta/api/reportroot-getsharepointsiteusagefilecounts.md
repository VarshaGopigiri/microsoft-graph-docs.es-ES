---
title: 'reportRoot: getSharePointSiteUsageFileCounts'
description: Obtiene el número total de archivos en todos los sitios y el número de archivos activos. Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.
ms.openlocfilehash: 06e44a5fcfa6213578b841a5f3c6638859b0706e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086014"
---
# <a name="reportroot-getsharepointsiteusagefilecounts"></a><span data-ttu-id="223b9-104">reportRoot: getSharePointSiteUsageFileCounts</span><span class="sxs-lookup"><span data-stu-id="223b9-104">reportRoot: getSharePointSiteUsageFileCounts</span></span>

> <span data-ttu-id="223b9-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="223b9-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="223b9-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="223b9-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="223b9-107">Obtiene el número total de archivos en todos los sitios y el número de archivos activos.</span><span class="sxs-lookup"><span data-stu-id="223b9-107">Get the total number of files across all sites and the number of active files.</span></span> <span data-ttu-id="223b9-108">Un archivo (usuario o sistema) se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="223b9-108">A file (user or system) is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span>

> <span data-ttu-id="223b9-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span><span class="sxs-lookup"><span data-stu-id="223b9-109">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint site usage](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span></span>

## <a name="permissions"></a><span data-ttu-id="223b9-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="223b9-110">Permissions</span></span>

<span data-ttu-id="223b9-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="223b9-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="223b9-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="223b9-113">Permission type</span></span>                        | <span data-ttu-id="223b9-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="223b9-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="223b9-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="223b9-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="223b9-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="223b9-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="223b9-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="223b9-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="223b9-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="223b9-118">Not supported.</span></span>                           |
| <span data-ttu-id="223b9-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="223b9-119">Application</span></span>                            | <span data-ttu-id="223b9-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="223b9-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="223b9-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="223b9-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointSiteUsageFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="223b9-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="223b9-122">Function parameters</span></span>

<span data-ttu-id="223b9-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="223b9-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="223b9-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="223b9-124">Parameter</span></span> | <span data-ttu-id="223b9-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="223b9-125">Type</span></span>   | <span data-ttu-id="223b9-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b9-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="223b9-127">period</span><span class="sxs-lookup"><span data-stu-id="223b9-127">period</span></span>    | <span data-ttu-id="223b9-128">cadena</span><span class="sxs-lookup"><span data-stu-id="223b9-128">string</span></span> | <span data-ttu-id="223b9-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="223b9-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="223b9-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="223b9-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="223b9-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="223b9-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="223b9-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="223b9-132">Required.</span></span> |

<span data-ttu-id="223b9-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223b9-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="223b9-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="223b9-134">The default output type is text/csv.</span></span> <span data-ttu-id="223b9-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="223b9-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="223b9-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="223b9-136">Request headers</span></span>

| <span data-ttu-id="223b9-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="223b9-137">Name</span></span>          | <span data-ttu-id="223b9-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="223b9-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="223b9-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="223b9-139">Authorization</span></span> | <span data-ttu-id="223b9-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="223b9-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="223b9-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="223b9-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="223b9-143">CSV</span><span class="sxs-lookup"><span data-stu-id="223b9-143">CSV</span></span>

<span data-ttu-id="223b9-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="223b9-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="223b9-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223b9-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="223b9-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="223b9-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="223b9-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="223b9-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="223b9-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="223b9-148">Report Refresh Date</span></span>
- <span data-ttu-id="223b9-149">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="223b9-149">Site Type</span></span>
- <span data-ttu-id="223b9-150">Total</span><span class="sxs-lookup"><span data-stu-id="223b9-150">Total</span></span>
- <span data-ttu-id="223b9-151">Activo</span><span class="sxs-lookup"><span data-stu-id="223b9-151">Active</span></span>
- <span data-ttu-id="223b9-152">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="223b9-152">Report Date</span></span>
- <span data-ttu-id="223b9-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="223b9-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="223b9-154">JSON</span><span class="sxs-lookup"><span data-stu-id="223b9-154">JSON</span></span>

<span data-ttu-id="223b9-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[sharePointSiteUsageFileCounts](../resources/sharepointsiteusagefilecounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223b9-155">If successful, this method returns a `200 OK` response code and a **[sharePointSiteUsageFileCounts](../resources/sharepointsiteusagefilecounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="223b9-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="223b9-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="223b9-157">CSV</span><span class="sxs-lookup"><span data-stu-id="223b9-157">CSV</span></span>

<span data-ttu-id="223b9-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="223b9-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="223b9-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="223b9-159">Request</span></span>

<span data-ttu-id="223b9-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="223b9-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointsiteusagefilecounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointSiteUsageFileCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="223b9-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="223b9-161">Response</span></span>

<span data-ttu-id="223b9-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223b9-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="223b9-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="223b9-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Type,Total,Active,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="223b9-164">JSON</span><span class="sxs-lookup"><span data-stu-id="223b9-164">JSON</span></span>

<span data-ttu-id="223b9-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="223b9-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="223b9-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="223b9-166">Request</span></span>

<span data-ttu-id="223b9-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="223b9-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointsiteusagefilecounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointSiteUsageFileCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="223b9-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="223b9-168">Response</span></span>

<span data-ttu-id="223b9-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="223b9-169">The following is an example of the response.</span></span>

> <span data-ttu-id="223b9-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="223b9-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharePointSiteUsageFileCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 255

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.sharePointSiteUsageFileCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "siteType": "All", 
      "total": 25687, 
      "active": 209, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```