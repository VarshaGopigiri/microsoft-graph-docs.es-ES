---
title: 'reportRoot: getTeamsDeviceUsageDistributionUserCounts'
description: Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.
ms.openlocfilehash: 135a3439d2e92ef28c7dbbdc6227035c2755e3ff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030566"
---
# <a name="reportroot-getteamsdeviceusagedistributionusercounts"></a><span data-ttu-id="2fefb-103">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="2fefb-103">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span></span>

<span data-ttu-id="2fefb-104">Obtenga el número de usuarios únicos de Microsoft Teams por tipo de dispositivo durante el período de tiempo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2fefb-104">Get the number of Microsoft Teams unique users by device type over the selected time period.</span></span>

## <a name="permissions"></a><span data-ttu-id="2fefb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2fefb-105">Permissions</span></span>

<span data-ttu-id="2fefb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2fefb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="2fefb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2fefb-108">Permission type</span></span>                        | <span data-ttu-id="2fefb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2fefb-109">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="2fefb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2fefb-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="2fefb-111">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2fefb-111">Reports.Read.All</span></span>                         |
| <span data-ttu-id="2fefb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2fefb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2fefb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2fefb-113">Not supported.</span></span>                           |
| <span data-ttu-id="2fefb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2fefb-114">Application</span></span>                            | <span data-ttu-id="2fefb-115">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="2fefb-115">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="2fefb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2fefb-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="2fefb-117">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="2fefb-117">Function parameters</span></span>

<span data-ttu-id="2fefb-118">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="2fefb-118">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="2fefb-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2fefb-119">Parameter</span></span> | <span data-ttu-id="2fefb-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="2fefb-120">Type</span></span>   | <span data-ttu-id="2fefb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fefb-121">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="2fefb-122">period</span><span class="sxs-lookup"><span data-stu-id="2fefb-122">period</span></span>    | <span data-ttu-id="2fefb-123">cadena</span><span class="sxs-lookup"><span data-stu-id="2fefb-123">string</span></span> | <span data-ttu-id="2fefb-124">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2fefb-124">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="2fefb-125">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="2fefb-125">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="2fefb-126">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="2fefb-126">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="2fefb-127">Necesario.</span><span class="sxs-lookup"><span data-stu-id="2fefb-127">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="2fefb-128">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2fefb-128">Request headers</span></span>

| <span data-ttu-id="2fefb-129">Nombre</span><span class="sxs-lookup"><span data-stu-id="2fefb-129">Name</span></span>          | <span data-ttu-id="2fefb-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fefb-130">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="2fefb-131">Authorization</span><span class="sxs-lookup"><span data-stu-id="2fefb-131">Authorization</span></span> | <span data-ttu-id="2fefb-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2fefb-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="2fefb-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fefb-134">Response</span></span>

<span data-ttu-id="2fefb-135">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="2fefb-135">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="2fefb-136">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2fefb-136">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="2fefb-137">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="2fefb-137">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="2fefb-138">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="2fefb-138">The CSV file has the following headers for columns:</span></span>

- <span data-ttu-id="2fefb-139">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="2fefb-139">Report Refresh Date</span></span>
- <span data-ttu-id="2fefb-140">Web</span><span class="sxs-lookup"><span data-stu-id="2fefb-140">Web</span></span>
- <span data-ttu-id="2fefb-141">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="2fefb-141">Windows Phone</span></span>
- <span data-ttu-id="2fefb-142">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="2fefb-142">Android Phone</span></span>
- <span data-ttu-id="2fefb-143">iOS</span><span class="sxs-lookup"><span data-stu-id="2fefb-143">iOS</span></span>
- <span data-ttu-id="2fefb-144">Mac</span><span class="sxs-lookup"><span data-stu-id="2fefb-144">Mac</span></span>
- <span data-ttu-id="2fefb-145">Windows</span><span class="sxs-lookup"><span data-stu-id="2fefb-145">Windows</span></span>
- <span data-ttu-id="2fefb-146">Período del informe</span><span class="sxs-lookup"><span data-stu-id="2fefb-146">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="2fefb-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2fefb-147">Example</span></span>

#### <a name="request"></a><span data-ttu-id="2fefb-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2fefb-148">Request</span></span>

<span data-ttu-id="2fefb-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2fefb-149">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="2fefb-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2fefb-150">Response</span></span>

<span data-ttu-id="2fefb-151">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2fefb-151">The following is an example of the response.</span></span>

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

<span data-ttu-id="2fefb-152">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="2fefb-152">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Period
```
