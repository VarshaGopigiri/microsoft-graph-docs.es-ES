---
title: 'reportRoot: getSkypeForBusinessParticipantActivityCounts'
description: Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización. Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 25dbb7b2ea84e6935e586f0c58bdc1882c0f8cac
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27948110"
---
# <a name="reportroot-getskypeforbusinessparticipantactivitycounts"></a><span data-ttu-id="2c268-104">reportRoot: getSkypeForBusinessParticipantActivityCounts</span><span class="sxs-lookup"><span data-stu-id="2c268-104">reportRoot: getSkypeForBusinessParticipantActivityCounts</span></span>

> <span data-ttu-id="2c268-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2c268-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2c268-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2c268-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2c268-107">Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="2c268-107">Get usage trends on the number and type of conference sessions that users from your organization participated in.</span></span> <span data-ttu-id="2c268-108">Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros.</span><span class="sxs-lookup"><span data-stu-id="2c268-108">Types of conference sessions include IM, audio/video, application sharing, web, and dial-in/out - 3rd party.</span></span>

> <span data-ttu-id="2c268-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de participantes de conferencias de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span><span class="sxs-lookup"><span data-stu-id="2c268-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference participant activity](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span></span>

## <a name="permissions"></a><span data-ttu-id="2c268-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="2c268-110">Permissions</span></span>

<span data-ttu-id="2c268-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2c268-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="2c268-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2c268-113">Permission type</span></span>                        | <span data-ttu-id="2c268-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2c268-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="2c268-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2c268-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="2c268-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2c268-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="2c268-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2c268-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2c268-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2c268-118">Not supported.</span></span>                           |
| <span data-ttu-id="2c268-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2c268-119">Application</span></span>                            | <span data-ttu-id="2c268-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2c268-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="2c268-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c268-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessParticipantActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="2c268-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="2c268-122">Function parameters</span></span>

<span data-ttu-id="2c268-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="2c268-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="2c268-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2c268-124">Parameter</span></span> | <span data-ttu-id="2c268-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c268-125">Type</span></span>   | <span data-ttu-id="2c268-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c268-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="2c268-127">period</span><span class="sxs-lookup"><span data-stu-id="2c268-127">period</span></span>    | <span data-ttu-id="2c268-128">cadena</span><span class="sxs-lookup"><span data-stu-id="2c268-128">string</span></span> | <span data-ttu-id="2c268-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2c268-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="2c268-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="2c268-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="2c268-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2c268-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="2c268-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="2c268-132">Required.</span></span> |

<span data-ttu-id="2c268-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c268-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="2c268-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="2c268-134">The default output type is text/csv.</span></span> <span data-ttu-id="2c268-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="2c268-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2c268-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c268-136">Request headers</span></span>

| <span data-ttu-id="2c268-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c268-137">Name</span></span>          | <span data-ttu-id="2c268-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c268-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="2c268-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c268-139">Authorization</span></span> | <span data-ttu-id="2c268-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c268-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="2c268-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c268-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="2c268-143">CSV</span><span class="sxs-lookup"><span data-stu-id="2c268-143">CSV</span></span>

<span data-ttu-id="2c268-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="2c268-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="2c268-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c268-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="2c268-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="2c268-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="2c268-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="2c268-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="2c268-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="2c268-148">Report Refresh Date</span></span>
- <span data-ttu-id="2c268-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="2c268-149">Report Date</span></span>
- <span data-ttu-id="2c268-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="2c268-150">Report Period</span></span>
- <span data-ttu-id="2c268-151">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="2c268-151">IM</span></span>
- <span data-ttu-id="2c268-152">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="2c268-152">Audio/Video</span></span>
- <span data-ttu-id="2c268-153">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2c268-153">App Sharing</span></span>
- <span data-ttu-id="2c268-154">Web</span><span class="sxs-lookup"><span data-stu-id="2c268-154">Web</span></span>
- <span data-ttu-id="2c268-155">Acceso telefónico local o aceptación de llamada de terceros</span><span class="sxs-lookup"><span data-stu-id="2c268-155">Dial-in/out 3rd Party</span></span>

### <a name="json"></a><span data-ttu-id="2c268-156">JSON</span><span class="sxs-lookup"><span data-stu-id="2c268-156">JSON</span></span>

<span data-ttu-id="2c268-157">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessParticipantActivityCounts](../resources/skypeforbusinessparticipantactivitycounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c268-157">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessParticipantActivityCounts](../resources/skypeforbusinessparticipantactivitycounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c268-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c268-158">Example</span></span>

### <a name="csv"></a><span data-ttu-id="2c268-159">CSV</span><span class="sxs-lookup"><span data-stu-id="2c268-159">CSV</span></span>

<span data-ttu-id="2c268-160">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="2c268-160">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="2c268-161">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c268-161">Request</span></span>

<span data-ttu-id="2c268-162">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c268-162">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessparticipantactivitycounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessParticipantActivityCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="2c268-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c268-163">Response</span></span>

<span data-ttu-id="2c268-164">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c268-164">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="2c268-165">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="2c268-165">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party
```

### <a name="json"></a><span data-ttu-id="2c268-166">JSON</span><span class="sxs-lookup"><span data-stu-id="2c268-166">JSON</span></span>

<span data-ttu-id="2c268-167">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="2c268-167">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="2c268-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c268-168">Request</span></span>

<span data-ttu-id="2c268-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c268-169">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessparticipantactivitycounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessParticipantActivityCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="2c268-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c268-170">Response</span></span>

<span data-ttu-id="2c268-171">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c268-171">The following is an example of the response.</span></span>

> <span data-ttu-id="2c268-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c268-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessParticipantActivityCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 296

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessParticipantActivityCounts)", 
  "value": [
    {
      "im": 162, 
      "audioVideo": 156, 
      "appSharing": 45, 
      "web": 12, 
      "dialInOut3rdParty": 2, 
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
