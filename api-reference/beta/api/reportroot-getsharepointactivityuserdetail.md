---
title: 'reportRoot: getSharePointActivityUserDetail'
description: Obtiene información sobre la actividad de SharePoint por usuario.
ms.openlocfilehash: 068fa24b1a906802294c050130424a9ac521501d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088507"
---
# <a name="reportroot-getsharepointactivityuserdetail"></a><span data-ttu-id="88150-103">reportRoot: getSharePointActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="88150-103">reportRoot: getSharePointActivityUserDetail</span></span>

> <span data-ttu-id="88150-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="88150-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="88150-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="88150-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="88150-106">Obtiene información sobre la actividad de SharePoint por usuario.</span><span class="sxs-lookup"><span data-stu-id="88150-106">Get details about SharePoint activity by user.</span></span>

> <span data-ttu-id="88150-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span><span class="sxs-lookup"><span data-stu-id="88150-107">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint activity](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span></span>

## <a name="permissions"></a><span data-ttu-id="88150-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="88150-108">Permissions</span></span>

<span data-ttu-id="88150-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="88150-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="88150-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88150-111">Permission type</span></span>                        | <span data-ttu-id="88150-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88150-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="88150-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88150-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="88150-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="88150-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="88150-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88150-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88150-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="88150-116">Not supported.</span></span>                           |
| <span data-ttu-id="88150-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88150-117">Application</span></span>                            | <span data-ttu-id="88150-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="88150-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="88150-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88150-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointActivityUserDetail(period='{period_value}')
GET /reports/getSharePointActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="88150-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="88150-120">Function parameters</span></span>

<span data-ttu-id="88150-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="88150-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="88150-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="88150-122">Parameter</span></span> | <span data-ttu-id="88150-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="88150-123">Type</span></span>   | <span data-ttu-id="88150-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="88150-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="88150-125">period</span><span class="sxs-lookup"><span data-stu-id="88150-125">period</span></span>    | <span data-ttu-id="88150-126">cadena</span><span class="sxs-lookup"><span data-stu-id="88150-126">string</span></span> | <span data-ttu-id="88150-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="88150-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="88150-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="88150-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="88150-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="88150-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="88150-130">date</span><span class="sxs-lookup"><span data-stu-id="88150-130">date</span></span>      | <span data-ttu-id="88150-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="88150-131">Date</span></span>   | <span data-ttu-id="88150-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="88150-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="88150-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="88150-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="88150-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="88150-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="88150-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="88150-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="88150-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88150-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="88150-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="88150-137">The default output type is text/csv.</span></span> <span data-ttu-id="88150-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="88150-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="88150-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88150-139">Request headers</span></span>

| <span data-ttu-id="88150-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="88150-140">Name</span></span>          | <span data-ttu-id="88150-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="88150-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="88150-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="88150-142">Authorization</span></span> | <span data-ttu-id="88150-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88150-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="88150-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88150-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="88150-146">CSV</span><span class="sxs-lookup"><span data-stu-id="88150-146">CSV</span></span>

<span data-ttu-id="88150-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="88150-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="88150-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88150-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="88150-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="88150-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="88150-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="88150-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="88150-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="88150-151">Report Refresh Date</span></span>
- <span data-ttu-id="88150-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="88150-152">User Principal Name</span></span>
- <span data-ttu-id="88150-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="88150-153">Is Deleted</span></span>
- <span data-ttu-id="88150-154">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="88150-154">Deleted Date</span></span>
- <span data-ttu-id="88150-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="88150-155">Last Activity Date</span></span>
- <span data-ttu-id="88150-156">Número de archivos vistos o editados</span><span class="sxs-lookup"><span data-stu-id="88150-156">Viewed Or Edited File Count</span></span>
- <span data-ttu-id="88150-157">Número de archivos sincronizados</span><span class="sxs-lookup"><span data-stu-id="88150-157">Synced File Count</span></span>
- <span data-ttu-id="88150-158">Número de archivos compartidos internamente</span><span class="sxs-lookup"><span data-stu-id="88150-158">Shared Internally File Count</span></span>
- <span data-ttu-id="88150-159">Número de archivos compartidos externamente</span><span class="sxs-lookup"><span data-stu-id="88150-159">Shared Externally File Count</span></span>
- <span data-ttu-id="88150-160">Número de páginas visitadas</span><span class="sxs-lookup"><span data-stu-id="88150-160">Visited Page Count</span></span>
- <span data-ttu-id="88150-161">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="88150-161">Assigned Products</span></span>
- <span data-ttu-id="88150-162">Período del informe</span><span class="sxs-lookup"><span data-stu-id="88150-162">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="88150-163">JSON</span><span class="sxs-lookup"><span data-stu-id="88150-163">JSON</span></span>

<span data-ttu-id="88150-164">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[sharePointActivityUserDetail](../resources/sharepointactivityuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88150-164">If successful, this method returns a `200 OK` response code and a **[sharePointActivityUserDetail](../resources/sharepointactivityuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="88150-165">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="88150-165">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="88150-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88150-166">Example</span></span>

### <a name="csv"></a><span data-ttu-id="88150-167">CSV</span><span class="sxs-lookup"><span data-stu-id="88150-167">CSV</span></span>

<span data-ttu-id="88150-168">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="88150-168">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="88150-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88150-169">Request</span></span>

<span data-ttu-id="88150-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88150-170">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivityuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="88150-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88150-171">Response</span></span>

<span data-ttu-id="88150-172">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88150-172">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="88150-173">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="88150-173">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Viewed Or Edited File Count,Synced File Count,Shared Internally File Count,Shared Externally File Count,Visited Page Count,Assigned Products,Report Period
```

### <a name="json"></a><span data-ttu-id="88150-174">JSON</span><span class="sxs-lookup"><span data-stu-id="88150-174">JSON</span></span>

<span data-ttu-id="88150-175">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="88150-175">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="88150-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88150-176">Request</span></span>

<span data-ttu-id="88150-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88150-177">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivityuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="88150-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88150-178">Response</span></span>

<span data-ttu-id="88150-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88150-179">The following is an example of the response.</span></span>

> <span data-ttu-id="88150-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88150-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharePointActivityUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 473

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.sharePointActivityUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userPrincipalName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "lastActivityDate": "2017-09-01", 
      "viewedOrEditedFileCount": 4, 
      "syncedFileCount": 0, 
      "sharedInternallyFileCount": 0, 
      "sharedExternallyFileCount": 0, 
      "visitedPageCount": 1, 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5"
      ], 
      "reportPeriod": "7"
    }
  ]
}
```