---
title: 'reportRoot: getOffice365ServicesUserCounts'
description: Obtiene el número de usuarios por tipo de actividad y servicio.
localization_priority: Normal
ms.openlocfilehash: dd196e971a55acd3c3beebe8d8e526f443fbe62b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827583"
---
# <a name="reportroot-getoffice365servicesusercounts"></a><span data-ttu-id="614d0-103">reportRoot: getOffice365ServicesUserCounts</span><span class="sxs-lookup"><span data-stu-id="614d0-103">reportRoot: getOffice365ServicesUserCounts</span></span>

> <span data-ttu-id="614d0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="614d0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="614d0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="614d0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="614d0-106">Obtiene el número de usuarios por tipo de actividad y servicio.</span><span class="sxs-lookup"><span data-stu-id="614d0-106">Get the count of users by activity type and service.</span></span>

> <span data-ttu-id="614d0-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="614d0-107">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="614d0-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="614d0-108">Permissions</span></span>

<span data-ttu-id="614d0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="614d0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="614d0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="614d0-111">Permission type</span></span>                        | <span data-ttu-id="614d0-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="614d0-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="614d0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="614d0-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="614d0-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="614d0-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="614d0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="614d0-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="614d0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="614d0-116">Not supported.</span></span>                           |
| <span data-ttu-id="614d0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="614d0-117">Application</span></span>                            | <span data-ttu-id="614d0-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="614d0-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="614d0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="614d0-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ServicesUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="614d0-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="614d0-120">Function parameters</span></span>

<span data-ttu-id="614d0-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="614d0-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="614d0-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="614d0-122">Parameter</span></span> | <span data-ttu-id="614d0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="614d0-123">Type</span></span>   | <span data-ttu-id="614d0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="614d0-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="614d0-125">period</span><span class="sxs-lookup"><span data-stu-id="614d0-125">period</span></span>    | <span data-ttu-id="614d0-126">cadena</span><span class="sxs-lookup"><span data-stu-id="614d0-126">string</span></span> | <span data-ttu-id="614d0-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="614d0-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="614d0-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="614d0-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="614d0-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="614d0-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="614d0-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="614d0-130">Required.</span></span> |

<span data-ttu-id="614d0-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="614d0-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="614d0-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="614d0-132">The default output type is text/csv.</span></span> <span data-ttu-id="614d0-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="614d0-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="614d0-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="614d0-134">Request headers</span></span>

| <span data-ttu-id="614d0-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="614d0-135">Name</span></span>          | <span data-ttu-id="614d0-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="614d0-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="614d0-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="614d0-137">Authorization</span></span> | <span data-ttu-id="614d0-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="614d0-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="614d0-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="614d0-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="614d0-141">CSV</span><span class="sxs-lookup"><span data-stu-id="614d0-141">CSV</span></span>

<span data-ttu-id="614d0-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="614d0-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="614d0-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="614d0-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="614d0-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="614d0-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="614d0-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="614d0-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="614d0-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="614d0-146">Report Refresh Date</span></span>
- <span data-ttu-id="614d0-147">Exchange activo</span><span class="sxs-lookup"><span data-stu-id="614d0-147">Exchange Active</span></span>
- <span data-ttu-id="614d0-148">Exchange inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-148">Exchange Inactive</span></span>
- <span data-ttu-id="614d0-149">OneDrive activo</span><span class="sxs-lookup"><span data-stu-id="614d0-149">OneDrive Active</span></span>
- <span data-ttu-id="614d0-150">OneDrive inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-150">OneDrive Inactive</span></span>
- <span data-ttu-id="614d0-151">SharePoint activo</span><span class="sxs-lookup"><span data-stu-id="614d0-151">SharePoint Active</span></span>
- <span data-ttu-id="614d0-152">SharePoint inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-152">SharePoint Inactive</span></span>
- <span data-ttu-id="614d0-153">Skype Empresarial activo</span><span class="sxs-lookup"><span data-stu-id="614d0-153">Skype For Business Active</span></span>
- <span data-ttu-id="614d0-154">Skype Empresarial inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-154">Skype For Business Inactive</span></span>
- <span data-ttu-id="614d0-155">Yammer activo</span><span class="sxs-lookup"><span data-stu-id="614d0-155">Yammer Active</span></span>
- <span data-ttu-id="614d0-156">Yammer inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-156">Yammer Inactive</span></span>
- <span data-ttu-id="614d0-157">Teams activo</span><span class="sxs-lookup"><span data-stu-id="614d0-157">Teams Active</span></span>
- <span data-ttu-id="614d0-158">Teams inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-158">Teams Inactive</span></span>
- <span data-ttu-id="614d0-159">Período del informe</span><span class="sxs-lookup"><span data-stu-id="614d0-159">Report Period</span></span>

<span data-ttu-id="614d0-160">No se admiten las siguientes columnas en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="614d0-160">The following columns are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="614d0-161">Yammer activo</span><span class="sxs-lookup"><span data-stu-id="614d0-161">Yammer Active</span></span>
- <span data-ttu-id="614d0-162">Yammer inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-162">Yammer Inactive</span></span>
- <span data-ttu-id="614d0-163">Teams activo</span><span class="sxs-lookup"><span data-stu-id="614d0-163">Teams Active</span></span>
- <span data-ttu-id="614d0-164">Teams inactivo</span><span class="sxs-lookup"><span data-stu-id="614d0-164">Teams Inactive</span></span>

### <a name="json"></a><span data-ttu-id="614d0-165">JSON</span><span class="sxs-lookup"><span data-stu-id="614d0-165">JSON</span></span>

<span data-ttu-id="614d0-166">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365ServicesUserCounts](../resources/office365servicesusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="614d0-166">If successful, this method returns a `200 OK` response code and an **[office365ServicesUserCounts](../resources/office365servicesusercounts.md)** object in the response body.</span></span>

<span data-ttu-id="614d0-167">No se admiten las siguientes propiedades en el objeto **[office365ServicesUserCounts](../resources/office365servicesusercounts.md)** en China de Microsoft Graph operado por 21Vianet:</span><span class="sxs-lookup"><span data-stu-id="614d0-167">The following properties in **[office365ServicesUserCounts](../resources/office365servicesusercounts.md)** object are not supported in Microsoft Graph China operated by 21Vianet:</span></span>

- <span data-ttu-id="614d0-168">yammerActive</span><span class="sxs-lookup"><span data-stu-id="614d0-168">yammerActive</span></span>
- <span data-ttu-id="614d0-169">yammerInactive</span><span class="sxs-lookup"><span data-stu-id="614d0-169">yammerInactive</span></span>
- <span data-ttu-id="614d0-170">teamsActive</span><span class="sxs-lookup"><span data-stu-id="614d0-170">teamsActive</span></span>
- <span data-ttu-id="614d0-171">teamsInactive</span><span class="sxs-lookup"><span data-stu-id="614d0-171">teamsInactive</span></span>

## <a name="example"></a><span data-ttu-id="614d0-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="614d0-172">Example</span></span>

### <a name="csv"></a><span data-ttu-id="614d0-173">CSV</span><span class="sxs-lookup"><span data-stu-id="614d0-173">CSV</span></span>

<span data-ttu-id="614d0-174">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="614d0-174">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="614d0-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="614d0-175">Request</span></span>

<span data-ttu-id="614d0-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="614d0-176">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365servicesusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ServicesUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="614d0-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="614d0-177">Response</span></span>

<span data-ttu-id="614d0-178">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="614d0-178">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="614d0-179">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="614d0-179">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Exchange Active,Exchange Inactive,OneDrive Active,OneDrive Inactive,SharePoint Active,SharePoint Inactive,Skype For Business Active,Skype For Business Inactive,Yammer Active,Yammer Inactive,Teams Active,Teams Inactive,Report Period
```

### <a name="json"></a><span data-ttu-id="614d0-180">JSON</span><span class="sxs-lookup"><span data-stu-id="614d0-180">JSON</span></span> 

<span data-ttu-id="614d0-181">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="614d0-181">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="614d0-182">Solicitud</span><span class="sxs-lookup"><span data-stu-id="614d0-182">Request</span></span>

<span data-ttu-id="614d0-183">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="614d0-183">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365servicesusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365ServicesUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="614d0-184">Respuesta</span><span class="sxs-lookup"><span data-stu-id="614d0-184">Response</span></span>

<span data-ttu-id="614d0-185">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="614d0-185">The following is an example of the response.</span></span>

> <span data-ttu-id="614d0-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="614d0-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365ServicesUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 458

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365ServicesUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "exchangeActive": 2591, 
      "exchangeInactive": 1426, 
      "oneDriveActive": 1800, 
      "oneDriveInactive": 2451, 
      "sharePointActive": 2286, 
      "sharePointInactive": 1815, 
      "skypeForBusinessActive": 2463, 
      "skypeForBusinessInactive": 1947, 
      "yammerActive": 473, 
      "yammerInactive": 2526, 
      "teamsActive": 846, 
      "teamsInactive": 1960, 
      "reportPeriod": "7"
    }
  ]
}
```
