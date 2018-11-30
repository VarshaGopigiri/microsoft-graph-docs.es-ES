---
title: 'reportRoot: getTeamsDeviceUsageDistributionUserCounts'
description: Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.
ms.openlocfilehash: b2416b8a4aa257f49807efb3f320fcf16cea4920
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088699"
---
# <a name="reportroot-getteamsdeviceusagedistributionusercounts"></a><span data-ttu-id="18407-103">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="18407-103">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span></span>

> <span data-ttu-id="18407-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="18407-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="18407-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="18407-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="18407-106">Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="18407-106">Get the number of Microsoft Teams unique users by device type over the selected time period.</span></span>

## <a name="permissions"></a><span data-ttu-id="18407-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="18407-107">Permissions</span></span>

<span data-ttu-id="18407-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="18407-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="18407-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="18407-110">Permission type</span></span>                        | <span data-ttu-id="18407-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="18407-111">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="18407-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="18407-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="18407-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="18407-113">Reports.Read.All</span></span>                         |
| <span data-ttu-id="18407-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="18407-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="18407-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="18407-115">Not supported.</span></span>                           |
| <span data-ttu-id="18407-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="18407-116">Application</span></span>                            | <span data-ttu-id="18407-117">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="18407-117">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="18407-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="18407-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')
```

## <a name="function-parameters"></a><span data-ttu-id="18407-119">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="18407-119">Function parameters</span></span>

<span data-ttu-id="18407-120">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="18407-120">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="18407-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="18407-121">Parameter</span></span> | <span data-ttu-id="18407-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="18407-122">Type</span></span>   | <span data-ttu-id="18407-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="18407-123">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="18407-124">period</span><span class="sxs-lookup"><span data-stu-id="18407-124">period</span></span>    | <span data-ttu-id="18407-125">cadena</span><span class="sxs-lookup"><span data-stu-id="18407-125">string</span></span> | <span data-ttu-id="18407-126">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="18407-126">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="18407-127">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="18407-127">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="18407-128">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="18407-128">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="18407-129">Necesario.</span><span class="sxs-lookup"><span data-stu-id="18407-129">Required.</span></span> |

<span data-ttu-id="18407-130">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18407-130">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="18407-131">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="18407-131">The default output type is text/csv.</span></span> <span data-ttu-id="18407-132">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="18407-132">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="18407-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="18407-133">Request headers</span></span>

| <span data-ttu-id="18407-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="18407-134">Name</span></span>          | <span data-ttu-id="18407-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="18407-135">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="18407-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="18407-136">Authorization</span></span> | <span data-ttu-id="18407-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="18407-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="18407-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18407-139">Response</span></span>

### <a name="csv"></a><span data-ttu-id="18407-140">CSV</span><span class="sxs-lookup"><span data-stu-id="18407-140">CSV</span></span>

<span data-ttu-id="18407-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="18407-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="18407-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18407-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="18407-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="18407-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="18407-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="18407-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="18407-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="18407-145">Report Refresh Date</span></span>
- <span data-ttu-id="18407-146">Web</span><span class="sxs-lookup"><span data-stu-id="18407-146">Web</span></span>
- <span data-ttu-id="18407-147">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="18407-147">Windows Phone</span></span>
- <span data-ttu-id="18407-148">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="18407-148">Android Phone</span></span>
- <span data-ttu-id="18407-149">iOS</span><span class="sxs-lookup"><span data-stu-id="18407-149">iOS</span></span>
- <span data-ttu-id="18407-150">Mac</span><span class="sxs-lookup"><span data-stu-id="18407-150">Mac</span></span>
- <span data-ttu-id="18407-151">Windows</span><span class="sxs-lookup"><span data-stu-id="18407-151">Windows</span></span>
- <span data-ttu-id="18407-152">Período del informe</span><span class="sxs-lookup"><span data-stu-id="18407-152">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="18407-153">JSON</span><span class="sxs-lookup"><span data-stu-id="18407-153">JSON</span></span>

<span data-ttu-id="18407-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsDeviceUsageDistributionUserCounts](../resources/teamsdeviceusagedistributionusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18407-154">If successful, this method returns a `200 OK` response code and a **[teamsDeviceUsageDistributionUserCounts](../resources/teamsdeviceusagedistributionusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="18407-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18407-155">Example</span></span>

### <a name="csv"></a><span data-ttu-id="18407-156">CSV</span><span class="sxs-lookup"><span data-stu-id="18407-156">CSV</span></span>

<span data-ttu-id="18407-157">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="18407-157">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="18407-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18407-158">Request</span></span>

<span data-ttu-id="18407-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18407-159">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="18407-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18407-160">Response</span></span>

<span data-ttu-id="18407-161">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18407-161">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="18407-162">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="18407-162">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Period
```

### <a name="json"></a><span data-ttu-id="18407-163">JSON</span><span class="sxs-lookup"><span data-stu-id="18407-163">JSON</span></span>

<span data-ttu-id="18407-164">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="18407-164">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="18407-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="18407-165">Request</span></span>

<span data-ttu-id="18407-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="18407-166">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="18407-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="18407-167">Response</span></span>

<span data-ttu-id="18407-168">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="18407-168">The following is an example of the response.</span></span>

> <span data-ttu-id="18407-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="18407-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsDeviceUsageDistributionUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 243

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsDeviceUsageDistributionUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "web": 51, 
      "windowsPhone": 2, 
      "androidPhone": 34, 
      "ios": 76, 
      "mac": 40, 
      "windows": 491, 
      "reportPeriod": "7"
    }
  ]
}
```
