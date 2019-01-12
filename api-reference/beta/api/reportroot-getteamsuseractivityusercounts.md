---
title: 'reportRoot: getTeamsUserActivityUserCounts'
description: Obtener el número de usuarios de Microsoft Teams por tipo de actividad. Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 1cc651d1237ca9455ff6f6ab402ba3c6332f9873
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975865"
---
# <a name="reportroot-getteamsuseractivityusercounts"></a><span data-ttu-id="66167-104">reportRoot: getTeamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="66167-104">reportRoot: getTeamsUserActivityUserCounts</span></span>

> <span data-ttu-id="66167-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66167-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66167-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66167-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="66167-107">Obtener el número de usuarios de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="66167-107">Get the number of Microsoft Teams users by activity type.</span></span> <span data-ttu-id="66167-108">Los tipos de actividad son el número de mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipos.</span><span class="sxs-lookup"><span data-stu-id="66167-108">The activity types are number of teams chat messages, private chat messages, calls, or meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="66167-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="66167-109">Permissions</span></span>

<span data-ttu-id="66167-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="66167-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="66167-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="66167-112">Permission type</span></span>                        | <span data-ttu-id="66167-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="66167-113">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="66167-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="66167-114">Delegated (work or school account)</span></span>     | <span data-ttu-id="66167-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="66167-115">Reports.Read.All</span></span>                         |
| <span data-ttu-id="66167-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="66167-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66167-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="66167-117">Not supported.</span></span>                           |
| <span data-ttu-id="66167-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="66167-118">Application</span></span>                            | <span data-ttu-id="66167-119">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="66167-119">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="66167-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66167-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserCounts(period='D7')
```

## <a name="function-parameters"></a><span data-ttu-id="66167-121">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="66167-121">Function parameters</span></span>

<span data-ttu-id="66167-122">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="66167-122">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="66167-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="66167-123">Parameter</span></span> | <span data-ttu-id="66167-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="66167-124">Type</span></span>   | <span data-ttu-id="66167-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="66167-125">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="66167-126">period</span><span class="sxs-lookup"><span data-stu-id="66167-126">period</span></span>    | <span data-ttu-id="66167-127">cadena</span><span class="sxs-lookup"><span data-stu-id="66167-127">string</span></span> | <span data-ttu-id="66167-128">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="66167-128">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="66167-129">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="66167-129">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="66167-130">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="66167-130">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="66167-131">Necesario.</span><span class="sxs-lookup"><span data-stu-id="66167-131">Required.</span></span> |

<span data-ttu-id="66167-132">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66167-132">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="66167-133">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="66167-133">The default output type is text/csv.</span></span> <span data-ttu-id="66167-134">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="66167-134">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="66167-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66167-135">Request headers</span></span>

| <span data-ttu-id="66167-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="66167-136">Name</span></span>          | <span data-ttu-id="66167-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="66167-137">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="66167-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="66167-138">Authorization</span></span> | <span data-ttu-id="66167-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66167-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="66167-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66167-141">Response</span></span>

### <a name="csv"></a><span data-ttu-id="66167-142">CSV</span><span class="sxs-lookup"><span data-stu-id="66167-142">CSV</span></span>

<span data-ttu-id="66167-143">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="66167-143">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="66167-144">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66167-144">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="66167-145">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="66167-145">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="66167-146">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="66167-146">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="66167-147">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="66167-147">Report Refresh Date</span></span>
- <span data-ttu-id="66167-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="66167-148">Report Date</span></span>
- <span data-ttu-id="66167-149">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="66167-149">Team Chat Messages</span></span>
- <span data-ttu-id="66167-150">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="66167-150">Private Chat Messages</span></span>
- <span data-ttu-id="66167-151">Llamadas</span><span class="sxs-lookup"><span data-stu-id="66167-151">Calls</span></span>
- <span data-ttu-id="66167-152">Reuniones</span><span class="sxs-lookup"><span data-stu-id="66167-152">Meetings</span></span>
- <span data-ttu-id="66167-153">Otras acciones</span><span class="sxs-lookup"><span data-stu-id="66167-153">Other Actions</span></span>
- <span data-ttu-id="66167-154">Período del informe</span><span class="sxs-lookup"><span data-stu-id="66167-154">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="66167-155">JSON</span><span class="sxs-lookup"><span data-stu-id="66167-155">JSON</span></span>

<span data-ttu-id="66167-156">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[teamsUserActivityUserCounts](../resources/teamsuseractivityusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66167-156">If successful, this method returns a `200 OK` response code and a **[teamsUserActivityUserCounts](../resources/teamsuseractivityusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="66167-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66167-157">Example</span></span>

### <a name="csv"></a><span data-ttu-id="66167-158">CSV</span><span class="sxs-lookup"><span data-stu-id="66167-158">CSV</span></span>

<span data-ttu-id="66167-159">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="66167-159">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="66167-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66167-160">Request</span></span>

<span data-ttu-id="66167-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66167-161">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="66167-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66167-162">Response</span></span>

<span data-ttu-id="66167-163">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66167-163">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="66167-164">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="66167-164">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Other Actions,Report Period
```

### <a name="json"></a><span data-ttu-id="66167-165">JSON</span><span class="sxs-lookup"><span data-stu-id="66167-165">JSON</span></span>

<span data-ttu-id="66167-166">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="66167-166">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="66167-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66167-167">Request</span></span>

<span data-ttu-id="66167-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66167-168">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getTeamsUserActivityUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="66167-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66167-169">Response</span></span>

<span data-ttu-id="66167-170">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66167-170">The following is an example of the response.</span></span>

> <span data-ttu-id="66167-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66167-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.teamsUserActivityUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 291

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.teamsUserActivityUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "teamChatMessages": 30, 
      "privateChatMessages": 21, 
      "calls": 6, 
      "meetings": 2, 
      "otherActions": 17, 
      "reportPeriod": "7"
    }
  ]
}
```
