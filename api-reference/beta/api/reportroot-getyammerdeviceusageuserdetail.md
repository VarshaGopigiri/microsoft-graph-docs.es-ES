---
title: 'reportRoot: función getYammerDeviceUsageUserDetail'
description: Obtiene información sobre el uso de dispositivos de Yammer por usuario.
localization_priority: Normal
ms.openlocfilehash: f5d1635d3e72cdc2f66ff437dd74fee4bb2cd8d5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868259"
---
# <a name="reportroot-getyammerdeviceusageuserdetail-function"></a><span data-ttu-id="e9699-103">reportRoot: función getYammerDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="e9699-103">reportRoot: getYammerDeviceUsageUserDetail function</span></span>

> <span data-ttu-id="e9699-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e9699-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e9699-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e9699-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e9699-106">Obtiene información sobre el uso de dispositivos de Yammer por usuario.</span><span class="sxs-lookup"><span data-stu-id="e9699-106">Get details about Yammer device usage by user.</span></span>

> <span data-ttu-id="e9699-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span><span class="sxs-lookup"><span data-stu-id="e9699-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="e9699-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e9699-108">Permissions</span></span>

<span data-ttu-id="e9699-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e9699-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e9699-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e9699-111">Permission type</span></span>                        | <span data-ttu-id="e9699-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e9699-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="e9699-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e9699-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="e9699-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9699-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="e9699-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e9699-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e9699-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e9699-116">Not supported.</span></span>                           |
| <span data-ttu-id="e9699-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e9699-117">Application</span></span>                            | <span data-ttu-id="e9699-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e9699-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e9699-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e9699-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageUserDetail(period='{period_value}')
GET /reports/getYammerDeviceUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="e9699-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e9699-120">Function parameters</span></span>

<span data-ttu-id="e9699-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="e9699-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="e9699-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e9699-122">Parameter</span></span> | <span data-ttu-id="e9699-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9699-123">Type</span></span>   | <span data-ttu-id="e9699-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9699-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="e9699-125">period</span><span class="sxs-lookup"><span data-stu-id="e9699-125">period</span></span>    | <span data-ttu-id="e9699-126">cadena</span><span class="sxs-lookup"><span data-stu-id="e9699-126">string</span></span> | <span data-ttu-id="e9699-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e9699-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="e9699-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="e9699-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="e9699-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e9699-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="e9699-130">date</span><span class="sxs-lookup"><span data-stu-id="e9699-130">date</span></span>      | <span data-ttu-id="e9699-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="e9699-131">Date</span></span>   | <span data-ttu-id="e9699-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="e9699-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="e9699-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="e9699-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="e9699-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="e9699-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="e9699-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="e9699-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="e9699-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9699-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="e9699-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="e9699-137">The default output type is text/csv.</span></span> <span data-ttu-id="e9699-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="e9699-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e9699-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e9699-139">Request headers</span></span>

| <span data-ttu-id="e9699-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="e9699-140">Name</span></span>          | <span data-ttu-id="e9699-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9699-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="e9699-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="e9699-142">Authorization</span></span> | <span data-ttu-id="e9699-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9699-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="e9699-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9699-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="e9699-146">CSV</span><span class="sxs-lookup"><span data-stu-id="e9699-146">CSV</span></span>

<span data-ttu-id="e9699-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="e9699-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="e9699-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9699-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="e9699-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="e9699-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="e9699-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="e9699-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="e9699-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="e9699-151">Report Refresh Date</span></span>
- <span data-ttu-id="e9699-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="e9699-152">User Principal Name</span></span>
- <span data-ttu-id="e9699-153">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="e9699-153">Display Name</span></span>
- <span data-ttu-id="e9699-154">Estado del usuario</span><span class="sxs-lookup"><span data-stu-id="e9699-154">User State</span></span>
- <span data-ttu-id="e9699-155">Fecha de cambio de estado</span><span class="sxs-lookup"><span data-stu-id="e9699-155">State Change Date</span></span>
- <span data-ttu-id="e9699-156">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="e9699-156">Last Activity Date</span></span>
- <span data-ttu-id="e9699-157">Web usada</span><span class="sxs-lookup"><span data-stu-id="e9699-157">Used Web</span></span>
- <span data-ttu-id="e9699-158">Windows Phone usado</span><span class="sxs-lookup"><span data-stu-id="e9699-158">Used Windows Phone</span></span>
- <span data-ttu-id="e9699-159">Teléfono Android usado</span><span class="sxs-lookup"><span data-stu-id="e9699-159">Used Android Phone</span></span>
- <span data-ttu-id="e9699-160">iPhone usado</span><span class="sxs-lookup"><span data-stu-id="e9699-160">Used iPhone</span></span>
- <span data-ttu-id="e9699-161">iPad usado</span><span class="sxs-lookup"><span data-stu-id="e9699-161">Used iPad</span></span>
- <span data-ttu-id="e9699-162">Otros usados</span><span class="sxs-lookup"><span data-stu-id="e9699-162">Used Others</span></span>
- <span data-ttu-id="e9699-163">Período del informe</span><span class="sxs-lookup"><span data-stu-id="e9699-163">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="e9699-164">JSON</span><span class="sxs-lookup"><span data-stu-id="e9699-164">JSON</span></span>

<span data-ttu-id="e9699-165">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerDeviceUsageUserDetail](../resources/yammerdeviceusageuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9699-165">If successful, this method returns a `200 OK` response code and a **[yammerDeviceUsageUserDetail](../resources/yammerdeviceusageuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="e9699-166">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="e9699-166">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="e9699-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e9699-167">Example</span></span>

### <a name="csv"></a><span data-ttu-id="e9699-168">CSV</span><span class="sxs-lookup"><span data-stu-id="e9699-168">CSV</span></span>

<span data-ttu-id="e9699-169">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="e9699-169">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="e9699-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9699-170">Request</span></span>

<span data-ttu-id="e9699-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9699-171">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusageuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="e9699-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9699-172">Response</span></span>

<span data-ttu-id="e9699-173">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9699-173">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="e9699-174">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9699-174">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,User State,State Change Date,Last Activity Date,Used Web,Used Windows Phone,Used Android Phone,Used iPhone,Used iPad,Used Others,Report Period
```

### <a name="json"></a><span data-ttu-id="e9699-175">JSON</span><span class="sxs-lookup"><span data-stu-id="e9699-175">JSON</span></span>

<span data-ttu-id="e9699-176">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="e9699-176">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="e9699-177">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e9699-177">Request</span></span>

<span data-ttu-id="e9699-178">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e9699-178">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusageuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="e9699-179">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e9699-179">Response</span></span>

<span data-ttu-id="e9699-180">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e9699-180">The following is an example of the response.</span></span>

> <span data-ttu-id="e9699-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e9699-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.yammerDeviceUsageUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 442

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.yammerDeviceUsageUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-06", 
      "userPrincipalName": "userPrincipalName-value", 
      "displayName": "displayName-value", 
      "userState": "active", 
      "stateChangeDate": "2012-06-26", 
      "lastActivityDate": "2017-09-06", 
      "usedWeb": true, 
      "usedWindowsPhone": false, 
      "usedAndroidPhone": false, 
      "usediPhone": false, 
      "usediPad": false, 
      "usedOthers": false, 
      "reportPeriod": "7"
    }
  ]
}
```
