---
title: 'reportRoot: getOneDriveActivityUserDetail'
description: Obtiene información sobre las actividades de OneDrive por usuario.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 660a42d597ce7878f1fa8a5cacaf5dc6b42e8438
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27969628"
---
# <a name="reportroot-getonedriveactivityuserdetail"></a><span data-ttu-id="6662a-103">reportRoot: getOneDriveActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="6662a-103">reportRoot: getOneDriveActivityUserDetail</span></span>

> <span data-ttu-id="6662a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6662a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6662a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6662a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6662a-106">Obtiene información sobre las actividades de OneDrive por usuario.</span><span class="sxs-lookup"><span data-stu-id="6662a-106">Get details about OneDrive activity by user.</span></span>

> <span data-ttu-id="6662a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="6662a-107">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="6662a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6662a-108">Permissions</span></span>

<span data-ttu-id="6662a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6662a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6662a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6662a-111">Permission type</span></span>                        | <span data-ttu-id="6662a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6662a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="6662a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6662a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="6662a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6662a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="6662a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6662a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6662a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6662a-116">Not supported.</span></span>                           |
| <span data-ttu-id="6662a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6662a-117">Application</span></span>                            | <span data-ttu-id="6662a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6662a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="6662a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6662a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveActivityUserDetail(period='{period_value}')
GET /reports/getOneDriveActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="6662a-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="6662a-120">Function parameters</span></span>

<span data-ttu-id="6662a-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="6662a-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="6662a-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6662a-122">Parameter</span></span> | <span data-ttu-id="6662a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6662a-123">Type</span></span>   | <span data-ttu-id="6662a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6662a-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="6662a-125">period</span><span class="sxs-lookup"><span data-stu-id="6662a-125">period</span></span>    | <span data-ttu-id="6662a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="6662a-126">string</span></span> | <span data-ttu-id="6662a-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6662a-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="6662a-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="6662a-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="6662a-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6662a-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="6662a-130">date</span><span class="sxs-lookup"><span data-stu-id="6662a-130">date</span></span>      | <span data-ttu-id="6662a-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="6662a-131">Date</span></span>   | <span data-ttu-id="6662a-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="6662a-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="6662a-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="6662a-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="6662a-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="6662a-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="6662a-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="6662a-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="6662a-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6662a-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="6662a-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="6662a-137">The default output type is text/csv.</span></span> <span data-ttu-id="6662a-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="6662a-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="6662a-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6662a-139">Request headers</span></span>

| <span data-ttu-id="6662a-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="6662a-140">Name</span></span>          | <span data-ttu-id="6662a-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="6662a-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="6662a-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="6662a-142">Authorization</span></span> | <span data-ttu-id="6662a-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6662a-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="6662a-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6662a-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="6662a-146">CSV</span><span class="sxs-lookup"><span data-stu-id="6662a-146">CSV</span></span>

<span data-ttu-id="6662a-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="6662a-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="6662a-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6662a-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="6662a-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="6662a-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="6662a-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="6662a-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="6662a-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="6662a-151">Report Refresh Date</span></span>
- <span data-ttu-id="6662a-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="6662a-152">User Principal Name</span></span>
- <span data-ttu-id="6662a-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="6662a-153">Is Deleted</span></span>
- <span data-ttu-id="6662a-154">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="6662a-154">Deleted Date</span></span>
- <span data-ttu-id="6662a-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="6662a-155">Last Activity Date</span></span>
- <span data-ttu-id="6662a-156">Número de archivos vistos o editados</span><span class="sxs-lookup"><span data-stu-id="6662a-156">Viewed Or Edited File Count</span></span>
- <span data-ttu-id="6662a-157">Número de archivos sincronizados</span><span class="sxs-lookup"><span data-stu-id="6662a-157">Synced File Count</span></span>
- <span data-ttu-id="6662a-158">Número de archivos compartidos internamente</span><span class="sxs-lookup"><span data-stu-id="6662a-158">Shared Internally File Count</span></span>
- <span data-ttu-id="6662a-159">Número de archivos compartidos externamente</span><span class="sxs-lookup"><span data-stu-id="6662a-159">Shared Externally File Count</span></span>
- <span data-ttu-id="6662a-160">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="6662a-160">Assigned Products</span></span>
- <span data-ttu-id="6662a-161">Período del informe</span><span class="sxs-lookup"><span data-stu-id="6662a-161">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="6662a-162">JSON</span><span class="sxs-lookup"><span data-stu-id="6662a-162">JSON</span></span>

<span data-ttu-id="6662a-163">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[oneDriveActivityUserDetail](../resources/onedriveactivityuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6662a-163">If successful, this method returns a `200 OK` response code and a **[oneDriveActivityUserDetail](../resources/onedriveactivityuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="6662a-164">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="6662a-164">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="6662a-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6662a-165">Example</span></span>

### <a name="csv"></a><span data-ttu-id="6662a-166">CSV</span><span class="sxs-lookup"><span data-stu-id="6662a-166">CSV</span></span>

<span data-ttu-id="6662a-167">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="6662a-167">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="6662a-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6662a-168">Request</span></span>

<span data-ttu-id="6662a-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6662a-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveactivityuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveActivityUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="6662a-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6662a-170">Response</span></span>

<span data-ttu-id="6662a-171">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6662a-171">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="6662a-172">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="6662a-172">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Viewed Or Edited File Count,Synced File Count,Shared Internally File Count,Shared Externally File Count,Assigned Products,Report Period
```

### <a name="json"></a><span data-ttu-id="6662a-173">JSON</span><span class="sxs-lookup"><span data-stu-id="6662a-173">JSON</span></span>

<span data-ttu-id="6662a-174">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="6662a-174">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="6662a-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6662a-175">Request</span></span>

<span data-ttu-id="6662a-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6662a-176">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveactivityuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveActivityUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="6662a-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6662a-177">Response</span></span>

<span data-ttu-id="6662a-178">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6662a-178">The following is an example of the response.</span></span>

> <span data-ttu-id="6662a-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6662a-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.oneDriveActivityUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 450

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.oneDriveActivityUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userPrincipalName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "lastActivityDate": "2017-09-01", 
      "viewedOrEditedFileCount": 1, 
      "syncedFileCount": 0, 
      "sharedInternallyFileCount": 0, 
      "sharedExternallyFileCount": 0, 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5"
      ], 
      "reportPeriod": "7"
    }
  ]
}
```
