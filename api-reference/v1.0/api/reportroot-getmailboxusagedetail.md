---
title: 'reportRoot: getMailboxUsageDetail'
description: Obtiene información sobre el uso de buzones.
ms.openlocfilehash: df29ff0386d618f0da16b21fbe1d9ae72f183524
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029608"
---
# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="35402-103">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="35402-103">reportRoot: getMailboxUsageDetail</span></span>

<span data-ttu-id="35402-104">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="35402-104">Get details about mailbox usage.</span></span>

> <span data-ttu-id="35402-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="35402-105">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="35402-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="35402-106">Permissions</span></span>

<span data-ttu-id="35402-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35402-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="35402-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35402-109">Permission type</span></span>                        | <span data-ttu-id="35402-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35402-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="35402-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35402-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="35402-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="35402-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="35402-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35402-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35402-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="35402-114">Not supported.</span></span>                           |
| <span data-ttu-id="35402-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35402-115">Application</span></span>                            | <span data-ttu-id="35402-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="35402-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="35402-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35402-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="35402-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="35402-118">Function parameters</span></span>

<span data-ttu-id="35402-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="35402-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="35402-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="35402-120">Parameter</span></span> | <span data-ttu-id="35402-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="35402-121">Type</span></span>   | <span data-ttu-id="35402-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="35402-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="35402-123">period</span><span class="sxs-lookup"><span data-stu-id="35402-123">period</span></span>    | <span data-ttu-id="35402-124">cadena</span><span class="sxs-lookup"><span data-stu-id="35402-124">string</span></span> | <span data-ttu-id="35402-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="35402-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="35402-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="35402-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="35402-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="35402-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="35402-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="35402-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="35402-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35402-129">Request headers</span></span>

| <span data-ttu-id="35402-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="35402-130">Name</span></span>          | <span data-ttu-id="35402-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="35402-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="35402-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="35402-132">Authorization</span></span> | <span data-ttu-id="35402-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35402-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="35402-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="35402-135">If-None-Match</span></span> | <span data-ttu-id="35402-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="35402-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="35402-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="35402-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="35402-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35402-138">Response</span></span>

<span data-ttu-id="35402-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="35402-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="35402-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35402-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="35402-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="35402-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="35402-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="35402-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="35402-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="35402-143">Report Refresh Date</span></span>
- <span data-ttu-id="35402-144">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="35402-144">User Principal Name</span></span>
- <span data-ttu-id="35402-145">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="35402-145">Display Name</span></span>
- <span data-ttu-id="35402-146">Eliminado</span><span class="sxs-lookup"><span data-stu-id="35402-146">Is Deleted</span></span>
- <span data-ttu-id="35402-147">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="35402-147">Deleted Date</span></span>
- <span data-ttu-id="35402-148">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="35402-148">Created Date</span></span>
- <span data-ttu-id="35402-149">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="35402-149">Last Activity Date</span></span>
- <span data-ttu-id="35402-150">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="35402-150">Item Count</span></span>
- <span data-ttu-id="35402-151">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="35402-151">Storage Used (Byte)</span></span>
- <span data-ttu-id="35402-152">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="35402-152">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="35402-153">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="35402-153">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="35402-154">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="35402-154">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="35402-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="35402-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="35402-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35402-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="35402-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35402-157">Request</span></span>

<span data-ttu-id="35402-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35402-158">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="35402-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35402-159">Response</span></span>

<span data-ttu-id="35402-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35402-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="35402-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="35402-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```
