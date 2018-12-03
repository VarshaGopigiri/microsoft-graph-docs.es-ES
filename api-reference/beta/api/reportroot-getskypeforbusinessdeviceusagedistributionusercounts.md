---
title: 'reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts'
description: Obtiene el número de usuarios que usan dispositivos únicos en la organización. En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.
ms.openlocfilehash: bee105fc41d18543c611f05d2a3e389ff6a84526
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085084"
---
# <a name="reportroot-getskypeforbusinessdeviceusagedistributionusercounts"></a><span data-ttu-id="5109d-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="5109d-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span></span>

> <span data-ttu-id="5109d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5109d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5109d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5109d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5109d-107">Obtiene el número de usuarios que usan dispositivos únicos en la organización.</span><span class="sxs-lookup"><span data-stu-id="5109d-107">Get the number of users using unique devices in your organization.</span></span> <span data-ttu-id="5109d-108">En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.</span><span class="sxs-lookup"><span data-stu-id="5109d-108">The report will show you the number of users per device including Windows, Windows phone, Android phone, iPhone, and iPad.</span></span>

> <span data-ttu-id="5109d-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="5109d-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="5109d-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="5109d-110">Permissions</span></span>

<span data-ttu-id="5109d-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5109d-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="5109d-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5109d-113">Permission type</span></span>                        | <span data-ttu-id="5109d-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5109d-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5109d-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5109d-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="5109d-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5109d-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="5109d-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5109d-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5109d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5109d-118">Not supported.</span></span>                           |
| <span data-ttu-id="5109d-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5109d-119">Application</span></span>                            | <span data-ttu-id="5109d-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5109d-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="5109d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5109d-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="5109d-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="5109d-122">Function parameters</span></span>

<span data-ttu-id="5109d-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="5109d-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="5109d-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5109d-124">Parameter</span></span> | <span data-ttu-id="5109d-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="5109d-125">Type</span></span>   | <span data-ttu-id="5109d-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="5109d-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5109d-127">period</span><span class="sxs-lookup"><span data-stu-id="5109d-127">period</span></span>    | <span data-ttu-id="5109d-128">cadena</span><span class="sxs-lookup"><span data-stu-id="5109d-128">string</span></span> | <span data-ttu-id="5109d-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5109d-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5109d-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="5109d-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5109d-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="5109d-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="5109d-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="5109d-132">Required.</span></span> |

<span data-ttu-id="5109d-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5109d-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="5109d-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="5109d-134">The default output type is text/csv.</span></span> <span data-ttu-id="5109d-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="5109d-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5109d-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5109d-136">Request headers</span></span>

| <span data-ttu-id="5109d-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="5109d-137">Name</span></span>          | <span data-ttu-id="5109d-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="5109d-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5109d-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="5109d-139">Authorization</span></span> | <span data-ttu-id="5109d-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5109d-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="5109d-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5109d-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="5109d-143">CSV</span><span class="sxs-lookup"><span data-stu-id="5109d-143">CSV</span></span>

<span data-ttu-id="5109d-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="5109d-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5109d-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5109d-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5109d-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="5109d-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5109d-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="5109d-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="5109d-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="5109d-148">Report Refresh Date</span></span>
- <span data-ttu-id="5109d-149">Windows</span><span class="sxs-lookup"><span data-stu-id="5109d-149">Windows</span></span>
- <span data-ttu-id="5109d-150">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="5109d-150">Windows Phone</span></span>
- <span data-ttu-id="5109d-151">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="5109d-151">Android Phone</span></span>
- <span data-ttu-id="5109d-152">iPhone</span><span class="sxs-lookup"><span data-stu-id="5109d-152">iPhone</span></span>
- <span data-ttu-id="5109d-153">iPad</span><span class="sxs-lookup"><span data-stu-id="5109d-153">iPad</span></span>
- <span data-ttu-id="5109d-154">Período del informe</span><span class="sxs-lookup"><span data-stu-id="5109d-154">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="5109d-155">JSON</span><span class="sxs-lookup"><span data-stu-id="5109d-155">JSON</span></span>

<span data-ttu-id="5109d-156">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessDeviceUsageDistributionUserCounts](../resources/skypeforbusinessdeviceusagedistributionusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5109d-156">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessDeviceUsageDistributionUserCounts](../resources/skypeforbusinessdeviceusagedistributionusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5109d-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5109d-157">Example</span></span>

### <a name="csv"></a><span data-ttu-id="5109d-158">CSV</span><span class="sxs-lookup"><span data-stu-id="5109d-158">CSV</span></span>

<span data-ttu-id="5109d-159">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="5109d-159">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="5109d-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5109d-160">Request</span></span>

<span data-ttu-id="5109d-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5109d-161">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusagedistributionusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="5109d-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5109d-162">Response</span></span>

<span data-ttu-id="5109d-163">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5109d-163">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="5109d-164">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="5109d-164">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Period
```

### <a name="json"></a><span data-ttu-id="5109d-165">JSON</span><span class="sxs-lookup"><span data-stu-id="5109d-165">JSON</span></span>

<span data-ttu-id="5109d-166">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="5109d-166">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="5109d-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5109d-167">Request</span></span>

<span data-ttu-id="5109d-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5109d-168">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusagedistributionusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="5109d-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5109d-169">Response</span></span>

<span data-ttu-id="5109d-170">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5109d-170">The following is an example of the response.</span></span>

> <span data-ttu-id="5109d-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5109d-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessDeviceUsageDistributionUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 275

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessDeviceUsageDistributionUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "windows": 122, 
      "windowsPhone": 8, 
      "androidPhone": 19, 
      "iPhone": 28, 
      "iPad": 1, 
      "reportPeriod": "7"
    }
  ]
}
```