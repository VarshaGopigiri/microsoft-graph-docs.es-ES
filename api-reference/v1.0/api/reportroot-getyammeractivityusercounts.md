---
title: 'reportRoot: getYammerActivityUserCounts'
description: Obtiene las tendencias sobre el número de usuarios únicos que publicaron, leyeron y etiquetaron como “Me gusta” mensajes de Yammer.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: bd49374f339034dfa9c43f5cca7299287b40ffd1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27956167"
---
# <a name="reportroot-getyammeractivityusercounts"></a><span data-ttu-id="592fd-103">reportRoot: getYammerActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="592fd-103">reportRoot: getYammerActivityUserCounts</span></span>

<span data-ttu-id="592fd-104">Obtiene las tendencias sobre el número de usuarios únicos que publicaron, leyeron y etiquetaron como “Me gusta” mensajes de Yammer.</span><span class="sxs-lookup"><span data-stu-id="592fd-104">Get the trends on the number of unique users who posted, read, and liked Yammer messages.</span></span>

> <span data-ttu-id="592fd-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Yammer](https://support.office.com/client/Yammer-activity-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a).</span><span class="sxs-lookup"><span data-stu-id="592fd-105">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer Activity](https://support.office.com/client/Yammer-activity-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a).</span></span>

## <a name="permissions"></a><span data-ttu-id="592fd-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="592fd-106">Permissions</span></span>

<span data-ttu-id="592fd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="592fd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="592fd-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="592fd-109">Permission type</span></span>                        | <span data-ttu-id="592fd-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="592fd-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="592fd-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="592fd-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="592fd-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="592fd-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="592fd-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="592fd-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="592fd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="592fd-114">Not supported.</span></span>                           |
| <span data-ttu-id="592fd-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="592fd-115">Application</span></span>                            | <span data-ttu-id="592fd-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="592fd-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="592fd-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="592fd-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="592fd-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="592fd-118">Function parameters</span></span>

<span data-ttu-id="592fd-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="592fd-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="592fd-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="592fd-120">Parameter</span></span> | <span data-ttu-id="592fd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="592fd-121">Type</span></span>   | <span data-ttu-id="592fd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="592fd-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="592fd-123">period</span><span class="sxs-lookup"><span data-stu-id="592fd-123">period</span></span>    | <span data-ttu-id="592fd-124">cadena</span><span class="sxs-lookup"><span data-stu-id="592fd-124">string</span></span> | <span data-ttu-id="592fd-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="592fd-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="592fd-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="592fd-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="592fd-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="592fd-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="592fd-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="592fd-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="592fd-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="592fd-129">Request headers</span></span>

| <span data-ttu-id="592fd-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="592fd-130">Name</span></span>          | <span data-ttu-id="592fd-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="592fd-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="592fd-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="592fd-132">Authorization</span></span> | <span data-ttu-id="592fd-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="592fd-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="592fd-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="592fd-135">If-None-Match</span></span> | <span data-ttu-id="592fd-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="592fd-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="592fd-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="592fd-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="592fd-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="592fd-138">Response</span></span>

<span data-ttu-id="592fd-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="592fd-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="592fd-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="592fd-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="592fd-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="592fd-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="592fd-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="592fd-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="592fd-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="592fd-143">Report Refresh Date</span></span>
- <span data-ttu-id="592fd-144">Etiquetado como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="592fd-144">Liked</span></span>
- <span data-ttu-id="592fd-145">Publicado</span><span class="sxs-lookup"><span data-stu-id="592fd-145">Posted</span></span>
- <span data-ttu-id="592fd-146">Leído</span><span class="sxs-lookup"><span data-stu-id="592fd-146">Read</span></span>
- <span data-ttu-id="592fd-147">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="592fd-147">Report Date</span></span>
- <span data-ttu-id="592fd-148">Período del informe</span><span class="sxs-lookup"><span data-stu-id="592fd-148">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="592fd-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="592fd-149">Example</span></span>

#### <a name="request"></a><span data-ttu-id="592fd-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="592fd-150">Request</span></span>

<span data-ttu-id="592fd-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="592fd-151">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammeractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="592fd-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="592fd-152">Response</span></span>

<span data-ttu-id="592fd-153">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="592fd-153">The following is an example of the response.</span></span>

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

<span data-ttu-id="592fd-154">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="592fd-154">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Liked,Posted,Read,Report Date,Report Period
```
