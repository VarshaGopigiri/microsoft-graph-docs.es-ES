---
title: 'reportRoot: getOneDriveActivityFileCounts'
description: Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 247df845ac174f58bfd12fd401d3442ff93dd6af
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980408"
---
# <a name="reportroot-getonedriveactivityfilecounts"></a><span data-ttu-id="c4033-103">reportRoot: getOneDriveActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="c4033-103">reportRoot: getOneDriveActivityFileCounts</span></span>

<span data-ttu-id="c4033-104">Obtiene el número de usuarios con licencia únicos que realizaron interacciones con archivos en una cuenta de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="c4033-104">Get the number of unique, licensed users that performed file interactions against any OneDrive account.</span></span>

> <span data-ttu-id="c4033-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="c4033-105">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="c4033-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c4033-106">Permissions</span></span>

<span data-ttu-id="c4033-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4033-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c4033-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4033-109">Permission type</span></span>                        | <span data-ttu-id="c4033-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4033-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c4033-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4033-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="c4033-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c4033-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c4033-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4033-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c4033-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4033-114">Not supported.</span></span>                           |
| <span data-ttu-id="c4033-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4033-115">Application</span></span>                            | <span data-ttu-id="c4033-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c4033-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c4033-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4033-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOneDriveActivityFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="c4033-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="c4033-118">Function parameters</span></span>

<span data-ttu-id="c4033-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c4033-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c4033-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c4033-120">Parameter</span></span> | <span data-ttu-id="c4033-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4033-121">Type</span></span>   | <span data-ttu-id="c4033-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4033-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c4033-123">period</span><span class="sxs-lookup"><span data-stu-id="c4033-123">period</span></span>    | <span data-ttu-id="c4033-124">cadena</span><span class="sxs-lookup"><span data-stu-id="c4033-124">string</span></span> | <span data-ttu-id="c4033-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c4033-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c4033-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c4033-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c4033-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c4033-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c4033-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="c4033-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c4033-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4033-129">Request headers</span></span>

| <span data-ttu-id="c4033-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="c4033-130">Name</span></span>          | <span data-ttu-id="c4033-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4033-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="c4033-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="c4033-132">Authorization</span></span> | <span data-ttu-id="c4033-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4033-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="c4033-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="c4033-135">If-None-Match</span></span> | <span data-ttu-id="c4033-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="c4033-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="c4033-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c4033-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="c4033-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4033-138">Response</span></span>

<span data-ttu-id="c4033-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c4033-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c4033-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4033-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c4033-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c4033-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c4033-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c4033-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c4033-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c4033-143">Report Refresh Date</span></span>
- <span data-ttu-id="c4033-144">Visto o editado</span><span class="sxs-lookup"><span data-stu-id="c4033-144">Viewed Or Edited</span></span>
- <span data-ttu-id="c4033-145">Sincronizado</span><span class="sxs-lookup"><span data-stu-id="c4033-145">Synced</span></span>
- <span data-ttu-id="c4033-146">Compartido internamente</span><span class="sxs-lookup"><span data-stu-id="c4033-146">Shared Internally</span></span>
- <span data-ttu-id="c4033-147">Compartido externamente</span><span class="sxs-lookup"><span data-stu-id="c4033-147">Shared Externally</span></span>
- <span data-ttu-id="c4033-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="c4033-148">Report Date</span></span>
- <span data-ttu-id="c4033-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c4033-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="c4033-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4033-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c4033-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4033-151">Request</span></span>

<span data-ttu-id="c4033-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4033-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveactivityfilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveActivityFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="c4033-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4033-153">Response</span></span>

<span data-ttu-id="c4033-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4033-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="c4033-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c4033-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Viewed Or Edited,Synced,Shared Internally,Shared Externally,Report Date,Report Period
```
