---
title: 'reportRoot: getOffice365ActiveUserCounts'
description: Obtiene el número de usuarios activos diarios en el período de informe por producto.
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 3469cbcf2dee789ca848f88d43d8eb3ff640f9c7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980037"
---
# <a name="reportroot-getoffice365activeusercounts"></a><span data-ttu-id="14e48-103">reportRoot: getOffice365ActiveUserCounts</span><span class="sxs-lookup"><span data-stu-id="14e48-103">reportRoot: getOffice365ActiveUserCounts</span></span>

<span data-ttu-id="14e48-104">Obtiene el número de usuarios activos diarios en el período de informe por producto.</span><span class="sxs-lookup"><span data-stu-id="14e48-104">Get the count of daily active users in the reporting period by product.</span></span>

> <span data-ttu-id="14e48-105">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="14e48-105">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="14e48-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="14e48-106">Permissions</span></span>

<span data-ttu-id="14e48-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="14e48-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="14e48-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="14e48-109">Permission type</span></span>                        | <span data-ttu-id="14e48-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="14e48-110">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="14e48-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="14e48-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="14e48-112">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="14e48-112">Reports.Read.All</span></span>                         |
| <span data-ttu-id="14e48-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="14e48-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="14e48-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="14e48-114">Not supported.</span></span>                           |
| <span data-ttu-id="14e48-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="14e48-115">Application</span></span>                            | <span data-ttu-id="14e48-116">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="14e48-116">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="14e48-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="14e48-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ActiveUserCounts(period='{period_value}')
```

## <a name="function-parameters"></a><span data-ttu-id="14e48-118">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="14e48-118">Function parameters</span></span>

<span data-ttu-id="14e48-119">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="14e48-119">In the request URL, provide the following parameter with a valid value.</span></span>

| <span data-ttu-id="14e48-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="14e48-120">Parameter</span></span> | <span data-ttu-id="14e48-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="14e48-121">Type</span></span>   | <span data-ttu-id="14e48-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="14e48-122">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="14e48-123">period</span><span class="sxs-lookup"><span data-stu-id="14e48-123">period</span></span>    | <span data-ttu-id="14e48-124">cadena</span><span class="sxs-lookup"><span data-stu-id="14e48-124">string</span></span> | <span data-ttu-id="14e48-125">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="14e48-125">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="14e48-126">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="14e48-126">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="14e48-127">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="14e48-127">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="14e48-128">Necesario.</span><span class="sxs-lookup"><span data-stu-id="14e48-128">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="14e48-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="14e48-129">Request headers</span></span>

| <span data-ttu-id="14e48-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="14e48-130">Name</span></span>          | <span data-ttu-id="14e48-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="14e48-131">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="14e48-132">Authorization</span><span class="sxs-lookup"><span data-stu-id="14e48-132">Authorization</span></span> | <span data-ttu-id="14e48-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="14e48-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="14e48-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14e48-135">Response</span></span>

<span data-ttu-id="14e48-136">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="14e48-136">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="14e48-137">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14e48-137">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="14e48-138">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="14e48-138">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="14e48-139">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="14e48-139">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="14e48-140">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="14e48-140">Report Refresh Date</span></span>
- <span data-ttu-id="14e48-141">Office 365</span><span class="sxs-lookup"><span data-stu-id="14e48-141">Office 365</span></span>
- <span data-ttu-id="14e48-142">Exchange</span><span class="sxs-lookup"><span data-stu-id="14e48-142">Exchange</span></span>
- <span data-ttu-id="14e48-143">OneDrive</span><span class="sxs-lookup"><span data-stu-id="14e48-143">OneDrive</span></span>
- <span data-ttu-id="14e48-144">SharePoint</span><span class="sxs-lookup"><span data-stu-id="14e48-144">SharePoint</span></span>
- <span data-ttu-id="14e48-145">Skype Empresarial</span><span class="sxs-lookup"><span data-stu-id="14e48-145">Skype For Business</span></span> 
- <span data-ttu-id="14e48-146">Yammer</span><span class="sxs-lookup"><span data-stu-id="14e48-146">Yammer</span></span>
- <span data-ttu-id="14e48-147">Teams</span><span class="sxs-lookup"><span data-stu-id="14e48-147">Teams</span></span>
- <span data-ttu-id="14e48-148">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="14e48-148">Report Date</span></span>
- <span data-ttu-id="14e48-149">Período del informe</span><span class="sxs-lookup"><span data-stu-id="14e48-149">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="14e48-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="14e48-150">Example</span></span>

#### <a name="request"></a><span data-ttu-id="14e48-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="14e48-151">Request</span></span>

<span data-ttu-id="14e48-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="14e48-152">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getoffice365activeusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ActiveUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="14e48-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="14e48-153">Response</span></span>

<span data-ttu-id="14e48-154">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="14e48-154">The following is an example of the response.</span></span>

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

<span data-ttu-id="14e48-155">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="14e48-155">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Office 365,Exchange,OneDrive,SharePoint,Skype For Business,Yammer,Teams,Report Date,Report Period
```
