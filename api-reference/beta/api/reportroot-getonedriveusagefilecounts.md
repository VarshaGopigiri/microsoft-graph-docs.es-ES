---
title: 'reportRoot: getOneDriveUsageFileCounts'
description: Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos. Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.
localization_priority: Normal
ms.openlocfilehash: dc42e6e12171c0f7fe5b26886b06ec694af68878
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883310"
---
# <a name="reportroot-getonedriveusagefilecounts"></a><span data-ttu-id="e9e63-104">reportRoot: getOneDriveUsageFileCounts</span><span class="sxs-lookup"><span data-stu-id="e9e63-104">reportRoot: getOneDriveUsageFileCounts</span></span>

> <span data-ttu-id="e9e63-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9e63-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9e63-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9e63-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9e63-107">Obtiene el número total de archivos en todos los sitios y cuántos son archivos activos.</span><span class="sxs-lookup"><span data-stu-id="e9e63-107">Get the total number of files across all sites and how many are active files.</span></span> <span data-ttu-id="e9e63-108">Un archivo se considera activo si se guardó, sincronizó, modificó o compartió dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="e9e63-108">A file is considered active if it has been saved, synced, modified, or shared within the specified time period.</span></span>

> <span data-ttu-id="e9e63-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="e9e63-109">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="e9e63-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9e63-110">Permissions</span></span>

<span data-ttu-id="e9e63-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9e63-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e9e63-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9e63-113">Permission type</span></span>                        | <span data-ttu-id="e9e63-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9e63-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="e9e63-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9e63-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="e9e63-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9e63-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="e9e63-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9e63-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9e63-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9e63-118">Not supported.</span></span>                           |
| <span data-ttu-id="e9e63-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9e63-119">Application</span></span>                            | <span data-ttu-id="e9e63-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9e63-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e9e63-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9e63-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="e9e63-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e9e63-122">Function parameters</span></span>

<span data-ttu-id="e9e63-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="e9e63-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="e9e63-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e9e63-124">Parameter</span></span> | <span data-ttu-id="e9e63-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9e63-125">Type</span></span>   | <span data-ttu-id="e9e63-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9e63-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="e9e63-127">period</span><span class="sxs-lookup"><span data-stu-id="e9e63-127">period</span></span>    | <span data-ttu-id="e9e63-128">cadena</span><span class="sxs-lookup"><span data-stu-id="e9e63-128">string</span></span> | <span data-ttu-id="e9e63-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e9e63-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="e9e63-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="e9e63-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="e9e63-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e9e63-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="e9e63-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e9e63-132">Required.</span></span> |

<span data-ttu-id="e9e63-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e63-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="e9e63-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="e9e63-134">The default output type is text/csv.</span></span> <span data-ttu-id="e9e63-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="e9e63-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e9e63-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e63-136">Request headers</span></span>

| <span data-ttu-id="e9e63-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9e63-137">Name</span></span>          | <span data-ttu-id="e9e63-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9e63-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="e9e63-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9e63-139">Authorization</span></span> | <span data-ttu-id="e9e63-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9e63-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="e9e63-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e63-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="e9e63-143">CSV</span><span class="sxs-lookup"><span data-stu-id="e9e63-143">CSV</span></span>

<span data-ttu-id="e9e63-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="e9e63-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="e9e63-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e63-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="e9e63-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="e9e63-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="e9e63-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="e9e63-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="e9e63-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="e9e63-148">Report Refresh Date</span></span>
- <span data-ttu-id="e9e63-149">Tipo de sitio</span><span class="sxs-lookup"><span data-stu-id="e9e63-149">Site Type</span></span>
- <span data-ttu-id="e9e63-150">Total</span><span class="sxs-lookup"><span data-stu-id="e9e63-150">Total</span></span>
- <span data-ttu-id="e9e63-151">Activo</span><span class="sxs-lookup"><span data-stu-id="e9e63-151">Active</span></span>
- <span data-ttu-id="e9e63-152">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="e9e63-152">Report Date</span></span>
- <span data-ttu-id="e9e63-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="e9e63-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="e9e63-154">JSON</span><span class="sxs-lookup"><span data-stu-id="e9e63-154">JSON</span></span>

<span data-ttu-id="e9e63-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[oneDriveUsageFileCounts](../resources/onedriveusagefilecounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e63-155">If successful, this method returns a `200 OK` response code and a **[oneDriveUsageFileCounts](../resources/onedriveusagefilecounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e9e63-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9e63-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="e9e63-157">CSV</span><span class="sxs-lookup"><span data-stu-id="e9e63-157">CSV</span></span>

<span data-ttu-id="e9e63-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="e9e63-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="e9e63-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e63-159">Request</span></span>

<span data-ttu-id="e9e63-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9e63-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusagefilecounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageFileCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="e9e63-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e63-161">Response</span></span>

<span data-ttu-id="e9e63-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e63-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="e9e63-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9e63-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

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

### <a name="json"></a><span data-ttu-id="e9e63-164">JSON</span><span class="sxs-lookup"><span data-stu-id="e9e63-164">JSON</span></span>

<span data-ttu-id="e9e63-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="e9e63-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="e9e63-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9e63-166">Request</span></span>

<span data-ttu-id="e9e63-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9e63-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusagefilecounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageFileCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="e9e63-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9e63-168">Response</span></span>

<span data-ttu-id="e9e63-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9e63-169">The following is an example of the response.</span></span>

> <span data-ttu-id="e9e63-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9e63-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.oneDriveUsageFileCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 251

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.oneDriveUsageFileCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "siteType": "All", 
      "total": 297960, 
      "active": 4679, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
