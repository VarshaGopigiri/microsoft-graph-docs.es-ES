---
title: 'reportRoot: getTeamsUserActivityCounts'
description: Obtener el número de actividades de Microsoft Teams por tipo de actividad. Los tipos de actividad son mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipo.
ms.openlocfilehash: 2ad0382dec905aab3490a66047916e5028d7b75f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088692"
---
# <a name="reportroot-getteamsuseractivitycounts"></a><span data-ttu-id="75fe0-104">reportRoot: getTeamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="75fe0-104">reportRoot: getTeamsUserActivityCounts</span></span>

> <span data-ttu-id="75fe0-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="75fe0-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="75fe0-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="75fe0-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="75fe0-107">Obtener el número de actividades de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="75fe0-107">Get the number of Microsoft Teams activities by activity type.</span></span> <span data-ttu-id="75fe0-108">Los tipos de actividad son mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipo.</span><span class="sxs-lookup"><span data-stu-id="75fe0-108">The activity types are team chat messages, private chat messages, calls, and meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="75fe0-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="75fe0-109">Permissions</span></span>

<span data-ttu-id="75fe0-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="75fe0-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="75fe0-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="75fe0-112">Permission type</span></span>                        | <span data-ttu-id="75fe0-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="75fe0-113">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="75fe0-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="75fe0-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="75fe0-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="75fe0-115">Reports.Read.All</span></span>                         |
| <span data-ttu-id="75fe0-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="75fe0-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="75fe0-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="75fe0-117">Not supported.</span></span>                           |
| <span data-ttu-id="75fe0-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="75fe0-118">Application</span></span>                            | <span data-ttu-id="75fe0-119">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="75fe0-119">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="75fe0-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="75fe0-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityCounts(period='D7')
```

## <a name="function-parameters"></a><span data-ttu-id="75fe0-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="75fe0-121">Function parameters</span></span>

<span data-ttu-id="75fe0-122">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="75fe0-122">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="75fe0-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="75fe0-123">Parameter</span></span> | <span data-ttu-id="75fe0-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="75fe0-124">Type</span></span>   | <span data-ttu-id="75fe0-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="75fe0-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="75fe0-126">period</span><span class="sxs-lookup"><span data-stu-id="75fe0-126">period</span></span>    | <span data-ttu-id="75fe0-127">cadena</span><span class="sxs-lookup"><span data-stu-id="75fe0-127">string</span></span> | <span data-ttu-id="75fe0-128">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="75fe0-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="75fe0-129">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="75fe0-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="75fe0-130">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="75fe0-130">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="75fe0-131">Necesario.</span><span class="sxs-lookup"><span data-stu-id="75fe0-131">Required.</span></span> |

<span data-ttu-id="75fe0-132">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75fe0-132">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="75fe0-133">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="75fe0-133">The default output type is text/csv.</span></span> <span data-ttu-id="75fe0-134">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="75fe0-134">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="75fe0-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="75fe0-135">Request headers</span></span>

| <span data-ttu-id="75fe0-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="75fe0-136">Name</span></span>          | <span data-ttu-id="75fe0-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="75fe0-137">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="75fe0-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="75fe0-138">Authorization</span></span> | <span data-ttu-id="75fe0-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="75fe0-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="75fe0-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75fe0-141">Response</span></span>

### <a name="csv"></a><span data-ttu-id="75fe0-142">CSV</span><span class="sxs-lookup"><span data-stu-id="75fe0-142">CSV</span></span>

<span data-ttu-id="75fe0-143">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="75fe0-143">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="75fe0-144">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75fe0-144">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="75fe0-145">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="75fe0-145">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="75fe0-146">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="75fe0-146">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="75fe0-147">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="75fe0-147">Report Refresh Date</span></span>
- <span data-ttu-id="75fe0-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="75fe0-148">Report Date</span></span>
- <span data-ttu-id="75fe0-149">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="75fe0-149">Team Chat Messages</span></span>
- <span data-ttu-id="75fe0-150">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="75fe0-150">Private Chat Messages</span></span>
- <span data-ttu-id="75fe0-151">Llamadas</span><span class="sxs-lookup"><span data-stu-id="75fe0-151">Calls</span></span>
- <span data-ttu-id="75fe0-152">Reuniones</span><span class="sxs-lookup"><span data-stu-id="75fe0-152">Meetings</span></span>
- <span data-ttu-id="75fe0-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="75fe0-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="75fe0-154">JSON</span><span class="sxs-lookup"><span data-stu-id="75fe0-154">JSON</span></span>

<span data-ttu-id="75fe0-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsUserActivityCounts](../resources/teamsuseractivitycounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75fe0-155">If successful, this method returns a `200 OK` response code and a **[teamsUserActivityCounts](../resources/teamsuseractivitycounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="75fe0-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="75fe0-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="75fe0-157">CSV</span><span class="sxs-lookup"><span data-stu-id="75fe0-157">CSV</span></span>

<span data-ttu-id="75fe0-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="75fe0-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="75fe0-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75fe0-159">Request</span></span>

<span data-ttu-id="75fe0-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75fe0-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivitycounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="75fe0-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75fe0-161">Response</span></span>

<span data-ttu-id="75fe0-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75fe0-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```
<span data-ttu-id="75fe0-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="75fe0-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Report Period
```

### <a name="json"></a><span data-ttu-id="75fe0-164">JSON</span><span class="sxs-lookup"><span data-stu-id="75fe0-164">JSON</span></span>

<span data-ttu-id="75fe0-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="75fe0-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="75fe0-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="75fe0-166">Request</span></span>

<span data-ttu-id="75fe0-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="75fe0-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivitycounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="75fe0-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="75fe0-168">Response</span></span>

<span data-ttu-id="75fe0-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="75fe0-169">The following is an example of the response.</span></span>

> <span data-ttu-id="75fe0-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="75fe0-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsUserActivityCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 277

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsUserActivityCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "teamChatMessages": 26, 
      "privateChatMessages": 17, 
      "calls": 4, 
      "meetings": 0, 
      "reportPeriod": "7"
    }
  ]
}
```