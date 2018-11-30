---
title: 'reportRoot: getOffice365GroupsActivityFileCounts'
description: Obtiene el número total de archivos y cuántos estaban activos en todos los sitios de grupo asociados con un grupo de Office 365.
ms.openlocfilehash: 33050098ef970894ec08a1c264848b2bd92128c1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029330"
---
# <a name="reportroot-getoffice365groupsactivityfilecounts"></a><span data-ttu-id="bc02e-103">reportRoot: getOffice365GroupsActivityFileCounts</span><span class="sxs-lookup"><span data-stu-id="bc02e-103">reportRoot: getOffice365GroupsActivityFileCounts</span></span>

<span data-ttu-id="bc02e-104">Obtiene el número total de archivos y cuántos estaban activos en todos los sitios de grupo asociados con un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc02e-104">Get the total number of files and how many of them were active across all group sites associated with an Office 365 Group.</span></span>

> <span data-ttu-id="bc02e-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="bc02e-105">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="bc02e-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="bc02e-106">Permissions</span></span>

<span data-ttu-id="bc02e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bc02e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="bc02e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bc02e-109">Permission type</span></span>                        | <span data-ttu-id="bc02e-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bc02e-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="bc02e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bc02e-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="bc02e-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bc02e-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="bc02e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bc02e-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bc02e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bc02e-114">Not supported.</span></span>                           |
| <span data-ttu-id="bc02e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bc02e-115">Application</span></span>                            | <span data-ttu-id="bc02e-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="bc02e-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="bc02e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc02e-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365GroupsActivityFileCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="bc02e-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="bc02e-118">Function parameters</span></span>

<span data-ttu-id="bc02e-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="bc02e-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="bc02e-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bc02e-120">Parameter</span></span> | <span data-ttu-id="bc02e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc02e-121">Type</span></span>   | <span data-ttu-id="bc02e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc02e-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="bc02e-123">period</span><span class="sxs-lookup"><span data-stu-id="bc02e-123">period</span></span>    | <span data-ttu-id="bc02e-124">cadena</span><span class="sxs-lookup"><span data-stu-id="bc02e-124">string</span></span> | <span data-ttu-id="bc02e-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bc02e-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="bc02e-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="bc02e-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="bc02e-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="bc02e-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="bc02e-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="bc02e-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="bc02e-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc02e-129">Request headers</span></span>

| <span data-ttu-id="bc02e-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc02e-130">Name</span></span>          | <span data-ttu-id="bc02e-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc02e-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="bc02e-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc02e-132">Authorization</span></span> | <span data-ttu-id="bc02e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc02e-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="bc02e-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="bc02e-135">If-None-Match</span></span> | <span data-ttu-id="bc02e-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="bc02e-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="bc02e-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc02e-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="bc02e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc02e-138">Response</span></span>

<span data-ttu-id="bc02e-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="bc02e-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="bc02e-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc02e-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="bc02e-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="bc02e-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="bc02e-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="bc02e-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="bc02e-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="bc02e-143">Report Refresh Date</span></span>
- <span data-ttu-id="bc02e-144">Total</span><span class="sxs-lookup"><span data-stu-id="bc02e-144">Total</span></span>
- <span data-ttu-id="bc02e-145">Activo</span><span class="sxs-lookup"><span data-stu-id="bc02e-145">Active</span></span>
- <span data-ttu-id="bc02e-146">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="bc02e-146">Report Date</span></span>
- <span data-ttu-id="bc02e-147">Período del informe</span><span class="sxs-lookup"><span data-stu-id="bc02e-147">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="bc02e-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc02e-148">Example</span></span>

#### <a name="request"></a><span data-ttu-id="bc02e-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc02e-149">Request</span></span>

<span data-ttu-id="bc02e-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc02e-150">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365groupsactivityfilecounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityFileCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="bc02e-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc02e-151">Response</span></span>

<span data-ttu-id="bc02e-152">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc02e-152">The following is an example of the response.</span></span>

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

<span data-ttu-id="bc02e-153">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc02e-153">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```