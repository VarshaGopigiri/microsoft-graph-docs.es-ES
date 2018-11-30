---
title: 'reportRoot: getMailboxUsageDetail'
description: Obtiene información sobre el uso de buzones.
ms.openlocfilehash: 317d258a51250992c47b20675bb2cb580ce408dd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083148"
---
# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="fe7f7-103">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="fe7f7-103">reportRoot: getMailboxUsageDetail</span></span>

> <span data-ttu-id="fe7f7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe7f7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe7f7-106">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-106">Get details about mailbox usage.</span></span>

> <span data-ttu-id="fe7f7-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="fe7f7-107">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="fe7f7-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="fe7f7-108">Permissions</span></span>

<span data-ttu-id="fe7f7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fe7f7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="fe7f7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fe7f7-111">Permission type</span></span>                        | <span data-ttu-id="fe7f7-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="fe7f7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="fe7f7-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="fe7f7-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="fe7f7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fe7f7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-116">Not supported.</span></span>                           |
| <span data-ttu-id="fe7f7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fe7f7-117">Application</span></span>                            | <span data-ttu-id="fe7f7-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="fe7f7-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="fe7f7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fe7f7-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="fe7f7-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="fe7f7-120">Function parameters</span></span>

<span data-ttu-id="fe7f7-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="fe7f7-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fe7f7-122">Parameter</span></span> | <span data-ttu-id="fe7f7-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe7f7-123">Type</span></span>   | <span data-ttu-id="fe7f7-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe7f7-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="fe7f7-125">period</span><span class="sxs-lookup"><span data-stu-id="fe7f7-125">period</span></span>    | <span data-ttu-id="fe7f7-126">cadena</span><span class="sxs-lookup"><span data-stu-id="fe7f7-126">string</span></span> | <span data-ttu-id="fe7f7-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="fe7f7-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="fe7f7-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="fe7f7-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-130">Required.</span></span> |

<span data-ttu-id="fe7f7-131">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-131">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="fe7f7-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-132">The default output type is text/csv.</span></span> <span data-ttu-id="fe7f7-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="fe7f7-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fe7f7-134">Request headers</span></span>

| <span data-ttu-id="fe7f7-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="fe7f7-135">Name</span></span>          | <span data-ttu-id="fe7f7-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe7f7-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="fe7f7-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="fe7f7-137">Authorization</span></span> | <span data-ttu-id="fe7f7-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="fe7f7-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe7f7-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="fe7f7-141">CSV</span><span class="sxs-lookup"><span data-stu-id="fe7f7-141">CSV</span></span>

<span data-ttu-id="fe7f7-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="fe7f7-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="fe7f7-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="fe7f7-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="fe7f7-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="fe7f7-146">Report Refresh Date</span></span>
- <span data-ttu-id="fe7f7-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="fe7f7-147">User Principal Name</span></span>
- <span data-ttu-id="fe7f7-148">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="fe7f7-148">Display Name</span></span>
- <span data-ttu-id="fe7f7-149">Eliminado</span><span class="sxs-lookup"><span data-stu-id="fe7f7-149">Is Deleted</span></span>
- <span data-ttu-id="fe7f7-150">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="fe7f7-150">Deleted Date</span></span>
- <span data-ttu-id="fe7f7-151">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="fe7f7-151">Created Date</span></span>
- <span data-ttu-id="fe7f7-152">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="fe7f7-152">Last Activity Date</span></span>
- <span data-ttu-id="fe7f7-153">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="fe7f7-153">Item Count</span></span>
- <span data-ttu-id="fe7f7-154">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-154">Storage Used (Byte)</span></span>
- <span data-ttu-id="fe7f7-155">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-155">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="fe7f7-156">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-156">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="fe7f7-157">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="fe7f7-157">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="fe7f7-158">Período del informe</span><span class="sxs-lookup"><span data-stu-id="fe7f7-158">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="fe7f7-159">JSON</span><span class="sxs-lookup"><span data-stu-id="fe7f7-159">JSON</span></span>

<span data-ttu-id="fe7f7-160">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[mailboxUsageDetail](../resources/mailboxusagedetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-160">If successful, this method returns a `200 OK` response code and a **[mailboxUsageDetail](../resources/mailboxusagedetail.md)** object in the response body.</span></span>

<span data-ttu-id="fe7f7-161">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-161">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="fe7f7-162">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fe7f7-162">Example</span></span>

### <a name="csv"></a><span data-ttu-id="fe7f7-163">CSV</span><span class="sxs-lookup"><span data-stu-id="fe7f7-163">CSV</span></span>

<span data-ttu-id="fe7f7-164">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-164">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="fe7f7-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe7f7-165">Request</span></span>

<span data-ttu-id="fe7f7-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-166">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagedetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="fe7f7-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe7f7-167">Response</span></span>

<span data-ttu-id="fe7f7-168">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-168">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="fe7f7-169">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-169">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```

### <a name="json"></a><span data-ttu-id="fe7f7-170">JSON</span><span class="sxs-lookup"><span data-stu-id="fe7f7-170">JSON</span></span>

<span data-ttu-id="fe7f7-171">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-171">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="fe7f7-172">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fe7f7-172">Request</span></span>

<span data-ttu-id="fe7f7-173">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-173">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getmailboxusagedetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getMailboxUsageDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="fe7f7-174">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fe7f7-174">Response</span></span>

<span data-ttu-id="fe7f7-175">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-175">The following is an example of the response.</span></span>

> <span data-ttu-id="fe7f7-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fe7f7-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailboxUsageDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 526

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.mailboxUsageDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userPrincipalName-value", 
      "displayName": "displayName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "createdDate": "2016-03-30", 
      "lastActivityDate": "2017-09-01", 
      "itemCount": 138481, 
      "storageUsedInBytes": 10414748704, 
      "issueWarningQuotaInBytes": 10522698752, 
      "prohibitSendQuotaInBytes": 10630040576, 
      "prohibitSendReceiveQuotaInBytes": 10737418240, 
      "reportPeriod": "7"
    }
  ]
}
```
