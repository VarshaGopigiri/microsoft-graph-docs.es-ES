---
title: 'reportRoot: getEmailAppUsageVersionsUserCounts'
description: Obtiene el número de usuarios únicos por versión de escritorio de Outlook.
ms.openlocfilehash: 730bae521523f51a3ab41c1d480439fd4bc4a305
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031354"
---
# <a name="reportroot-getemailappusageversionsusercounts"></a><span data-ttu-id="873f1-103">reportRoot: getEmailAppUsageVersionsUserCounts</span><span class="sxs-lookup"><span data-stu-id="873f1-103">reportRoot: getEmailAppUsageVersionsUserCounts</span></span>

<span data-ttu-id="873f1-104">Obtiene el número de usuarios únicos por versión de escritorio de Outlook.</span><span class="sxs-lookup"><span data-stu-id="873f1-104">Get the count of unique users by Outlook desktop version.</span></span>

> <span data-ttu-id="873f1-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de aplicaciones de correo electrónico](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span><span class="sxs-lookup"><span data-stu-id="873f1-105">**Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).</span></span>

## <a name="permissions"></a><span data-ttu-id="873f1-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="873f1-106">Permissions</span></span>

<span data-ttu-id="873f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="873f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="873f1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="873f1-109">Permission type</span></span>                        | <span data-ttu-id="873f1-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="873f1-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="873f1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="873f1-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="873f1-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="873f1-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="873f1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="873f1-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="873f1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="873f1-114">Not supported.</span></span>                           |
| <span data-ttu-id="873f1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="873f1-115">Application</span></span>                            | <span data-ttu-id="873f1-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="873f1-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="873f1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="873f1-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageVersionsUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="873f1-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="873f1-118">Function parameters</span></span>

<span data-ttu-id="873f1-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="873f1-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="873f1-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="873f1-120">Parameter</span></span> | <span data-ttu-id="873f1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="873f1-121">Type</span></span>   | <span data-ttu-id="873f1-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="873f1-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="873f1-123">period</span><span class="sxs-lookup"><span data-stu-id="873f1-123">period</span></span>    | <span data-ttu-id="873f1-124">cadena</span><span class="sxs-lookup"><span data-stu-id="873f1-124">string</span></span> | <span data-ttu-id="873f1-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="873f1-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="873f1-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="873f1-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="873f1-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="873f1-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="873f1-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="873f1-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="873f1-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="873f1-129">Request headers</span></span>

| <span data-ttu-id="873f1-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="873f1-130">Name</span></span>          | <span data-ttu-id="873f1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="873f1-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="873f1-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="873f1-132">Authorization</span></span> | <span data-ttu-id="873f1-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="873f1-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="873f1-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="873f1-135">If-None-Match</span></span> | <span data-ttu-id="873f1-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="873f1-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="873f1-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="873f1-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="873f1-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="873f1-138">Response</span></span>

<span data-ttu-id="873f1-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="873f1-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="873f1-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="873f1-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="873f1-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="873f1-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="873f1-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="873f1-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="873f1-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="873f1-143">Report Refresh Date</span></span>
- <span data-ttu-id="873f1-144">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="873f1-144">Outlook 2016</span></span>
- <span data-ttu-id="873f1-145">Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="873f1-145">Outlook 2013</span></span>
- <span data-ttu-id="873f1-146">Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="873f1-146">Outlook 2010</span></span>
- <span data-ttu-id="873f1-147">Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="873f1-147">Outlook 2007</span></span>
- <span data-ttu-id="873f1-148">Sin determinar</span><span class="sxs-lookup"><span data-stu-id="873f1-148">Undetermined</span></span>
- <span data-ttu-id="873f1-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="873f1-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="873f1-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="873f1-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="873f1-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="873f1-151">Request</span></span>

<span data-ttu-id="873f1-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="873f1-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getemailappusageversionsusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getEmailAppUsageVersionsUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="873f1-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="873f1-153">Response</span></span>

<span data-ttu-id="873f1-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="873f1-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="873f1-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="873f1-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Outlook 2016,Outlook 2013,Outlook 2010,Outlook 2007,Undetermined,Report Period
```