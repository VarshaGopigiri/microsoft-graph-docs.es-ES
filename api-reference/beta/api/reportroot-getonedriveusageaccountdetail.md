---
title: 'reportRoot: getOneDriveUsageAccountDetail'
description: Obtiene información sobre el uso de OneDrive por cuenta.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 1aa7de008f1791908786111a87c1ab046df7f42e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960304"
---
# <a name="reportroot-getonedriveusageaccountdetail"></a><span data-ttu-id="0d2de-103">reportRoot: getOneDriveUsageAccountDetail</span><span class="sxs-lookup"><span data-stu-id="0d2de-103">reportRoot: getOneDriveUsageAccountDetail</span></span>

> <span data-ttu-id="0d2de-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0d2de-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0d2de-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0d2de-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0d2de-106">Obtiene información sobre el uso de OneDrive por cuenta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-106">Get details about OneDrive usage by account.</span></span>

> <span data-ttu-id="0d2de-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span><span class="sxs-lookup"><span data-stu-id="0d2de-107">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business usage](https://support.office.com/client/OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680).</span></span>

## <a name="permissions"></a><span data-ttu-id="0d2de-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="0d2de-108">Permissions</span></span>

<span data-ttu-id="0d2de-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0d2de-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0d2de-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0d2de-111">Permission type</span></span>                        | <span data-ttu-id="0d2de-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0d2de-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="0d2de-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0d2de-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="0d2de-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0d2de-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="0d2de-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0d2de-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0d2de-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0d2de-116">Not supported.</span></span>                           |
| <span data-ttu-id="0d2de-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0d2de-117">Application</span></span>                            | <span data-ttu-id="0d2de-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0d2de-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="0d2de-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d2de-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveUsageAccountDetail(period='{period_value}')
GET /reports/getOneDriveUsageAccountDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="0d2de-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="0d2de-120">Function parameters</span></span>

<span data-ttu-id="0d2de-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="0d2de-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="0d2de-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0d2de-122">Parameter</span></span> | <span data-ttu-id="0d2de-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d2de-123">Type</span></span>   | <span data-ttu-id="0d2de-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d2de-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="0d2de-125">period</span><span class="sxs-lookup"><span data-stu-id="0d2de-125">period</span></span>    | <span data-ttu-id="0d2de-126">cadena</span><span class="sxs-lookup"><span data-stu-id="0d2de-126">string</span></span> | <span data-ttu-id="0d2de-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0d2de-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="0d2de-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="0d2de-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="0d2de-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0d2de-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="0d2de-130">date</span><span class="sxs-lookup"><span data-stu-id="0d2de-130">date</span></span>      | <span data-ttu-id="0d2de-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="0d2de-131">Date</span></span>   | <span data-ttu-id="0d2de-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="0d2de-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="0d2de-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="0d2de-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="0d2de-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="0d2de-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="0d2de-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="0d2de-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="0d2de-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="0d2de-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="0d2de-137">The default output type is text/csv.</span></span> <span data-ttu-id="0d2de-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="0d2de-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0d2de-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2de-139">Request headers</span></span>

| <span data-ttu-id="0d2de-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d2de-140">Name</span></span>          | <span data-ttu-id="0d2de-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d2de-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="0d2de-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="0d2de-142">Authorization</span></span> | <span data-ttu-id="0d2de-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0d2de-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="0d2de-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d2de-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="0d2de-146">CSV</span><span class="sxs-lookup"><span data-stu-id="0d2de-146">CSV</span></span>

<span data-ttu-id="0d2de-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="0d2de-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="0d2de-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="0d2de-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="0d2de-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="0d2de-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="0d2de-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="0d2de-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="0d2de-151">Report Refresh Date</span></span>
- <span data-ttu-id="0d2de-152">Dirección URL del sitio</span><span class="sxs-lookup"><span data-stu-id="0d2de-152">Site URL</span></span>
- <span data-ttu-id="0d2de-153">Nombre para mostrar del propietario</span><span class="sxs-lookup"><span data-stu-id="0d2de-153">Owner Display Name</span></span>
- <span data-ttu-id="0d2de-154">Eliminado</span><span class="sxs-lookup"><span data-stu-id="0d2de-154">Is Deleted</span></span>
- <span data-ttu-id="0d2de-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="0d2de-155">Last Activity Date</span></span>
- <span data-ttu-id="0d2de-156">Número de archivos</span><span class="sxs-lookup"><span data-stu-id="0d2de-156">File Count</span></span>
- <span data-ttu-id="0d2de-157">Número de archivos activos</span><span class="sxs-lookup"><span data-stu-id="0d2de-157">Active File Count</span></span>
- <span data-ttu-id="0d2de-158">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="0d2de-158">Storage Used (Byte)</span></span>
- <span data-ttu-id="0d2de-159">Almacenamiento asignado (bytes)</span><span class="sxs-lookup"><span data-stu-id="0d2de-159">Storage Allocated (Byte)</span></span>
- <span data-ttu-id="0d2de-160">Período del informe</span><span class="sxs-lookup"><span data-stu-id="0d2de-160">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="0d2de-161">JSON</span><span class="sxs-lookup"><span data-stu-id="0d2de-161">JSON</span></span>

<span data-ttu-id="0d2de-162">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[oneDriveUsageAccountDetail](../resources/onedriveusageaccountdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-162">If successful, this method returns a `200 OK` response code and a **[oneDriveUsageAccountDetail](../resources/onedriveusageaccountdetail.md)** object in the response body.</span></span>

<span data-ttu-id="0d2de-163">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="0d2de-163">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="0d2de-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d2de-164">Example</span></span>

<span data-ttu-id="0d2de-165">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="0d2de-165">The following is an example that outputs CSV.</span></span>

### <a name="csv"></a><span data-ttu-id="0d2de-166">CSV</span><span class="sxs-lookup"><span data-stu-id="0d2de-166">CSV</span></span>

#### <a name="request"></a><span data-ttu-id="0d2de-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2de-167">Request</span></span>

<span data-ttu-id="0d2de-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d2de-168">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusageaccountdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageAccountDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="0d2de-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d2de-169">Response</span></span>

<span data-ttu-id="0d2de-170">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-170">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="0d2de-171">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="0d2de-171">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Site URL,Owner Display Name,Is Deleted,Last Activity Date,File Count,Active File Count,Storage Used (Byte),Storage Allocated (Byte),Report Period
```

### <a name="json"></a><span data-ttu-id="0d2de-172">JSON</span><span class="sxs-lookup"><span data-stu-id="0d2de-172">JSON</span></span>

<span data-ttu-id="0d2de-173">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="0d2de-173">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="0d2de-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d2de-174">Request</span></span>

<span data-ttu-id="0d2de-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d2de-175">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveusageaccountdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveUsageAccountDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="0d2de-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d2de-176">Response</span></span>

<span data-ttu-id="0d2de-177">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d2de-177">The following is an example of the response.</span></span>

> <span data-ttu-id="0d2de-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0d2de-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.oneDriveUsageAccountDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 400

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.oneDriveUsageAccountDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "siteUrl": "siteUrl-value", 
      "ownerDisplayName": "ownerDisplayName-value", 
      "isDeleted": false, 
      "lastActivityDate": "2017-09-01", 
      "fileCount": 9, 
      "activeFileCount": 5, 
      "storageUsedInBytes": 12190375, 
      "storageAllocatedInBytes": 549755813880, 
      "reportPeriod": "7"
    }
  ]
}
```
