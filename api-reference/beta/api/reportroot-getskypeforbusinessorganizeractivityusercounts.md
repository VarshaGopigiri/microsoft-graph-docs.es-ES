---
title: 'reportRoot: getSkypeForBusinessOrganizerActivityUserCounts'
description: Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de conferencia realizadas y organizadas por los usuarios de la organización. Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web, acceso telefónico local o aceptación de llamada de terceros, y acceso telefónico local o aceptación de llamada de Microsoft.
localization_priority: Normal
ms.openlocfilehash: 2285062ea40a4e0dc9b1468a926dc2ec6fac5564
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886222"
---
# <a name="reportroot-getskypeforbusinessorganizeractivityusercounts"></a><span data-ttu-id="77aeb-104">reportRoot: getSkypeForBusinessOrganizerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="77aeb-104">reportRoot: getSkypeForBusinessOrganizerActivityUserCounts</span></span>

> <span data-ttu-id="77aeb-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="77aeb-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="77aeb-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="77aeb-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="77aeb-107">Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de conferencia realizadas y organizadas por los usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="77aeb-107">Get usage trends on the number of unique users and type of conference sessions held and organized by users in your organization.</span></span> <span data-ttu-id="77aeb-108">Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web, acceso telefónico local o aceptación de llamada de terceros, y acceso telefónico local o aceptación de llamada de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77aeb-108">Types of conference sessions include IM, audio/video, application sharing, web, dial-in/out - 3rd party, and dial-in/out Microsoft.</span></span>

> <span data-ttu-id="77aeb-109">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de organizador de conferencia de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254).</span><span class="sxs-lookup"><span data-stu-id="77aeb-109">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference organizer activity](https://support.office.com/client/Skype-for-Business-Online-conference-organized-activity-03a255d4-0e1d-4b24-b73d-7a62fae36254).</span></span>

## <a name="permissions"></a><span data-ttu-id="77aeb-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="77aeb-110">Permissions</span></span>

<span data-ttu-id="77aeb-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="77aeb-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="77aeb-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="77aeb-113">Permission type</span></span>                        | <span data-ttu-id="77aeb-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="77aeb-114">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="77aeb-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="77aeb-115">Delegated (work or school account)</span></span>     | <span data-ttu-id="77aeb-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="77aeb-116">Reports.Read.All</span></span>                         |
| <span data-ttu-id="77aeb-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="77aeb-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="77aeb-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="77aeb-118">Not supported.</span></span>                           |
| <span data-ttu-id="77aeb-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="77aeb-119">Application</span></span>                            | <span data-ttu-id="77aeb-120">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="77aeb-120">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="77aeb-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="77aeb-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessOrganizerActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="77aeb-122">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="77aeb-122">Function parameters</span></span>

<span data-ttu-id="77aeb-123">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="77aeb-123">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="77aeb-124">Parámetro</span><span class="sxs-lookup"><span data-stu-id="77aeb-124">Parameter</span></span> | <span data-ttu-id="77aeb-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="77aeb-125">Type</span></span>   | <span data-ttu-id="77aeb-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="77aeb-126">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="77aeb-127">period</span><span class="sxs-lookup"><span data-stu-id="77aeb-127">period</span></span>    | <span data-ttu-id="77aeb-128">cadena</span><span class="sxs-lookup"><span data-stu-id="77aeb-128">string</span></span> | <span data-ttu-id="77aeb-129">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="77aeb-129">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="77aeb-130">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="77aeb-130">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="77aeb-131">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="77aeb-131">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="77aeb-132">Necesario.</span><span class="sxs-lookup"><span data-stu-id="77aeb-132">Required.</span></span> |

<span data-ttu-id="77aeb-133">Este método admite la `$format` [parámetro de consulta de OData](/graph/query-parameters) para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77aeb-133">This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response.</span></span> <span data-ttu-id="77aeb-134">El tipo de salida predeterminado es texto o csv.</span><span class="sxs-lookup"><span data-stu-id="77aeb-134">The default output type is text/csv.</span></span> <span data-ttu-id="77aeb-135">Sin embargo, si desea especificar el tipo de salida, puede usar el parámetro de consulta de OData $format establecido en texto o csv o application/json.</span><span class="sxs-lookup"><span data-stu-id="77aeb-135">However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.</span></span>

## <a name="request-headers"></a><span data-ttu-id="77aeb-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="77aeb-136">Request headers</span></span>

| <span data-ttu-id="77aeb-137">Nombre</span><span class="sxs-lookup"><span data-stu-id="77aeb-137">Name</span></span>          | <span data-ttu-id="77aeb-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="77aeb-138">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="77aeb-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="77aeb-139">Authorization</span></span> | <span data-ttu-id="77aeb-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="77aeb-p107">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="77aeb-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77aeb-142">Response</span></span>

### <a name="csv"></a><span data-ttu-id="77aeb-143">CSV</span><span class="sxs-lookup"><span data-stu-id="77aeb-143">CSV</span></span>

<span data-ttu-id="77aeb-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="77aeb-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="77aeb-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77aeb-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="77aeb-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="77aeb-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="77aeb-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="77aeb-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="77aeb-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="77aeb-148">Report Refresh Date</span></span>
- <span data-ttu-id="77aeb-149">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="77aeb-149">Report Date</span></span>
- <span data-ttu-id="77aeb-150">Período del informe</span><span class="sxs-lookup"><span data-stu-id="77aeb-150">Report Period</span></span>
- <span data-ttu-id="77aeb-151">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="77aeb-151">IM</span></span>
- <span data-ttu-id="77aeb-152">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="77aeb-152">Audio/Video</span></span>
- <span data-ttu-id="77aeb-153">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="77aeb-153">App Sharing</span></span>
- <span data-ttu-id="77aeb-154">Web</span><span class="sxs-lookup"><span data-stu-id="77aeb-154">Web</span></span>
- <span data-ttu-id="77aeb-155">Acceso telefónico local o aceptación de llamada de terceros</span><span class="sxs-lookup"><span data-stu-id="77aeb-155">Dial-in/out 3rd Party</span></span>
- <span data-ttu-id="77aeb-156">Acceso telefónico local o aceptación de llamada de Microsoft</span><span class="sxs-lookup"><span data-stu-id="77aeb-156">Dial-in/out Microsoft</span></span>

### <a name="json"></a><span data-ttu-id="77aeb-157">JSON</span><span class="sxs-lookup"><span data-stu-id="77aeb-157">JSON</span></span>

<span data-ttu-id="77aeb-158">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto **[skypeForBusinessOrganizerActivityUserCounts](../resources/skypeforbusinessorganizeractivityusercounts.md)** en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77aeb-158">If successful, this method returns a `200 OK` response code and a **[skypeForBusinessOrganizerActivityUserCounts](../resources/skypeforbusinessorganizeractivityusercounts.md)** object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="77aeb-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="77aeb-159">Example</span></span>

### <a name="csv"></a><span data-ttu-id="77aeb-160">CSV</span><span class="sxs-lookup"><span data-stu-id="77aeb-160">CSV</span></span>

<span data-ttu-id="77aeb-161">El siguiente es un ejemplo que muestra los resultados CSV.</span><span class="sxs-lookup"><span data-stu-id="77aeb-161">The following is an example that outputs CSV.</span></span>

#### <a name="request"></a><span data-ttu-id="77aeb-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77aeb-162">Request</span></span>

<span data-ttu-id="77aeb-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77aeb-163">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessorganizeractivityusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessOrganizerActivityUserCounts(period='D7')?$format=text/csv
```

#### <a name="response"></a><span data-ttu-id="77aeb-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77aeb-164">Response</span></span>

<span data-ttu-id="77aeb-165">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77aeb-165">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="77aeb-166">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="77aeb-166">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party,Dial-in/out Microsoft
```

### <a name="json"></a><span data-ttu-id="77aeb-167">JSON</span><span class="sxs-lookup"><span data-stu-id="77aeb-167">JSON</span></span>

<span data-ttu-id="77aeb-168">El siguiente es un ejemplo que devuelve JSON.</span><span class="sxs-lookup"><span data-stu-id="77aeb-168">The following is an example that returns JSON.</span></span>

#### <a name="request"></a><span data-ttu-id="77aeb-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="77aeb-169">Request</span></span>

<span data-ttu-id="77aeb-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="77aeb-170">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getskypeforbusinessorganizeractivityusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getSkypeForBusinessOrganizerActivityUserCounts(period='D7')?$format=application/json
```

#### <a name="response"></a><span data-ttu-id="77aeb-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="77aeb-171">Response</span></span>

<span data-ttu-id="77aeb-172">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77aeb-172">The following is an example of the response.</span></span>

> <span data-ttu-id="77aeb-p109">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="77aeb-p109">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.skypeForBusinessOrganizerActivityUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 319

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.skypeForBusinessOrganizerActivityUserCounts)", 
  "value": [
    {
      "im": 37, 
      "audioVideo": 42, 
      "appSharing": 35, 
      "web": 3, 
      "dialInOut3rdParty": 0, 
      "dialInOutMicrosoft": 36, 
      "reportRefreshDate": "2017-09-01", 
      "reportDate": "2017-09-01", 
      "reportPeriod": "7"
    }
  ]
}
```
