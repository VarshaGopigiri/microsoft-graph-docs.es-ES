---
title: 'reportRoot: getYammerDeviceUsageDistributionUserCounts'
description: Obtiene el número de usuarios por tipo de dispositivo.
ms.openlocfilehash: 722abbb0211344be1a505d621304198407792e43
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085661"
---
# <a name="reportroot-getyammerdeviceusagedistributionusercounts"></a><span data-ttu-id="15f72-103">reportRoot: getYammerDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="15f72-103">reportRoot: getYammerDeviceUsageDistributionUserCounts</span></span>

> <span data-ttu-id="15f72-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15f72-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15f72-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15f72-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="15f72-106">Obtiene el número de usuarios por tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15f72-106">Get the number of users by device type.</span></span>

> <span data-ttu-id="15f72-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span><span class="sxs-lookup"><span data-stu-id="15f72-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="15f72-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="15f72-108">Permissions</span></span>

<span data-ttu-id="15f72-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="15f72-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="15f72-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15f72-111">Permission type</span></span>                        | <span data-ttu-id="15f72-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15f72-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="15f72-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15f72-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="15f72-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="15f72-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="15f72-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15f72-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="15f72-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15f72-116">Not supported.</span></span>                           |
| <span data-ttu-id="15f72-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15f72-117">Application</span></span>                            | <span data-ttu-id="15f72-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="15f72-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="15f72-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15f72-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="15f72-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="15f72-120">Function parameters</span></span>

<span data-ttu-id="15f72-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="15f72-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="15f72-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="15f72-122">Parameter</span></span> | <span data-ttu-id="15f72-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="15f72-123">Type</span></span>   | <span data-ttu-id="15f72-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="15f72-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="15f72-125">period</span><span class="sxs-lookup"><span data-stu-id="15f72-125">period</span></span>    | <span data-ttu-id="15f72-126">cadena</span><span class="sxs-lookup"><span data-stu-id="15f72-126">string</span></span> | <span data-ttu-id="15f72-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="15f72-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="15f72-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="15f72-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="15f72-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="15f72-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="15f72-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="15f72-130">Required.</span></span> |

<span data-ttu-id="15f72-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15f72-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="15f72-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="15f72-132">The default output type is text/csv.</span></span> <span data-ttu-id="15f72-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="15f72-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="15f72-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15f72-134">Request headers</span></span>

| <span data-ttu-id="15f72-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="15f72-135">Name</span></span>          | <span data-ttu-id="15f72-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="15f72-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="15f72-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="15f72-137">Authorization</span></span> | <span data-ttu-id="15f72-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="15f72-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="15f72-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15f72-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="15f72-141">CSV</span><span class="sxs-lookup"><span data-stu-id="15f72-141">CSV</span></span>

<span data-ttu-id="15f72-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="15f72-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="15f72-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15f72-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="15f72-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="15f72-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="15f72-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="15f72-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="15f72-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="15f72-146">Report Refresh Date</span></span>
- <span data-ttu-id="15f72-147">Web</span><span class="sxs-lookup"><span data-stu-id="15f72-147">Web</span></span>
- <span data-ttu-id="15f72-148">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="15f72-148">Windows Phone</span></span>
- <span data-ttu-id="15f72-149">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="15f72-149">Android Phone</span></span>
- <span data-ttu-id="15f72-150">iPhone</span><span class="sxs-lookup"><span data-stu-id="15f72-150">iPhone</span></span>
- <span data-ttu-id="15f72-151">iPad</span><span class="sxs-lookup"><span data-stu-id="15f72-151">iPad</span></span>
- <span data-ttu-id="15f72-152">Otro</span><span class="sxs-lookup"><span data-stu-id="15f72-152">Other</span></span>
- <span data-ttu-id="15f72-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="15f72-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="15f72-154">JSON</span><span class="sxs-lookup"><span data-stu-id="15f72-154">JSON</span></span>

<span data-ttu-id="15f72-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerDeviceUsageDistributionUserCounts](../resources/yammerdeviceusagedistributionusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15f72-155">If successful, this method returns a `200 OK` response code and a **[yammerDeviceUsageDistributionUserCounts](../resources/yammerdeviceusagedistributionusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15f72-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15f72-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="15f72-157">CSV</span><span class="sxs-lookup"><span data-stu-id="15f72-157">CSV</span></span>

<span data-ttu-id="15f72-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="15f72-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="15f72-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15f72-159">Request</span></span>

<span data-ttu-id="15f72-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15f72-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusagedistributionusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageDistributionUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="15f72-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15f72-161">Response</span></span>

<span data-ttu-id="15f72-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15f72-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="15f72-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="15f72-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iPhone,iPad,Other,Report Period
```

### <a name="json"></a><span data-ttu-id="15f72-164">JSON</span><span class="sxs-lookup"><span data-stu-id="15f72-164">JSON</span></span>

<span data-ttu-id="15f72-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="15f72-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="15f72-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15f72-166">Request</span></span>

<span data-ttu-id="15f72-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15f72-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusagedistributionusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageDistributionUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="15f72-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15f72-168">Response</span></span>

<span data-ttu-id="15f72-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15f72-169">The following is an example of the response.</span></span>

> <span data-ttu-id="15f72-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15f72-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.yammerDeviceUsageDistributionUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 271

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.yammerDeviceUsageDistributionUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "web": 138, 
      "windowsPhone": 1, 
      "androidPhone": 29, 
      "iPhone": 40, 
      "iPad": 2, 
      "other": 2, 
      "reportPeriod": "7"
    }
  ]
}
```