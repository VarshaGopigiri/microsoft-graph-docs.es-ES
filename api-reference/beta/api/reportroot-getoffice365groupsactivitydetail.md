---
title: 'reportRoot: getOffice365GroupsActivityDetail'
description: Obtiene información sobre la actividad de Grupos de Office 365 por grupo.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: c70f8ccdb2d27c96a652c0db4d16ee0ca70ec132
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983593"
---
# <a name="reportroot-getoffice365groupsactivitydetail"></a><span data-ttu-id="7c323-103">reportRoot: getOffice365GroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="7c323-103">reportRoot: getOffice365GroupsActivityDetail</span></span>

> <span data-ttu-id="7c323-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c323-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c323-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c323-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c323-106">Obtiene información sobre la actividad de Grupos de Office 365 por grupo.</span><span class="sxs-lookup"><span data-stu-id="7c323-106">Get details about Office 365 Groups activity by group.</span></span>

> <span data-ttu-id="7c323-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="7c323-107">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="7c323-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7c323-108">Permissions</span></span>

<span data-ttu-id="7c323-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7c323-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7c323-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7c323-111">Permission type</span></span>                        | <span data-ttu-id="7c323-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7c323-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7c323-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7c323-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="7c323-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7c323-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7c323-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7c323-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7c323-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7c323-116">Not supported.</span></span>                           |
| <span data-ttu-id="7c323-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7c323-117">Application</span></span>                            | <span data-ttu-id="7c323-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7c323-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7c323-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7c323-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityDetail(period='{period_value}')
GET /reports/getOffice365GroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="7c323-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="7c323-120">Function parameters</span></span>

<span data-ttu-id="7c323-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7c323-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="7c323-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7c323-122">Parameter</span></span> | <span data-ttu-id="7c323-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c323-123">Type</span></span>   | <span data-ttu-id="7c323-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c323-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7c323-125">period</span><span class="sxs-lookup"><span data-stu-id="7c323-125">period</span></span>    | <span data-ttu-id="7c323-126">cadena</span><span class="sxs-lookup"><span data-stu-id="7c323-126">string</span></span> | <span data-ttu-id="7c323-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7c323-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7c323-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7c323-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7c323-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7c323-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="7c323-130">date</span><span class="sxs-lookup"><span data-stu-id="7c323-130">date</span></span>      | <span data-ttu-id="7c323-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="7c323-131">Date</span></span>   | <span data-ttu-id="7c323-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="7c323-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="7c323-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="7c323-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="7c323-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="7c323-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="7c323-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="7c323-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="7c323-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c323-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="7c323-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="7c323-137">The default output type is text/csv.</span></span> <span data-ttu-id="7c323-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="7c323-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7c323-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7c323-139">Request headers</span></span>

| <span data-ttu-id="7c323-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c323-140">Name</span></span>          | <span data-ttu-id="7c323-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c323-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="7c323-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="7c323-142">Authorization</span></span> | <span data-ttu-id="7c323-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7c323-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="7c323-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c323-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="7c323-146">CSV</span><span class="sxs-lookup"><span data-stu-id="7c323-146">CSV</span></span>

<span data-ttu-id="7c323-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7c323-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7c323-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c323-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7c323-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7c323-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7c323-150">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7c323-150">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7c323-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7c323-151">Report Refresh Date</span></span>
- <span data-ttu-id="7c323-152">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="7c323-152">Group Display Name</span></span>
- <span data-ttu-id="7c323-153">Eliminado</span><span class="sxs-lookup"><span data-stu-id="7c323-153">Is Deleted</span></span>
- <span data-ttu-id="7c323-154">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="7c323-154">Owner Principal Name</span></span>
- <span data-ttu-id="7c323-155">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="7c323-155">Last Activity Date</span></span>
- <span data-ttu-id="7c323-156">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="7c323-156">Group Type</span></span>
- <span data-ttu-id="7c323-157">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="7c323-157">Member Count</span></span>
- <span data-ttu-id="7c323-158">Número de miembros externos</span><span class="sxs-lookup"><span data-stu-id="7c323-158">External Member Count</span></span>
- <span data-ttu-id="7c323-159">Número de correos electrónicos recibidos de Exchange</span><span class="sxs-lookup"><span data-stu-id="7c323-159">Exchange Received Email Count</span></span>
- <span data-ttu-id="7c323-160">Número de archivos activos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="7c323-160">SharePoint Active File Count</span></span>
- <span data-ttu-id="7c323-161">Número de mensajes publicados en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-161">Yammer Posted Message Count</span></span>
- <span data-ttu-id="7c323-162">Número de mensajes leídos en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-162">Yammer Read Message Count</span></span>
- <span data-ttu-id="7c323-163">Número de mensajes etiquetados como “Me gusta” en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-163">Yammer Liked Message Count</span></span>
- <span data-ttu-id="7c323-164">Número total de elementos de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="7c323-164">Exchange Mailbox Total Item Count</span></span>
- <span data-ttu-id="7c323-165">Almacenamiento usado de buzones de Exchange (bytes)</span><span class="sxs-lookup"><span data-stu-id="7c323-165">Exchange Mailbox Storage Used (Byte)</span></span>
- <span data-ttu-id="7c323-166">Número total de archivos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="7c323-166">SharePoint Total File Count</span></span>
- <span data-ttu-id="7c323-167">Almacenamiento usado de sitios de SharePoint (bytes)</span><span class="sxs-lookup"><span data-stu-id="7c323-167">SharePoint Site Storage Used (Byte)</span></span>
- <span data-ttu-id="7c323-168">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7c323-168">Report Period</span></span>

<span data-ttu-id="7c323-169">No se admiten las siguientes columnas en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="7c323-169">The following columns are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="7c323-170">Número de mensajes publicados en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-170">Yammer Posted Message Count</span></span>
- <span data-ttu-id="7c323-171">Número de mensajes leídos en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-171">Yammer Read Message Count</span></span>
- <span data-ttu-id="7c323-172">Número de mensajes etiquetados como “Me gusta” en Yammer</span><span class="sxs-lookup"><span data-stu-id="7c323-172">Yammer Liked Message Count</span></span>

### <a name="json"></a><span data-ttu-id="7c323-173">JSON</span><span class="sxs-lookup"><span data-stu-id="7c323-173">JSON</span></span>

<span data-ttu-id="7c323-174">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c323-174">If successful, this method returns a `200 OK` response code and an **[office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md)** object in the response body.</span></span>

<span data-ttu-id="7c323-175">No se admiten las siguientes propiedades en el objeto **[office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md)** en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="7c323-175">The following properties in **[office365GroupsActivityDetail](../resources/office365groupsactivitydetail.md)** object are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="7c323-176">yammerPostedMessageCount</span><span class="sxs-lookup"><span data-stu-id="7c323-176">yammerPostedMessageCount</span></span>
- <span data-ttu-id="7c323-177">yammerReadMessageCount</span><span class="sxs-lookup"><span data-stu-id="7c323-177">yammerReadMessageCount</span></span>
- <span data-ttu-id="7c323-178">yammerLikedMessageCount</span><span class="sxs-lookup"><span data-stu-id="7c323-178">yammerLikedMessageCount</span></span>

<span data-ttu-id="7c323-179">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="7c323-179">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="7c323-180">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c323-180">Example</span></span>

### <a name="csv"></a><span data-ttu-id="7c323-181">CSV</span><span class="sxs-lookup"><span data-stu-id="7c323-181">CSV</span></span>

<span data-ttu-id="7c323-182">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="7c323-182">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="7c323-183">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c323-183">Request</span></span>

<span data-ttu-id="7c323-184">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c323-184">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365groupsactivitydetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365GroupsActivityDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="7c323-185">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c323-185">Response</span></span>

<span data-ttu-id="7c323-186">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c323-186">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="7c323-187">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c323-187">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Member Count,External Member Count,Exchange Received Email Count,SharePoint Active File Count,Yammer Posted Message Count,Yammer Read Message Count,Yammer Liked Message Count,Exchange Mailbox Total Item Count,Exchange Mailbox Storage Used (Byte),SharePoint Total File Count,SharePoint Site Storage Used (Byte),Report Period
```

### <a name="json"></a><span data-ttu-id="7c323-188">JSON</span><span class="sxs-lookup"><span data-stu-id="7c323-188">JSON</span></span>

<span data-ttu-id="7c323-189">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="7c323-189">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="7c323-190">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7c323-190">Request</span></span>

<span data-ttu-id="7c323-191">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7c323-191">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365groupsactivitydetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365GroupsActivityDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="7c323-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7c323-192">Response</span></span>

<span data-ttu-id="7c323-193">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7c323-193">The following is an example of the response.</span></span>

> <span data-ttu-id="7c323-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7c323-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365GroupsActivityDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 674

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365GroupsActivityDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "groupDisplayName": "groupDisplayName-value", 
      "isDeleted": false, 
      "ownerPrincipalName": "ownerDisplayName-value", 
      "lastActivityDate": "2017-08-31", 
      "groupType": "Private", 
      "memberCount": 5, 
      "externalMemberCount": 0, 
      "exchangeReceivedEmailCount": 341, 
      "sharePointActiveFileCount": 0, 
      "yammerPostedMessageCount": 0, 
      "yammerReadMessageCount": 0, 
      "yammerLikedMessageCount": 0, 
      "exchangeMailboxTotalItemCount": 343, 
      "exchangeMailboxStorageUsedInBytes": 3724609, 
      "sharePointTotalFileCount": 0, 
      "sharePointSiteStorageUsedInBytes": 0, 
      "reportPeriod": "30"
    }
  ]
}
```
