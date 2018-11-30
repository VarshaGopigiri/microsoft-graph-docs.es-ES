---
title: 'reportRoot: getSkypeForBusinessActivityUserCounts'
description: Obtiene las tendencias sobre el número de usuarios únicos que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial. En el informe, también se incluye el número de sesiones de punto a punto.
ms.openlocfilehash: 9a797d9af29d9964c2b1797f82be2c28893337d0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030807"
---
# <a name="reportroot-getskypeforbusinessactivityusercounts"></a><span data-ttu-id="41c04-104">reportRoot: getSkypeForBusinessActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="41c04-104">reportRoot: getSkypeForBusinessActivityUserCounts</span></span>

<span data-ttu-id="41c04-105">Obtiene las tendencias sobre el número de usuarios únicos que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="41c04-105">Get the trends on how many unique users organized and participated in conference sessions held in your organization through Skype for Business.</span></span> <span data-ttu-id="41c04-106">En el informe, también se incluye el número de sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="41c04-106">The report also includes the number of peer-to-peer sessions.</span></span>

> <span data-ttu-id="41c04-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="41c04-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="41c04-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="41c04-108">Permissions</span></span>

<span data-ttu-id="41c04-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="41c04-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="41c04-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41c04-111">Permission type</span></span>                        | <span data-ttu-id="41c04-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41c04-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="41c04-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41c04-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="41c04-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="41c04-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="41c04-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41c04-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="41c04-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41c04-116">Not supported.</span></span>                           |
| <span data-ttu-id="41c04-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41c04-117">Application</span></span>                            | <span data-ttu-id="41c04-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="41c04-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="41c04-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41c04-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="41c04-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="41c04-120">Function parameters</span></span>

<span data-ttu-id="41c04-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="41c04-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="41c04-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="41c04-122">Parameter</span></span> | <span data-ttu-id="41c04-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="41c04-123">Type</span></span>   | <span data-ttu-id="41c04-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="41c04-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="41c04-125">period</span><span class="sxs-lookup"><span data-stu-id="41c04-125">period</span></span>    | <span data-ttu-id="41c04-126">cadena</span><span class="sxs-lookup"><span data-stu-id="41c04-126">string</span></span> | <span data-ttu-id="41c04-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="41c04-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="41c04-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="41c04-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="41c04-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="41c04-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="41c04-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="41c04-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="41c04-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41c04-131">Request headers</span></span>

| <span data-ttu-id="41c04-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="41c04-132">Name</span></span>          | <span data-ttu-id="41c04-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="41c04-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="41c04-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="41c04-134">Authorization</span></span> | <span data-ttu-id="41c04-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41c04-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="41c04-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="41c04-137">If-None-Match</span></span> | <span data-ttu-id="41c04-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="41c04-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="41c04-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="41c04-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="41c04-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c04-140">Response</span></span>

<span data-ttu-id="41c04-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="41c04-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="41c04-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41c04-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="41c04-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="41c04-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="41c04-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="41c04-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="41c04-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="41c04-145">Report Refresh Date</span></span>
- <span data-ttu-id="41c04-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="41c04-146">Report Date</span></span>
- <span data-ttu-id="41c04-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="41c04-147">Report Period</span></span>
- <span data-ttu-id="41c04-148">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="41c04-148">Peer-to-peer</span></span>
- <span data-ttu-id="41c04-149">Organizado</span><span class="sxs-lookup"><span data-stu-id="41c04-149">Organized</span></span>
- <span data-ttu-id="41c04-150">Participado</span><span class="sxs-lookup"><span data-stu-id="41c04-150">Participated</span></span>

## <a name="example"></a><span data-ttu-id="41c04-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41c04-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="41c04-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41c04-152">Request</span></span>

<span data-ttu-id="41c04-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41c04-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="41c04-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c04-154">Response</span></span>

<span data-ttu-id="41c04-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41c04-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="41c04-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="41c04-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,Peer-to-peer,Organized,Participated
```
