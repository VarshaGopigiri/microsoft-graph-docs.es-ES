---
title: 'reportRoot: getOffice365ServicesUserCounts'
description: Obtiene el número de usuarios por tipo de actividad y servicio.
ms.openlocfilehash: ce594cc38ba62d70ee0a849342a6c2add0b3e602
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031047"
---
# <a name="reportroot-getoffice365servicesusercounts"></a><span data-ttu-id="c9bc3-103">reportRoot: getOffice365ServicesUserCounts</span><span class="sxs-lookup"><span data-stu-id="c9bc3-103">reportRoot: getOffice365ServicesUserCounts</span></span>

<span data-ttu-id="c9bc3-104">Obtiene el número de usuarios por tipo de actividad y servicio.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-104">Get the count of users by activity type and service.</span></span>

> <span data-ttu-id="c9bc3-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="c9bc3-105">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="c9bc3-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="c9bc3-106">Permissions</span></span>

<span data-ttu-id="c9bc3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c9bc3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="c9bc3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c9bc3-109">Permission type</span></span>                        | <span data-ttu-id="c9bc3-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c9bc3-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="c9bc3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c9bc3-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="c9bc3-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9bc3-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="c9bc3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c9bc3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c9bc3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-114">Not supported.</span></span>                           |
| <span data-ttu-id="c9bc3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c9bc3-115">Application</span></span>                            | <span data-ttu-id="c9bc3-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="c9bc3-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="c9bc3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c9bc3-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ServicesUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="c9bc3-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="c9bc3-118">Function parameters</span></span>

<span data-ttu-id="c9bc3-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="c9bc3-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c9bc3-120">Parameter</span></span> | <span data-ttu-id="c9bc3-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-121">Type</span></span>   | <span data-ttu-id="c9bc3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9bc3-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="c9bc3-123">period</span><span class="sxs-lookup"><span data-stu-id="c9bc3-123">period</span></span>    | <span data-ttu-id="c9bc3-124">cadena</span><span class="sxs-lookup"><span data-stu-id="c9bc3-124">string</span></span> | <span data-ttu-id="c9bc3-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="c9bc3-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="c9bc3-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="c9bc3-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="c9bc3-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c9bc3-129">Request headers</span></span>

| <span data-ttu-id="c9bc3-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="c9bc3-130">Name</span></span>          | <span data-ttu-id="c9bc3-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9bc3-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="c9bc3-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="c9bc3-132">Authorization</span></span> | <span data-ttu-id="c9bc3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="c9bc3-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="c9bc3-135">If-None-Match</span></span> | <span data-ttu-id="c9bc3-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="c9bc3-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="c9bc3-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9bc3-138">Response</span></span>

<span data-ttu-id="c9bc3-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="c9bc3-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="c9bc3-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="c9bc3-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="c9bc3-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="c9bc3-143">Report Refresh Date</span></span>
- <span data-ttu-id="c9bc3-144">Exchange activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-144">Exchange Active</span></span>
- <span data-ttu-id="c9bc3-145">Exchange inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-145">Exchange Inactive</span></span>
- <span data-ttu-id="c9bc3-146">OneDrive activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-146">OneDrive Active</span></span>
- <span data-ttu-id="c9bc3-147">OneDrive inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-147">OneDrive Inactive</span></span>
- <span data-ttu-id="c9bc3-148">SharePoint activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-148">SharePoint Active</span></span>
- <span data-ttu-id="c9bc3-149">SharePoint inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-149">SharePoint Inactive</span></span>
- <span data-ttu-id="c9bc3-150">Skype Empresarial activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-150">Skype For Business Active</span></span>
- <span data-ttu-id="c9bc3-151">Skype Empresarial inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-151">Skype For Business Inactive</span></span>
- <span data-ttu-id="c9bc3-152">Yammer activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-152">Yammer Active</span></span>
- <span data-ttu-id="c9bc3-153">Yammer inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-153">Yammer Inactive</span></span>
- <span data-ttu-id="c9bc3-154">Teams activo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-154">Teams Active</span></span>
- <span data-ttu-id="c9bc3-155">Teams inactivo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-155">Teams Inactive</span></span>
- <span data-ttu-id="c9bc3-156">Período del informe</span><span class="sxs-lookup"><span data-stu-id="c9bc3-156">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="c9bc3-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c9bc3-157">Example</span></span>

#### <a name="request"></a><span data-ttu-id="c9bc3-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c9bc3-158">Request</span></span>

<span data-ttu-id="c9bc3-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-159">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365servicesusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ServicesUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="c9bc3-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c9bc3-160">Response</span></span>

<span data-ttu-id="c9bc3-161">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-161">The following is an example of the response.</span></span>

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

<span data-ttu-id="c9bc3-162">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9bc3-162">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Exchange Active,Exchange Inactive,OneDrive Active,OneDrive Inactive,SharePoint Active,SharePoint Inactive,Skype For Business Active,Skype For Business Inactive,Yammer Active,Yammer Inactive,Teams Active,Teams Inactive,Report Period
```
