---
title: 'reportRoot: getOffice365ActiveUserDetail'
description: Obtiene información sobre los usuarios activos de Office 365.
localization_priority: Priority
ms.prod: reports
ms.openlocfilehash: 876cf79d8a784460e8e1ba7977b0d89fc3565672
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919325"
---
# <a name="reportroot-getoffice365activeuserdetail"></a><span data-ttu-id="b84d0-103">reportRoot: getOffice365ActiveUserDetail</span><span class="sxs-lookup"><span data-stu-id="b84d0-103">reportRoot: getOffice365ActiveUserDetail</span></span>

<span data-ttu-id="b84d0-104">Obtiene información sobre los usuarios activos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="b84d0-104">Get details about Office 365 active users.</span></span>

> <span data-ttu-id="b84d0-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="b84d0-105">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="b84d0-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="b84d0-106">Permissions</span></span>

<span data-ttu-id="b84d0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b84d0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="b84d0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b84d0-109">Permission type</span></span>                        | <span data-ttu-id="b84d0-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b84d0-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="b84d0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b84d0-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="b84d0-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b84d0-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="b84d0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b84d0-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b84d0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b84d0-114">Not supported.</span></span>                           |
| <span data-ttu-id="b84d0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b84d0-115">Application</span></span>                            | <span data-ttu-id="b84d0-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="b84d0-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="b84d0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b84d0-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOffice365ActiveUserDetail(period='{period_value}')
GET /reports/getOffice365ActiveUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="b84d0-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="b84d0-118">Function parameters</span></span>

<span data-ttu-id="b84d0-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="b84d0-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="b84d0-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b84d0-120">Parameter</span></span> | <span data-ttu-id="b84d0-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b84d0-121">Type</span></span>   | <span data-ttu-id="b84d0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b84d0-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="b84d0-123">period</span><span class="sxs-lookup"><span data-stu-id="b84d0-123">period</span></span>    | <span data-ttu-id="b84d0-124">cadena</span><span class="sxs-lookup"><span data-stu-id="b84d0-124">string</span></span> | <span data-ttu-id="b84d0-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b84d0-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="b84d0-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="b84d0-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="b84d0-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="b84d0-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="b84d0-128">date</span><span class="sxs-lookup"><span data-stu-id="b84d0-128">date</span></span>      | <span data-ttu-id="b84d0-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="b84d0-129">Date</span></span>   | <span data-ttu-id="b84d0-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="b84d0-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="b84d0-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="b84d0-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="b84d0-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="b84d0-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="b84d0-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="b84d0-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="b84d0-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b84d0-134">Request headers</span></span>

| <span data-ttu-id="b84d0-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="b84d0-135">Name</span></span>          | <span data-ttu-id="b84d0-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="b84d0-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="b84d0-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="b84d0-137">Authorization</span></span> | <span data-ttu-id="b84d0-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b84d0-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="b84d0-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="b84d0-140">If-None-Match</span></span> | <span data-ttu-id="b84d0-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="b84d0-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="b84d0-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b84d0-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="b84d0-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b84d0-143">Response</span></span>

<span data-ttu-id="b84d0-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="b84d0-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="b84d0-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b84d0-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="b84d0-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="b84d0-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="b84d0-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="b84d0-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="b84d0-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="b84d0-148">Report Refresh Date</span></span>
- <span data-ttu-id="b84d0-149">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="b84d0-149">User Principal Name</span></span>
- <span data-ttu-id="b84d0-150">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="b84d0-150">Display Name</span></span>
- <span data-ttu-id="b84d0-151">Eliminado</span><span class="sxs-lookup"><span data-stu-id="b84d0-151">Is Deleted</span></span>
- <span data-ttu-id="b84d0-152">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="b84d0-152">Deleted Date</span></span>
- <span data-ttu-id="b84d0-153">Tiene una licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="b84d0-153">Has Exchange License</span></span>
- <span data-ttu-id="b84d0-154">Tiene una licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="b84d0-154">Has OneDrive License</span></span>
- <span data-ttu-id="b84d0-155">Tiene de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="b84d0-155">Has SharePoint License</span></span>
- <span data-ttu-id="b84d0-156">Tiene una licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="b84d0-156">Has Skype For Business License</span></span>
- <span data-ttu-id="b84d0-157">Tiene una licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="b84d0-157">Has Yammer License</span></span>
- <span data-ttu-id="b84d0-158">Tiene una licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="b84d0-158">Has Teams License</span></span>
- <span data-ttu-id="b84d0-159">Fecha de la última actividad de Exchange</span><span class="sxs-lookup"><span data-stu-id="b84d0-159">Exchange Last Activity Date</span></span>
- <span data-ttu-id="b84d0-160">Fecha de la última actividad de OneDrive</span><span class="sxs-lookup"><span data-stu-id="b84d0-160">OneDrive Last Activity Date</span></span>
- <span data-ttu-id="b84d0-161">Fecha de la última actividad de SharePoint</span><span class="sxs-lookup"><span data-stu-id="b84d0-161">SharePoint Last Activity Date</span></span>
- <span data-ttu-id="b84d0-162">Fecha de la última actividad de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="b84d0-162">Skype For Business Last Activity Date</span></span>
- <span data-ttu-id="b84d0-163">Fecha de la última actividad de Yammer</span><span class="sxs-lookup"><span data-stu-id="b84d0-163">Yammer Last Activity Date</span></span>
- <span data-ttu-id="b84d0-164">Fecha de la última actividad de Teams</span><span class="sxs-lookup"><span data-stu-id="b84d0-164">Teams Last Activity Date</span></span>
- <span data-ttu-id="b84d0-165">Fecha de asignación de licencia de Exchange</span><span class="sxs-lookup"><span data-stu-id="b84d0-165">Exchange License Assign Date</span></span>
- <span data-ttu-id="b84d0-166">Fecha de asignación de licencia de licencia de OneDrive</span><span class="sxs-lookup"><span data-stu-id="b84d0-166">OneDrive License Assign Date</span></span>
- <span data-ttu-id="b84d0-167">Fecha de asignación de licencia de SharePoint</span><span class="sxs-lookup"><span data-stu-id="b84d0-167">SharePoint License Assign Date</span></span>
- <span data-ttu-id="b84d0-168">Fecha de asignación de licencia de Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="b84d0-168">Skype For Business License Assign Date</span></span>
- <span data-ttu-id="b84d0-169">Fecha de asignación de licencia de Yammer</span><span class="sxs-lookup"><span data-stu-id="b84d0-169">Yammer License Assign Date</span></span>
- <span data-ttu-id="b84d0-170">Fecha de asignación de licencia de Teams</span><span class="sxs-lookup"><span data-stu-id="b84d0-170">Teams License Assign Date</span></span>
- <span data-ttu-id="b84d0-171">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="b84d0-171">Assigned Products</span></span>

## <a name="example"></a><span data-ttu-id="b84d0-172">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b84d0-172">Example</span></span>

#### <a name="request"></a><span data-ttu-id="b84d0-173">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b84d0-173">Request</span></span>

<span data-ttu-id="b84d0-174">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b84d0-174">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="b84d0-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b84d0-175">Response</span></span>

<span data-ttu-id="b84d0-176">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b84d0-176">The following is an example of the response.</span></span>

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

<span data-ttu-id="b84d0-177">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="b84d0-177">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Has Exchange License,Has OneDrive License,Has SharePoint License,Has Skype For Business License,Has Yammer License,Has Teams License,Exchange Last Activity Date,OneDrive Last Activity Date,SharePoint Last Activity Date,Skype For Business Last Activity Date,Yammer Last Activity Date,Teams Last Activity Date,Exchange License Assign Date,OneDrive License Assign Date,SharePoint License Assign Date,Skype For Business License Assign Date,Yammer License Assign Date,Teams License Assign Date,Assigned Products
```
