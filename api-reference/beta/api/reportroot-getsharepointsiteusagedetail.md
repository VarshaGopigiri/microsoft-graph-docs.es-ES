---
title: 'reportRoot: getSharePointSiteUsageDetail'
description: Obtiene información sobre el uso del sitio de SharePoint.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 8d10d055a4dc3ae7de33d46200510a0c45315c09
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27942566"
---
# <a name="reportroot-getsharepointsiteusagedetail"></a><span data-ttu-id="22741-103">reportRoot: getSharePointSiteUsageDetail</span><span class="sxs-lookup"><span data-stu-id="22741-103">reportRoot: getSharePointSiteUsageDetail</span></span>

> <span data-ttu-id="22741-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="22741-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="22741-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="22741-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="22741-106">Obtiene información sobre el uso del sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="22741-106">Get details about SharePoint site usage.</span></span>

> <span data-ttu-id="22741-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de sitio de SharePoint](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span><span class="sxs-lookup"><span data-stu-id="22741-107">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint site usage](https://support.office.com/client/SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213).</span></span>

## <a name="permissions"></a><span data-ttu-id="22741-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="22741-108">Permissions</span></span>

<span data-ttu-id="22741-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="22741-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="22741-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="22741-111">Permission type</span></span>                        | <span data-ttu-id="22741-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="22741-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="22741-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="22741-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="22741-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="22741-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="22741-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="22741-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="22741-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="22741-116">Not supported.</span></span>                           |
| <span data-ttu-id="22741-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="22741-117">Application</span></span>                            | <span data-ttu-id="22741-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="22741-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="22741-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="22741-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointSiteUsageDetail(period='{period_value}')
GET /reports/getSharePointSiteUsageDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="22741-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="22741-120">Function parameters</span></span>

<span data-ttu-id="22741-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="22741-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="22741-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="22741-122">Parameter</span></span> | <span data-ttu-id="22741-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="22741-123">Type</span></span>   | <span data-ttu-id="22741-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="22741-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="22741-125">period</span><span class="sxs-lookup"><span data-stu-id="22741-125">period</span></span>    | <span data-ttu-id="22741-126">cadena</span><span class="sxs-lookup"><span data-stu-id="22741-126">string</span></span> | <span data-ttu-id="22741-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="22741-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="22741-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="22741-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="22741-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="22741-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="22741-130">date</span><span class="sxs-lookup"><span data-stu-id="22741-130">date</span></span>      | <span data-ttu-id="22741-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="22741-131">Date</span></span>   | <span data-ttu-id="22741-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="22741-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="22741-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="22741-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="22741-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="22741-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="22741-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="22741-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="22741-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22741-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="22741-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="22741-137">The default output type is text/csv.</span></span> <span data-ttu-id="22741-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="22741-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="22741-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="22741-139">Request headers</span></span>

| <span data-ttu-id="22741-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="22741-140">Name</span></span>          | <span data-ttu-id="22741-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="22741-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="22741-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="22741-142">Authorization</span></span> | <span data-ttu-id="22741-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="22741-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="22741-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22741-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="22741-146">CSV</span><span class="sxs-lookup"><span data-stu-id="22741-146">CSV</span></span>

<span data-ttu-id="22741-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="22741-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="22741-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22741-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="22741-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="22741-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="22741-150">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="22741-150">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="22741-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="22741-151">Report Refresh Date</span></span>
- <span data-ttu-id="22741-152">Identificador de sitio</span><span class="sxs-lookup"><span data-stu-id="22741-152">Site Id</span></span>
- <span data-ttu-id="22741-153">Dirección URL del sitio</span><span class="sxs-lookup"><span data-stu-id="22741-153">Site URL</span></span>
- <span data-ttu-id="22741-154">Nombre para mostrar del propietario</span><span class="sxs-lookup"><span data-stu-id="22741-154">Owner Display Name</span></span>
- <span data-ttu-id="22741-155">Eliminado</span><span class="sxs-lookup"><span data-stu-id="22741-155">Is Deleted</span></span>
- <span data-ttu-id="22741-156">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="22741-156">Last Activity Date</span></span>
- <span data-ttu-id="22741-157">Número de archivos</span><span class="sxs-lookup"><span data-stu-id="22741-157">File Count</span></span>
- <span data-ttu-id="22741-158">Número de archivos activos</span><span class="sxs-lookup"><span data-stu-id="22741-158">Active File Count</span></span>
- <span data-ttu-id="22741-159">Número de vistas de página</span><span class="sxs-lookup"><span data-stu-id="22741-159">Page View Count</span></span>
- <span data-ttu-id="22741-160">Número de páginas visitadas</span><span class="sxs-lookup"><span data-stu-id="22741-160">Visited Page Count</span></span>
- <span data-ttu-id="22741-161">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="22741-161">Storage Used (Byte)</span></span>
- <span data-ttu-id="22741-162">Almacenamiento asignado (bytes)</span><span class="sxs-lookup"><span data-stu-id="22741-162">Storage Allocated (Byte)</span></span>
- <span data-ttu-id="22741-163">Plantilla de web raíz</span><span class="sxs-lookup"><span data-stu-id="22741-163">Root Web Template</span></span>
- <span data-ttu-id="22741-164">Período del informe</span><span class="sxs-lookup"><span data-stu-id="22741-164">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="22741-165">JSON</span><span class="sxs-lookup"><span data-stu-id="22741-165">JSON</span></span>

<span data-ttu-id="22741-166">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[sharePointSiteUsageDetail](../resources/sharepointsiteusagedetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22741-166">If successful, this method returns a `200 OK` response code and a **[sharePointSiteUsageDetail](../resources/sharepointsiteusagedetail.md)** object in the response body.</span></span>

<span data-ttu-id="22741-167">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="22741-167">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="22741-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="22741-168">Example</span></span>

### <a name="csv"></a><span data-ttu-id="22741-169">CSV</span><span class="sxs-lookup"><span data-stu-id="22741-169">CSV</span></span>

<span data-ttu-id="22741-170">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="22741-170">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="22741-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22741-171">Request</span></span>

<span data-ttu-id="22741-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22741-172">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointsiteusagedetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointSiteUsageDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="22741-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22741-173">Response</span></span>

<span data-ttu-id="22741-174">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22741-174">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="22741-175">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="22741-175">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site Id,Site URL,Owner Display Name,Is Deleted,Last Activity Date,File Count,Active File Count,Page View Count,Visited Page Count,Storage Used (Byte),Storage Allocated (Byte),Root Web Template,Report Period
```

### <a name="json"></a><span data-ttu-id="22741-176">JSON</span><span class="sxs-lookup"><span data-stu-id="22741-176">JSON</span></span>

<span data-ttu-id="22741-177">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="22741-177">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="22741-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="22741-178">Request</span></span>

<span data-ttu-id="22741-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="22741-179">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointsiteusagedetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointSiteUsageDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="22741-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="22741-180">Response</span></span>

<span data-ttu-id="22741-181">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="22741-181">The following is an example of the response.</span></span>

> <span data-ttu-id="22741-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="22741-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharePointSiteUsageDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 484

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.sharePointSiteUsageDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "siteId": "siteId-value", 
      "siteUrl": "siteUrl-value", 
      "ownerDisplayName": "ownerDisplayName-value", 
      "isDeleted": false, 
      "lastActivityDate": "2017-09-01", 
      "fileCount": 170, 
      "activeFileCount": 25, 
      "pageViewCount": 7, 
      "visitedPageCount": 3, 
      "storageUsedInBytes": 63442116, 
      "storageAllocatedInBytes": 2748779094400, 
      "rootWebTemplate": "Publishing Site", 
      "reportPeriod": "7"
    }
  ]
}
```
