---
title: 'reportRoot: getOffice365ActiveUserDetail'
description: Obtiene información sobre los usuarios activos de Office 365.
ms.openlocfilehash: d14ef5dfab0bde7264fbaa6f82007bdfa2300da8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031513"
---
# <a name="reportroot-getoffice365activeuserdetail"></a><span data-ttu-id="01cf3-103">reportRoot: getOffice365ActiveUserDetail</span><span class="sxs-lookup"><span data-stu-id="01cf3-103">reportRoot: getOffice365ActiveUserDetail</span></span>

<span data-ttu-id="01cf3-104">Obtiene información sobre los usuarios activos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="01cf3-104">Get details about Office 365 active users.</span></span>

> <span data-ttu-id="01cf3-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="01cf3-105">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="01cf3-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="01cf3-106">Permissions</span></span>

<span data-ttu-id="01cf3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01cf3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="01cf3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01cf3-109">Permission type</span></span>                        | <span data-ttu-id="01cf3-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01cf3-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="01cf3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01cf3-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="01cf3-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="01cf3-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="01cf3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01cf3-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="01cf3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01cf3-114">Not supported.</span></span>                           |
| <span data-ttu-id="01cf3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01cf3-115">Application</span></span>                            | <span data-ttu-id="01cf3-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="01cf3-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="01cf3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01cf3-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOffice365ActiveUserDetail(period='{period_value}')
GET /reports/getOffice365ActiveUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="01cf3-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="01cf3-118">Function parameters</span></span>

<span data-ttu-id="01cf3-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="01cf3-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="01cf3-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="01cf3-120">Parameter</span></span> | <span data-ttu-id="01cf3-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="01cf3-121">Type</span></span>   | <span data-ttu-id="01cf3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="01cf3-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="01cf3-123">period</span><span class="sxs-lookup"><span data-stu-id="01cf3-123">period</span></span>    | <span data-ttu-id="01cf3-124">cadena</span><span class="sxs-lookup"><span data-stu-id="01cf3-124">string</span></span> | <span data-ttu-id="01cf3-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="01cf3-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="01cf3-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="01cf3-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="01cf3-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="01cf3-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="01cf3-128">date</span><span class="sxs-lookup"><span data-stu-id="01cf3-128">date</span></span>      | <span data-ttu-id="01cf3-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="01cf3-129">Date</span></span>   | <span data-ttu-id="01cf3-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="01cf3-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="01cf3-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="01cf3-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="01cf3-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="01cf3-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="01cf3-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="01cf3-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="01cf3-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01cf3-134">Request headers</span></span>

| <span data-ttu-id="01cf3-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="01cf3-135">Name</span></span>          | <span data-ttu-id="01cf3-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="01cf3-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="01cf3-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="01cf3-137">Authorization</span></span> | <span data-ttu-id="01cf3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01cf3-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="01cf3-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="01cf3-140">If-None-Match</span></span> | <span data-ttu-id="01cf3-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="01cf3-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="01cf3-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="01cf3-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="01cf3-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01cf3-143">Response</span></span>

<span data-ttu-id="01cf3-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="01cf3-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="01cf3-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01cf3-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="01cf3-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="01cf3-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="01cf3-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="01cf3-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="01cf3-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="01cf3-148">Report Refresh Date</span></span>
- <span data-ttu-id="01cf3-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="01cf3-149">User Principal Name</span></span>
- <span data-ttu-id="01cf3-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="01cf3-150">Display Name</span></span>
- <span data-ttu-id="01cf3-151">Eliminado</span><span class="sxs-lookup"><span data-stu-id="01cf3-151">Is Deleted</span></span>
- <span data-ttu-id="01cf3-152">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="01cf3-152">Deleted Date</span></span>
- <span data-ttu-id="01cf3-153">Tiene una licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="01cf3-153">Has Exchange License</span></span>
- <span data-ttu-id="01cf3-154">Tiene una licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="01cf3-154">Has OneDrive License</span></span>
- <span data-ttu-id="01cf3-155">Tiene de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="01cf3-155">Has SharePoint License</span></span>
- <span data-ttu-id="01cf3-156">Tiene una licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="01cf3-156">Has Skype For Business License</span></span>
- <span data-ttu-id="01cf3-157">Tiene una licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="01cf3-157">Has Yammer License</span></span>
- <span data-ttu-id="01cf3-158">Tiene una licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="01cf3-158">Has Teams License</span></span>
- <span data-ttu-id="01cf3-159">Fecha de la última actividad de Exchange</span><span class="sxs-lookup"><span data-stu-id="01cf3-159">Exchange Last Activity Date</span></span>
- <span data-ttu-id="01cf3-160">Fecha de la última actividad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="01cf3-160">OneDrive Last Activity Date</span></span>
- <span data-ttu-id="01cf3-161">Fecha de la última actividad de SharePoint</span><span class="sxs-lookup"><span data-stu-id="01cf3-161">SharePoint Last Activity Date</span></span>
- <span data-ttu-id="01cf3-162">Fecha de la última actividad de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="01cf3-162">Skype For Business Last Activity Date</span></span>
- <span data-ttu-id="01cf3-163">Fecha de la última actividad de Yammer</span><span class="sxs-lookup"><span data-stu-id="01cf3-163">Yammer Last Activity Date</span></span>
- <span data-ttu-id="01cf3-164">Fecha de la última actividad de Teams</span><span class="sxs-lookup"><span data-stu-id="01cf3-164">Teams Last Activity Date</span></span>
- <span data-ttu-id="01cf3-165">Fecha de asignación de licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="01cf3-165">Exchange License Assign Date</span></span>
- <span data-ttu-id="01cf3-166">Fecha de asignación de licencia de licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="01cf3-166">OneDrive License Assign Date</span></span>
- <span data-ttu-id="01cf3-167">Fecha de asignación de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="01cf3-167">SharePoint License Assign Date</span></span>
- <span data-ttu-id="01cf3-168">Fecha de asignación de licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="01cf3-168">Skype For Business License Assign Date</span></span>
- <span data-ttu-id="01cf3-169">Fecha de asignación de licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="01cf3-169">Yammer License Assign Date</span></span>
- <span data-ttu-id="01cf3-170">Fecha de asignación de licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="01cf3-170">Teams License Assign Date</span></span>
- <span data-ttu-id="01cf3-171">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="01cf3-171">Assigned Products</span></span>

## <a name="example"></a><span data-ttu-id="01cf3-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01cf3-172">Example</span></span>

#### <a name="request"></a><span data-ttu-id="01cf3-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01cf3-173">Request</span></span>

<span data-ttu-id="01cf3-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01cf3-174">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="01cf3-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01cf3-175">Response</span></span>

<span data-ttu-id="01cf3-176">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01cf3-176">The following is an example of the response.</span></span>

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

<span data-ttu-id="01cf3-177">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="01cf3-177">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Has Exchange License,Has OneDrive License,Has SharePoint License,Has Skype For Business License,Has Yammer License,Has Teams License,Exchange Last Activity Date,OneDrive Last Activity Date,SharePoint Last Activity Date,Skype For Business Last Activity Date,Yammer Last Activity Date,Teams Last Activity Date,Exchange License Assign Date,OneDrive License Assign Date,SharePoint License Assign Date,Skype For Business License Assign Date,Yammer License Assign Date,Teams License Assign Date,Assigned Products
```
