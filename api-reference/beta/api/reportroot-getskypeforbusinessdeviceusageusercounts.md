---
title: 'reportRoot: getSkypeForBusinessDeviceUsageUserCounts'
description: Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial. También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.
localization_priority: Normal
ms.openlocfilehash: 677899902bc90dbbf4ae31eba7c9bf6961f7a7d9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822319"
---
# <a name="reportroot-getskypeforbusinessdeviceusageusercounts"></a><span data-ttu-id="f3f10-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="f3f10-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span></span>

> <span data-ttu-id="f3f10-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3f10-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3f10-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3f10-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f3f10-107">Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="f3f10-107">Get the usage trends on how many users in your organization have connected using the Skype for Business app.</span></span> <span data-ttu-id="f3f10-108">También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.</span><span class="sxs-lookup"><span data-stu-id="f3f10-108">You will also get a breakdown by the type of device (Windows, Windows phone, Android phone, iPhone, or iPad) on which the Skype for Business client app is installed and used across your organization.</span></span>

> <span data-ttu-id="f3f10-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="f3f10-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="f3f10-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="f3f10-110">Permissions</span></span>

<span data-ttu-id="f3f10-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3f10-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f3f10-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3f10-113">Permission type</span></span>                        | <span data-ttu-id="f3f10-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3f10-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f3f10-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3f10-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="f3f10-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f3f10-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="f3f10-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3f10-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f3f10-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3f10-118">Not supported.</span></span>                           |
| <span data-ttu-id="f3f10-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3f10-119">Application</span></span>                            | <span data-ttu-id="f3f10-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f3f10-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f3f10-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3f10-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="f3f10-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="f3f10-122">Function parameters</span></span>

<span data-ttu-id="f3f10-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="f3f10-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="f3f10-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f3f10-124">Parameter</span></span> | <span data-ttu-id="f3f10-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3f10-125">Type</span></span>   | <span data-ttu-id="f3f10-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3f10-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f3f10-127">period</span><span class="sxs-lookup"><span data-stu-id="f3f10-127">period</span></span>    | <span data-ttu-id="f3f10-128">cadena</span><span class="sxs-lookup"><span data-stu-id="f3f10-128">string</span></span> | <span data-ttu-id="f3f10-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f3f10-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f3f10-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="f3f10-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f3f10-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f3f10-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="f3f10-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="f3f10-132">Required.</span></span> |

<span data-ttu-id="f3f10-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3f10-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="f3f10-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="f3f10-134">The default output type is text/csv.</span></span> <span data-ttu-id="f3f10-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="f3f10-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f3f10-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3f10-136">Request headers</span></span>

| <span data-ttu-id="f3f10-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="f3f10-137">Name</span></span>          | <span data-ttu-id="f3f10-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3f10-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="f3f10-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="f3f10-139">Authorization</span></span> | <span data-ttu-id="f3f10-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3f10-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="f3f10-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3f10-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="f3f10-143">CSV</span><span class="sxs-lookup"><span data-stu-id="f3f10-143">CSV</span></span>

<span data-ttu-id="f3f10-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="f3f10-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f3f10-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3f10-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f3f10-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="f3f10-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f3f10-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="f3f10-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f3f10-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="f3f10-148">Report Refresh Date</span></span>
- <span data-ttu-id="f3f10-149">Windows</span><span class="sxs-lookup"><span data-stu-id="f3f10-149">Windows</span></span>
- <span data-ttu-id="f3f10-150">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="f3f10-150">Windows Phone</span></span>
- <span data-ttu-id="f3f10-151">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="f3f10-151">Android Phone</span></span>
- <span data-ttu-id="f3f10-152">iPhone</span><span class="sxs-lookup"><span data-stu-id="f3f10-152">iPhone</span></span>
- <span data-ttu-id="f3f10-153">iPad</span><span class="sxs-lookup"><span data-stu-id="f3f10-153">iPad</span></span>
- <span data-ttu-id="f3f10-154">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="f3f10-154">Report Date</span></span>
- <span data-ttu-id="f3f10-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="f3f10-155">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="f3f10-156">JSON</span><span class="sxs-lookup"><span data-stu-id="f3f10-156">JSON</span></span>

<span data-ttu-id="f3f10-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessDeviceUsageUserCounts](../resources/skypeforbusinessdeviceusageusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3f10-157">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessDeviceUsageUserCounts](../resources/skypeforbusinessdeviceusageusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3f10-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3f10-158">Example</span></span>

### <a name="csv"></a><span data-ttu-id="f3f10-159">CSV</span><span class="sxs-lookup"><span data-stu-id="f3f10-159">CSV</span></span>

<span data-ttu-id="f3f10-160">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="f3f10-160">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="f3f10-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3f10-161">Request</span></span>

<span data-ttu-id="f3f10-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3f10-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="f3f10-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3f10-163">Response</span></span>

<span data-ttu-id="f3f10-164">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3f10-164">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="f3f10-165">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3f10-165">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

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

### <a name="json"></a><span data-ttu-id="f3f10-166">JSON</span><span class="sxs-lookup"><span data-stu-id="f3f10-166">JSON</span></span>

<span data-ttu-id="f3f10-167">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="f3f10-167">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="f3f10-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3f10-168">Request</span></span>

<span data-ttu-id="f3f10-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3f10-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="f3f10-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3f10-170">Response</span></span>

<span data-ttu-id="f3f10-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3f10-171">The following is an example of the response.</span></span>

> <span data-ttu-id="f3f10-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3f10-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

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
