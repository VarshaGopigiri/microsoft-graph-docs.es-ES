# <a name="reportroot-getoffice365servicesusercounts"></a><span data-ttu-id="f5f3e-101">reportRoot: getOffice365ServicesUserCounts</span><span class="sxs-lookup"><span data-stu-id="f5f3e-101">reportRoot: getOffice365ServicesUserCounts</span></span>

<span data-ttu-id="f5f3e-102">Obtiene el número de usuarios por tipo de actividad y servicio.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-102">Get the count of users by activity type and service.</span></span>

> <span data-ttu-id="f5f3e-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Usuarios activos](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span><span class="sxs-lookup"><span data-stu-id="f5f3e-103">**Note:** For details about different report views and names, see [Office 365 Reports - Active Users](https://support.office.com/client/Active-Users-fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d).</span></span>

## <a name="permissions"></a><span data-ttu-id="f5f3e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="f5f3e-104">Permissions</span></span>

<span data-ttu-id="f5f3e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f5f3e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="f5f3e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f5f3e-107">Permission type</span></span>                        | <span data-ttu-id="f5f3e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f5f3e-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="f5f3e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f5f3e-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="f5f3e-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-110">Not supported.</span></span>                           |
| <span data-ttu-id="f5f3e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f5f3e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f5f3e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-112">Not supported.</span></span>                           |
| <span data-ttu-id="f5f3e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f5f3e-113">Application</span></span>                            | <span data-ttu-id="f5f3e-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="f5f3e-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="f5f3e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f5f3e-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getOffice365ServicesUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="f5f3e-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f3e-116">Request parameters</span></span>

<span data-ttu-id="f5f3e-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="f5f3e-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f5f3e-118">Parameter</span></span> | <span data-ttu-id="f5f3e-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-119">Type</span></span>   | <span data-ttu-id="f5f3e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5f3e-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="f5f3e-121">period</span><span class="sxs-lookup"><span data-stu-id="f5f3e-121">period</span></span>    | <span data-ttu-id="f5f3e-122">cadena</span><span class="sxs-lookup"><span data-stu-id="f5f3e-122">string</span></span> | <span data-ttu-id="f5f3e-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="f5f3e-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="f5f3e-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="f5f3e-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="f5f3e-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f3e-127">Request headers</span></span>

| <span data-ttu-id="f5f3e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="f5f3e-128">Name</span></span>          | <span data-ttu-id="f5f3e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="f5f3e-129">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="f5f3e-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="f5f3e-130">Authorization</span></span> | <span data-ttu-id="f5f3e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-p103">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="f5f3e-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="f5f3e-133">If-None-Match</span></span> | <span data-ttu-id="f5f3e-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="f5f3e-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="f5f3e-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5f3e-136">Response</span></span>

<span data-ttu-id="f5f3e-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="f5f3e-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="f5f3e-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="f5f3e-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="f5f3e-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="f5f3e-141">Report Refresh Date</span></span>
- <span data-ttu-id="f5f3e-142">Exchange activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-142">Exchange Active</span></span>
- <span data-ttu-id="f5f3e-143">Exchange inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-143">Exchange Inactive</span></span>
- <span data-ttu-id="f5f3e-144">OneDrive activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-144">OneDrive Active</span></span>
- <span data-ttu-id="f5f3e-145">OneDrive inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-145">OneDrive Inactive</span></span>
- <span data-ttu-id="f5f3e-146">SharePoint activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-146">SharePoint Active</span></span>
- <span data-ttu-id="f5f3e-147">SharePoint inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-147">SharePoint Inactive</span></span>
- <span data-ttu-id="f5f3e-148">Skype Empresarial activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-148">Skype For Business Active</span></span>
- <span data-ttu-id="f5f3e-149">Skype Empresarial inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-149">Skype For Business Inactive</span></span>
- <span data-ttu-id="f5f3e-150">Yammer activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-150">Yammer Active</span></span>
- <span data-ttu-id="f5f3e-151">Yammer inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-151">Yammer Inactive</span></span>
- <span data-ttu-id="f5f3e-152">Teams activo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-152">Teams Active</span></span>
- <span data-ttu-id="f5f3e-153">Teams inactivo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-153">Teams Inactive</span></span>
- <span data-ttu-id="f5f3e-154">Período del informe</span><span class="sxs-lookup"><span data-stu-id="f5f3e-154">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="f5f3e-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f5f3e-155">Example</span></span>

#### <a name="request"></a><span data-ttu-id="f5f3e-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f5f3e-156">Request</span></span>

<span data-ttu-id="f5f3e-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-157">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getoffice365servicesusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOffice365ServicesUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="f5f3e-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f5f3e-158">Response</span></span>

<span data-ttu-id="f5f3e-159">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-159">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="f5f3e-160">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5f3e-160">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Exchange Active,Exchange Inactive,OneDrive Active,OneDrive Inactive,SharePoint Active,SharePoint Inactive,Skype For Business Active,Skype For Business Inactive,Yammer Active,Yammer Inactive,Teams Active,Teams Inactive,Report Period
```
