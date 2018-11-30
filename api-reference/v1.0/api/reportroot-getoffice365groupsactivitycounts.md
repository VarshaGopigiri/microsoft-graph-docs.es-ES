---
title: 'reportRoot: getOffice365GroupsActivityCounts'
description: Obtiene el número de actividades de grupo en cargas de trabajo en grupo.
ms.openlocfilehash: 02bb861dbd26981d0d9190a3d82f2693f4ad3752
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029900"
---
# <a name="reportroot-getoffice365groupsactivitycounts"></a><span data-ttu-id="a8c24-103">reportRoot: getOffice365GroupsActivityCounts</span><span class="sxs-lookup"><span data-stu-id="a8c24-103">reportRoot: getOffice365GroupsActivityCounts</span></span>

<span data-ttu-id="a8c24-104">Obtiene el número de actividades de grupo en cargas de trabajo en grupo.</span><span class="sxs-lookup"><span data-stu-id="a8c24-104">Get the number of group activities across group workloads.</span></span>

> <span data-ttu-id="a8c24-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="a8c24-105">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="a8c24-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="a8c24-106">Permissions</span></span>

<span data-ttu-id="a8c24-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a8c24-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="a8c24-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a8c24-109">Permission type</span></span>                        | <span data-ttu-id="a8c24-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a8c24-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="a8c24-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a8c24-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="a8c24-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="a8c24-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="a8c24-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a8c24-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a8c24-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a8c24-114">Not supported.</span></span>                           |
| <span data-ttu-id="a8c24-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a8c24-115">Application</span></span>                            | <span data-ttu-id="a8c24-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="a8c24-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="a8c24-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a8c24-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="a8c24-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="a8c24-118">Function parameters</span></span>

<span data-ttu-id="a8c24-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="a8c24-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="a8c24-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a8c24-120">Parameter</span></span> | <span data-ttu-id="a8c24-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8c24-121">Type</span></span>   | <span data-ttu-id="a8c24-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c24-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="a8c24-123">period</span><span class="sxs-lookup"><span data-stu-id="a8c24-123">period</span></span>    | <span data-ttu-id="a8c24-124">cadena</span><span class="sxs-lookup"><span data-stu-id="a8c24-124">string</span></span> | <span data-ttu-id="a8c24-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="a8c24-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="a8c24-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="a8c24-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="a8c24-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="a8c24-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="a8c24-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="a8c24-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="a8c24-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a8c24-129">Request headers</span></span>

| <span data-ttu-id="a8c24-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8c24-130">Name</span></span>          | <span data-ttu-id="a8c24-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8c24-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="a8c24-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="a8c24-132">Authorization</span></span> | <span data-ttu-id="a8c24-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a8c24-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="a8c24-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="a8c24-135">If-None-Match</span></span> | <span data-ttu-id="a8c24-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="a8c24-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="a8c24-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8c24-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="a8c24-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8c24-138">Response</span></span>

<span data-ttu-id="a8c24-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="a8c24-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="a8c24-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8c24-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="a8c24-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="a8c24-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="a8c24-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="a8c24-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="a8c24-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="a8c24-143">Report Refresh Date</span></span>
- <span data-ttu-id="a8c24-144">Correos electrónicos de Exchange recibidos</span><span class="sxs-lookup"><span data-stu-id="a8c24-144">Exchange Emails Received</span></span>
- <span data-ttu-id="a8c24-145">Mensajes de Yammer publicados</span><span class="sxs-lookup"><span data-stu-id="a8c24-145">Yammer Messages Posted</span></span>
- <span data-ttu-id="a8c24-146">Mensajes de Yammer leídos</span><span class="sxs-lookup"><span data-stu-id="a8c24-146">Yammer Messages Read</span></span>
- <span data-ttu-id="a8c24-147">Mensajes de Yammer etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="a8c24-147">Yammer Messages Liked</span></span>
- <span data-ttu-id="a8c24-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="a8c24-148">Report Date</span></span>
- <span data-ttu-id="a8c24-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="a8c24-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="a8c24-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a8c24-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="a8c24-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a8c24-151">Request</span></span>

<span data-ttu-id="a8c24-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a8c24-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365groupsactivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="a8c24-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a8c24-153">Response</span></span>

<span data-ttu-id="a8c24-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a8c24-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="a8c24-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="a8c24-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Exchange Emails Received,Yammer Messages Posted,Yammer Messages Read,Yammer Messages Liked,Report Date,Report Period
```
