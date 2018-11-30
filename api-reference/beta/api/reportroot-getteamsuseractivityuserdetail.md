---
title: 'reportRoot: getTeamsUserActivityUserDetail'
description: Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.
ms.openlocfilehash: a28848e94df9bfeb759277b92542cdf7626aad39
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082947"
---
# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="0497d-103">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="0497d-103">reportRoot: getTeamsUserActivityUserDetail</span></span>

> <span data-ttu-id="0497d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0497d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0497d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0497d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0497d-106">Obtenga información sobre la actividad de usuario de Microsoft Teams por usuario.</span><span class="sxs-lookup"><span data-stu-id="0497d-106">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="0497d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="0497d-107">Permissions</span></span>

<span data-ttu-id="0497d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0497d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="0497d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0497d-110">Permission type</span></span>                        | <span data-ttu-id="0497d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0497d-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="0497d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0497d-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="0497d-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0497d-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="0497d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0497d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0497d-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0497d-115">Not supported.</span></span>                           |
| <span data-ttu-id="0497d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0497d-116">Application</span></span>                            | <span data-ttu-id="0497d-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0497d-117">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="0497d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0497d-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='D7')
GET /reports/getTeamsUserActivityUserDetail(date=2017-09-01)
```

## <a name="function-parameters"></a><span data-ttu-id="0497d-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="0497d-119">Function parameters</span></span>

<span data-ttu-id="0497d-120">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="0497d-120">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="0497d-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0497d-121">Parameter</span></span> | <span data-ttu-id="0497d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="0497d-122">Type</span></span>   | <span data-ttu-id="0497d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="0497d-123">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="0497d-124">period</span><span class="sxs-lookup"><span data-stu-id="0497d-124">period</span></span>    | <span data-ttu-id="0497d-125">cadena</span><span class="sxs-lookup"><span data-stu-id="0497d-125">string</span></span> | <span data-ttu-id="0497d-126">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0497d-126">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="0497d-127">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="0497d-127">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="0497d-128">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0497d-128">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="0497d-129">date</span><span class="sxs-lookup"><span data-stu-id="0497d-129">date</span></span>      | <span data-ttu-id="0497d-130">Fecha</span><span class="sxs-lookup"><span data-stu-id="0497d-130">Date</span></span>   | <span data-ttu-id="0497d-131">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="0497d-131">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="0497d-132">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="0497d-132">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="0497d-133">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="0497d-133">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="0497d-134">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="0497d-134">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="0497d-135">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0497d-135">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="0497d-136">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="0497d-136">The default output type is text/csv.</span></span> <span data-ttu-id="0497d-137">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="0497d-137">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="0497d-138">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0497d-138">Request headers</span></span>

| <span data-ttu-id="0497d-139">Nombre</span><span class="sxs-lookup"><span data-stu-id="0497d-139">Name</span></span>          | <span data-ttu-id="0497d-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="0497d-140">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="0497d-141">Authorization</span><span class="sxs-lookup"><span data-stu-id="0497d-141">Authorization</span></span> | <span data-ttu-id="0497d-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0497d-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="0497d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0497d-144">Response</span></span>

### <a name="csv"></a><span data-ttu-id="0497d-145">CSV</span><span class="sxs-lookup"><span data-stu-id="0497d-145">CSV</span></span>

<span data-ttu-id="0497d-146">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="0497d-146">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="0497d-147">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0497d-147">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="0497d-148">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="0497d-148">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="0497d-149">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="0497d-149">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="0497d-150">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="0497d-150">Report Refresh Date</span></span>
- <span data-ttu-id="0497d-151">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="0497d-151">User Principal Name</span></span>
- <span data-ttu-id="0497d-152">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="0497d-152">Last Activity Date</span></span>
- <span data-ttu-id="0497d-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="0497d-153">Is Deleted</span></span>
- <span data-ttu-id="0497d-154">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="0497d-154">Deleted Date</span></span>
- <span data-ttu-id="0497d-155">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="0497d-155">Assigned Products</span></span>
- <span data-ttu-id="0497d-156">Recuento de mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="0497d-156">Team Chat Message Count</span></span>
- <span data-ttu-id="0497d-157">Recuento de mensajes de chat privado</span><span class="sxs-lookup"><span data-stu-id="0497d-157">Private Chat Message Count</span></span>
- <span data-ttu-id="0497d-158">Recuento de llamadas</span><span class="sxs-lookup"><span data-stu-id="0497d-158">Call Count</span></span>
- <span data-ttu-id="0497d-159">Recuento de reuniones</span><span class="sxs-lookup"><span data-stu-id="0497d-159">Meeting Count</span></span>
- <span data-ttu-id="0497d-160">Tiene otra acción</span><span class="sxs-lookup"><span data-stu-id="0497d-160">Has Other Action</span></span>
- <span data-ttu-id="0497d-161">Período del informe</span><span class="sxs-lookup"><span data-stu-id="0497d-161">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="0497d-162">JSON</span><span class="sxs-lookup"><span data-stu-id="0497d-162">JSON</span></span>

<span data-ttu-id="0497d-163">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsUserActivityUserDetail](../resources/teamsuseractivityuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0497d-163">If successful, this method returns a `200 OK` response code and a **[teamsUserActivityUserDetail](../resources/teamsuseractivityuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="0497d-164">El tamaño de página predeterminado para esta solicitud es 2.000 elementos.</span><span class="sxs-lookup"><span data-stu-id="0497d-164">The default page size for this request is 2000 items.</span></span>

## <a name="example"></a><span data-ttu-id="0497d-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0497d-165">Example</span></span>

### <a name="csv"></a><span data-ttu-id="0497d-166">CSV</span><span class="sxs-lookup"><span data-stu-id="0497d-166">CSV</span></span>

<span data-ttu-id="0497d-167">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="0497d-167">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="0497d-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0497d-168">Request</span></span>

<span data-ttu-id="0497d-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0497d-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="0497d-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0497d-170">Response</span></span>

<span data-ttu-id="0497d-171">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0497d-171">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="0497d-172">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="0497d-172">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```

### <a name="json"></a><span data-ttu-id="0497d-173">JSON</span><span class="sxs-lookup"><span data-stu-id="0497d-173">JSON</span></span>

<span data-ttu-id="0497d-174">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="0497d-174">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="0497d-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0497d-175">Request</span></span>

<span data-ttu-id="0497d-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0497d-176">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="0497d-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0497d-177">Response</span></span>

<span data-ttu-id="0497d-178">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0497d-178">The following is an example of the response.</span></span>

> <span data-ttu-id="0497d-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0497d-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsUserActivityUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 452

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsUserActivityUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userPrincipalName-value", 
      "lastActivityDate": "2017-09-01", 
      "isDeleted": false, 
      "deletedDate": null, 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5"
      ], 
      "teamChatMessageCount": 0, 
      "privateChatMessageCount": 49, 
      "callCount": 2, 
      "meetingCount": 0, 
      "hasOtherAction": true, 
      "reportPeriod": "7"
    }
  ]
}
```