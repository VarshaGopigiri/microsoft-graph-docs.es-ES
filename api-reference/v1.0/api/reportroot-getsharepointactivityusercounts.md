---
title: 'reportRoot: getSharePointActivityUserCounts'
description: Obtiene la tendencia del número de usuarios activos. Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado.
localization_priority: Normal
ms.openlocfilehash: 369083472795194f2110f4e94fd02d5ab40b5feb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846161"
---
# <a name="reportroot-getsharepointactivityusercounts"></a><span data-ttu-id="7a6af-104">reportRoot: getSharePointActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="7a6af-104">reportRoot: getSharePointActivityUserCounts</span></span>

<span data-ttu-id="7a6af-105">Obtiene la tendencia del número de usuarios activos.</span><span class="sxs-lookup"><span data-stu-id="7a6af-105">Get the trend in the number of active users.</span></span> <span data-ttu-id="7a6af-106">Un usuario se considera activo si ejecutó una actividad de archivos (guardar, sincronizar, modificar o compartir), o bien si visitó una página dentro del período de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="7a6af-106">A user is considered active if he or she has executed a file activity (save, sync, modify, or share) or visited a page within the specified time period.</span></span>

> <span data-ttu-id="7a6af-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de SharePoint](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span><span class="sxs-lookup"><span data-stu-id="7a6af-107">**Note:** For details about different report views and names, see [Office 365 Reports - SharePoint activity](https://support.office.com/client/SharePoint-activity-a91c958f-1279-499d-9959-12f0de08dc8f).</span></span>

## <a name="permissions"></a><span data-ttu-id="7a6af-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="7a6af-108">Permissions</span></span>

<span data-ttu-id="7a6af-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7a6af-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="7a6af-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7a6af-111">Permission type</span></span>                        | <span data-ttu-id="7a6af-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7a6af-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="7a6af-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7a6af-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="7a6af-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a6af-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="7a6af-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7a6af-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7a6af-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7a6af-116">Not supported.</span></span>                           |
| <span data-ttu-id="7a6af-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7a6af-117">Application</span></span>                            | <span data-ttu-id="7a6af-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="7a6af-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="7a6af-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7a6af-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSharePointActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="7a6af-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="7a6af-120">Function parameters</span></span>

<span data-ttu-id="7a6af-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="7a6af-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="7a6af-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7a6af-122">Parameter</span></span> | <span data-ttu-id="7a6af-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a6af-123">Type</span></span>   | <span data-ttu-id="7a6af-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a6af-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="7a6af-125">period</span><span class="sxs-lookup"><span data-stu-id="7a6af-125">period</span></span>    | <span data-ttu-id="7a6af-126">cadena</span><span class="sxs-lookup"><span data-stu-id="7a6af-126">string</span></span> | <span data-ttu-id="7a6af-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a6af-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="7a6af-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="7a6af-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="7a6af-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="7a6af-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="7a6af-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="7a6af-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="7a6af-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7a6af-131">Request headers</span></span>

| <span data-ttu-id="7a6af-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a6af-132">Name</span></span>          | <span data-ttu-id="7a6af-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a6af-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="7a6af-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="7a6af-134">Authorization</span></span> | <span data-ttu-id="7a6af-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7a6af-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="7a6af-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="7a6af-137">If-None-Match</span></span> | <span data-ttu-id="7a6af-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="7a6af-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="7a6af-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7a6af-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="7a6af-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a6af-140">Response</span></span>

<span data-ttu-id="7a6af-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="7a6af-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="7a6af-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a6af-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="7a6af-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="7a6af-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="7a6af-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="7a6af-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="7a6af-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="7a6af-145">Report Refresh Date</span></span>
- <span data-ttu-id="7a6af-146">Página visitada</span><span class="sxs-lookup"><span data-stu-id="7a6af-146">Visited Page</span></span>
- <span data-ttu-id="7a6af-147">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="7a6af-147">Viewed Or Edited</span></span>
- <span data-ttu-id="7a6af-148">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="7a6af-148">Synced</span></span>
- <span data-ttu-id="7a6af-149">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="7a6af-149">Shared Internally</span></span>
- <span data-ttu-id="7a6af-150">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="7a6af-150">Shared Externally</span></span>
- <span data-ttu-id="7a6af-151">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="7a6af-151">Report Date</span></span>
- <span data-ttu-id="7a6af-152">Período del informe</span><span class="sxs-lookup"><span data-stu-id="7a6af-152">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="7a6af-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7a6af-153">Example</span></span>

#### <a name="request"></a><span data-ttu-id="7a6af-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7a6af-154">Request</span></span>

<span data-ttu-id="7a6af-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a6af-155">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getsharepointactivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSharePointActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="7a6af-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7a6af-156">Response</span></span>

<span data-ttu-id="7a6af-157">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a6af-157">The following is an example of the response.</span></span>

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

<span data-ttu-id="7a6af-158">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a6af-158">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Visited Page,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```
