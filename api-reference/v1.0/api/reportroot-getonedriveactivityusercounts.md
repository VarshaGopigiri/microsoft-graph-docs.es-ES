---
title: 'reportRoot: getOneDriveActivityUserCounts'
description: Obtiene la tendencia en el número de usuarios de OneDrive activos.
ms.openlocfilehash: 53209749d0ac8de9a349e7c519cde2e054281221
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032201"
---
# <a name="reportroot-getonedriveactivityusercounts"></a><span data-ttu-id="59f9f-103">reportRoot: getOneDriveActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="59f9f-103">reportRoot: getOneDriveActivityUserCounts</span></span>

<span data-ttu-id="59f9f-104">Obtiene la tendencia en el número de usuarios de OneDrive activos.</span><span class="sxs-lookup"><span data-stu-id="59f9f-104">Get the trend in the number of active OneDrive users.</span></span>

> <span data-ttu-id="59f9f-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="59f9f-105">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="59f9f-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="59f9f-106">Permissions</span></span>

<span data-ttu-id="59f9f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="59f9f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="59f9f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59f9f-109">Permission type</span></span>                        | <span data-ttu-id="59f9f-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59f9f-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="59f9f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59f9f-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="59f9f-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="59f9f-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="59f9f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59f9f-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="59f9f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59f9f-114">Not supported.</span></span>                           |
| <span data-ttu-id="59f9f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59f9f-115">Application</span></span>                            | <span data-ttu-id="59f9f-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="59f9f-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="59f9f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59f9f-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveActivityUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="59f9f-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="59f9f-118">Function parameters</span></span>

<span data-ttu-id="59f9f-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="59f9f-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="59f9f-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="59f9f-120">Parameter</span></span> | <span data-ttu-id="59f9f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="59f9f-121">Type</span></span>   | <span data-ttu-id="59f9f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="59f9f-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="59f9f-123">period</span><span class="sxs-lookup"><span data-stu-id="59f9f-123">period</span></span>    | <span data-ttu-id="59f9f-124">cadena</span><span class="sxs-lookup"><span data-stu-id="59f9f-124">string</span></span> | <span data-ttu-id="59f9f-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="59f9f-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="59f9f-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="59f9f-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="59f9f-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="59f9f-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="59f9f-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="59f9f-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="59f9f-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59f9f-129">Request headers</span></span>

| <span data-ttu-id="59f9f-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="59f9f-130">Name</span></span>          | <span data-ttu-id="59f9f-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="59f9f-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="59f9f-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="59f9f-132">Authorization</span></span> | <span data-ttu-id="59f9f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="59f9f-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="59f9f-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="59f9f-135">If-None-Match</span></span> | <span data-ttu-id="59f9f-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="59f9f-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="59f9f-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="59f9f-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="59f9f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59f9f-138">Response</span></span>

<span data-ttu-id="59f9f-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="59f9f-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="59f9f-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59f9f-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="59f9f-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="59f9f-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="59f9f-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="59f9f-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="59f9f-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="59f9f-143">Report Refresh Date</span></span>
- <span data-ttu-id="59f9f-144">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="59f9f-144">Viewed Or Edited</span></span>
- <span data-ttu-id="59f9f-145">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="59f9f-145">Synced</span></span>
- <span data-ttu-id="59f9f-146">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="59f9f-146">Shared Internally</span></span>
- <span data-ttu-id="59f9f-147">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="59f9f-147">Shared Externally</span></span>
- <span data-ttu-id="59f9f-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="59f9f-148">Report Date</span></span>
- <span data-ttu-id="59f9f-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="59f9f-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="59f9f-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59f9f-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="59f9f-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59f9f-151">Request</span></span>

<span data-ttu-id="59f9f-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59f9f-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveactivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="59f9f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59f9f-153">Response</span></span>

<span data-ttu-id="59f9f-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59f9f-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="59f9f-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="59f9f-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```
