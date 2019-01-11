---
title: 'reportRoot: getMailboxUsageMailboxCounts'
description: Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe. Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico.
localization_priority: Normal
ms.openlocfilehash: c1b15824ab5313d1c581509936a84f5af2daee84
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856290"
---
# <a name="reportroot-getmailboxusagemailboxcounts"></a><span data-ttu-id="a4920-104">reportRoot: getMailboxUsageMailboxCounts</span><span class="sxs-lookup"><span data-stu-id="a4920-104">reportRoot: getMailboxUsageMailboxCounts</span></span>

> <span data-ttu-id="a4920-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4920-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4920-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4920-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a4920-107">Obtiene el número total de buzones de usuario en la organización y cuantos están activos cada día del período del informe.</span><span class="sxs-lookup"><span data-stu-id="a4920-107">Get the total number of user mailboxes in your organization and how many are active each day of the reporting period.</span></span> <span data-ttu-id="a4920-108">Un buzón se considera activo si el usuario envió o leyó cualquier correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="a4920-108">A mailbox is considered active if the user sent or read any email.</span></span>

> <span data-ttu-id="a4920-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="a4920-109">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="a4920-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="a4920-110">Permissions</span></span>

<span data-ttu-id="a4920-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a4920-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a4920-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a4920-113">Permission type</span></span>                        | <span data-ttu-id="a4920-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a4920-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="a4920-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a4920-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="a4920-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="a4920-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="a4920-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a4920-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a4920-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a4920-118">Not supported.</span></span>                           |
| <span data-ttu-id="a4920-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a4920-119">Application</span></span>                            | <span data-ttu-id="a4920-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="a4920-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="a4920-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a4920-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageMailboxCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="a4920-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="a4920-122">Function parameters</span></span>

<span data-ttu-id="a4920-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="a4920-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="a4920-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a4920-124">Parameter</span></span> | <span data-ttu-id="a4920-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4920-125">Type</span></span>   | <span data-ttu-id="a4920-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4920-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="a4920-127">period</span><span class="sxs-lookup"><span data-stu-id="a4920-127">period</span></span>    | <span data-ttu-id="a4920-128">cadena</span><span class="sxs-lookup"><span data-stu-id="a4920-128">string</span></span> | <span data-ttu-id="a4920-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="a4920-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="a4920-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="a4920-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="a4920-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="a4920-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="a4920-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="a4920-132">Required.</span></span> |

<span data-ttu-id="a4920-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4920-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="a4920-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="a4920-134">The default output type is text/csv.</span></span> <span data-ttu-id="a4920-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="a4920-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a4920-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a4920-136">Request headers</span></span>

| <span data-ttu-id="a4920-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="a4920-137">Name</span></span>          | <span data-ttu-id="a4920-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4920-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="a4920-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="a4920-139">Authorization</span></span> | <span data-ttu-id="a4920-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a4920-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="a4920-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4920-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="a4920-143">CSV</span><span class="sxs-lookup"><span data-stu-id="a4920-143">CSV</span></span>

<span data-ttu-id="a4920-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="a4920-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="a4920-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4920-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="a4920-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="a4920-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="a4920-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="a4920-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="a4920-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="a4920-148">Report Refresh Date</span></span>
- <span data-ttu-id="a4920-149">Total</span><span class="sxs-lookup"><span data-stu-id="a4920-149">Total</span></span>
- <span data-ttu-id="a4920-150">Activo</span><span class="sxs-lookup"><span data-stu-id="a4920-150">Active</span></span>
- <span data-ttu-id="a4920-151">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="a4920-151">Report Date</span></span>
- <span data-ttu-id="a4920-152">Período del informe</span><span class="sxs-lookup"><span data-stu-id="a4920-152">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="a4920-153">JSON</span><span class="sxs-lookup"><span data-stu-id="a4920-153">JSON</span></span>

<span data-ttu-id="a4920-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[mailboxUsageMailboxCounts](../resources/mailboxusagemailboxcounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4920-154">If successful, this method returns a `200 OK` response code and a **[mailboxUsageMailboxCounts](../resources/mailboxusagemailboxcounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a4920-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a4920-155">Example</span></span>

### <a name="csv"></a><span data-ttu-id="a4920-156">CSV</span><span class="sxs-lookup"><span data-stu-id="a4920-156">CSV</span></span>

<span data-ttu-id="a4920-157">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="a4920-157">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="a4920-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4920-158">Request</span></span>

<span data-ttu-id="a4920-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4920-159">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagemailboxcounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageMailboxCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="a4920-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4920-160">Response</span></span>

<span data-ttu-id="a4920-161">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4920-161">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="a4920-162">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4920-162">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="a4920-163">JSON</span><span class="sxs-lookup"><span data-stu-id="a4920-163">JSON</span></span>

<span data-ttu-id="a4920-164">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="a4920-164">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="a4920-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a4920-165">Request</span></span>

<span data-ttu-id="a4920-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a4920-166">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagemailboxcounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageMailboxCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="a4920-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a4920-167">Response</span></span>

<span data-ttu-id="a4920-168">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a4920-168">The following is an example of the response.</span></span>

> <span data-ttu-id="a4920-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a4920-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxUsageMailboxCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 232

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.mailboxUsageMailboxCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "total": 202, 
      "active": 198, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
