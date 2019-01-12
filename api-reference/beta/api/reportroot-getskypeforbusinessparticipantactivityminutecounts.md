---
title: 'reportRoot: getSkypeForBusinessParticipantActivityMinuteCounts'
description: Obtiene tendencias de uso sobre la duración en minutos y el tipo de las sesiones de conferencia en las que participaron los usuarios de la organización. En los tipos de sesiones de conferencia, se incluyen sesiones de audio o vídeo.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 8f7f1953241753ac1170216db1a590ea7e4be8d9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945891"
---
# <a name="reportroot-getskypeforbusinessparticipantactivityminutecounts"></a><span data-ttu-id="bd1b0-104">reportRoot: getSkypeForBusinessParticipantActivityMinuteCounts</span><span class="sxs-lookup"><span data-stu-id="bd1b0-104">reportRoot: getSkypeForBusinessParticipantActivityMinuteCounts</span></span>

> <span data-ttu-id="bd1b0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bd1b0-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bd1b0-107">Obtiene tendencias de uso sobre la duración en minutos y el tipo de las sesiones de conferencia en las que participaron los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-107">Get usage trends on the length in minutes and type of conference sessions that users from your organization participated in.</span></span> <span data-ttu-id="bd1b0-108">En los tipos de sesiones de conferencia, se incluyen sesiones de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-108">Types of conference sessions include audio/video.</span></span>

> <span data-ttu-id="bd1b0-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de participantes de conferencias de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span><span class="sxs-lookup"><span data-stu-id="bd1b0-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference participant activity](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span></span>

## <a name="permissions"></a><span data-ttu-id="bd1b0-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="bd1b0-110">Permissions</span></span>

<span data-ttu-id="bd1b0-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bd1b0-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bd1b0-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bd1b0-113">Permission type</span></span>                        | <span data-ttu-id="bd1b0-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bd1b0-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="bd1b0-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bd1b0-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="bd1b0-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bd1b0-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="bd1b0-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bd1b0-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bd1b0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-118">Not supported.</span></span>                           |
| <span data-ttu-id="bd1b0-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bd1b0-119">Application</span></span>                            | <span data-ttu-id="bd1b0-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bd1b0-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="bd1b0-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bd1b0-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessParticipantActivityMinuteCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="bd1b0-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="bd1b0-122">Function parameters</span></span>

<span data-ttu-id="bd1b0-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="bd1b0-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bd1b0-124">Parameter</span></span> | <span data-ttu-id="bd1b0-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="bd1b0-125">Type</span></span>   | <span data-ttu-id="bd1b0-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd1b0-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="bd1b0-127">period</span><span class="sxs-lookup"><span data-stu-id="bd1b0-127">period</span></span>    | <span data-ttu-id="bd1b0-128">cadena</span><span class="sxs-lookup"><span data-stu-id="bd1b0-128">string</span></span> | <span data-ttu-id="bd1b0-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="bd1b0-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="bd1b0-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="bd1b0-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-132">Required.</span></span> |

<span data-ttu-id="bd1b0-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="bd1b0-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-134">The default output type is text/csv.</span></span> <span data-ttu-id="bd1b0-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="bd1b0-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bd1b0-136">Request headers</span></span>

| <span data-ttu-id="bd1b0-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="bd1b0-137">Name</span></span>          | <span data-ttu-id="bd1b0-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd1b0-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="bd1b0-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="bd1b0-139">Authorization</span></span> | <span data-ttu-id="bd1b0-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="bd1b0-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd1b0-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="bd1b0-143">CSV</span><span class="sxs-lookup"><span data-stu-id="bd1b0-143">CSV</span></span>

<span data-ttu-id="bd1b0-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="bd1b0-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="bd1b0-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="bd1b0-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="bd1b0-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="bd1b0-148">Report Refresh Date</span></span>
- <span data-ttu-id="bd1b0-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="bd1b0-149">Report Date</span></span>
- <span data-ttu-id="bd1b0-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="bd1b0-150">Report Period</span></span>
- <span data-ttu-id="bd1b0-151">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="bd1b0-151">Audio/Video</span></span>

### <a name="json"></a><span data-ttu-id="bd1b0-152">JSON</span><span class="sxs-lookup"><span data-stu-id="bd1b0-152">JSON</span></span>

<span data-ttu-id="bd1b0-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessParticipantActivityMinuteCounts](../resources/skypeforbusinessparticipantactivityminutecounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-153">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessParticipantActivityMinuteCounts](../resources/skypeforbusinessparticipantactivityminutecounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bd1b0-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bd1b0-154">Example</span></span>

### <a name="csv"></a><span data-ttu-id="bd1b0-155">CSV</span><span class="sxs-lookup"><span data-stu-id="bd1b0-155">CSV</span></span>

<span data-ttu-id="bd1b0-156">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-156">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="bd1b0-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd1b0-157">Request</span></span>

<span data-ttu-id="bd1b0-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessparticipantactivityminutecounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessParticipantActivityMinuteCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="bd1b0-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd1b0-159">Response</span></span>

<span data-ttu-id="bd1b0-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-160">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="bd1b0-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,Audio/Video
```

### <a name="json"></a><span data-ttu-id="bd1b0-162">JSON</span><span class="sxs-lookup"><span data-stu-id="bd1b0-162">JSON</span></span>

<span data-ttu-id="bd1b0-163">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-163">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="bd1b0-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bd1b0-164">Request</span></span>

<span data-ttu-id="bd1b0-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-165">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessparticipantactivityminutecounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessParticipantActivityMinuteCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="bd1b0-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bd1b0-166">Response</span></span>

<span data-ttu-id="bd1b0-167">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-167">The following is an example of the response.</span></span>

> <span data-ttu-id="bd1b0-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bd1b0-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessParticipantActivityMinuteCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 247

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessParticipantActivityMinuteCounts)", 
  "value": [
    {
      "audiovideo": 6267, 
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
