---
title: 'reportRoot: getSkypeForBusinessPeerToPeerActivityCounts'
description: Obtiene tendencias de uso sobre el número y el tipo de sesiones realizadas en la organización. Entre los tipos de sesiones, se incluyen la mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: d26b5a310a131b44814bcce3781953a29487fa85
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990442"
---
# <a name="reportroot-getskypeforbusinesspeertopeeractivitycounts"></a><span data-ttu-id="7a50e-104">reportRoot: getSkypeForBusinessPeerToPeerActivityCounts</span><span class="sxs-lookup"><span data-stu-id="7a50e-104">reportRoot: getSkypeForBusinessPeerToPeerActivityCounts</span></span>

> <span data-ttu-id="7a50e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7a50e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7a50e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7a50e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7a50e-107">Obtiene tendencias de uso sobre el número y el tipo de sesiones realizadas en la organización.</span><span class="sxs-lookup"><span data-stu-id="7a50e-107">Get usage trends on the number and type of sessions held in your organization.</span></span> <span data-ttu-id="7a50e-108">Entre los tipos de sesiones, se incluyen la mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos.</span><span class="sxs-lookup"><span data-stu-id="7a50e-108">Types of sessions include IM, audio, video, application sharing, and file transfer.</span></span>

> <span data-ttu-id="7a50e-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de punto a punto de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).</span><span class="sxs-lookup"><span data-stu-id="7a50e-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business peer-to-peer activity](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).</span></span>

## <a name="permissions"></a><span data-ttu-id="7a50e-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="7a50e-110">Permissions</span></span>

<span data-ttu-id="7a50e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a50e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7a50e-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a50e-113">Permission type</span></span>                        | <span data-ttu-id="7a50e-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a50e-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7a50e-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a50e-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="7a50e-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a50e-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7a50e-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a50e-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7a50e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a50e-118">Not supported.</span></span>                           |
| <span data-ttu-id="7a50e-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a50e-119">Application</span></span>                            | <span data-ttu-id="7a50e-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a50e-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7a50e-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a50e-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessPeerToPeerActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="7a50e-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="7a50e-122">Function parameters</span></span>

<span data-ttu-id="7a50e-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7a50e-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="7a50e-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7a50e-124">Parameter</span></span> | <span data-ttu-id="7a50e-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a50e-125">Type</span></span>   | <span data-ttu-id="7a50e-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a50e-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7a50e-127">period</span><span class="sxs-lookup"><span data-stu-id="7a50e-127">period</span></span>    | <span data-ttu-id="7a50e-128">cadena</span><span class="sxs-lookup"><span data-stu-id="7a50e-128">string</span></span> | <span data-ttu-id="7a50e-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a50e-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7a50e-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7a50e-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7a50e-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a50e-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="7a50e-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7a50e-132">Required.</span></span> |

<span data-ttu-id="7a50e-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a50e-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="7a50e-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="7a50e-134">The default output type is text/csv.</span></span> <span data-ttu-id="7a50e-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="7a50e-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="7a50e-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a50e-136">Request headers</span></span>

| <span data-ttu-id="7a50e-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a50e-137">Name</span></span>          | <span data-ttu-id="7a50e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a50e-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="7a50e-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a50e-139">Authorization</span></span> | <span data-ttu-id="7a50e-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a50e-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="7a50e-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a50e-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="7a50e-143">CSV</span><span class="sxs-lookup"><span data-stu-id="7a50e-143">CSV</span></span>

<span data-ttu-id="7a50e-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7a50e-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7a50e-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a50e-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7a50e-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7a50e-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7a50e-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7a50e-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7a50e-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7a50e-148">Report Refresh Date</span></span>
- <span data-ttu-id="7a50e-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="7a50e-149">Report Date</span></span>
- <span data-ttu-id="7a50e-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7a50e-150">Report Period</span></span>
- <span data-ttu-id="7a50e-151">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="7a50e-151">IM</span></span>
- <span data-ttu-id="7a50e-152">Audio</span><span class="sxs-lookup"><span data-stu-id="7a50e-152">Audio</span></span>
- <span data-ttu-id="7a50e-153">Vídeo</span><span class="sxs-lookup"><span data-stu-id="7a50e-153">Video</span></span>
- <span data-ttu-id="7a50e-154">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7a50e-154">App Sharing</span></span>
- <span data-ttu-id="7a50e-155">Transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="7a50e-155">File Transfer</span></span>

### <a name="json"></a><span data-ttu-id="7a50e-156">JSON</span><span class="sxs-lookup"><span data-stu-id="7a50e-156">JSON</span></span>

<span data-ttu-id="7a50e-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessPeerToPeerActivityCounts](../resources/skypeforbusinesspeertopeeractivitycounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a50e-157">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessPeerToPeerActivityCounts](../resources/skypeforbusinesspeertopeeractivitycounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7a50e-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a50e-158">Example</span></span>

### <a name="csv"></a><span data-ttu-id="7a50e-159">CSV</span><span class="sxs-lookup"><span data-stu-id="7a50e-159">CSV</span></span>

<span data-ttu-id="7a50e-160">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="7a50e-160">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="7a50e-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a50e-161">Request</span></span>

<span data-ttu-id="7a50e-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a50e-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinesspeertopeeractivitycounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessPeerToPeerActivityCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="7a50e-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a50e-163">Response</span></span>

<span data-ttu-id="7a50e-164">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a50e-164">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="7a50e-165">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a50e-165">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio,Video,App Sharing,File Transfer
```

### <a name="json"></a><span data-ttu-id="7a50e-166">JSON</span><span class="sxs-lookup"><span data-stu-id="7a50e-166">JSON</span></span>

<span data-ttu-id="7a50e-167">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="7a50e-167">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="7a50e-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a50e-168">Request</span></span>

<span data-ttu-id="7a50e-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a50e-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinesspeertopeeractivitycounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessPeerToPeerActivityCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="7a50e-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a50e-170">Response</span></span>

<span data-ttu-id="7a50e-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a50e-171">The following is an example of the response.</span></span>

> <span data-ttu-id="7a50e-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7a50e-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessPeerToPeerActivityCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 288

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessPeerToPeerActivityCounts)", 
  "value": [
    {
      "im": 1177, 
      "audio": 107, 
      "video": 7, 
      "appSharing": 74, 
      "fileTransfer": 24, 
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
