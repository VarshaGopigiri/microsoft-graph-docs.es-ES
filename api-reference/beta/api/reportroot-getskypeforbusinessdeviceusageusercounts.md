---
title: 'reportRoot: getSkypeForBusinessDeviceUsageUserCounts'
description: Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial. También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.
ms.openlocfilehash: 21f8746a94860834ad6fdb2465a672f264fee145
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083158"
---
# <a name="reportroot-getskypeforbusinessdeviceusageusercounts"></a><span data-ttu-id="c30fe-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="c30fe-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span></span>

> <span data-ttu-id="c30fe-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c30fe-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c30fe-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c30fe-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c30fe-107">Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="c30fe-107">Get the usage trends on how many users in your organization have connected using the Skype for Business app.</span></span> <span data-ttu-id="c30fe-108">También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.</span><span class="sxs-lookup"><span data-stu-id="c30fe-108">You will also get a breakdown by the type of device (Windows, Windows phone, Android phone, iPhone, or iPad) on which the Skype for Business client app is installed and used across your organization.</span></span>

> <span data-ttu-id="c30fe-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="c30fe-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="c30fe-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="c30fe-110">Permissions</span></span>

<span data-ttu-id="c30fe-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c30fe-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c30fe-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c30fe-113">Permission type</span></span>                        | <span data-ttu-id="c30fe-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c30fe-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c30fe-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c30fe-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="c30fe-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c30fe-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c30fe-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c30fe-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c30fe-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c30fe-118">Not supported.</span></span>                           |
| <span data-ttu-id="c30fe-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c30fe-119">Application</span></span>                            | <span data-ttu-id="c30fe-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c30fe-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c30fe-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c30fe-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="c30fe-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="c30fe-122">Function parameters</span></span>

<span data-ttu-id="c30fe-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c30fe-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c30fe-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c30fe-124">Parameter</span></span> | <span data-ttu-id="c30fe-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="c30fe-125">Type</span></span>   | <span data-ttu-id="c30fe-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="c30fe-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c30fe-127">period</span><span class="sxs-lookup"><span data-stu-id="c30fe-127">period</span></span>    | <span data-ttu-id="c30fe-128">cadena</span><span class="sxs-lookup"><span data-stu-id="c30fe-128">string</span></span> | <span data-ttu-id="c30fe-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c30fe-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c30fe-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c30fe-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c30fe-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c30fe-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c30fe-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="c30fe-132">Required.</span></span> |

<span data-ttu-id="c30fe-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c30fe-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="c30fe-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="c30fe-134">The default output type is text/csv.</span></span> <span data-ttu-id="c30fe-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="c30fe-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c30fe-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c30fe-136">Request headers</span></span>

| <span data-ttu-id="c30fe-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="c30fe-137">Name</span></span>          | <span data-ttu-id="c30fe-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="c30fe-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="c30fe-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="c30fe-139">Authorization</span></span> | <span data-ttu-id="c30fe-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c30fe-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="c30fe-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c30fe-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="c30fe-143">CSV</span><span class="sxs-lookup"><span data-stu-id="c30fe-143">CSV</span></span>

<span data-ttu-id="c30fe-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c30fe-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c30fe-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c30fe-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c30fe-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c30fe-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c30fe-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c30fe-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c30fe-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c30fe-148">Report Refresh Date</span></span>
- <span data-ttu-id="c30fe-149">Windows</span><span class="sxs-lookup"><span data-stu-id="c30fe-149">Windows</span></span>
- <span data-ttu-id="c30fe-150">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="c30fe-150">Windows Phone</span></span>
- <span data-ttu-id="c30fe-151">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="c30fe-151">Android Phone</span></span>
- <span data-ttu-id="c30fe-152">iPhone</span><span class="sxs-lookup"><span data-stu-id="c30fe-152">iPhone</span></span>
- <span data-ttu-id="c30fe-153">iPad</span><span class="sxs-lookup"><span data-stu-id="c30fe-153">iPad</span></span>
- <span data-ttu-id="c30fe-154">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="c30fe-154">Report Date</span></span>
- <span data-ttu-id="c30fe-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c30fe-155">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="c30fe-156">JSON</span><span class="sxs-lookup"><span data-stu-id="c30fe-156">JSON</span></span>

<span data-ttu-id="c30fe-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessDeviceUsageUserCounts](../resources/skypeforbusinessdeviceusageusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c30fe-157">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessDeviceUsageUserCounts](../resources/skypeforbusinessdeviceusageusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c30fe-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c30fe-158">Example</span></span>

### <a name="csv"></a><span data-ttu-id="c30fe-159">CSV</span><span class="sxs-lookup"><span data-stu-id="c30fe-159">CSV</span></span>

<span data-ttu-id="c30fe-160">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="c30fe-160">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="c30fe-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c30fe-161">Request</span></span>

<span data-ttu-id="c30fe-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c30fe-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="c30fe-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c30fe-163">Response</span></span>

<span data-ttu-id="c30fe-164">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c30fe-164">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="c30fe-165">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c30fe-165">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="c30fe-166">JSON</span><span class="sxs-lookup"><span data-stu-id="c30fe-166">JSON</span></span>

<span data-ttu-id="c30fe-167">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="c30fe-167">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="c30fe-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c30fe-168">Request</span></span>

<span data-ttu-id="c30fe-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c30fe-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="c30fe-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c30fe-170">Response</span></span>

<span data-ttu-id="c30fe-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c30fe-171">The following is an example of the response.</span></span>

> <span data-ttu-id="c30fe-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c30fe-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessDeviceUsageUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 289

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessDeviceUsageUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "windows": 403, 
      "windowsPhone": 2, 
      "androidPhone": 13, 
      "iPhone": 26, 
      "iPad": 0, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
