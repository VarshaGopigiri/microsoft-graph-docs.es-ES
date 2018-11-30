---
title: 'reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts'
description: Obtiene el número de usuarios que usan dispositivos únicos en la organización. En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.
ms.openlocfilehash: a911cc4cac8d7c6f2465f0d7f3220770ca21f351
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032246"
---
# <a name="reportroot-getskypeforbusinessdeviceusagedistributionusercounts"></a><span data-ttu-id="3d606-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="3d606-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span></span>

<span data-ttu-id="3d606-105">Obtiene el número de usuarios que usan dispositivos únicos en la organización.</span><span class="sxs-lookup"><span data-stu-id="3d606-105">Get the number of users using unique devices in your organization.</span></span> <span data-ttu-id="3d606-106">En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.</span><span class="sxs-lookup"><span data-stu-id="3d606-106">The report will show you the number of users per device including Windows, Windows phone, Android phone, iPhone, and iPad.</span></span>

> <span data-ttu-id="3d606-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="3d606-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="3d606-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="3d606-108">Permissions</span></span>

<span data-ttu-id="3d606-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3d606-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="3d606-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3d606-111">Permission type</span></span>                        | <span data-ttu-id="3d606-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3d606-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="3d606-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3d606-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="3d606-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d606-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="3d606-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3d606-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3d606-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3d606-116">Not supported.</span></span>                           |
| <span data-ttu-id="3d606-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3d606-117">Application</span></span>                            | <span data-ttu-id="3d606-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="3d606-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="3d606-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3d606-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="3d606-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="3d606-120">Function parameters</span></span>

<span data-ttu-id="3d606-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="3d606-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="3d606-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3d606-122">Parameter</span></span> | <span data-ttu-id="3d606-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d606-123">Type</span></span>   | <span data-ttu-id="3d606-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d606-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="3d606-125">period</span><span class="sxs-lookup"><span data-stu-id="3d606-125">period</span></span>    | <span data-ttu-id="3d606-126">cadena</span><span class="sxs-lookup"><span data-stu-id="3d606-126">string</span></span> | <span data-ttu-id="3d606-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d606-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="3d606-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="3d606-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="3d606-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="3d606-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="3d606-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="3d606-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="3d606-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3d606-131">Request headers</span></span>

| <span data-ttu-id="3d606-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="3d606-132">Name</span></span>          | <span data-ttu-id="3d606-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d606-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="3d606-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="3d606-134">Authorization</span></span> | <span data-ttu-id="3d606-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3d606-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="3d606-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="3d606-137">If-None-Match</span></span> | <span data-ttu-id="3d606-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="3d606-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="3d606-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d606-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="3d606-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d606-140">Response</span></span>

<span data-ttu-id="3d606-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="3d606-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="3d606-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d606-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="3d606-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="3d606-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="3d606-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="3d606-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="3d606-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="3d606-145">Report Refresh Date</span></span>
- <span data-ttu-id="3d606-146">Windows</span><span class="sxs-lookup"><span data-stu-id="3d606-146">Windows</span></span>
- <span data-ttu-id="3d606-147">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="3d606-147">Windows Phone</span></span>
- <span data-ttu-id="3d606-148">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="3d606-148">Android Phone</span></span>
- <span data-ttu-id="3d606-149">iPhone</span><span class="sxs-lookup"><span data-stu-id="3d606-149">iPhone</span></span>
- <span data-ttu-id="3d606-150">iPad</span><span class="sxs-lookup"><span data-stu-id="3d606-150">iPad</span></span>
- <span data-ttu-id="3d606-151">Período del informe</span><span class="sxs-lookup"><span data-stu-id="3d606-151">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="3d606-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d606-152">Example</span></span>

#### <a name="request"></a><span data-ttu-id="3d606-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3d606-153">Request</span></span>

<span data-ttu-id="3d606-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3d606-154">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessdeviceusagedistributionusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="3d606-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3d606-155">Response</span></span>

<span data-ttu-id="3d606-156">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3d606-156">The following is an example of the response.</span></span>

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

<span data-ttu-id="3d606-157">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="3d606-157">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Period
```
