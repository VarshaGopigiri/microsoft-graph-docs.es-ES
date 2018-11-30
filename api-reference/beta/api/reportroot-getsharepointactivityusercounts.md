---
title: 'reportRoot: getSharePointActivityUserCounts'
description: Obtiene la tendencia del número de usuarios activos. Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado.
ms.openlocfilehash: d0b68e2c5f62be7e52389d9bcb7b53aae1f60736
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091134"
---
# <a name="reportroot-getsharepointactivityusercounts"></a><span data-ttu-id="99180-104">reportRoot: getSharePointActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="99180-104">reportRoot: getSharePointActivityUserCounts</span></span>

> <span data-ttu-id="99180-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="99180-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="99180-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="99180-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="99180-107">Obtiene la tendencia del número de usuarios activos.</span><span class="sxs-lookup"><span data-stu-id="99180-107">Get the trend in the number of active users.</span></span> <span data-ttu-id="99180-108">Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="99180-108">A user is considered active if he or she has executed a file activity (save, sync, modify, or share) or visited a page within the specified time period.</span></span>

> <span data-ttu-id="99180-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span><span class="sxs-lookup"><span data-stu-id="99180-109">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint activity](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span></span>

## <a name="permissions"></a><span data-ttu-id="99180-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="99180-110">Permissions</span></span>

<span data-ttu-id="99180-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="99180-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="99180-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99180-113">Permission type</span></span>                        | <span data-ttu-id="99180-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99180-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="99180-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99180-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="99180-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="99180-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="99180-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99180-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="99180-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="99180-118">Not supported.</span></span>                           |
| <span data-ttu-id="99180-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99180-119">Application</span></span>                            | <span data-ttu-id="99180-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="99180-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="99180-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99180-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="99180-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="99180-122">Function parameters</span></span>

<span data-ttu-id="99180-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="99180-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="99180-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="99180-124">Parameter</span></span> | <span data-ttu-id="99180-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="99180-125">Type</span></span>   | <span data-ttu-id="99180-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="99180-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="99180-127">period</span><span class="sxs-lookup"><span data-stu-id="99180-127">period</span></span>    | <span data-ttu-id="99180-128">cadena</span><span class="sxs-lookup"><span data-stu-id="99180-128">string</span></span> | <span data-ttu-id="99180-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="99180-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="99180-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="99180-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="99180-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="99180-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="99180-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="99180-132">Required.</span></span> |

<span data-ttu-id="99180-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99180-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="99180-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="99180-134">The default output type is text/csv.</span></span> <span data-ttu-id="99180-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="99180-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="99180-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99180-136">Request headers</span></span>

| <span data-ttu-id="99180-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="99180-137">Name</span></span>          | <span data-ttu-id="99180-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="99180-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="99180-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="99180-139">Authorization</span></span> | <span data-ttu-id="99180-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99180-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="99180-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99180-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="99180-143">CSV</span><span class="sxs-lookup"><span data-stu-id="99180-143">CSV</span></span>

<span data-ttu-id="99180-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="99180-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="99180-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99180-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="99180-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="99180-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="99180-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="99180-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="99180-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="99180-148">Report Refresh Date</span></span>
- <span data-ttu-id="99180-149">Página visitada</span><span class="sxs-lookup"><span data-stu-id="99180-149">Visited Page</span></span>
- <span data-ttu-id="99180-150">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="99180-150">Viewed Or Edited</span></span>
- <span data-ttu-id="99180-151">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="99180-151">Synced</span></span>
- <span data-ttu-id="99180-152">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="99180-152">Shared Internally</span></span>
- <span data-ttu-id="99180-153">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="99180-153">Shared Externally</span></span>
- <span data-ttu-id="99180-154">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="99180-154">Report Date</span></span>
- <span data-ttu-id="99180-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="99180-155">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="99180-156">JSON</span><span class="sxs-lookup"><span data-stu-id="99180-156">JSON</span></span>

<span data-ttu-id="99180-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[sharePointActivityUserCounts](../resources/sharepointactivityusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99180-157">If successful, this method returns a `200 OK` response code and a **[sharePointActivityUserCounts](../resources/sharepointactivityusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="99180-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99180-158">Example</span></span>

### <a name="csv"></a><span data-ttu-id="99180-159">CSV</span><span class="sxs-lookup"><span data-stu-id="99180-159">CSV</span></span>

<span data-ttu-id="99180-160">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="99180-160">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="99180-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99180-161">Request</span></span>

<span data-ttu-id="99180-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99180-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivityusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="99180-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99180-163">Response</span></span>

<span data-ttu-id="99180-164">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99180-164">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="99180-165">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="99180-165">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Visited Page,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="99180-166">JSON</span><span class="sxs-lookup"><span data-stu-id="99180-166">JSON</span></span>

<span data-ttu-id="99180-167">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="99180-167">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="99180-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99180-168">Request</span></span>

<span data-ttu-id="99180-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99180-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivityusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="99180-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99180-170">Response</span></span>

<span data-ttu-id="99180-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99180-171">The following is an example of the response.</span></span>

> <span data-ttu-id="99180-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99180-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharePointActivityUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 302

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.sharePointActivityUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "visitedPage": 56, 
      "viewedOrEdited": 163, 
      "synced": 7, 
      "sharedInternally": 10, 
      "sharedExternally": 1, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
