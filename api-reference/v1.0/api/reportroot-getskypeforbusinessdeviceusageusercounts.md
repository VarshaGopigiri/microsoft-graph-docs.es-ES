---
title: 'reportRoot: getSkypeForBusinessDeviceUsageUserCounts'
description: Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial. También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.
localization_priority: Normal
ms.openlocfilehash: 9b4f86079a1ce4a12ce3e480c148c588361bd9b3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875818"
---
# <a name="reportroot-getskypeforbusinessdeviceusageusercounts"></a><span data-ttu-id="4110d-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span><span class="sxs-lookup"><span data-stu-id="4110d-104">reportRoot: getSkypeForBusinessDeviceUsageUserCounts</span></span>

<span data-ttu-id="4110d-105">Obtiene las tendencias de uso sobre el número de usuarios de la organización que se conectaron con la aplicación de Skype Empresarial.</span><span class="sxs-lookup"><span data-stu-id="4110d-105">Get the usage trends on how many users in your organization have connected using the Skype for Business app.</span></span> <span data-ttu-id="4110d-106">También obtendrá un desglose por el tipo de dispositivo (Windows, teléfono Windows, teléfono Android, iPhone o iPad) donde se instaló y se usó la aplicación cliente de Skype Empresarial en la organización.</span><span class="sxs-lookup"><span data-stu-id="4110d-106">You will also get a breakdown by the type of device (Windows, Windows phone, Android phone, iPhone, or iPad) on which the Skype for Business client app is installed and used across your organization.</span></span>

> <span data-ttu-id="4110d-107">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Clientes usados de Skype Empresarial](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span><span class="sxs-lookup"><span data-stu-id="4110d-107">**Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business clients used](https://support.office.com/client/Skype-for-Business-clients-used-b9019c36-034f-40c7-acb0-c2a0400b03c3).</span></span>

## <a name="permissions"></a><span data-ttu-id="4110d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="4110d-108">Permissions</span></span>

<span data-ttu-id="4110d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4110d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="4110d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4110d-111">Permission type</span></span>                        | <span data-ttu-id="4110d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4110d-112">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="4110d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4110d-113">Delegated (work or school account)</span></span>     | <span data-ttu-id="4110d-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4110d-114">Reports.Read.All</span></span>                         |
| <span data-ttu-id="4110d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4110d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4110d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4110d-116">Not supported.</span></span>                           |
| <span data-ttu-id="4110d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4110d-117">Application</span></span>                            | <span data-ttu-id="4110d-118">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="4110d-118">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="4110d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4110d-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getSkypeForBusinessDeviceUsageUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="4110d-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="4110d-120">Function parameters</span></span>

<span data-ttu-id="4110d-121">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="4110d-121">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="4110d-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4110d-122">Parameter</span></span> | <span data-ttu-id="4110d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="4110d-123">Type</span></span>   | <span data-ttu-id="4110d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="4110d-124">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="4110d-125">period</span><span class="sxs-lookup"><span data-stu-id="4110d-125">period</span></span>    | <span data-ttu-id="4110d-126">cadena</span><span class="sxs-lookup"><span data-stu-id="4110d-126">string</span></span> | <span data-ttu-id="4110d-127">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="4110d-127">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="4110d-128">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="4110d-128">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="4110d-129">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="4110d-129">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="4110d-130">Necesario.</span><span class="sxs-lookup"><span data-stu-id="4110d-130">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="4110d-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4110d-131">Request headers</span></span>

| <span data-ttu-id="4110d-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="4110d-132">Name</span></span>          | <span data-ttu-id="4110d-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="4110d-133">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="4110d-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="4110d-134">Authorization</span></span> | <span data-ttu-id="4110d-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4110d-p105">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="4110d-137">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="4110d-137">If-None-Match</span></span> | <span data-ttu-id="4110d-138">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="4110d-138">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="4110d-139">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4110d-139">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="4110d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4110d-140">Response</span></span>

<span data-ttu-id="4110d-141">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="4110d-141">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="4110d-142">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4110d-142">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="4110d-143">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="4110d-143">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="4110d-144">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="4110d-144">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="4110d-145">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="4110d-145">Report Refresh Date</span></span>
- <span data-ttu-id="4110d-146">Windows</span><span class="sxs-lookup"><span data-stu-id="4110d-146">Windows</span></span>
- <span data-ttu-id="4110d-147">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="4110d-147">Windows Phone</span></span>
- <span data-ttu-id="4110d-148">Teléfono Android</span><span class="sxs-lookup"><span data-stu-id="4110d-148">Android Phone</span></span>
- <span data-ttu-id="4110d-149">iPhone</span><span class="sxs-lookup"><span data-stu-id="4110d-149">iPhone</span></span>
- <span data-ttu-id="4110d-150">iPad</span><span class="sxs-lookup"><span data-stu-id="4110d-150">iPad</span></span>
- <span data-ttu-id="4110d-151">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="4110d-151">Report Date</span></span>
- <span data-ttu-id="4110d-152">Período del informe</span><span class="sxs-lookup"><span data-stu-id="4110d-152">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="4110d-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4110d-153">Example</span></span>

#### <a name="request"></a><span data-ttu-id="4110d-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4110d-154">Request</span></span>

<span data-ttu-id="4110d-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4110d-155">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getskypeforbusinessdeviceusageusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getSkypeForBusinessDeviceUsageUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="4110d-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4110d-156">Response</span></span>

<span data-ttu-id="4110d-157">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4110d-157">The following is an example of the response.</span></span>

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

<span data-ttu-id="4110d-158">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="4110d-158">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Windows,Windows Phone,Android Phone,iPhone,iPad,Report Date,Report Period
```
