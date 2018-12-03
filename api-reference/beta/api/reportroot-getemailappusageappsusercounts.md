---
title: 'reportRoot: getEmailAppUsageAppsUserCounts'
description: Obtiene el número de usuarios únicos por aplicación de correo electrónico.
ms.openlocfilehash: 02750508c318b8ececb076bd597709973f567b38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085392"
---
# <a name="reportroot-getemailappusageappsusercounts"></a><span data-ttu-id="32c9f-103">reportRoot: getEmailAppUsageAppsUserCounts</span><span class="sxs-lookup"><span data-stu-id="32c9f-103">reportRoot: getEmailAppUsageAppsUserCounts</span></span>

> <span data-ttu-id="32c9f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="32c9f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="32c9f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="32c9f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="32c9f-106">Obtiene el número de usuarios únicos por aplicación de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="32c9f-106">Get the count of unique users per email app.</span></span>

> <span data-ttu-id="32c9f-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="32c9f-107">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="32c9f-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="32c9f-108">Permissions</span></span>

<span data-ttu-id="32c9f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="32c9f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="32c9f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32c9f-111">Permission type</span></span>                        | <span data-ttu-id="32c9f-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32c9f-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="32c9f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32c9f-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="32c9f-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="32c9f-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="32c9f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32c9f-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="32c9f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32c9f-116">Not supported.</span></span>                           |
| <span data-ttu-id="32c9f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32c9f-117">Application</span></span>                            | <span data-ttu-id="32c9f-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="32c9f-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="32c9f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32c9f-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageAppsUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="32c9f-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="32c9f-120">Function parameters</span></span>

<span data-ttu-id="32c9f-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="32c9f-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="32c9f-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="32c9f-122">Parameter</span></span> | <span data-ttu-id="32c9f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="32c9f-123">Type</span></span>   | <span data-ttu-id="32c9f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c9f-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="32c9f-125">period</span><span class="sxs-lookup"><span data-stu-id="32c9f-125">period</span></span>    | <span data-ttu-id="32c9f-126">cadena</span><span class="sxs-lookup"><span data-stu-id="32c9f-126">string</span></span> | <span data-ttu-id="32c9f-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="32c9f-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="32c9f-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="32c9f-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="32c9f-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="32c9f-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="32c9f-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="32c9f-130">Required.</span></span> |

<span data-ttu-id="32c9f-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32c9f-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="32c9f-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="32c9f-132">The default output type is text/csv.</span></span> <span data-ttu-id="32c9f-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="32c9f-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="32c9f-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32c9f-134">Request headers</span></span>

| <span data-ttu-id="32c9f-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="32c9f-135">Name</span></span>          | <span data-ttu-id="32c9f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="32c9f-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="32c9f-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="32c9f-137">Authorization</span></span> | <span data-ttu-id="32c9f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="32c9f-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="32c9f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32c9f-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="32c9f-141">CSV</span><span class="sxs-lookup"><span data-stu-id="32c9f-141">CSV</span></span>

<span data-ttu-id="32c9f-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="32c9f-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="32c9f-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32c9f-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="32c9f-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="32c9f-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="32c9f-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="32c9f-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="32c9f-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="32c9f-146">Report Refresh Date</span></span>
- <span data-ttu-id="32c9f-147">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="32c9f-147">Mail For Mac</span></span>
- <span data-ttu-id="32c9f-148">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="32c9f-148">Outlook For Mac</span></span>
- <span data-ttu-id="32c9f-149">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="32c9f-149">Outlook For Windows</span></span>
- <span data-ttu-id="32c9f-150">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="32c9f-150">Outlook For Mobile</span></span>
- <span data-ttu-id="32c9f-151">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="32c9f-151">Other For Mobile</span></span>
- <span data-ttu-id="32c9f-152">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="32c9f-152">Outlook For Web</span></span>
- <span data-ttu-id="32c9f-153">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="32c9f-153">POP3 App</span></span>
- <span data-ttu-id="32c9f-154">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="32c9f-154">IMAP4 App</span></span>
- <span data-ttu-id="32c9f-155">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="32c9f-155">SMTP App</span></span>
- <span data-ttu-id="32c9f-156">Período del informe</span><span class="sxs-lookup"><span data-stu-id="32c9f-156">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="32c9f-157">JSON</span><span class="sxs-lookup"><span data-stu-id="32c9f-157">JSON</span></span>

<span data-ttu-id="32c9f-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[emailAppUsageAppsUserCounts](../resources/emailappusageappsusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32c9f-158">If successful, this method returns a `200 OK` response code and an **[emailAppUsageAppsUserCounts](../resources/emailappusageappsusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="32c9f-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32c9f-159">Example</span></span>

### <a name="csv"></a><span data-ttu-id="32c9f-160">CSV</span><span class="sxs-lookup"><span data-stu-id="32c9f-160">CSV</span></span>

<span data-ttu-id="32c9f-161">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="32c9f-161">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="32c9f-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32c9f-162">Request</span></span>

<span data-ttu-id="32c9f-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32c9f-163">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageappsusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageAppsUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="32c9f-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32c9f-164">Response</span></span>

<span data-ttu-id="32c9f-165">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32c9f-165">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="32c9f-166">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="32c9f-166">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```

### <a name="json"></a><span data-ttu-id="32c9f-167">JSON</span><span class="sxs-lookup"><span data-stu-id="32c9f-167">JSON</span></span>

<span data-ttu-id="32c9f-168">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="32c9f-168">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="32c9f-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32c9f-169">Request</span></span>

<span data-ttu-id="32c9f-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32c9f-170">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageappsusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageAppsUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="32c9f-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32c9f-171">Response</span></span>

<span data-ttu-id="32c9f-172">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32c9f-172">The following is an example of the response.</span></span>

> <span data-ttu-id="32c9f-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32c9f-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.emailAppUsageAppsUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 345

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.emailAppUsageAppsUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "mailForMac": 4, 
      "outlookForMac": 105, 
      "outlookForWindows": 1589, 
      "outlookForMobile": 1116, 
      "otherForMobile": 485, 
      "outlookForWeb": 753, 
      "pop3App": 0, 
      "imap4App": 0, 
      "smtpApp": 0, 
      "reportPeriod": "7"
    }
  ]
}
```