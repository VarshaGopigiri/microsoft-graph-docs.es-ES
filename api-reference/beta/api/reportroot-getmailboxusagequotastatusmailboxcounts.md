---
title: 'reportRoot: getMailboxUsageQuotaStatusMailboxCounts'
description: Obtiene el número de buzones de usuario en cada categoría de cuota.
localization_priority: Normal
ms.openlocfilehash: e27418900e79597fcaac7795003983e71b91f66d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823754"
---
# <a name="reportroot-getmailboxusagequotastatusmailboxcounts"></a><span data-ttu-id="3d241-103">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="3d241-103">reportRoot: getMailboxUsageQuotaStatusMailboxCounts</span></span>

> <span data-ttu-id="3d241-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3d241-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3d241-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3d241-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3d241-106">Obtiene el número de buzones de usuario en cada categoría de cuota.</span><span class="sxs-lookup"><span data-stu-id="3d241-106">Get the count of user mailboxes in each quota category.</span></span>

> <span data-ttu-id="3d241-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="3d241-107">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="3d241-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d241-108">Permissions</span></span>

<span data-ttu-id="3d241-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d241-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3d241-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d241-111">Permission type</span></span>                        | <span data-ttu-id="3d241-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d241-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3d241-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d241-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="3d241-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d241-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="3d241-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d241-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d241-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d241-116">Not supported.</span></span>                           |
| <span data-ttu-id="3d241-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d241-117">Application</span></span>                            | <span data-ttu-id="3d241-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d241-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3d241-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d241-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageQuotaStatusMailboxCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="3d241-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3d241-120">Function parameters</span></span>

<span data-ttu-id="3d241-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3d241-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="3d241-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3d241-122">Parameter</span></span> | <span data-ttu-id="3d241-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d241-123">Type</span></span>   | <span data-ttu-id="3d241-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d241-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3d241-125">period</span><span class="sxs-lookup"><span data-stu-id="3d241-125">period</span></span>    | <span data-ttu-id="3d241-126">cadena</span><span class="sxs-lookup"><span data-stu-id="3d241-126">string</span></span> | <span data-ttu-id="3d241-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d241-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3d241-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3d241-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3d241-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d241-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="3d241-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3d241-130">Required.</span></span> |

<span data-ttu-id="3d241-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d241-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="3d241-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="3d241-132">The default output type is text/csv.</span></span> <span data-ttu-id="3d241-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="3d241-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3d241-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d241-134">Request headers</span></span>

| <span data-ttu-id="3d241-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d241-135">Name</span></span>          | <span data-ttu-id="3d241-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d241-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="3d241-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d241-137">Authorization</span></span> | <span data-ttu-id="3d241-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d241-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="3d241-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d241-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="3d241-141">CSV</span><span class="sxs-lookup"><span data-stu-id="3d241-141">CSV</span></span>

<span data-ttu-id="3d241-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3d241-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3d241-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d241-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3d241-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3d241-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3d241-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3d241-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="3d241-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3d241-146">Report Refresh Date</span></span>
- <span data-ttu-id="3d241-147">Por debajo del límite</span><span class="sxs-lookup"><span data-stu-id="3d241-147">Under Limit</span></span>
- <span data-ttu-id="3d241-148">Advertencia emitida</span><span class="sxs-lookup"><span data-stu-id="3d241-148">Warning Issued</span></span>
- <span data-ttu-id="3d241-149">Envío prohibido</span><span class="sxs-lookup"><span data-stu-id="3d241-149">Send Prohibited</span></span>
- <span data-ttu-id="3d241-150">Envío o recepción prohibidos</span><span class="sxs-lookup"><span data-stu-id="3d241-150">Send/Receive Prohibited</span></span>
- <span data-ttu-id="3d241-151">Indeterminado</span><span class="sxs-lookup"><span data-stu-id="3d241-151">Indeterminate</span></span>
- <span data-ttu-id="3d241-152">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="3d241-152">Report Date</span></span>
- <span data-ttu-id="3d241-153">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3d241-153">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="3d241-154">JSON</span><span class="sxs-lookup"><span data-stu-id="3d241-154">JSON</span></span>

<span data-ttu-id="3d241-155">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[mailboxUsageQuotaStatusMailboxCounts](../resources/mailboxusagequotastatusmailboxcounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d241-155">If successful, this method returns a `200 OK` response code and a **[mailboxUsageQuotaStatusMailboxCounts](../resources/mailboxusagequotastatusmailboxcounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3d241-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d241-156">Example</span></span>

### <a name="csv"></a><span data-ttu-id="3d241-157">CSV</span><span class="sxs-lookup"><span data-stu-id="3d241-157">CSV</span></span>

<span data-ttu-id="3d241-158">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="3d241-158">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="3d241-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d241-159">Request</span></span>

<span data-ttu-id="3d241-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d241-160">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagequotastatusmailboxcounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageQuotaStatusMailboxCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="3d241-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d241-161">Response</span></span>

<span data-ttu-id="3d241-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d241-162">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="3d241-163">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d241-163">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Under Limit,Warning Issued,Send Prohibited,Send/Receive Prohibited,Indeterminate,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="3d241-164">JSON</span><span class="sxs-lookup"><span data-stu-id="3d241-164">JSON</span></span>

<span data-ttu-id="3d241-165">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="3d241-165">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="3d241-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d241-166">Request</span></span>

<span data-ttu-id="3d241-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d241-167">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagequotastatusmailboxcounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageQuotaStatusMailboxCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="3d241-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d241-168">Response</span></span>

<span data-ttu-id="3d241-169">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d241-169">The following is an example of the response.</span></span>

> <span data-ttu-id="3d241-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3d241-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxUsageQuotaStatusMailboxCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 311

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.mailboxUsageQuotaMailboxStatusCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "underLimit": 155, 
      "warningIssued": 0, 
      "sendProhibited": 0, 
      "sendReceiveProhibited": 0, 
      "indeterminate": 14, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
