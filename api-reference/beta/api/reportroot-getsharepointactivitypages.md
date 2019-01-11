---
title: 'reportRoot: getSharePointActivityPages'
description: Obtiene el número de páginas únicas visitadas por los usuarios.
localization_priority: Normal
ms.openlocfilehash: 2c9f39467940b6aeab2a26568cb0e11c7dd4c616
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816726"
---
# <a name="reportroot-getsharepointactivitypages"></a><span data-ttu-id="3ecf7-103">reportRoot: getSharePointActivityPages</span><span class="sxs-lookup"><span data-stu-id="3ecf7-103">reportRoot: getSharePointActivityPages</span></span>

> <span data-ttu-id="3ecf7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3ecf7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3ecf7-106">Obtiene el número de páginas únicas visitadas por los usuarios.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-106">Get the number of unique pages visited by users.</span></span>

> <span data-ttu-id="3ecf7-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span><span class="sxs-lookup"><span data-stu-id="3ecf7-107">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint activity](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span></span>

## <a name="permissions"></a><span data-ttu-id="3ecf7-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3ecf7-108">Permissions</span></span>

<span data-ttu-id="3ecf7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3ecf7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3ecf7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3ecf7-111">Permission type</span></span>                        | <span data-ttu-id="3ecf7-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3ecf7-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3ecf7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3ecf7-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="3ecf7-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3ecf7-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="3ecf7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3ecf7-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3ecf7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-116">Not supported.</span></span>                           |
| <span data-ttu-id="3ecf7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3ecf7-117">Application</span></span>                            | <span data-ttu-id="3ecf7-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3ecf7-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3ecf7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3ecf7-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointActivityPages(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="3ecf7-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3ecf7-120">Function parameters</span></span>

<span data-ttu-id="3ecf7-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="3ecf7-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3ecf7-122">Parameter</span></span> | <span data-ttu-id="3ecf7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ecf7-123">Type</span></span>   | <span data-ttu-id="3ecf7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ecf7-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3ecf7-125">period</span><span class="sxs-lookup"><span data-stu-id="3ecf7-125">period</span></span>    | <span data-ttu-id="3ecf7-126">cadena</span><span class="sxs-lookup"><span data-stu-id="3ecf7-126">string</span></span> | <span data-ttu-id="3ecf7-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3ecf7-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3ecf7-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="3ecf7-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-130">Required.</span></span> |

<span data-ttu-id="3ecf7-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="3ecf7-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-132">The default output type is text/csv.</span></span> <span data-ttu-id="3ecf7-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3ecf7-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3ecf7-134">Request headers</span></span>

| <span data-ttu-id="3ecf7-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="3ecf7-135">Name</span></span>          | <span data-ttu-id="3ecf7-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ecf7-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="3ecf7-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="3ecf7-137">Authorization</span></span> | <span data-ttu-id="3ecf7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="3ecf7-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ecf7-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="3ecf7-141">CSV</span><span class="sxs-lookup"><span data-stu-id="3ecf7-141">CSV</span></span>

<span data-ttu-id="3ecf7-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3ecf7-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3ecf7-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3ecf7-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="3ecf7-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3ecf7-146">Report Refresh Date</span></span>
- <span data-ttu-id="3ecf7-147">Número de páginas visitadas</span><span class="sxs-lookup"><span data-stu-id="3ecf7-147">Visited Page Count</span></span>
- <span data-ttu-id="3ecf7-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="3ecf7-148">Report Date</span></span>
- <span data-ttu-id="3ecf7-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3ecf7-149">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="3ecf7-150">JSON</span><span class="sxs-lookup"><span data-stu-id="3ecf7-150">JSON</span></span>

<span data-ttu-id="3ecf7-151">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[sharePointActivityPages](../resources/sharepointactivitypages.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-151">If successful, this method returns a `200 OK` response code and a **[sharePointActivityPages](../resources/sharepointactivitypages.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3ecf7-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ecf7-152">Example</span></span>

### <a name="csv"></a><span data-ttu-id="3ecf7-153">CSV</span><span class="sxs-lookup"><span data-stu-id="3ecf7-153">CSV</span></span>

<span data-ttu-id="3ecf7-154">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-154">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="3ecf7-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ecf7-155">Request</span></span>

<span data-ttu-id="3ecf7-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-156">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivitypages_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityPages(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="3ecf7-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ecf7-157">Response</span></span>

<span data-ttu-id="3ecf7-158">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-158">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="3ecf7-159">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Visited Page Count,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="3ecf7-160">JSON</span><span class="sxs-lookup"><span data-stu-id="3ecf7-160">JSON</span></span>

<span data-ttu-id="3ecf7-161">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-161">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="3ecf7-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3ecf7-162">Request</span></span>

<span data-ttu-id="3ecf7-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-163">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getsharepointactivitypages_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSharePointActivityPages(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="3ecf7-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3ecf7-164">Response</span></span>

<span data-ttu-id="3ecf7-165">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-165">The following is an example of the response.</span></span>

> <span data-ttu-id="3ecf7-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3ecf7-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.sharePointActivityPages"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.sharePointActivityPages)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "visitedPageCount": 195, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
