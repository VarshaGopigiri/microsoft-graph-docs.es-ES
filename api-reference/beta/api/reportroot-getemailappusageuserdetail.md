---
title: 'reportRoot: getEmailAppUsageUserDetail'
description: Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: c6508985ad71570bb59679456ddc4ea9d2a853d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27992024"
---
# <a name="reportroot-getemailappusageuserdetail"></a><span data-ttu-id="7b0a4-103">reportRoot: getEmailAppUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="7b0a4-103">reportRoot: getEmailAppUsageUserDetail</span></span>

> <span data-ttu-id="7b0a4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7b0a4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7b0a4-106">Obtiene información sobre las actividades que realizaron los usuarios en las diferentes aplicaciones de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-106">Get details about which activities users performed on the various email apps.</span></span>

> <span data-ttu-id="7b0a4-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="7b0a4-107">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="7b0a4-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7b0a4-108">Permissions</span></span>

<span data-ttu-id="7b0a4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7b0a4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7b0a4-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b0a4-111">Permission type</span></span>                        | <span data-ttu-id="7b0a4-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b0a4-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7b0a4-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b0a4-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="7b0a4-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b0a4-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7b0a4-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b0a4-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7b0a4-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-116">Not supported.</span></span>                           |
| <span data-ttu-id="7b0a4-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b0a4-117">Application</span></span>                            | <span data-ttu-id="7b0a4-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7b0a4-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7b0a4-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b0a4-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageUserDetail(period='{period_value}')
GET /reports/getEmailAppUsageUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="7b0a4-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="7b0a4-120">Function parameters</span></span>

<span data-ttu-id="7b0a4-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="7b0a4-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7b0a4-122">Parameter</span></span> | <span data-ttu-id="7b0a4-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b0a4-123">Type</span></span>   | <span data-ttu-id="7b0a4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b0a4-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7b0a4-125">period</span><span class="sxs-lookup"><span data-stu-id="7b0a4-125">period</span></span>    | <span data-ttu-id="7b0a4-126">cadena</span><span class="sxs-lookup"><span data-stu-id="7b0a4-126">string</span></span> | <span data-ttu-id="7b0a4-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7b0a4-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7b0a4-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="7b0a4-130">date</span><span class="sxs-lookup"><span data-stu-id="7b0a4-130">date</span></span>      | <span data-ttu-id="7b0a4-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="7b0a4-131">Date</span></span>   | <span data-ttu-id="7b0a4-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="7b0a4-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="7b0a4-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="7b0a4-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="7b0a4-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="7b0a4-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-137">The default output type is text/csv.</span></span> <span data-ttu-id="7b0a4-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7b0a4-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b0a4-139">Request headers</span></span>

| <span data-ttu-id="7b0a4-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b0a4-140">Name</span></span>          | <span data-ttu-id="7b0a4-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b0a4-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="7b0a4-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="7b0a4-142">Authorization</span></span> | <span data-ttu-id="7b0a4-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="7b0a4-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b0a4-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="7b0a4-146">CSV</span><span class="sxs-lookup"><span data-stu-id="7b0a4-146">CSV</span></span>

<span data-ttu-id="7b0a4-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7b0a4-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7b0a4-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7b0a4-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7b0a4-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7b0a4-151">Report Refresh Date</span></span>
- <span data-ttu-id="7b0a4-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="7b0a4-152">User Principal Name</span></span>
- <span data-ttu-id="7b0a4-153">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="7b0a4-153">Display Name</span></span>
- <span data-ttu-id="7b0a4-154">Eliminado</span><span class="sxs-lookup"><span data-stu-id="7b0a4-154">Is Deleted</span></span>
- <span data-ttu-id="7b0a4-155">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="7b0a4-155">Deleted Date</span></span>
- <span data-ttu-id="7b0a4-156">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="7b0a4-156">Last Activity Date</span></span>
- <span data-ttu-id="7b0a4-157">Mail para Mac</span><span class="sxs-lookup"><span data-stu-id="7b0a4-157">Mail For Mac</span></span>
- <span data-ttu-id="7b0a4-158">Outlook para Mac</span><span class="sxs-lookup"><span data-stu-id="7b0a4-158">Outlook For Mac</span></span>
- <span data-ttu-id="7b0a4-159">Outlook para Windows</span><span class="sxs-lookup"><span data-stu-id="7b0a4-159">Outlook For Windows</span></span>
- <span data-ttu-id="7b0a4-160">Outlook para móviles</span><span class="sxs-lookup"><span data-stu-id="7b0a4-160">Outlook For Mobile</span></span>
- <span data-ttu-id="7b0a4-161">Otros para móviles</span><span class="sxs-lookup"><span data-stu-id="7b0a4-161">Other For Mobile</span></span>
- <span data-ttu-id="7b0a4-162">Outlook para web</span><span class="sxs-lookup"><span data-stu-id="7b0a4-162">Outlook For Web</span></span>
- <span data-ttu-id="7b0a4-163">Aplicación POP3</span><span class="sxs-lookup"><span data-stu-id="7b0a4-163">POP3 App</span></span>
- <span data-ttu-id="7b0a4-164">Aplicación IMAP4</span><span class="sxs-lookup"><span data-stu-id="7b0a4-164">IMAP4 App</span></span>
- <span data-ttu-id="7b0a4-165">Aplicación SMTP</span><span class="sxs-lookup"><span data-stu-id="7b0a4-165">SMTP App</span></span>
- <span data-ttu-id="7b0a4-166">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7b0a4-166">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="7b0a4-167">JSON</span><span class="sxs-lookup"><span data-stu-id="7b0a4-167">JSON</span></span>

<span data-ttu-id="7b0a4-168">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[emailAppUsageUserDetail](../resources/emailappusageuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-168">If successful, this method returns a `200 OK` response code and an **[emailAppUsageUserDetail](../resources/emailappusageuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="7b0a4-169">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-169">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="7b0a4-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b0a4-170">Example</span></span>

### <a name="csv"></a><span data-ttu-id="7b0a4-171">CSV</span><span class="sxs-lookup"><span data-stu-id="7b0a4-171">CSV</span></span>

<span data-ttu-id="7b0a4-172">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-172">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="7b0a4-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b0a4-173">Request</span></span>

<span data-ttu-id="7b0a4-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-174">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="7b0a4-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b0a4-175">Response</span></span>

<span data-ttu-id="7b0a4-176">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-176">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="7b0a4-177">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-177">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Last Activity Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```

### <a name="json"></a><span data-ttu-id="7b0a4-178">JSON</span><span class="sxs-lookup"><span data-stu-id="7b0a4-178">JSON</span></span>

<span data-ttu-id="7b0a4-179">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-179">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="7b0a4-180">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b0a4-180">Request</span></span>

<span data-ttu-id="7b0a4-181">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-181">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="7b0a4-182">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b0a4-182">Response</span></span>

<span data-ttu-id="7b0a4-183">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-183">The following is an example of the response.</span></span>

> <span data-ttu-id="7b0a4-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b0a4-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.emailAppUsageUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 515

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.emailAppUsageUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userPrincipalName-value", 
      "displayName": "displayName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "lastActivityDate": "2017-09-01", 
      "mailForMac": [ ], 
      "outlookForMac": [ ], 
      "outlookForWindows": [ ], 
      "outlookForMobile": [
        "Undetermined"
      ], 
      "otherForMobile": [ ], 
      "outlookForWeb": [
        "Undetermined"
      ], 
      "pop3App": [ ], 
      "imap4App": [ ], 
      "smtpApp": [ ], 
      "reportPeriod": "7"
    }
  ]
}
```
