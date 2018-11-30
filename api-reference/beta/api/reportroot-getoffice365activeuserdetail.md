---
title: 'reportRoot: getOffice365ActiveUserDetail'
description: Obtiene información sobre los usuarios activos de Office 365.
ms.openlocfilehash: 340428bba0bbba8c333cde98e7ad38f28186e662
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084767"
---
# <a name="reportroot-getoffice365activeuserdetail"></a><span data-ttu-id="d0544-103">reportRoot: getOffice365ActiveUserDetail</span><span class="sxs-lookup"><span data-stu-id="d0544-103">reportRoot: getOffice365ActiveUserDetail</span></span>

> <span data-ttu-id="d0544-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0544-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0544-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0544-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0544-106">Obtiene información sobre los usuarios activos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0544-106">Get details about Office 365 active users.</span></span>

> <span data-ttu-id="d0544-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="d0544-107">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="d0544-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="d0544-108">Permissions</span></span>

<span data-ttu-id="d0544-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d0544-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="d0544-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0544-111">Permission type</span></span>                        | <span data-ttu-id="d0544-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0544-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="d0544-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0544-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="d0544-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="d0544-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="d0544-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0544-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d0544-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0544-116">Not supported.</span></span>                           |
| <span data-ttu-id="d0544-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0544-117">Application</span></span>                            | <span data-ttu-id="d0544-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="d0544-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="d0544-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0544-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActiveUserDetail(period='{period_value}')
GET /reports/getOffice365ActiveUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="d0544-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="d0544-120">Function parameters</span></span>

<span data-ttu-id="d0544-121">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="d0544-121">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="d0544-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d0544-122">Parameter</span></span> | <span data-ttu-id="d0544-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0544-123">Type</span></span>   | <span data-ttu-id="d0544-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0544-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="d0544-125">period</span><span class="sxs-lookup"><span data-stu-id="d0544-125">period</span></span>    | <span data-ttu-id="d0544-126">cadena</span><span class="sxs-lookup"><span data-stu-id="d0544-126">string</span></span> | <span data-ttu-id="d0544-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="d0544-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="d0544-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="d0544-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="d0544-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="d0544-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="d0544-130">date</span><span class="sxs-lookup"><span data-stu-id="d0544-130">date</span></span>      | <span data-ttu-id="d0544-131">Fecha</span><span class="sxs-lookup"><span data-stu-id="d0544-131">Date</span></span>   | <span data-ttu-id="d0544-132">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="d0544-132">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="d0544-133">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="d0544-133">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="d0544-134">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="d0544-134">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="d0544-135">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="d0544-135">**Note:** You need to set either period or date in the URL.</span></span>

<span data-ttu-id="d0544-136">Este método admite los [parámetros de consulta OData](/graph/query-parameters) `$format`, `$top` y `$skipToken` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0544-136">This method supports the `$format`, `$top`, and `$skipToken` [OData query parameters](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="d0544-137">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="d0544-137">The default output type is text/csv.</span></span> <span data-ttu-id="d0544-138">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="d0544-138">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d0544-139">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0544-139">Request headers</span></span>

| <span data-ttu-id="d0544-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="d0544-140">Name</span></span>          | <span data-ttu-id="d0544-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0544-141">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="d0544-142">Authorization</span><span class="sxs-lookup"><span data-stu-id="d0544-142">Authorization</span></span> | <span data-ttu-id="d0544-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d0544-p106">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="d0544-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0544-145">Response</span></span>

### <a name="csv"></a><span data-ttu-id="d0544-146">CSV</span><span class="sxs-lookup"><span data-stu-id="d0544-146">CSV</span></span>

<span data-ttu-id="d0544-147">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="d0544-147">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="d0544-148">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0544-148">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="d0544-149">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="d0544-149">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="d0544-150">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="d0544-150">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="d0544-151">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="d0544-151">Report Refresh Date</span></span>
- <span data-ttu-id="d0544-152">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="d0544-152">User Principal Name</span></span>
- <span data-ttu-id="d0544-153">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="d0544-153">Display Name</span></span>
- <span data-ttu-id="d0544-154">Eliminado</span><span class="sxs-lookup"><span data-stu-id="d0544-154">Is Deleted</span></span>
- <span data-ttu-id="d0544-155">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="d0544-155">Deleted Date</span></span>
- <span data-ttu-id="d0544-156">Tiene una licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0544-156">Has Exchange License</span></span>
- <span data-ttu-id="d0544-157">Tiene una licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="d0544-157">Has OneDrive License</span></span>
- <span data-ttu-id="d0544-158">Tiene de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="d0544-158">Has SharePoint License</span></span>
- <span data-ttu-id="d0544-159">Tiene una licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="d0544-159">Has Skype For Business License</span></span>
- <span data-ttu-id="d0544-160">Tiene una licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-160">Has Yammer License</span></span>
- <span data-ttu-id="d0544-161">Tiene una licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-161">Has Teams License</span></span>
- <span data-ttu-id="d0544-162">Fecha de la última actividad de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0544-162">Exchange Last Activity Date</span></span>
- <span data-ttu-id="d0544-163">Fecha de la última actividad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="d0544-163">OneDrive Last Activity Date</span></span>
- <span data-ttu-id="d0544-164">Fecha de la última actividad de SharePoint</span><span class="sxs-lookup"><span data-stu-id="d0544-164">SharePoint Last Activity Date</span></span>
- <span data-ttu-id="d0544-165">Fecha de la última actividad de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="d0544-165">Skype For Business Last Activity Date</span></span>
- <span data-ttu-id="d0544-166">Fecha de la última actividad de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-166">Yammer Last Activity Date</span></span>
- <span data-ttu-id="d0544-167">Fecha de la última actividad de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-167">Teams Last Activity Date</span></span>
- <span data-ttu-id="d0544-168">Fecha de asignación de licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="d0544-168">Exchange License Assign Date</span></span>
- <span data-ttu-id="d0544-169">Fecha de asignación de licencia de licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="d0544-169">OneDrive License Assign Date</span></span>
- <span data-ttu-id="d0544-170">Fecha de asignación de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="d0544-170">SharePoint License Assign Date</span></span>
- <span data-ttu-id="d0544-171">Fecha de asignación de licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="d0544-171">Skype For Business License Assign Date</span></span>
- <span data-ttu-id="d0544-172">Fecha de asignación de licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-172">Yammer License Assign Date</span></span>
- <span data-ttu-id="d0544-173">Fecha de asignación de licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-173">Teams License Assign Date</span></span>
- <span data-ttu-id="d0544-174">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="d0544-174">Assigned Products</span></span>

<span data-ttu-id="d0544-175">No se admiten las siguientes columnas en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="d0544-175">The following columns are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="d0544-176">Tiene una licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-176">Has Yammer License</span></span>
- <span data-ttu-id="d0544-177">Tiene una licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-177">Has Teams License</span></span>
- <span data-ttu-id="d0544-178">Fecha de la última actividad de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-178">Yammer Last Activity Date</span></span>
- <span data-ttu-id="d0544-179">Fecha de la última actividad de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-179">Teams Last Activity Date</span></span>
- <span data-ttu-id="d0544-180">Fecha de asignación de licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="d0544-180">Yammer License Assign Date</span></span>
- <span data-ttu-id="d0544-181">Fecha de asignación de licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="d0544-181">Teams License Assign Date</span></span>

### <a name="json"></a><span data-ttu-id="d0544-182">JSON</span><span class="sxs-lookup"><span data-stu-id="d0544-182">JSON</span></span>

<span data-ttu-id="d0544-183">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ActiveUserDetail](../resources/office365activeuserdetail.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0544-183">If successful, this method returns a `200 OK` response code and an **[office365ActiveUserDetail](../resources/office365activeuserdetail.md)** object in the response body.</span></span>

<span data-ttu-id="d0544-184">No se admiten las siguientes propiedades en el objeto **[office365ActiveUserDetail](../resources/office365activeuserdetail.md)** en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="d0544-184">The following properties in **[office365ActiveUserDetail](../resources/office365activeuserdetail.md)** object are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="d0544-185">hasYammerLicense</span><span class="sxs-lookup"><span data-stu-id="d0544-185">hasYammerLicense</span></span>
- <span data-ttu-id="d0544-186">hasTeamsLicense</span><span class="sxs-lookup"><span data-stu-id="d0544-186">hasTeamsLicense</span></span>
- <span data-ttu-id="d0544-187">yammerLastActivityDate</span><span class="sxs-lookup"><span data-stu-id="d0544-187">yammerLastActivityDate</span></span>
- <span data-ttu-id="d0544-188">teamsLastActivityDate</span><span class="sxs-lookup"><span data-stu-id="d0544-188">teamsLastActivityDate</span></span>
- <span data-ttu-id="d0544-189">yammerLicenseAssignDate</span><span class="sxs-lookup"><span data-stu-id="d0544-189">yammerLicenseAssignDate</span></span>
- <span data-ttu-id="d0544-190">teamsLicenseAssignDate</span><span class="sxs-lookup"><span data-stu-id="d0544-190">teamsLicenseAssignDate</span></span>

<span data-ttu-id="d0544-191">El tamaño de página predeterminado para esta solicitud es 200 artículos.</span><span class="sxs-lookup"><span data-stu-id="d0544-191">The default page size for this request is 200 items.</span></span>

## <a name="example"></a><span data-ttu-id="d0544-192">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0544-192">Example</span></span>

### <a name="csv"></a><span data-ttu-id="d0544-193">CSV</span><span class="sxs-lookup"><span data-stu-id="d0544-193">CSV</span></span>

<span data-ttu-id="d0544-194">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="d0544-194">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="d0544-195">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0544-195">Request</span></span>

<span data-ttu-id="d0544-196">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0544-196">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activeuserdetail_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActiveUserDetail(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="d0544-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0544-197">Response</span></span>

<span data-ttu-id="d0544-198">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0544-198">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="d0544-199">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="d0544-199">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Has Exchange License,Has OneDrive License,Has SharePoint License,Has Skype For Business License,Has Yammer License,Has Teams License,Exchange Last Activity Date,OneDrive Last Activity Date,SharePoint Last Activity Date,Skype For Business Last Activity Date,Yammer Last Activity Date,Teams Last Activity Date,Exchange License Assign Date,OneDrive License Assign Date,SharePoint License Assign Date,Skype For Business License Assign Date,Yammer License Assign Date,Teams License Assign Date,Assigned Products
```

### <a name="json"></a><span data-ttu-id="d0544-200">JSON</span><span class="sxs-lookup"><span data-stu-id="d0544-200">JSON</span></span>

<span data-ttu-id="d0544-201">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="d0544-201">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="d0544-202">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0544-202">Request</span></span>

<span data-ttu-id="d0544-203">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0544-203">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activeuserdetail_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActiveUserDetail(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="d0544-204">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0544-204">Response</span></span>

<span data-ttu-id="d0544-205">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0544-205">The following is an example of the response.</span></span>

> <span data-ttu-id="d0544-p108">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0544-p108">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActiveUserDetail"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 853

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActiveUserDetail)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "userPrincipalName": "userprincipalname-value", 
      "displayName": "displayname-value", 
      "isDeleted": false, 
      "deletedDate": null, 
      "hasExchangeLicense": true, 
      "hasOneDriveLicense": false, 
      "hasSharePointLicense": false, 
      "hasSkypeForBusinessLicense": false, 
      "hasYammerLicense": false, 
      "hasTeamsLicense": false, 
      "exchangeLastActivityDate": "2017-08-30", 
      "oneDriveLastActivityDate": null, 
      "sharePointLastActivityDate": null, 
      "skypeForBusinessLastActivityDate": null, 
      "yammerLastActivityDate": null, 
      "teamsLastActivityDate": null, 
      "exchangeLicenseAssignDate": "2016-05-03", 
      "oneDriveLicenseAssignDate": null, 
      "sharePointLicenseAssignDate": null, 
      "skypeForBusinessLicenseAssignDate": null, 
      "yammerLicenseAssignDate": null, 
      "teamsLicenseAssignDate": null, 
      "assignedProducts": [
        "OFFICE 365 ENTERPRISE E5"
      ]
    }
  ]
}
```
