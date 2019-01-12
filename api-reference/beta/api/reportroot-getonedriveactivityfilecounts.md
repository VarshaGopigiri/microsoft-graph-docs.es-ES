---
title: 'reportRoot: getOneDriveActivityFileCounts'
description: Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 6f7b791a361beca03c65a97a59bbd0c15881924d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27924065"
---
# <a name="reportroot-getonedriveactivityfilecounts"></a><span data-ttu-id="ee745-103">reportRoot: getOneDriveActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="ee745-103">reportRoot: getOneDriveActivityFileCounts</span></span>

> <span data-ttu-id="ee745-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee745-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee745-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee745-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee745-106">Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ee745-106">Get the number of unique, licensed users that performed file interactions against any OneDrive account.</span></span>

> <span data-ttu-id="ee745-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="ee745-107">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="ee745-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ee745-108">Permissions</span></span>

<span data-ttu-id="ee745-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ee745-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ee745-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ee745-111">Permission type</span></span>                        | <span data-ttu-id="ee745-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ee745-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ee745-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ee745-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="ee745-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee745-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ee745-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ee745-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ee745-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ee745-116">Not supported.</span></span>                           |
| <span data-ttu-id="ee745-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ee745-117">Application</span></span>                            | <span data-ttu-id="ee745-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ee745-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ee745-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ee745-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveActivityFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ee745-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ee745-120">Function parameters</span></span>

<span data-ttu-id="ee745-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ee745-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ee745-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ee745-122">Parameter</span></span> | <span data-ttu-id="ee745-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee745-123">Type</span></span>   | <span data-ttu-id="ee745-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee745-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ee745-125">period</span><span class="sxs-lookup"><span data-stu-id="ee745-125">period</span></span>    | <span data-ttu-id="ee745-126">cadena</span><span class="sxs-lookup"><span data-stu-id="ee745-126">string</span></span> | <span data-ttu-id="ee745-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ee745-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ee745-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ee745-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ee745-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ee745-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ee745-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ee745-130">Required.</span></span> |

<span data-ttu-id="ee745-131">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee745-131">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="ee745-132">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="ee745-132">The default output type is text/csv.</span></span> <span data-ttu-id="ee745-133">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="ee745-133">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ee745-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ee745-134">Request headers</span></span>

| <span data-ttu-id="ee745-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="ee745-135">Name</span></span>          | <span data-ttu-id="ee745-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee745-136">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="ee745-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="ee745-137">Authorization</span></span> | <span data-ttu-id="ee745-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ee745-p105">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="ee745-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee745-140">Response</span></span>

### <a name="csv"></a><span data-ttu-id="ee745-141">CSV</span><span class="sxs-lookup"><span data-stu-id="ee745-141">CSV</span></span>

<span data-ttu-id="ee745-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ee745-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ee745-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee745-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ee745-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ee745-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ee745-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ee745-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ee745-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ee745-146">Report Refresh Date</span></span>
- <span data-ttu-id="ee745-147">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="ee745-147">Viewed Or Edited</span></span>
- <span data-ttu-id="ee745-148">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="ee745-148">Synced</span></span>
- <span data-ttu-id="ee745-149">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="ee745-149">Shared Internally</span></span>
- <span data-ttu-id="ee745-150">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="ee745-150">Shared Externally</span></span>
- <span data-ttu-id="ee745-151">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ee745-151">Report Date</span></span>
- <span data-ttu-id="ee745-152">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ee745-152">Report Period</span></span>

### <a name="json"></a><span data-ttu-id="ee745-153">JSON</span><span class="sxs-lookup"><span data-stu-id="ee745-153">JSON</span></span>

<span data-ttu-id="ee745-154">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[siteActivitySummary](../resources/siteactivitysummary.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee745-154">If successful, this method returns a `200 OK` response code and a **[siteActivitySummary](../resources/siteactivitysummary.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ee745-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ee745-155">Example</span></span>

### <a name="csv"></a><span data-ttu-id="ee745-156">CSV</span><span class="sxs-lookup"><span data-stu-id="ee745-156">CSV</span></span>

<span data-ttu-id="ee745-157">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="ee745-157">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="ee745-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee745-158">Request</span></span>

<span data-ttu-id="ee745-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee745-159">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveactivityfilecounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveActivityFileCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="ee745-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee745-160">Response</span></span>

<span data-ttu-id="ee745-161">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee745-161">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="ee745-162">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ee745-162">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```

### <a name="json"></a><span data-ttu-id="ee745-163">JSON</span><span class="sxs-lookup"><span data-stu-id="ee745-163">JSON</span></span>

<span data-ttu-id="ee745-164">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="ee745-164">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="ee745-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ee745-165">Request</span></span>

<span data-ttu-id="ee745-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ee745-166">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getonedriveactivityfilecounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getOneDriveActivityFileCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="ee745-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ee745-167">Response</span></span>

<span data-ttu-id="ee745-168">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ee745-168">The following is an example of the response.</span></span>

> <span data-ttu-id="ee745-p107">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ee745-p107">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.siteActivitySummary"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 280

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.siteActivitySummary)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "viewedOrEdited": 1997, 
      "synced": 24756, 
      "sharedInternally": 7, 
      "sharedExternally": 0, 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
