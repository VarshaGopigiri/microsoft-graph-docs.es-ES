---
title: 'reportRoot: getYammerGroupsActivityCounts'
description: Obtiene el número de mensajes de Yammer publicados, leídos y etiquetados como “Me gusta” en grupos.
ms.openlocfilehash: 2850bf9e1076f545005721062ee8cf4733d55bb5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088505"
---
# <a name="reportroot-getyammergroupsactivitycounts"></a><span data-ttu-id="ab291-103">reportRoot: getYammerGroupsActivityCounts</span><span class="sxs-lookup"><span data-stu-id="ab291-103">reportRoot: getYammerGroupsActivityCounts</span></span>

> <span data-ttu-id="ab291-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab291-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab291-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab291-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab291-106">Obtiene el número de mensajes de Yammer publicados, leídos y etiquetados como “Me gusta” en grupos.</span><span class="sxs-lookup"><span data-stu-id="ab291-106">Get the number of Yammer messages posted, read, and liked in groups.</span></span>

> <span data-ttu-id="ab291-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="ab291-107">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="ab291-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab291-108">Permissions</span></span>

<span data-ttu-id="ab291-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ab291-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ab291-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab291-111">Permission type</span></span>                        | <span data-ttu-id="ab291-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab291-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ab291-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab291-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="ab291-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ab291-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ab291-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab291-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab291-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab291-116">Not supported.</span></span>                           |
| <span data-ttu-id="ab291-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab291-117">Application</span></span>                            | <span data-ttu-id="ab291-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ab291-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ab291-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab291-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ab291-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ab291-120">Function parameters</span></span>

<span data-ttu-id="ab291-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ab291-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ab291-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ab291-122">Parameter</span></span> | <span data-ttu-id="ab291-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab291-123">Type</span></span>   | <span data-ttu-id="ab291-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab291-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ab291-125">period</span><span class="sxs-lookup"><span data-stu-id="ab291-125">period</span></span>    | <span data-ttu-id="ab291-126">cadena</span><span class="sxs-lookup"><span data-stu-id="ab291-126">string</span></span> | <span data-ttu-id="ab291-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ab291-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ab291-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ab291-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ab291-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ab291-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ab291-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ab291-130">Required.</span></span> |

<span data-ttu-id="ab291-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab291-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="ab291-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="ab291-132">The default output type is text/csv.</span></span> <span data-ttu-id="ab291-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="ab291-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ab291-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab291-134">Request headers</span></span>

| <span data-ttu-id="ab291-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab291-135">Name</span></span>          | <span data-ttu-id="ab291-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab291-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="ab291-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab291-137">Authorization</span></span> | <span data-ttu-id="ab291-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab291-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="ab291-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab291-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="ab291-141">CSV</span><span class="sxs-lookup"><span data-stu-id="ab291-141">CSV</span></span>

<span data-ttu-id="ab291-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ab291-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ab291-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab291-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ab291-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ab291-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ab291-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ab291-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ab291-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ab291-146">Report Refresh Date</span></span>
- <span data-ttu-id="ab291-147">Etiquetado como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="ab291-147">Liked</span></span>
- <span data-ttu-id="ab291-148">Publicado</span><span class="sxs-lookup"><span data-stu-id="ab291-148">Posted</span></span>
- <span data-ttu-id="ab291-149">Leído</span><span class="sxs-lookup"><span data-stu-id="ab291-149">Read</span></span>
- <span data-ttu-id="ab291-150">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ab291-150">Report Date</span></span>
- <span data-ttu-id="ab291-151">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ab291-151">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="ab291-152">JSON</span><span class="sxs-lookup"><span data-stu-id="ab291-152">JSON</span></span>

<span data-ttu-id="ab291-153">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[yammerGroupsActivityCounts](../resources/yammergroupsactivitycounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab291-153">If successful, this method returns a `200 OK` response code and a **[yammerGroupsActivityCounts](../resources/yammergroupsactivitycounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ab291-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab291-154">Example</span></span>

### <a name="csv"></a><span data-ttu-id="ab291-155">CSV</span><span class="sxs-lookup"><span data-stu-id="ab291-155">CSV</span></span>

<span data-ttu-id="ab291-156">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="ab291-156">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="ab291-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab291-157">Request</span></span>

<span data-ttu-id="ab291-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab291-158">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitycounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="ab291-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab291-159">Response</span></span>

<span data-ttu-id="ab291-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab291-160">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="ab291-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab291-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Liked,Posted,Read,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="ab291-162">JSON</span><span class="sxs-lookup"><span data-stu-id="ab291-162">JSON</span></span>

<span data-ttu-id="ab291-163">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="ab291-163">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="ab291-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab291-164">Request</span></span>

<span data-ttu-id="ab291-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab291-165">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitycounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getYammerGroupsActivityCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="ab291-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab291-166">Response</span></span>

<span data-ttu-id="ab291-167">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab291-167">The following is an example of the response.</span></span>

> <span data-ttu-id="ab291-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab291-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.yammerGroupsActivityCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 241

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.yammerGroupsActivityCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "liked": 13, 
      "posted": 50, 
      "read": 69, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
