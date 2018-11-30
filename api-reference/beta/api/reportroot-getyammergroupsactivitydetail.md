---
title: 'reportRoot: getYammerGroupsActivityDetail'
description: Obtiene información sobre la actividad de grupos de Yammer por grupo.
ms.openlocfilehash: c13e7160d667d479f4f4ecf17287934bb9c78aa5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083454"
---
# <a name="reportroot-getyammergroupsactivitydetail"></a><span data-ttu-id="38e71-103">reportRoot: getYammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="38e71-103">reportRoot: getYammerGroupsActivityDetail</span></span>

> <span data-ttu-id="38e71-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38e71-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38e71-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38e71-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="38e71-106">Obtiene información sobre la actividad de grupos de Yammer por grupo.</span><span class="sxs-lookup"><span data-stu-id="38e71-106">Get details about Yammer groups activity by group.</span></span>

> <span data-ttu-id="38e71-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="38e71-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="38e71-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="38e71-108">Permissions</span></span>

<span data-ttu-id="38e71-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38e71-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="38e71-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38e71-111">Permission type</span></span>                        | <span data-ttu-id="38e71-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38e71-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="38e71-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38e71-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="38e71-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="38e71-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="38e71-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38e71-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="38e71-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38e71-116">Not supported.</span></span>                           |
| <span data-ttu-id="38e71-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38e71-117">Application</span></span>                            | <span data-ttu-id="38e71-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="38e71-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="38e71-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38e71-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityDetail(period='{period_value}')
GET /reports/getYammerGroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="38e71-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="38e71-120">Function parameters</span></span>

<span data-ttu-id="38e71-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="38e71-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="38e71-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="38e71-122">Parameter</span></span> | <span data-ttu-id="38e71-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="38e71-123">Type</span></span>   | <span data-ttu-id="38e71-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="38e71-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="38e71-125">period</span><span class="sxs-lookup"><span data-stu-id="38e71-125">period</span></span>    | <span data-ttu-id="38e71-126">cadena</span><span class="sxs-lookup"><span data-stu-id="38e71-126">string</span></span> | <span data-ttu-id="38e71-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="38e71-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="38e71-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="38e71-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="38e71-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="38e71-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="38e71-130">date</span><span class="sxs-lookup"><span data-stu-id="38e71-130">date</span></span>      | <span data-ttu-id="38e71-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="38e71-131">Date</span></span>   | <span data-ttu-id="38e71-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="38e71-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="38e71-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="38e71-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="38e71-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="38e71-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="38e71-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="38e71-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="38e71-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38e71-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="38e71-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="38e71-137">The default output type is text/csv.</span></span> <span data-ttu-id="38e71-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="38e71-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="38e71-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38e71-139">Request headers</span></span>

| <span data-ttu-id="38e71-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="38e71-140">Name</span></span>          | <span data-ttu-id="38e71-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="38e71-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="38e71-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="38e71-142">Authorization</span></span> | <span data-ttu-id="38e71-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="38e71-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="38e71-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38e71-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="38e71-146">CSV</span><span class="sxs-lookup"><span data-stu-id="38e71-146">CSV</span></span>

<span data-ttu-id="38e71-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="38e71-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="38e71-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38e71-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="38e71-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="38e71-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="38e71-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="38e71-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="38e71-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="38e71-151">Report Refresh Date</span></span>
- <span data-ttu-id="38e71-152">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="38e71-152">Group Display Name</span></span>
- <span data-ttu-id="38e71-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="38e71-153">Is Deleted</span></span>
- <span data-ttu-id="38e71-154">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="38e71-154">Owner Principal Name</span></span>
- <span data-ttu-id="38e71-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="38e71-155">Last Activity Date</span></span>
- <span data-ttu-id="38e71-156">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="38e71-156">Group Type</span></span>
- <span data-ttu-id="38e71-157">Office 365 conectado</span><span class="sxs-lookup"><span data-stu-id="38e71-157">Office 365 Connected</span></span>
- <span data-ttu-id="38e71-158">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="38e71-158">Member Count</span></span>
- <span data-ttu-id="38e71-159">Número de publicaciones</span><span class="sxs-lookup"><span data-stu-id="38e71-159">Posted Count</span></span>
- <span data-ttu-id="38e71-160">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="38e71-160">Read Count</span></span>
- <span data-ttu-id="38e71-161">Número de etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="38e71-161">Liked Count</span></span>
- <span data-ttu-id="38e71-162">Período del informe</span><span class="sxs-lookup"><span data-stu-id="38e71-162">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="38e71-163">JSON</span><span class="sxs-lookup"><span data-stu-id="38e71-163">JSON</span></span>

<span data-ttu-id="38e71-164">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerGroupsActivityDetail](../resources/yammergroupsactivitydetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38e71-164">If successful, this method returns a `200 OK` response code and a **[yammerGroupsActivityDetail](../resources/yammergroupsactivitydetail.md)** object in the response body.</span></span>

<span data-ttu-id="38e71-165">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="38e71-165">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="38e71-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38e71-166">Example</span></span>

### <a name="csv"></a><span data-ttu-id="38e71-167">CSV</span><span class="sxs-lookup"><span data-stu-id="38e71-167">CSV</span></span>

<span data-ttu-id="38e71-168">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="38e71-168">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="38e71-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38e71-169">Request</span></span>

<span data-ttu-id="38e71-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38e71-170">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitydetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="38e71-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38e71-171">Response</span></span>

<span data-ttu-id="38e71-172">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38e71-172">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="38e71-173">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="38e71-173">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

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

### <a name="json"></a><span data-ttu-id="38e71-174">JSON</span><span class="sxs-lookup"><span data-stu-id="38e71-174">JSON</span></span>

<span data-ttu-id="38e71-175">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="38e71-175">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="38e71-176">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38e71-176">Request</span></span>

<span data-ttu-id="38e71-177">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38e71-177">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitydetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="38e71-178">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38e71-178">Response</span></span>

<span data-ttu-id="38e71-179">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38e71-179">The following is an example of the response.</span></span>

> <span data-ttu-id="38e71-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38e71-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
