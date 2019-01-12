---
title: 'reportRoot: getMailboxUsageDetail'
description: Obtiene información sobre el uso de buzones.
localization_priority: Priority
ms.prod: reports
ms.openlocfilehash: a4f412d8acdb32648ceb47e4aed6f2b7ff83268d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953486"
---
# <a name="reportroot-getmailboxusagedetail"></a><span data-ttu-id="283da-103">reportRoot: getMailboxUsageDetail</span><span class="sxs-lookup"><span data-stu-id="283da-103">reportRoot: getMailboxUsageDetail</span></span>

<span data-ttu-id="283da-104">Obtiene información sobre el uso de buzones.</span><span class="sxs-lookup"><span data-stu-id="283da-104">Get details about mailbox usage.</span></span>

> <span data-ttu-id="283da-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de buzones](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span><span class="sxs-lookup"><span data-stu-id="283da-105">**Note:** For details about different report views and names, see [Office 365 Reports - Mailbox usage](https://support.office.com/client/Mailbox-usage-beffbe01-ce2d-4614-9ae5-7898868e2729).</span></span>

## <a name="permissions"></a><span data-ttu-id="283da-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="283da-106">Permissions</span></span>

<span data-ttu-id="283da-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="283da-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="283da-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="283da-109">Permission type</span></span>                        | <span data-ttu-id="283da-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="283da-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="283da-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="283da-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="283da-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="283da-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="283da-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="283da-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="283da-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="283da-114">Not supported.</span></span>                           |
| <span data-ttu-id="283da-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="283da-115">Application</span></span>                            | <span data-ttu-id="283da-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="283da-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="283da-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="283da-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getMailboxUsageDetail(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="283da-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="283da-118">Function parameters</span></span>

<span data-ttu-id="283da-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="283da-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="283da-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="283da-120">Parameter</span></span> | <span data-ttu-id="283da-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="283da-121">Type</span></span>   | <span data-ttu-id="283da-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="283da-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="283da-123">period</span><span class="sxs-lookup"><span data-stu-id="283da-123">period</span></span>    | <span data-ttu-id="283da-124">cadena</span><span class="sxs-lookup"><span data-stu-id="283da-124">string</span></span> | <span data-ttu-id="283da-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="283da-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="283da-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="283da-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="283da-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="283da-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="283da-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="283da-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="283da-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="283da-129">Request headers</span></span>

| <span data-ttu-id="283da-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="283da-130">Name</span></span>          | <span data-ttu-id="283da-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="283da-131">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="283da-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="283da-132">Authorization</span></span> | <span data-ttu-id="283da-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="283da-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="283da-135">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="283da-135">If-None-Match</span></span> | <span data-ttu-id="283da-136">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="283da-136">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="283da-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="283da-137">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="283da-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="283da-138">Response</span></span>

<span data-ttu-id="283da-139">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="283da-139">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="283da-140">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="283da-140">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="283da-141">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="283da-141">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="283da-142">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="283da-142">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="283da-143">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="283da-143">Report Refresh Date</span></span>
- <span data-ttu-id="283da-144">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="283da-144">User Principal Name</span></span>
- <span data-ttu-id="283da-145">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="283da-145">Display Name</span></span>
- <span data-ttu-id="283da-146">Eliminado</span><span class="sxs-lookup"><span data-stu-id="283da-146">Is Deleted</span></span>
- <span data-ttu-id="283da-147">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="283da-147">Deleted Date</span></span>
- <span data-ttu-id="283da-148">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="283da-148">Created Date</span></span>
- <span data-ttu-id="283da-149">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="283da-149">Last Activity Date</span></span>
- <span data-ttu-id="283da-150">Número de elementos</span><span class="sxs-lookup"><span data-stu-id="283da-150">Item Count</span></span>
- <span data-ttu-id="283da-151">Almacenamiento usado (bytes)</span><span class="sxs-lookup"><span data-stu-id="283da-151">Storage Used (Byte)</span></span>
- <span data-ttu-id="283da-152">Cuota de advertencia de problema (bytes)</span><span class="sxs-lookup"><span data-stu-id="283da-152">Issue Warning Quota (Byte)</span></span>
- <span data-ttu-id="283da-153">Cuota de prohibición de envío (bytes)</span><span class="sxs-lookup"><span data-stu-id="283da-153">Prohibit Send Quota (Byte)</span></span>
- <span data-ttu-id="283da-154">Cuota de prohibición de envío o recepción (bytes)</span><span class="sxs-lookup"><span data-stu-id="283da-154">Prohibit Send/Receive Quota (Byte)</span></span>
- <span data-ttu-id="283da-155">Período del informe</span><span class="sxs-lookup"><span data-stu-id="283da-155">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="283da-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="283da-156">Example</span></span>

#### <a name="request"></a><span data-ttu-id="283da-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="283da-157">Request</span></span>

<span data-ttu-id="283da-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="283da-158">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getmailboxusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getMailboxUsageDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="283da-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="283da-159">Response</span></span>

<span data-ttu-id="283da-160">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="283da-160">The following is an example of the response.</span></span>

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

<span data-ttu-id="283da-161">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="283da-161">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,Is Deleted,Deleted Date,Created Date,Last Activity Date,Item Count,Storage Used (Byte),Issue Warning Quota (Byte),Prohibit Send Quota (Byte),Prohibit Send/Receive Quota (Byte),Report Period
```
