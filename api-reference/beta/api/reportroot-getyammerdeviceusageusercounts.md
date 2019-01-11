---
title: 'reportRoot: getYammerDeviceUsageUserCounts'
description: Obtiene el número de usuarios diario por tipo de dispositivo.
localization_priority: Normal
ms.openlocfilehash: 78c17de276e45b12936fcdf0f4b58c975388d101
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812624"
---
# <a name="reportroot-getyammerdeviceusageusercounts"></a><span data-ttu-id="cda9a-103">reportRoot: getYammerDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="cda9a-103">reportRoot: getYammerDeviceUsageUserCounts</span></span>

> <span data-ttu-id="cda9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cda9a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cda9a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cda9a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cda9a-106">Obtiene el número de usuarios diario por tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cda9a-106">Get the number of daily users by device type.</span></span>

> <span data-ttu-id="cda9a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span><span class="sxs-lookup"><span data-stu-id="cda9a-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="cda9a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="cda9a-108">Permissions</span></span>

<span data-ttu-id="cda9a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cda9a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="cda9a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cda9a-111">Permission type</span></span>                        | <span data-ttu-id="cda9a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cda9a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="cda9a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cda9a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="cda9a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="cda9a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="cda9a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cda9a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cda9a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cda9a-116">Not supported.</span></span>                           |
| <span data-ttu-id="cda9a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cda9a-117">Application</span></span>                            | <span data-ttu-id="cda9a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="cda9a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="cda9a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cda9a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="cda9a-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="cda9a-120">Function parameters</span></span>

<span data-ttu-id="cda9a-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="cda9a-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="cda9a-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cda9a-122">Parameter</span></span> | <span data-ttu-id="cda9a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="cda9a-123">Type</span></span>   | <span data-ttu-id="cda9a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cda9a-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="cda9a-125">period</span><span class="sxs-lookup"><span data-stu-id="cda9a-125">period</span></span>    | <span data-ttu-id="cda9a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="cda9a-126">string</span></span> | <span data-ttu-id="cda9a-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="cda9a-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="cda9a-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="cda9a-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="cda9a-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="cda9a-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="cda9a-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cda9a-130">Required.</span></span> |

<span data-ttu-id="cda9a-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cda9a-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="cda9a-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="cda9a-132">The default output type is text/csv.</span></span> <span data-ttu-id="cda9a-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="cda9a-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cda9a-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cda9a-134">Request headers</span></span>

| <span data-ttu-id="cda9a-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="cda9a-135">Name</span></span>          | <span data-ttu-id="cda9a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="cda9a-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="cda9a-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="cda9a-137">Authorization</span></span> | <span data-ttu-id="cda9a-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cda9a-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="cda9a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cda9a-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="cda9a-141">CSV</span><span class="sxs-lookup"><span data-stu-id="cda9a-141">CSV</span></span>

<span data-ttu-id="cda9a-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="cda9a-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="cda9a-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cda9a-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="cda9a-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="cda9a-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="cda9a-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="cda9a-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="cda9a-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="cda9a-146">Report Refresh Date</span></span>
- <span data-ttu-id="cda9a-147">Web</span><span class="sxs-lookup"><span data-stu-id="cda9a-147">Web</span></span>
- <span data-ttu-id="cda9a-148">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="cda9a-148">Windows Phone</span></span>
- <span data-ttu-id="cda9a-149">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="cda9a-149">Android Phone</span></span>
- <span data-ttu-id="cda9a-150">iPhone</span><span class="sxs-lookup"><span data-stu-id="cda9a-150">iPhone</span></span>
- <span data-ttu-id="cda9a-151">iPad</span><span class="sxs-lookup"><span data-stu-id="cda9a-151">iPad</span></span>
- <span data-ttu-id="cda9a-152">Otro</span><span class="sxs-lookup"><span data-stu-id="cda9a-152">Other</span></span>
- <span data-ttu-id="cda9a-153">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="cda9a-153">Report Date</span></span>
- <span data-ttu-id="cda9a-154">Período del informe</span><span class="sxs-lookup"><span data-stu-id="cda9a-154">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="cda9a-155">JSON</span><span class="sxs-lookup"><span data-stu-id="cda9a-155">JSON</span></span>

<span data-ttu-id="cda9a-156">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerDeviceUsageUserCounts](../resources/yammerdeviceusageusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cda9a-156">If successful, this method returns a `200 OK` response code and a **[yammerDeviceUsageUserCounts](../resources/yammerdeviceusageusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cda9a-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cda9a-157">Example</span></span>

### <a name="csv"></a><span data-ttu-id="cda9a-158">CSV</span><span class="sxs-lookup"><span data-stu-id="cda9a-158">CSV</span></span>

<span data-ttu-id="cda9a-159">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="cda9a-159">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="cda9a-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cda9a-160">Request</span></span>

<span data-ttu-id="cda9a-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cda9a-161">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusageusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="cda9a-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cda9a-162">Response</span></span>

<span data-ttu-id="cda9a-163">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cda9a-163">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="cda9a-164">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="cda9a-164">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iPhone,iPad,Other,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="cda9a-165">JSON</span><span class="sxs-lookup"><span data-stu-id="cda9a-165">JSON</span></span>

<span data-ttu-id="cda9a-166">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="cda9a-166">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="cda9a-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cda9a-167">Request</span></span>

<span data-ttu-id="cda9a-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cda9a-168">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusageusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerDeviceUsageUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="cda9a-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cda9a-169">Response</span></span>

<span data-ttu-id="cda9a-170">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cda9a-170">The following is an example of the response.</span></span>

> <span data-ttu-id="cda9a-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cda9a-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.yammerDeviceUsageUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 284

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.yammerDeviceUsageUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "web": 63, 
      "windowsPhone": 1, 
      "androidPhone": 17, 
      "iPhone": 23, 
      "iPad": 1, 
      "other": 2, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
