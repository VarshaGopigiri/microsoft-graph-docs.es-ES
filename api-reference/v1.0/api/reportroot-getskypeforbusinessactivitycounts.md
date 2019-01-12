---
title: 'reportRoot: getSkypeForBusinessActivityCounts'
description: Obtiene las tendencias sobre el número de usuarios que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial. En el informe, también se incluye el número de sesiones de punto a punto.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: e1a42d6612a29e8d65665174fb46defd2cb9185d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933872"
---
# <a name="reportroot-getskypeforbusinessactivitycounts"></a><span data-ttu-id="6199f-104">reportRoot: getSkypeForBusinessActivityCounts</span><span class="sxs-lookup"><span data-stu-id="6199f-104">reportRoot: getSkypeForBusinessActivityCounts</span></span>

<span data-ttu-id="6199f-105">Obtiene las tendencias sobre el número de usuarios que organizaron y participaron en sesiones de conferencia realizadas en la organización con Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="6199f-105">Get the trends on how many users organized and participated in conference sessions held in your organization through Skype for Business.</span></span> <span data-ttu-id="6199f-106">En el informe, también se incluye el número de sesiones de punto a punto.</span><span class="sxs-lookup"><span data-stu-id="6199f-106">The report also includes the number of peer-to-peer sessions.</span></span>

> <span data-ttu-id="6199f-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de Skype Empresarial](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span><span class="sxs-lookup"><span data-stu-id="6199f-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).</span></span>

## <a name="permissions"></a><span data-ttu-id="6199f-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6199f-108">Permissions</span></span>

<span data-ttu-id="6199f-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6199f-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="6199f-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6199f-111">Permission type</span></span>                        | <span data-ttu-id="6199f-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6199f-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="6199f-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6199f-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="6199f-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6199f-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="6199f-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6199f-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6199f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6199f-116">Not supported.</span></span>                           |
| <span data-ttu-id="6199f-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6199f-117">Application</span></span>                            | <span data-ttu-id="6199f-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="6199f-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="6199f-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6199f-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessActivityCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="6199f-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="6199f-120">Function parameters</span></span>

<span data-ttu-id="6199f-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="6199f-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="6199f-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6199f-122">Parameter</span></span> | <span data-ttu-id="6199f-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="6199f-123">Type</span></span>   | <span data-ttu-id="6199f-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6199f-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="6199f-125">period</span><span class="sxs-lookup"><span data-stu-id="6199f-125">period</span></span>    | <span data-ttu-id="6199f-126">cadena</span><span class="sxs-lookup"><span data-stu-id="6199f-126">string</span></span> | <span data-ttu-id="6199f-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6199f-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="6199f-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="6199f-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="6199f-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="6199f-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="6199f-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6199f-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="6199f-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6199f-131">Request headers</span></span>

| <span data-ttu-id="6199f-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="6199f-132">Name</span></span>          | <span data-ttu-id="6199f-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="6199f-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="6199f-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="6199f-134">Authorization</span></span> | <span data-ttu-id="6199f-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6199f-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="6199f-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="6199f-137">If-None-Match</span></span> | <span data-ttu-id="6199f-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="6199f-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="6199f-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6199f-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="6199f-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6199f-140">Response</span></span>

<span data-ttu-id="6199f-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="6199f-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="6199f-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6199f-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="6199f-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="6199f-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="6199f-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="6199f-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="6199f-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="6199f-145">Report Refresh Date</span></span>
- <span data-ttu-id="6199f-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="6199f-146">Report Date</span></span>
- <span data-ttu-id="6199f-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="6199f-147">Report Period</span></span>
- <span data-ttu-id="6199f-148">Punto a punto</span><span class="sxs-lookup"><span data-stu-id="6199f-148">Peer-to-peer</span></span>
- <span data-ttu-id="6199f-149">Organizado</span><span class="sxs-lookup"><span data-stu-id="6199f-149">Organized</span></span>
- <span data-ttu-id="6199f-150">Participado</span><span class="sxs-lookup"><span data-stu-id="6199f-150">Participated</span></span>

## <a name="example"></a><span data-ttu-id="6199f-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6199f-151">Example</span></span>

#### <a name="request"></a><span data-ttu-id="6199f-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6199f-152">Request</span></span>

<span data-ttu-id="6199f-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6199f-153">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessactivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="6199f-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6199f-154">Response</span></span>

<span data-ttu-id="6199f-155">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6199f-155">The following is an example of the response.</span></span>

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

<span data-ttu-id="6199f-156">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="6199f-156">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Report Period,Peer-to-peer,Organized,Participated
```
