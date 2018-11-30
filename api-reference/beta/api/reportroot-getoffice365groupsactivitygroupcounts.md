---
title: 'reportRoot: getOffice365GroupsActivityGroupCounts'
description: Obtiene el número total diario de grupos y cuántos de ellos estuvieron activos según las conversaciones de correo electrónico, las publicaciones de Yammer y las actividades en archivos de SharePoint.
ms.openlocfilehash: e1b70d9253c99239d6ef980de6edcfde03d7dbed
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085384"
---
# <a name="reportroot-getoffice365groupsactivitygroupcounts"></a><span data-ttu-id="2f765-103">reportRoot: getOffice365GroupsActivityGroupCounts</span><span class="sxs-lookup"><span data-stu-id="2f765-103">reportRoot: getOffice365GroupsActivityGroupCounts</span></span>

> <span data-ttu-id="2f765-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2f765-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2f765-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2f765-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2f765-106">Obtiene el número total diario de grupos y cuántos de ellos estuvieron activos según las conversaciones de correo electrónico, las publicaciones de Yammer y las actividades en archivos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2f765-106">Get the daily total number of groups and how many of them were active based on email conversations, Yammer posts, and SharePoint file activities.</span></span>

> <span data-ttu-id="2f765-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="2f765-107">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="2f765-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="2f765-108">Permissions</span></span>

<span data-ttu-id="2f765-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2f765-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="2f765-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2f765-111">Permission type</span></span>                        | <span data-ttu-id="2f765-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2f765-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="2f765-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2f765-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="2f765-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2f765-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="2f765-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2f765-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2f765-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2f765-116">Not supported.</span></span>                           |
| <span data-ttu-id="2f765-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2f765-117">Application</span></span>                            | <span data-ttu-id="2f765-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2f765-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="2f765-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2f765-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityGroupCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="2f765-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="2f765-120">Function parameters</span></span>

<span data-ttu-id="2f765-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="2f765-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="2f765-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2f765-122">Parameter</span></span> | <span data-ttu-id="2f765-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f765-123">Type</span></span>   | <span data-ttu-id="2f765-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f765-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="2f765-125">period</span><span class="sxs-lookup"><span data-stu-id="2f765-125">period</span></span>    | <span data-ttu-id="2f765-126">cadena</span><span class="sxs-lookup"><span data-stu-id="2f765-126">string</span></span> | <span data-ttu-id="2f765-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2f765-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="2f765-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="2f765-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="2f765-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2f765-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="2f765-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="2f765-130">Required.</span></span> |

<span data-ttu-id="2f765-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f765-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="2f765-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="2f765-132">The default output type is text/csv.</span></span> <span data-ttu-id="2f765-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="2f765-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2f765-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2f765-134">Request headers</span></span>

| <span data-ttu-id="2f765-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="2f765-135">Name</span></span>          | <span data-ttu-id="2f765-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f765-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="2f765-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="2f765-137">Authorization</span></span> | <span data-ttu-id="2f765-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2f765-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="2f765-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f765-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="2f765-141">CSV</span><span class="sxs-lookup"><span data-stu-id="2f765-141">CSV</span></span>

<span data-ttu-id="2f765-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="2f765-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="2f765-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f765-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="2f765-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="2f765-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="2f765-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="2f765-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="2f765-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="2f765-146">Report Refresh Date</span></span>
- <span data-ttu-id="2f765-147">Total</span><span class="sxs-lookup"><span data-stu-id="2f765-147">Total</span></span>
- <span data-ttu-id="2f765-148">Activo</span><span class="sxs-lookup"><span data-stu-id="2f765-148">Active</span></span>
- <span data-ttu-id="2f765-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="2f765-149">Report Date</span></span>
- <span data-ttu-id="2f765-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="2f765-150">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="2f765-151">JSON</span><span class="sxs-lookup"><span data-stu-id="2f765-151">JSON</span></span>

<span data-ttu-id="2f765-152">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[office365GroupsActivityGroupCounts](../resources/office365groupsactivitygroupcounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f765-152">If successful, this method returns a `200 OK` response code and an **[office365GroupsActivityGroupCounts](../resources/office365groupsactivitygroupcounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2f765-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2f765-153">Example</span></span>

### <a name="csv"></a><span data-ttu-id="2f765-154">CSV</span><span class="sxs-lookup"><span data-stu-id="2f765-154">CSV</span></span>

<span data-ttu-id="2f765-155">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="2f765-155">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="2f765-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f765-156">Request</span></span>

<span data-ttu-id="2f765-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f765-157">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365groupsactivitygroupcounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365GroupsActivityGroupCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="2f765-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f765-158">Response</span></span>

<span data-ttu-id="2f765-159">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f765-159">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="2f765-160">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="2f765-160">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

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

### <a name="json"></a><span data-ttu-id="2f765-161">JSON</span><span class="sxs-lookup"><span data-stu-id="2f765-161">JSON</span></span>

<span data-ttu-id="2f765-162">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="2f765-162">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="2f765-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2f765-163">Request</span></span>

<span data-ttu-id="2f765-164">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2f765-164">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365groupsactivitygroupcounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOffice365GroupsActivityGroupCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="2f765-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2f765-165">Response</span></span>

<span data-ttu-id="2f765-166">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2f765-166">The following is an example of the response.</span></span>

> <span data-ttu-id="2f765-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2f765-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.office365GroupsActivityGroupCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 240

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.office365GroupsActivityGroupCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "total": 5344, 
      "active": 0, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
