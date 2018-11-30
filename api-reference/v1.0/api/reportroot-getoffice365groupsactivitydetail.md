---
title: 'reportRoot: getOffice365GroupsActivityDetail'
description: Obtiene información sobre la actividad de Grupos de Office 365 por grupo.
ms.openlocfilehash: 18ff1ea1ee3bfc90cbf86bb4e99321198c583f06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031273"
---
# <a name="reportroot-getoffice365groupsactivitydetail"></a><span data-ttu-id="dc2ef-103">reportRoot: getOffice365GroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="dc2ef-103">reportRoot: getOffice365GroupsActivityDetail</span></span>

<span data-ttu-id="dc2ef-104">Obtiene información sobre la actividad de Grupos de Office 365 por grupo.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-104">Get details about Office 365 Groups activity by group.</span></span>

> <span data-ttu-id="dc2ef-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Grupos de Office 365](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span><span class="sxs-lookup"><span data-stu-id="dc2ef-105">**Note:** For details about different report views and names, see [Office 365 Reports - Office 365 groups](https://support.office.com/client/Office-365-groups-a27f1a99-3557-4f85-9560-a28e3d822a40).</span></span>

## <a name="permissions"></a><span data-ttu-id="dc2ef-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc2ef-106">Permissions</span></span>

<span data-ttu-id="dc2ef-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc2ef-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="dc2ef-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc2ef-109">Permission type</span></span>                        | <span data-ttu-id="dc2ef-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc2ef-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="dc2ef-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc2ef-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="dc2ef-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dc2ef-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="dc2ef-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc2ef-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc2ef-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-114">Not supported.</span></span>                           |
| <span data-ttu-id="dc2ef-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc2ef-115">Application</span></span>                            | <span data-ttu-id="dc2ef-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="dc2ef-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="dc2ef-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc2ef-117">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOffice365GroupsActivityDetail(period='{period_value}')
GET /reports/getOffice365GroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="dc2ef-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="dc2ef-118">Function parameters</span></span>

<span data-ttu-id="dc2ef-119">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-119">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="dc2ef-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dc2ef-120">Parameter</span></span> | <span data-ttu-id="dc2ef-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc2ef-121">Type</span></span>   | <span data-ttu-id="dc2ef-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc2ef-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="dc2ef-123">period</span><span class="sxs-lookup"><span data-stu-id="dc2ef-123">period</span></span>    | <span data-ttu-id="dc2ef-124">cadena</span><span class="sxs-lookup"><span data-stu-id="dc2ef-124">string</span></span> | <span data-ttu-id="dc2ef-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="dc2ef-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="dc2ef-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="dc2ef-128">date</span><span class="sxs-lookup"><span data-stu-id="dc2ef-128">date</span></span>      | <span data-ttu-id="dc2ef-129">Fecha</span><span class="sxs-lookup"><span data-stu-id="dc2ef-129">Date</span></span>   | <span data-ttu-id="dc2ef-130">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-130">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="dc2ef-131">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-131">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="dc2ef-132">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-132">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="dc2ef-133">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-133">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="dc2ef-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc2ef-134">Request headers</span></span>

| <span data-ttu-id="dc2ef-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc2ef-135">Name</span></span>          | <span data-ttu-id="dc2ef-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc2ef-136">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="dc2ef-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc2ef-137">Authorization</span></span> | <span data-ttu-id="dc2ef-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="dc2ef-140">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="dc2ef-140">If-None-Match</span></span> | <span data-ttu-id="dc2ef-141">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-141">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="dc2ef-142">Opcional.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-142">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="dc2ef-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc2ef-143">Response</span></span>

<span data-ttu-id="dc2ef-144">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-144">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="dc2ef-145">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-145">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="dc2ef-146">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-146">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="dc2ef-147">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-147">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="dc2ef-148">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="dc2ef-148">Report Refresh Date</span></span>
- <span data-ttu-id="dc2ef-149">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="dc2ef-149">Group Display Name</span></span>
- <span data-ttu-id="dc2ef-150">Eliminado</span><span class="sxs-lookup"><span data-stu-id="dc2ef-150">Is Deleted</span></span>
- <span data-ttu-id="dc2ef-151">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="dc2ef-151">Owner Principal Name</span></span>
- <span data-ttu-id="dc2ef-152">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="dc2ef-152">Last Activity Date</span></span>
- <span data-ttu-id="dc2ef-153">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="dc2ef-153">Group Type</span></span>
- <span data-ttu-id="dc2ef-154">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="dc2ef-154">Member Count</span></span>
- <span data-ttu-id="dc2ef-155">Número de miembros externos</span><span class="sxs-lookup"><span data-stu-id="dc2ef-155">External Member Count</span></span>
- <span data-ttu-id="dc2ef-156">Número de correos electrónicos recibidos de Exchange</span><span class="sxs-lookup"><span data-stu-id="dc2ef-156">Exchange Received Email Count</span></span>
- <span data-ttu-id="dc2ef-157">Número de archivos activos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="dc2ef-157">SharePoint Active File Count</span></span>
- <span data-ttu-id="dc2ef-158">Número de mensajes publicados en Yammer</span><span class="sxs-lookup"><span data-stu-id="dc2ef-158">Yammer Posted Message Count</span></span>
- <span data-ttu-id="dc2ef-159">Número de mensajes leídos en Yammer</span><span class="sxs-lookup"><span data-stu-id="dc2ef-159">Yammer Read Message Count</span></span>
- <span data-ttu-id="dc2ef-160">Número de mensajes etiquetados como “Me gusta” en Yammer</span><span class="sxs-lookup"><span data-stu-id="dc2ef-160">Yammer Liked Message Count</span></span>
- <span data-ttu-id="dc2ef-161">Número total de elementos de buzones de Exchange</span><span class="sxs-lookup"><span data-stu-id="dc2ef-161">Exchange Mailbox Total Item Count</span></span>
- <span data-ttu-id="dc2ef-162">Almacenamiento usado de buzones de Exchange (bytes)</span><span class="sxs-lookup"><span data-stu-id="dc2ef-162">Exchange Mailbox Storage Used (Byte)</span></span>
- <span data-ttu-id="dc2ef-163">Número total de archivos de SharePoint</span><span class="sxs-lookup"><span data-stu-id="dc2ef-163">SharePoint Total File Count</span></span>
- <span data-ttu-id="dc2ef-164">Almacenamiento usado de sitios de SharePoint (bytes)</span><span class="sxs-lookup"><span data-stu-id="dc2ef-164">SharePoint Site Storage Used (Byte)</span></span>
- <span data-ttu-id="dc2ef-165">Período del informe</span><span class="sxs-lookup"><span data-stu-id="dc2ef-165">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="dc2ef-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc2ef-166">Example</span></span>

#### <a name="request"></a><span data-ttu-id="dc2ef-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc2ef-167">Request</span></span>

<span data-ttu-id="dc2ef-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-168">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365groupsactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365GroupsActivityDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="dc2ef-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc2ef-169">Response</span></span>

<span data-ttu-id="dc2ef-170">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-170">The following is an example of the response.</span></span>

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

<span data-ttu-id="dc2ef-171">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc2ef-171">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Member Count,Guest Count,Exchange Received Email Count,SharePoint Active File Count,Yammer Posted Message Count,Yammer Read Message Count,Yammer Liked Message Count,Exchange Mailbox Total Item Count,Exchange Mailbox Storage Used (Byte),SharePoint Total File Count,SharePoint Site Storage Used (Byte),Report Period
```
