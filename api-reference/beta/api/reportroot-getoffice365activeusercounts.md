---
title: 'reportRoot: getOffice365ActiveUserCounts'
description: Obtiene el número de usuarios activos diarios en el período de informe por producto.
ms.openlocfilehash: 29cb7a18520774b192d5e9e71b62a7ca86fa9be5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085698"
---
# <a name="reportroot-getoffice365activeusercounts"></a><span data-ttu-id="e4b9a-103">reportRoot: getOffice365ActiveUserCounts</span><span class="sxs-lookup"><span data-stu-id="e4b9a-103">reportRoot: getOffice365ActiveUserCounts</span></span>

> <span data-ttu-id="e4b9a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e4b9a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e4b9a-106">Obtiene el número de usuarios activos diarios en el período de informe por producto.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-106">Get the count of daily active users in the reporting period by product.</span></span>

> <span data-ttu-id="e4b9a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="e4b9a-107">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="e4b9a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4b9a-108">Permissions</span></span>

<span data-ttu-id="e4b9a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4b9a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e4b9a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4b9a-111">Permission type</span></span>                        | <span data-ttu-id="e4b9a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4b9a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="e4b9a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4b9a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="e4b9a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e4b9a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="e4b9a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4b9a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4b9a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-116">Not supported.</span></span>                           |
| <span data-ttu-id="e4b9a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4b9a-117">Application</span></span>                            | <span data-ttu-id="e4b9a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="e4b9a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="e4b9a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4b9a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActiveUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="e4b9a-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e4b9a-120">Function parameters</span></span>

<span data-ttu-id="e4b9a-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="e4b9a-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e4b9a-122">Parameter</span></span> | <span data-ttu-id="e4b9a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4b9a-123">Type</span></span>   | <span data-ttu-id="e4b9a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4b9a-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="e4b9a-125">period</span><span class="sxs-lookup"><span data-stu-id="e4b9a-125">period</span></span>    | <span data-ttu-id="e4b9a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="e4b9a-126">string</span></span> | <span data-ttu-id="e4b9a-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="e4b9a-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="e4b9a-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="e4b9a-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-130">Required.</span></span> |

<span data-ttu-id="e4b9a-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="e4b9a-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-132">The default output type is text/csv.</span></span> <span data-ttu-id="e4b9a-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="e4b9a-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b9a-134">Request headers</span></span>

| <span data-ttu-id="e4b9a-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4b9a-135">Name</span></span>          | <span data-ttu-id="e4b9a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4b9a-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="e4b9a-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="e4b9a-137">Authorization</span></span> | <span data-ttu-id="e4b9a-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="e4b9a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4b9a-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="e4b9a-141">CSV</span><span class="sxs-lookup"><span data-stu-id="e4b9a-141">CSV</span></span>

<span data-ttu-id="e4b9a-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="e4b9a-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="e4b9a-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="e4b9a-145">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="e4b9a-145">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="e4b9a-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="e4b9a-146">Report Refresh Date</span></span>
- <span data-ttu-id="e4b9a-147">Office 365</span><span class="sxs-lookup"><span data-stu-id="e4b9a-147">Office 365</span></span>
- <span data-ttu-id="e4b9a-148">Exchange</span><span class="sxs-lookup"><span data-stu-id="e4b9a-148">Exchange</span></span>
- <span data-ttu-id="e4b9a-149">OneDrive</span><span class="sxs-lookup"><span data-stu-id="e4b9a-149">OneDrive</span></span>
- <span data-ttu-id="e4b9a-150">SharePoint</span><span class="sxs-lookup"><span data-stu-id="e4b9a-150">SharePoint</span></span>
- <span data-ttu-id="e4b9a-151">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="e4b9a-151">Skype For Business</span></span> 
- <span data-ttu-id="e4b9a-152">Yammer</span><span class="sxs-lookup"><span data-stu-id="e4b9a-152">Yammer</span></span>
- <span data-ttu-id="e4b9a-153">Teams</span><span class="sxs-lookup"><span data-stu-id="e4b9a-153">Teams</span></span>
- <span data-ttu-id="e4b9a-154">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="e4b9a-154">Report Date</span></span>
- <span data-ttu-id="e4b9a-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="e4b9a-155">Report Period</span></span>

<span data-ttu-id="e4b9a-156">No se admiten las siguientes columnas en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="e4b9a-156">The following columns are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="e4b9a-157">Yammer</span><span class="sxs-lookup"><span data-stu-id="e4b9a-157">Yammer</span></span>
- <span data-ttu-id="e4b9a-158">Teams</span><span class="sxs-lookup"><span data-stu-id="e4b9a-158">Teams</span></span>

### <a name="json"></a><span data-ttu-id="e4b9a-159">JSON</span><span class="sxs-lookup"><span data-stu-id="e4b9a-159">JSON</span></span>

<span data-ttu-id="e4b9a-160">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ActiveUserCounts](../resources/office365activeusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-160">If successful, this method returns a `200 OK` response code and an **[office365ActiveUserCounts](../resources/office365activeusercounts.md)** object in the response body.</span></span>

<span data-ttu-id="e4b9a-161">No se admiten las siguientes propiedades en el objeto **[office365ActiveUserCounts](../resources/office365activeusercounts.md)** en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="e4b9a-161">The following properties in **[office365ActiveUserCounts](../resources/office365activeusercounts.md)** object are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="e4b9a-162">yammer</span><span class="sxs-lookup"><span data-stu-id="e4b9a-162">yammer</span></span>
- <span data-ttu-id="e4b9a-163">equipos</span><span class="sxs-lookup"><span data-stu-id="e4b9a-163">teams</span></span>

## <a name="example"></a><span data-ttu-id="e4b9a-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4b9a-164">Example</span></span>

### <a name="csv"></a><span data-ttu-id="e4b9a-165">CSV</span><span class="sxs-lookup"><span data-stu-id="e4b9a-165">CSV</span></span>

<span data-ttu-id="e4b9a-166">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-166">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="e4b9a-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b9a-167">Request</span></span>

<span data-ttu-id="e4b9a-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-168">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activeusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActiveUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="e4b9a-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4b9a-169">Response</span></span>

<span data-ttu-id="e4b9a-170">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-170">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="e4b9a-171">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-171">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Office 365,Exchange,OneDrive,SharePoint,Skype For Business,Yammer,Teams,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="e4b9a-172">JSON</span><span class="sxs-lookup"><span data-stu-id="e4b9a-172">JSON</span></span>

<span data-ttu-id="e4b9a-173">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-173">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="e4b9a-174">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4b9a-174">Request</span></span>

<span data-ttu-id="e4b9a-175">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-175">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365activeusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ActiveUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="e4b9a-176">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4b9a-176">Response</span></span>

<span data-ttu-id="e4b9a-177">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-177">The following is an example of the response.</span></span>

> <span data-ttu-id="e4b9a-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4b9a-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ActiveUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 317

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ActiveUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "office365": 1718, 
      "exchange": 1429, 
      "oneDrive": 350, 
      "sharePoint": 795, 
      "skypeForBusiness": 251, 
      "yammer": 47, 
      "teams": 10, 
      "reportDate": "2017-08-29", 
      "reportPeriod": "7"
    }
  ]
}
```