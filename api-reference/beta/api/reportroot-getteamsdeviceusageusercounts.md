---
title: 'reportRoot: getTeamsDeviceUsageUserCounts'
description: Obtenga el número de usuarios únicos diario de Microsoft Teams por tipo de dispositivo.
ms.openlocfilehash: f672e434588f4a9d9a80ddb72bbd80e36c134b5e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091218"
---
# <a name="reportroot-getteamsdeviceusageusercounts"></a><span data-ttu-id="66ac2-103">reportRoot: getTeamsDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="66ac2-103">reportRoot: getTeamsDeviceUsageUserCounts</span></span>

> <span data-ttu-id="66ac2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66ac2-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66ac2-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66ac2-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="66ac2-106">Obtenga el número de usuarios únicos diario de Microsoft Teams por tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66ac2-106">Get the number of Microsoft Teams daily unique users by device type.</span></span>

## <a name="permissions"></a><span data-ttu-id="66ac2-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="66ac2-107">Permissions</span></span>

<span data-ttu-id="66ac2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66ac2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="66ac2-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66ac2-110">Permission type</span></span>                        | <span data-ttu-id="66ac2-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66ac2-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="66ac2-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66ac2-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="66ac2-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="66ac2-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="66ac2-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66ac2-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66ac2-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66ac2-115">Not supported.</span></span>                           |
| <span data-ttu-id="66ac2-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66ac2-116">Application</span></span>                            | <span data-ttu-id="66ac2-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="66ac2-117">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="66ac2-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66ac2-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageUserCounts(period='D7')
```

## <a name="function-parameters"></a><span data-ttu-id="66ac2-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="66ac2-119">Function parameters</span></span>

<span data-ttu-id="66ac2-120">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="66ac2-120">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="66ac2-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="66ac2-121">Parameter</span></span> | <span data-ttu-id="66ac2-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="66ac2-122">Type</span></span>   | <span data-ttu-id="66ac2-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ac2-123">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="66ac2-124">period</span><span class="sxs-lookup"><span data-stu-id="66ac2-124">period</span></span>    | <span data-ttu-id="66ac2-125">cadena</span><span class="sxs-lookup"><span data-stu-id="66ac2-125">string</span></span> | <span data-ttu-id="66ac2-126">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="66ac2-126">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="66ac2-127">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="66ac2-127">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="66ac2-128">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="66ac2-128">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="66ac2-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="66ac2-129">Required.</span></span> |

<span data-ttu-id="66ac2-130">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ac2-130">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="66ac2-131">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="66ac2-131">The default output type is text/csv.</span></span> <span data-ttu-id="66ac2-132">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="66ac2-132">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="66ac2-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66ac2-133">Request headers</span></span>

| <span data-ttu-id="66ac2-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="66ac2-134">Name</span></span>          | <span data-ttu-id="66ac2-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ac2-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="66ac2-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="66ac2-136">Authorization</span></span> | <span data-ttu-id="66ac2-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66ac2-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="66ac2-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66ac2-139">Response</span></span>

### <a name="csv"></a><span data-ttu-id="66ac2-140">CSV</span><span class="sxs-lookup"><span data-stu-id="66ac2-140">CSV</span></span>

<span data-ttu-id="66ac2-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="66ac2-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="66ac2-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ac2-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="66ac2-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="66ac2-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="66ac2-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="66ac2-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="66ac2-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="66ac2-145">Report Refresh Date</span></span>
- <span data-ttu-id="66ac2-146">Web</span><span class="sxs-lookup"><span data-stu-id="66ac2-146">Web</span></span>
- <span data-ttu-id="66ac2-147">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="66ac2-147">Windows Phone</span></span>
- <span data-ttu-id="66ac2-148">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="66ac2-148">Android Phone</span></span>
- <span data-ttu-id="66ac2-149">iOS</span><span class="sxs-lookup"><span data-stu-id="66ac2-149">iOS</span></span>
- <span data-ttu-id="66ac2-150">Mac</span><span class="sxs-lookup"><span data-stu-id="66ac2-150">Mac</span></span>
- <span data-ttu-id="66ac2-151">Windows</span><span class="sxs-lookup"><span data-stu-id="66ac2-151">Windows</span></span>
- <span data-ttu-id="66ac2-152">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="66ac2-152">Report Date</span></span>
- <span data-ttu-id="66ac2-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="66ac2-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="66ac2-154">JSON</span><span class="sxs-lookup"><span data-stu-id="66ac2-154">JSON</span></span>

<span data-ttu-id="66ac2-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsDeviceUsageUserCounts](../resources/teamsdeviceusageusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ac2-155">If successful, this method returns a `200 OK` response code and a **[teamsDeviceUsageUserCounts](../resources/teamsdeviceusageusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66ac2-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66ac2-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="66ac2-157">CSV</span><span class="sxs-lookup"><span data-stu-id="66ac2-157">CSV</span></span>

<span data-ttu-id="66ac2-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="66ac2-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="66ac2-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66ac2-159">Request</span></span>

<span data-ttu-id="66ac2-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66ac2-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusageusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="66ac2-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66ac2-161">Response</span></span>

<span data-ttu-id="66ac2-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ac2-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="66ac2-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="66ac2-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="66ac2-164">JSON</span><span class="sxs-lookup"><span data-stu-id="66ac2-164">JSON</span></span>

<span data-ttu-id="66ac2-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="66ac2-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="66ac2-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66ac2-166">Request</span></span>

<span data-ttu-id="66ac2-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66ac2-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusageusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="66ac2-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66ac2-168">Response</span></span>

<span data-ttu-id="66ac2-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66ac2-169">The following is an example of the response.</span></span>

> <span data-ttu-id="66ac2-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66ac2-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsDeviceUsageUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 269

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsDeviceUsageUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "web": 13, 
      "windowsPhone": 0, 
      "androidPhone": 22, 
      "ios": 75, 
      "mac": 16, 
      "windows": 257, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```