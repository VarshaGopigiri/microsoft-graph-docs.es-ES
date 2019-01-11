---
title: 'reportRoot: getYammerGroupsActivityDetail'
description: Obtiene información sobre la actividad de grupos de Yammer por grupo.
localization_priority: Normal
ms.openlocfilehash: 8329125c2bc1b1de5716668675d50c796c81039b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853602"
---
# <a name="reportroot-getyammergroupsactivitydetail"></a><span data-ttu-id="e168a-103">reportRoot: getYammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="e168a-103">reportRoot: getYammerGroupsActivityDetail</span></span>

> <span data-ttu-id="e168a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e168a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e168a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e168a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e168a-106">Obtiene información sobre la actividad de grupos de Yammer por grupo.</span><span class="sxs-lookup"><span data-stu-id="e168a-106">Get details about Yammer groups activity by group.</span></span>

> <span data-ttu-id="e168a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="e168a-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="e168a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e168a-108">Permissions</span></span>

<span data-ttu-id="e168a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e168a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e168a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e168a-111">Permission type</span></span>                        | <span data-ttu-id="e168a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e168a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="e168a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e168a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="e168a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e168a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="e168a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e168a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e168a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e168a-116">Not supported.</span></span>                           |
| <span data-ttu-id="e168a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e168a-117">Application</span></span>                            | <span data-ttu-id="e168a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e168a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e168a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e168a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityDetail(period='{period_value}')
GET /reports/getYammerGroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="e168a-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e168a-120">Function parameters</span></span>

<span data-ttu-id="e168a-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="e168a-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="e168a-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e168a-122">Parameter</span></span> | <span data-ttu-id="e168a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e168a-123">Type</span></span>   | <span data-ttu-id="e168a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e168a-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="e168a-125">period</span><span class="sxs-lookup"><span data-stu-id="e168a-125">period</span></span>    | <span data-ttu-id="e168a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="e168a-126">string</span></span> | <span data-ttu-id="e168a-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e168a-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="e168a-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="e168a-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="e168a-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e168a-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="e168a-130">date</span><span class="sxs-lookup"><span data-stu-id="e168a-130">date</span></span>      | <span data-ttu-id="e168a-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="e168a-131">Date</span></span>   | <span data-ttu-id="e168a-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="e168a-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="e168a-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="e168a-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="e168a-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="e168a-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="e168a-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="e168a-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="e168a-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e168a-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="e168a-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="e168a-137">The default output type is text/csv.</span></span> <span data-ttu-id="e168a-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="e168a-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e168a-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e168a-139">Request headers</span></span>

| <span data-ttu-id="e168a-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="e168a-140">Name</span></span>          | <span data-ttu-id="e168a-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="e168a-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="e168a-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="e168a-142">Authorization</span></span> | <span data-ttu-id="e168a-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e168a-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="e168a-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e168a-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="e168a-146">CSV</span><span class="sxs-lookup"><span data-stu-id="e168a-146">CSV</span></span>

<span data-ttu-id="e168a-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="e168a-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="e168a-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e168a-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="e168a-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="e168a-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="e168a-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="e168a-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="e168a-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="e168a-151">Report Refresh Date</span></span>
- <span data-ttu-id="e168a-152">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="e168a-152">Group Display Name</span></span>
- <span data-ttu-id="e168a-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="e168a-153">Is Deleted</span></span>
- <span data-ttu-id="e168a-154">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="e168a-154">Owner Principal Name</span></span>
- <span data-ttu-id="e168a-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="e168a-155">Last Activity Date</span></span>
- <span data-ttu-id="e168a-156">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="e168a-156">Group Type</span></span>
- <span data-ttu-id="e168a-157">Office 365 conectado</span><span class="sxs-lookup"><span data-stu-id="e168a-157">Office 365 Connected</span></span>
- <span data-ttu-id="e168a-158">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="e168a-158">Member Count</span></span>
- <span data-ttu-id="e168a-159">Número de publicaciones</span><span class="sxs-lookup"><span data-stu-id="e168a-159">Posted Count</span></span>
- <span data-ttu-id="e168a-160">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="e168a-160">Read Count</span></span>
- <span data-ttu-id="e168a-161">Número de etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="e168a-161">Liked Count</span></span>
- <span data-ttu-id="e168a-162">Período del informe</span><span class="sxs-lookup"><span data-stu-id="e168a-162">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="e168a-163">JSON</span><span class="sxs-lookup"><span data-stu-id="e168a-163">JSON</span></span>

<span data-ttu-id="e168a-164">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerGroupsActivityDetail](../resources/yammergroupsactivitydetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e168a-164">If successful, this method returns a `200 OK` response code and a **[yammerGroupsActivityDetail](../resources/yammergroupsactivitydetail.md)** object in the response body.</span></span>

<span data-ttu-id="e168a-165">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="e168a-165">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="e168a-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e168a-166">Example</span></span>

### <a name="csv"></a><span data-ttu-id="e168a-167">CSV</span><span class="sxs-lookup"><span data-stu-id="e168a-167">CSV</span></span>

<span data-ttu-id="e168a-168">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="e168a-168">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="e168a-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e168a-169">Request</span></span>

<span data-ttu-id="e168a-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e168a-170">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitydetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="e168a-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e168a-171">Response</span></span>

<span data-ttu-id="e168a-172">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e168a-172">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="e168a-173">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="e168a-173">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Office 365 Connected,Member Count,Posted Count,Read Count,Liked Count,Report Period
```

### <a name="json"></a><span data-ttu-id="e168a-174">JSON</span><span class="sxs-lookup"><span data-stu-id="e168a-174">JSON</span></span>

<span data-ttu-id="e168a-175">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="e168a-175">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="e168a-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e168a-176">Request</span></span>

<span data-ttu-id="e168a-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e168a-177">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitydetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="e168a-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e168a-178">Response</span></span>

<span data-ttu-id="e168a-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e168a-179">The following is an example of the response.</span></span>

> <span data-ttu-id="e168a-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e168a-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.yammerGroupsActivityDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 441

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.yammerGroupsActivityDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "groupDisplayName": "groupDisplayName-value", 
      "isDeleted": false, 
      "ownerPrincipalName": "ownerPrincipalName-value", 
      "lastActivityDate": "2017-08-30", 
      "groupType": "private", 
      "office365Connected": true, 
      "memberCount": 176, 
      "postedCount": 15, 
      "readCount": 24, 
      "likedCount": 3, 
      "reportPeriod": "7"
    }
  ]
}
```
