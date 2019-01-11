---
title: 'reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts'
description: Obtiene el número de usuarios que usan dispositivos únicos en la organización. En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.
localization_priority: Normal
ms.openlocfilehash: e8c9fcb5bf61dfcb1731db823c1c0a4f1521f93a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831034"
---
# <a name="reportroot-getskypeforbusinessdeviceusagedistributionusercounts"></a><span data-ttu-id="cd4db-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="cd4db-104">reportRoot: getSkypeForBusinessDeviceUsageDistributionUserCounts</span></span>

<span data-ttu-id="cd4db-105">Obtiene el número de usuarios que usan dispositivos únicos en la organización.</span><span class="sxs-lookup"><span data-stu-id="cd4db-105">Get the number of users using unique devices in your organization.</span></span> <span data-ttu-id="cd4db-106">En el informe, se mostrará el número de usuarios por dispositivo, como Windows, teléfonos Windows, teléfonos Android, iPhone y iPad.</span><span class="sxs-lookup"><span data-stu-id="cd4db-106">The report will show you the number of users per device including Windows, Windows phone, Android phone, iPhone, and iPad.</span></span>

> <span data-ttu-id="cd4db-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="cd4db-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="cd4db-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd4db-108">Permissions</span></span>

<span data-ttu-id="cd4db-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd4db-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="cd4db-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd4db-111">Permission type</span></span>                        | <span data-ttu-id="cd4db-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd4db-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="cd4db-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd4db-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="cd4db-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="cd4db-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="cd4db-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd4db-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd4db-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cd4db-116">Not supported.</span></span>                           |
| <span data-ttu-id="cd4db-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd4db-117">Application</span></span>                            | <span data-ttu-id="cd4db-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="cd4db-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="cd4db-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd4db-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="cd4db-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="cd4db-120">Function parameters</span></span>

<span data-ttu-id="cd4db-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="cd4db-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="cd4db-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="cd4db-122">Parameter</span></span> | <span data-ttu-id="cd4db-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd4db-123">Type</span></span>   | <span data-ttu-id="cd4db-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd4db-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="cd4db-125">period</span><span class="sxs-lookup"><span data-stu-id="cd4db-125">period</span></span>    | <span data-ttu-id="cd4db-126">cadena</span><span class="sxs-lookup"><span data-stu-id="cd4db-126">string</span></span> | <span data-ttu-id="cd4db-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="cd4db-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="cd4db-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="cd4db-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="cd4db-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="cd4db-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="cd4db-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="cd4db-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="cd4db-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd4db-131">Request headers</span></span>

| <span data-ttu-id="cd4db-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd4db-132">Name</span></span>          | <span data-ttu-id="cd4db-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd4db-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="cd4db-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="cd4db-134">Authorization</span></span> | <span data-ttu-id="cd4db-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cd4db-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="cd4db-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="cd4db-137">If-None-Match</span></span> | <span data-ttu-id="cd4db-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="cd4db-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="cd4db-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cd4db-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="cd4db-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd4db-140">Response</span></span>

<span data-ttu-id="cd4db-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="cd4db-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="cd4db-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd4db-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="cd4db-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="cd4db-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="cd4db-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="cd4db-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="cd4db-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="cd4db-145">Report Refresh Date</span></span>
- <span data-ttu-id="cd4db-146">Windows</span><span class="sxs-lookup"><span data-stu-id="cd4db-146">Windows</span></span>
- <span data-ttu-id="cd4db-147">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="cd4db-147">Windows Phone</span></span>
- <span data-ttu-id="cd4db-148">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="cd4db-148">Android Phone</span></span>
- <span data-ttu-id="cd4db-149">iPhone</span><span class="sxs-lookup"><span data-stu-id="cd4db-149">iPhone</span></span>
- <span data-ttu-id="cd4db-150">iPad</span><span class="sxs-lookup"><span data-stu-id="cd4db-150">iPad</span></span>
- <span data-ttu-id="cd4db-151">Período del informe</span><span class="sxs-lookup"><span data-stu-id="cd4db-151">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="cd4db-152">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd4db-152">Example</span></span>

#### <a name="request"></a><span data-ttu-id="cd4db-153">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd4db-153">Request</span></span>

<span data-ttu-id="cd4db-154">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cd4db-154">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessdeviceusagedistributionusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessDeviceUsageDistributionUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="cd4db-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd4db-155">Response</span></span>

<span data-ttu-id="cd4db-156">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd4db-156">The following is an example of the response.</span></span>

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

<span data-ttu-id="cd4db-157">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="cd4db-157">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Period
```
