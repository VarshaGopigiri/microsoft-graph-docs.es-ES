# <a name="reportroot-getyammerdeviceusageuserdetail-function"></a><span data-ttu-id="20ed6-101">reportRoot: función getYammerDeviceUsageUserDetail</span><span class="sxs-lookup"><span data-stu-id="20ed6-101">reportRoot: getYammerDeviceUsageUserDetail function</span></span>

<span data-ttu-id="20ed6-102">Obtiene información sobre el uso de dispositivos de Yammer por usuario.</span><span class="sxs-lookup"><span data-stu-id="20ed6-102">Get details about Yammer device usage by user.</span></span>

> <span data-ttu-id="20ed6-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Uso de dispositivos de Yammer](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span><span class="sxs-lookup"><span data-stu-id="20ed6-103">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer device usage](https://support.office.com/client/Yammer-device-usage-b793ffdd-effa-43d0-849a-b1ca2e899f38).</span></span>

## <a name="permissions"></a><span data-ttu-id="20ed6-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="20ed6-104">Permissions</span></span>

<span data-ttu-id="20ed6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="20ed6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="20ed6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="20ed6-107">Permission type</span></span>                        | <span data-ttu-id="20ed6-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="20ed6-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="20ed6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="20ed6-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="20ed6-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20ed6-110">Not supported.</span></span>                           |
| <span data-ttu-id="20ed6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="20ed6-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="20ed6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20ed6-112">Not supported.</span></span>                           |
| <span data-ttu-id="20ed6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="20ed6-113">Application</span></span>                            | <span data-ttu-id="20ed6-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="20ed6-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="20ed6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="20ed6-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerDeviceUsageUserDetail(period='{period_value}')
GET /reports/getYammerDeviceUsageUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="20ed6-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="20ed6-116">Request parameters</span></span>

<span data-ttu-id="20ed6-117">En la URL de la solicitud, especifique el parámetro de consulta seleccionado con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="20ed6-117">In the request URL, provide the chosen query parameter with a valid value.</span></span>

| <span data-ttu-id="20ed6-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="20ed6-118">Parameter</span></span> | <span data-ttu-id="20ed6-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="20ed6-119">Type</span></span>   | <span data-ttu-id="20ed6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="20ed6-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="20ed6-121">period</span><span class="sxs-lookup"><span data-stu-id="20ed6-121">period</span></span>    | <span data-ttu-id="20ed6-122">cadena</span><span class="sxs-lookup"><span data-stu-id="20ed6-122">string</span></span> | <span data-ttu-id="20ed6-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="20ed6-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="20ed6-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="20ed6-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="20ed6-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="20ed6-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="20ed6-126">date</span><span class="sxs-lookup"><span data-stu-id="20ed6-126">date</span></span>      | <span data-ttu-id="20ed6-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="20ed6-127">Date</span></span>   | <span data-ttu-id="20ed6-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="20ed6-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="20ed6-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="20ed6-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="20ed6-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="20ed6-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="20ed6-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="20ed6-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="20ed6-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="20ed6-132">Request headers</span></span>

| <span data-ttu-id="20ed6-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="20ed6-133">Name</span></span>          | <span data-ttu-id="20ed6-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="20ed6-134">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="20ed6-135">Authorization</span><span class="sxs-lookup"><span data-stu-id="20ed6-135">Authorization</span></span> | <span data-ttu-id="20ed6-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="20ed6-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="20ed6-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="20ed6-138">If-None-Match</span></span> | <span data-ttu-id="20ed6-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="20ed6-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="20ed6-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="20ed6-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="20ed6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20ed6-141">Response</span></span>

<span data-ttu-id="20ed6-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="20ed6-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="20ed6-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="20ed6-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="20ed6-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="20ed6-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="20ed6-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="20ed6-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="20ed6-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="20ed6-146">Report Refresh Date</span></span>
- <span data-ttu-id="20ed6-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="20ed6-147">User Principal Name</span></span>
- <span data-ttu-id="20ed6-148">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="20ed6-148">Display Name</span></span>
- <span data-ttu-id="20ed6-149">Estado del usuario</span><span class="sxs-lookup"><span data-stu-id="20ed6-149">User State</span></span>
- <span data-ttu-id="20ed6-150">Fecha de cambio de estado</span><span class="sxs-lookup"><span data-stu-id="20ed6-150">State Change Date</span></span>
- <span data-ttu-id="20ed6-151">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="20ed6-151">Last Activity Date</span></span>
- <span data-ttu-id="20ed6-152">Web usada</span><span class="sxs-lookup"><span data-stu-id="20ed6-152">Used Web</span></span>
- <span data-ttu-id="20ed6-153">Windows Phone usado</span><span class="sxs-lookup"><span data-stu-id="20ed6-153">Used Windows Phone</span></span>
- <span data-ttu-id="20ed6-154">Teléfono Android usado</span><span class="sxs-lookup"><span data-stu-id="20ed6-154">Used Android Phone</span></span>
- <span data-ttu-id="20ed6-155">iPhone usado</span><span class="sxs-lookup"><span data-stu-id="20ed6-155">Used iPhone</span></span>
- <span data-ttu-id="20ed6-156">iPad usado</span><span class="sxs-lookup"><span data-stu-id="20ed6-156">Used iPad</span></span>
- <span data-ttu-id="20ed6-157">Otros usados</span><span class="sxs-lookup"><span data-stu-id="20ed6-157">Used Others</span></span>
- <span data-ttu-id="20ed6-158">Período del informe</span><span class="sxs-lookup"><span data-stu-id="20ed6-158">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="20ed6-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20ed6-159">Example</span></span>

#### <a name="request"></a><span data-ttu-id="20ed6-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="20ed6-160">Request</span></span>

<span data-ttu-id="20ed6-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="20ed6-161">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammerdeviceusageuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerDeviceUsageUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="20ed6-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20ed6-162">Response</span></span>

<span data-ttu-id="20ed6-163">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="20ed6-163">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="20ed6-164">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="20ed6-164">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Display Name,User State,State Change Date,Last Activity Date,Used Web,Used Windows Phone,Used Android Phone,Used iPhone,Used iPad,Used Others,Report Period
```
