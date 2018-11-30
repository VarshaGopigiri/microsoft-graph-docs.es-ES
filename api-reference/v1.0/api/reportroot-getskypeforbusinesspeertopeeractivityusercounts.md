---
title: 'reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts'
description: Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de punto a punto realizadas en la organización. Entre los diferentes tipos, se incluyen sesiones de mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos en sesiones de punto a punto.
ms.openlocfilehash: 8abfba14ea31ed4caaa395274f286c01f4083daa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030144"
---
# <a name="reportroot-getskypeforbusinesspeertopeeractivityusercounts"></a><span data-ttu-id="ae346-104">reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="ae346-104">reportRoot: getSkypeForBusinessPeerToPeerActivityUserCounts</span></span>

<span data-ttu-id="ae346-105">Obtiene tendencias de uso sobre el número de usuarios únicos y el tipo de sesiones de punto a punto realizadas en la organización.</span><span class="sxs-lookup"><span data-stu-id="ae346-105">Get usage trends on the number of unique users and type of peer-to-peer sessions held in your organization.</span></span> <span data-ttu-id="ae346-106">Entre los diferentes tipos, se incluyen sesiones de mensajería instantánea, audio, vídeo, uso compartido de aplicaciones y transferencias de archivos en sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="ae346-106">Types of sessions include IM, audio, video, application sharing, and file transfers in peer-to-peer sessions.</span></span>

> <span data-ttu-id="ae346-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de punto a punto de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).</span><span class="sxs-lookup"><span data-stu-id="ae346-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business peer-to-peer activity](https://support.office.com/client/Skype-for-Business-Online-peertopeer-activity-d3b2d569-4ee9-44b8-92bf-d518142f0713).</span></span>

## <a name="permissions"></a><span data-ttu-id="ae346-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ae346-108">Permissions</span></span>

<span data-ttu-id="ae346-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ae346-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ae346-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ae346-111">Permission type</span></span>                        | <span data-ttu-id="ae346-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ae346-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="ae346-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ae346-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="ae346-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ae346-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="ae346-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ae346-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ae346-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ae346-116">Not supported.</span></span>                           |
| <span data-ttu-id="ae346-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ae346-117">Application</span></span>                            | <span data-ttu-id="ae346-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="ae346-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="ae346-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ae346-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="ae346-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="ae346-120">Function parameters</span></span>

<span data-ttu-id="ae346-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="ae346-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="ae346-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ae346-122">Parameter</span></span> | <span data-ttu-id="ae346-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae346-123">Type</span></span>   | <span data-ttu-id="ae346-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae346-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="ae346-125">period</span><span class="sxs-lookup"><span data-stu-id="ae346-125">period</span></span>    | <span data-ttu-id="ae346-126">cadena</span><span class="sxs-lookup"><span data-stu-id="ae346-126">string</span></span> | <span data-ttu-id="ae346-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ae346-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="ae346-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="ae346-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="ae346-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="ae346-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="ae346-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="ae346-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="ae346-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ae346-131">Request headers</span></span>

| <span data-ttu-id="ae346-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="ae346-132">Name</span></span>          | <span data-ttu-id="ae346-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae346-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="ae346-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="ae346-134">Authorization</span></span> | <span data-ttu-id="ae346-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ae346-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="ae346-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="ae346-137">If-None-Match</span></span> | <span data-ttu-id="ae346-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="ae346-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="ae346-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ae346-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="ae346-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae346-140">Response</span></span>

<span data-ttu-id="ae346-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="ae346-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="ae346-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae346-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="ae346-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="ae346-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="ae346-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="ae346-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="ae346-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="ae346-145">Report Refresh Date</span></span>
- <span data-ttu-id="ae346-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="ae346-146">Report Date</span></span>
- <span data-ttu-id="ae346-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="ae346-147">Report Period</span></span>
- <span data-ttu-id="ae346-148">Mensajería instantánea</span><span class="sxs-lookup"><span data-stu-id="ae346-148">IM</span></span>
- <span data-ttu-id="ae346-149">Audio</span><span class="sxs-lookup"><span data-stu-id="ae346-149">Audio</span></span>
- <span data-ttu-id="ae346-150">Vídeo</span><span class="sxs-lookup"><span data-stu-id="ae346-150">Video</span></span>
- <span data-ttu-id="ae346-151">Uso compartido de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ae346-151">App Sharing</span></span>
- <span data-ttu-id="ae346-152">Transferencia de archivos</span><span class="sxs-lookup"><span data-stu-id="ae346-152">File Transfer</span></span>

## <a name="example"></a><span data-ttu-id="ae346-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ae346-153">Example</span></span>

#### <a name="request"></a><span data-ttu-id="ae346-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ae346-154">Request</span></span>

<span data-ttu-id="ae346-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae346-155">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinesspeertopeeractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessPeerToPeerActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="ae346-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ae346-156">Response</span></span>

<span data-ttu-id="ae346-157">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae346-157">The following is an example of the response.</span></span>

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

<span data-ttu-id="ae346-158">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="ae346-158">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,IM,Audio,Video,App Sharing,File Transfer
```