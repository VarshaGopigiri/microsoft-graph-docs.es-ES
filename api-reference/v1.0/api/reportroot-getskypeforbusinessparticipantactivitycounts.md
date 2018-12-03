---
title: 'reportRoot: getSkypeForBusinessParticipantActivityCounts'
description: Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización. Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros.
ms.openlocfilehash: d271649bfc2883066fcd043cfd50a5347f663c6f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031168"
---
# <a name="reportroot-getskypeforbusinessparticipantactivitycounts"></a><span data-ttu-id="b152a-104">reportRoot: getSkypeForBusinessParticipantActivityCounts</span><span class="sxs-lookup"><span data-stu-id="b152a-104">reportRoot: getSkypeForBusinessParticipantActivityCounts</span></span>

<span data-ttu-id="b152a-105">Obtiene tendencias de uso sobre el número y el tipo de sesiones de conferencia en las que participaron usuarios de la organización.</span><span class="sxs-lookup"><span data-stu-id="b152a-105">Get usage trends on the number and type of conference sessions that users from your organization participated in.</span></span> <span data-ttu-id="b152a-106">Entre los tipos de sesiones de conferencia, se incluyen sesiones de mensajería instantánea, audio o vídeo, uso compartido de aplicaciones, web y acceso telefónico local o aceptación de llamada de terceros.</span><span class="sxs-lookup"><span data-stu-id="b152a-106">Types of conference sessions include IM, audio/video, application sharing, web, and dial-in/out - 3rd party.</span></span>

> <span data-ttu-id="b152a-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de participantes de conferencias de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span><span class="sxs-lookup"><span data-stu-id="b152a-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business conference participant activity](https://support.office.com/client/Skype-for-Business-Online-conference-participant-activity-c3c89995-65dd-4715-9e38-bb244c742c6b).</span></span>

## <a name="permissions"></a><span data-ttu-id="b152a-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="b152a-108">Permissions</span></span>

<span data-ttu-id="b152a-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b152a-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b152a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b152a-111">Permission type</span></span>                        | <span data-ttu-id="b152a-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b152a-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b152a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b152a-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="b152a-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b152a-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b152a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b152a-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b152a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b152a-116">Not supported.</span></span>                           |
| <span data-ttu-id="b152a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b152a-117">Application</span></span>                            | <span data-ttu-id="b152a-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b152a-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b152a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b152a-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessParticipantActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="b152a-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="b152a-120">Function parameters</span></span>

<span data-ttu-id="b152a-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="b152a-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="b152a-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b152a-122">Parameter</span></span> | <span data-ttu-id="b152a-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="b152a-123">Type</span></span>   | <span data-ttu-id="b152a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="b152a-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="b152a-125">period</span><span class="sxs-lookup"><span data-stu-id="b152a-125">period</span></span>    | <span data-ttu-id="b152a-126">cadena</span><span class="sxs-lookup"><span data-stu-id="b152a-126">string</span></span> | <span data-ttu-id="b152a-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b152a-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="b152a-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="b152a-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="b152a-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b152a-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="b152a-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="b152a-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="b152a-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b152a-131">Request headers</span></span>

| <span data-ttu-id="b152a-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="b152a-132">Name</span></span>          | <span data-ttu-id="b152a-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b152a-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="b152a-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="b152a-134">Authorization</span></span> | <span data-ttu-id="b152a-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b152a-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="b152a-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="b152a-137">If-None-Match</span></span> | <span data-ttu-id="b152a-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="b152a-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="b152a-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b152a-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="b152a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b152a-140">Response</span></span>

<span data-ttu-id="b152a-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b152a-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b152a-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b152a-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b152a-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b152a-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b152a-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="b152a-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="b152a-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b152a-145">Report Refresh Date</span></span>
- <span data-ttu-id="b152a-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="b152a-146">Report Date</span></span>
- <span data-ttu-id="b152a-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="b152a-147">Report Period</span></span>
- <span data-ttu-id="b152a-148">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="b152a-148">IM</span></span>
- <span data-ttu-id="b152a-149">Audio o vídeo</span><span class="sxs-lookup"><span data-stu-id="b152a-149">Audio/Video</span></span>
- <span data-ttu-id="b152a-150">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="b152a-150">App Sharing</span></span>
- <span data-ttu-id="b152a-151">Web</span><span class="sxs-lookup"><span data-stu-id="b152a-151">Web</span></span>
- <span data-ttu-id="b152a-152">Acceso telefónico local o aceptación de llamada de terceros</span><span class="sxs-lookup"><span data-stu-id="b152a-152">Dial-in/out 3rd Party</span></span>

## <a name="example"></a><span data-ttu-id="b152a-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b152a-153">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b152a-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b152a-154">Request</span></span>

<span data-ttu-id="b152a-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b152a-155">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessparticipantactivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessParticipantActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="b152a-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b152a-156">Response</span></span>

<span data-ttu-id="b152a-157">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b152a-157">The following is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.report"
} -->

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="b152a-158">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b152a-158">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio/Video,App Sharing,Web,Dial-in/out 3rd Party
```