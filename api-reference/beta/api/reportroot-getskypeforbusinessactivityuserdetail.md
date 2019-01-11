---
title: 'reportRoot: getSkypeForBusinessActivityUserDetail'
description: Obtiene información sobre la actividad de Skype Empresarial por usuario.
localization_priority: Normal
ms.openlocfilehash: 43bf2d7f08bc9a0033bd04f98687c7d03be5f2ea
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27872635"
---
# <a name="reportroot-getskypeforbusinessactivityuserdetail"></a><span data-ttu-id="f469e-103">reportRoot: getSkypeForBusinessActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="f469e-103">reportRoot: getSkypeForBusinessActivityUserDetail</span></span>

> <span data-ttu-id="f469e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f469e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f469e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f469e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f469e-106">Obtiene información sobre la actividad de Skype Empresarial por usuario.</span><span class="sxs-lookup"><span data-stu-id="f469e-106">Get details about Skype for Business activity by user.</span></span>

> <span data-ttu-id="f469e-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="f469e-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="f469e-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="f469e-108">Permissions</span></span>

<span data-ttu-id="f469e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f469e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="f469e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f469e-111">Permission type</span></span>                        | <span data-ttu-id="f469e-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f469e-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f469e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f469e-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="f469e-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f469e-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="f469e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f469e-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f469e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f469e-116">Not supported.</span></span>                           |
| <span data-ttu-id="f469e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f469e-117">Application</span></span>                            | <span data-ttu-id="f469e-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f469e-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f469e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f469e-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserDetail(period='{period_value}')
GET /reports/getSkypeForBusinessActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="f469e-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="f469e-120">Function parameters</span></span>

<span data-ttu-id="f469e-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="f469e-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="f469e-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f469e-122">Parameter</span></span> | <span data-ttu-id="f469e-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="f469e-123">Type</span></span>   | <span data-ttu-id="f469e-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f469e-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f469e-125">period</span><span class="sxs-lookup"><span data-stu-id="f469e-125">period</span></span>    | <span data-ttu-id="f469e-126">cadena</span><span class="sxs-lookup"><span data-stu-id="f469e-126">string</span></span> | <span data-ttu-id="f469e-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f469e-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f469e-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="f469e-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f469e-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f469e-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="f469e-130">date</span><span class="sxs-lookup"><span data-stu-id="f469e-130">date</span></span>      | <span data-ttu-id="f469e-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="f469e-131">Date</span></span>   | <span data-ttu-id="f469e-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="f469e-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="f469e-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="f469e-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="f469e-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="f469e-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="f469e-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="f469e-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="f469e-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f469e-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="f469e-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="f469e-137">The default output type is text/csv.</span></span> <span data-ttu-id="f469e-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="f469e-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="f469e-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f469e-139">Request headers</span></span>

| <span data-ttu-id="f469e-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="f469e-140">Name</span></span>          | <span data-ttu-id="f469e-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="f469e-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="f469e-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="f469e-142">Authorization</span></span> | <span data-ttu-id="f469e-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f469e-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="f469e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f469e-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="f469e-146">CSV</span><span class="sxs-lookup"><span data-stu-id="f469e-146">CSV</span></span>

<span data-ttu-id="f469e-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="f469e-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f469e-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f469e-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f469e-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="f469e-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f469e-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="f469e-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f469e-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="f469e-151">Report Refresh Date</span></span>
- <span data-ttu-id="f469e-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="f469e-152">User Principal Name</span></span>
- <span data-ttu-id="f469e-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="f469e-153">Is Deleted</span></span>
- <span data-ttu-id="f469e-154">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="f469e-154">Deleted Date</span></span>
- <span data-ttu-id="f469e-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="f469e-155">Last Activity Date</span></span>
- <span data-ttu-id="f469e-156">Número total de sesiones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-156">Total Peer-to-peer Session Count</span></span>
- <span data-ttu-id="f469e-157">Número total de conferencias organizadas</span><span class="sxs-lookup"><span data-stu-id="f469e-157">Total Organized Conference Count</span></span>
- <span data-ttu-id="f469e-158">Número total de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-158">Total Participated Conference Count</span></span>
- <span data-ttu-id="f469e-159">Fecha de la última actividad de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-159">Peer-to-peer Last Activity Date</span></span>
- <span data-ttu-id="f469e-160">Fecha de la última actividad de una conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-160">Organized Conference Last Activity Date</span></span>
- <span data-ttu-id="f469e-161">Fecha de la última actividad de una conferencia en la que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-161">Participated Conference Last Activity Date</span></span>
- <span data-ttu-id="f469e-162">Números de mensajes instantáneos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-162">Peer-to-peer IM Count</span></span>
- <span data-ttu-id="f469e-163">Número de sesiones de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-163">Peer-to-peer Audio Count</span></span>
- <span data-ttu-id="f469e-164">Minutos de audio de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-164">Peer-to-peer Audio Minutes</span></span>
- <span data-ttu-id="f469e-165">Número de sesiones de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-165">Peer-to-peer Video Count</span></span>
- <span data-ttu-id="f469e-166">Minutos de vídeo de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-166">Peer-to-peer Video Minutes</span></span>
- <span data-ttu-id="f469e-167">Número de sesiones de uso compartido de aplicaciones de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-167">Peer-to-peer App Sharing Count</span></span>
- <span data-ttu-id="f469e-168">Número de transferencias de archivos de punto a punto</span><span class="sxs-lookup"><span data-stu-id="f469e-168">Peer-to-peer File Transfer Count</span></span>
- <span data-ttu-id="f469e-169">Número de mensajes instantáneos de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-169">Organized Conference IM Count</span></span>
- <span data-ttu-id="f469e-170">Número de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-170">Organized Conference Audio/Video Count</span></span>
- <span data-ttu-id="f469e-171">Minutos de sesiones de audio o vídeo de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-171">Organized Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="f469e-172">Número de sesiones de uso compartido de aplicaciones se conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-172">Organized Conference App Sharing Count</span></span>
- <span data-ttu-id="f469e-173">Número de sesiones web de conferencia organizada</span><span class="sxs-lookup"><span data-stu-id="f469e-173">Organized Conference Web Count</span></span>
- <span data-ttu-id="f469e-174">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por terceros</span><span class="sxs-lookup"><span data-stu-id="f469e-174">Organized Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="f469e-175">Número de conferencias de acceso telefónico local o aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="f469e-175">Organized Conference Dial-in/out Microsoft Count</span></span>
- <span data-ttu-id="f469e-176">Minutos de conferencias de acceso telefónico local organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="f469e-176">Organized Conference Dial-in Microsoft Minutes</span></span>
- <span data-ttu-id="f469e-177">Minutos de conferencias por aceptación de llamada organizadas por Microsoft</span><span class="sxs-lookup"><span data-stu-id="f469e-177">Organized Conference Dial-out Microsoft Minutes</span></span>
- <span data-ttu-id="f469e-178">Recuento de mensajería instantánea de conferencias participó</span><span class="sxs-lookup"><span data-stu-id="f469e-178">Participated Conference IM Count</span></span>
- <span data-ttu-id="f469e-179">Número de sesiones de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-179">Participated Conference Audio/Video Count</span></span>
- <span data-ttu-id="f469e-180">Minutos de audio o vídeo de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-180">Participated Conference Audio/Video Minutes</span></span>
- <span data-ttu-id="f469e-181">Número de sesiones de uso compartido de aplicaciones de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-181">Participated Conference App Sharing Count</span></span>
- <span data-ttu-id="f469e-182">Número de sesiones web de conferencias en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-182">Participated Conference Web Count</span></span>
- <span data-ttu-id="f469e-183">Número de conferencias de acceso telefónico local o aceptación de llamada de terceros en las que participó</span><span class="sxs-lookup"><span data-stu-id="f469e-183">Participated Conference Dial-in/out 3rd Party Count</span></span>
- <span data-ttu-id="f469e-184">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="f469e-184">Assigned Products</span></span>
- <span data-ttu-id="f469e-185">Período del informe</span><span class="sxs-lookup"><span data-stu-id="f469e-185">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="f469e-186">JSON</span><span class="sxs-lookup"><span data-stu-id="f469e-186">JSON</span></span>

<span data-ttu-id="f469e-187">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessActivityUserDetail](../resources/skypeforbusinessactivityuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f469e-187">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessActivityUserDetail](../resources/skypeforbusinessactivityuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="f469e-188">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="f469e-188">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="f469e-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f469e-189">Example</span></span>

### <a name="csv"></a><span data-ttu-id="f469e-190">CSV</span><span class="sxs-lookup"><span data-stu-id="f469e-190">CSV</span></span>

<span data-ttu-id="f469e-191">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="f469e-191">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="f469e-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f469e-192">Request</span></span>

<span data-ttu-id="f469e-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f469e-193">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessactivityuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessActivityUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="f469e-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f469e-194">Response</span></span>

<span data-ttu-id="f469e-195">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f469e-195">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="f469e-196">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="f469e-196">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Total Peer-to-peer Session Count,Total Organized Conference Count,Total Participated Conference Count,Peer-to-peer Last Activity Date,Organized Conference Last Activity Date,Participated Conference Last Activity Date,Peer-to-peer IM Count,Peer-to-peer Audio Count,Peer-to-peer Audio Minutes,Peer-to-peer Video Count,Peer-to-peer Video Minutes,Peer-to-peer App Sharing Count,Peer-to-peer File Transfer Count,Organized Conference IM Count,Organized Conference Audio/Video Count,Organized Conference Audio/Video Minutes,Organized Conference App Sharing Count,Organized Conference Web Count,Organized Conference Dial-in/out 3rd Party Count,Organized Conference Dial-in/out Microsoft Count,Organized Conference Dial-in Microsoft Minutes,Organized Conference Dial-out Microsoft Minutes,Participated Conference IM Count,Participated Conference Audio/Video Count,Participated Conference Audio/Video Minutes,Participated Conference App Sharing Count,Participated Conference Web Count,Participated Conference Dial-in/out 3rd Party Count,Assigned Products,Report Period
```

### <a name="json"></a><span data-ttu-id="f469e-197">JSON</span><span class="sxs-lookup"><span data-stu-id="f469e-197">JSON</span></span>

<span data-ttu-id="f469e-198">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="f469e-198">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="f469e-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f469e-199">Request</span></span>

<span data-ttu-id="f469e-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f469e-200">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessactivityuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessActivityUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="f469e-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f469e-201">Response</span></span>

<span data-ttu-id="f469e-202">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f469e-202">The following is an example of the response.</span></span>

> <span data-ttu-id="f469e-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f469e-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessActivityUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1419

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessActivityUserDetail)", 
  "value": [
    {
      "totalPeerToPeerSessionCount": 12, 
      "totalOrganizedConferenceCount": 0, 
      "totalParticipatedConferenceCount": 1, 
      "peerToPeerLastActivityDate": "2017-09-01", 
      "organizedConferenceLastActivityDate": null, 
      "participatedConferenceLastActivityDate": "2017-08-31", 
      "peerToPeerIMCount": 12, 
      "peerToPeerAudioCount": 0, 
      "peerToPeerAudioMinutes": 0, 
      "peerToPeerVideoCount": 0, 
      "peerToPeerVideoMinutes": 0, 
      "peerToPeerAppSharingCount": 0, 
      "peerToPeerFileTransferCount": 0, 
      "organizedConferenceIMCount": 0, 
      "organizedConferenceAudioVideoCount": 0, 
      "organizedConferenceAudioVideoMinutes": 0, 
      "organizedConferenceAppSharingCount": 0, 
      "organizedConferenceWebCount": 0, 
      "organizedConferenceDialInOut3rdPartyCount": 0, 
      "organizedConferenceCloudDialInOutMicrosoftCount": 0, 
      "organizedConferenceCloudDialInMicrosoftMinutes": 0, 
      "organizedConferenceCloudDialOutMicrosoftMinutes": 0, 
      "participatedConferenceIMCount": 0, 
      "participatedConferenceAudioVideoCount": 1, 
      "participatedConferenceAudioVideoMinutes": 69, 
      "participatedConferenceAppSharingCount": 0, 
      "participatedConferenceWebCount": 0, 
      "participatedConferenceDialInOut3rdPartyCount": 0, 
      "reportRefreshDate": "2017-09-06", 
      "userPrincipalName": "userPrincipalName-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "lastActivityDate": "2017-09-01", 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5", 
      ], 
      "reportPeriod": "7"
    }
  ]
}
```
