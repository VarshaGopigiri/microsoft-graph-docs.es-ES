# <a name="reportroot-getonedriveactivityuserdetail"></a><span data-ttu-id="9cbba-101">reportRoot: getOneDriveActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="9cbba-101">reportRoot: getOneDriveActivityUserDetail</span></span>

<span data-ttu-id="9cbba-102">Obtiene información sobre las actividades de OneDrive por usuario.</span><span class="sxs-lookup"><span data-stu-id="9cbba-102">Get details about OneDrive activity by user.</span></span>

> <span data-ttu-id="9cbba-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de OneDrive para la Empresa](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span><span class="sxs-lookup"><span data-stu-id="9cbba-103">**Note:** For details about different report views and names, see [Office 365 Reports - OneDrive for Business activity](https://support.office.com/client/OneDrive-for-Business-user-activity-8bbe4bf8-221b-46d6-99a5-2fb3c8ef9353).</span></span>

## <a name="permissions"></a><span data-ttu-id="9cbba-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="9cbba-104">Permissions</span></span>

<span data-ttu-id="9cbba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9cbba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="9cbba-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9cbba-107">Permission type</span></span>                        | <span data-ttu-id="9cbba-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9cbba-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="9cbba-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9cbba-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="9cbba-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="9cbba-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="9cbba-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9cbba-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9cbba-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9cbba-112">Not supported.</span></span>                           |
| <span data-ttu-id="9cbba-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9cbba-113">Application</span></span>                            | <span data-ttu-id="9cbba-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="9cbba-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="9cbba-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9cbba-115">HTTP request</span></span>

<!-- { "blockType": "samples" } --> 

```http
GET /reports/getOneDriveActivityUserDetail(period='{period_value}')
GET /reports/getOneDriveActivityUserDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="9cbba-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="9cbba-116">Function parameters</span></span>

<span data-ttu-id="9cbba-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="9cbba-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="9cbba-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9cbba-118">Parameter</span></span> | <span data-ttu-id="9cbba-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9cbba-119">Type</span></span>   | <span data-ttu-id="9cbba-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cbba-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="9cbba-121">period</span><span class="sxs-lookup"><span data-stu-id="9cbba-121">period</span></span>    | <span data-ttu-id="9cbba-122">cadena</span><span class="sxs-lookup"><span data-stu-id="9cbba-122">string</span></span> | <span data-ttu-id="9cbba-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9cbba-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="9cbba-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="9cbba-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="9cbba-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="9cbba-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="9cbba-126">date</span><span class="sxs-lookup"><span data-stu-id="9cbba-126">date</span></span>      | <span data-ttu-id="9cbba-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="9cbba-127">Date</span></span>   | <span data-ttu-id="9cbba-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="9cbba-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="9cbba-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="9cbba-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="9cbba-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="9cbba-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="9cbba-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="9cbba-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="9cbba-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cbba-132">Request headers</span></span>

| <span data-ttu-id="9cbba-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="9cbba-133">Name</span></span>          | <span data-ttu-id="9cbba-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cbba-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="9cbba-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="9cbba-135">Authorization</span></span> | <span data-ttu-id="9cbba-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9cbba-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="9cbba-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="9cbba-138">If-None-Match</span></span> | <span data-ttu-id="9cbba-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="9cbba-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="9cbba-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9cbba-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="9cbba-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cbba-141">Response</span></span>

<span data-ttu-id="9cbba-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="9cbba-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="9cbba-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cbba-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="9cbba-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="9cbba-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="9cbba-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="9cbba-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="9cbba-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="9cbba-146">Report Refresh Date</span></span>
- <span data-ttu-id="9cbba-147">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="9cbba-147">User Principal Name</span></span>
- <span data-ttu-id="9cbba-148">Eliminado</span><span class="sxs-lookup"><span data-stu-id="9cbba-148">Is Deleted</span></span>
- <span data-ttu-id="9cbba-149">Fecha de eliminación</span><span class="sxs-lookup"><span data-stu-id="9cbba-149">Deleted Date</span></span>
- <span data-ttu-id="9cbba-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="9cbba-150">Last Activity Date</span></span>
- <span data-ttu-id="9cbba-151">Número de archivos vistos o editados</span><span class="sxs-lookup"><span data-stu-id="9cbba-151">Viewed Or Edited File Count</span></span>
- <span data-ttu-id="9cbba-152">Número de archivos sincronizados</span><span class="sxs-lookup"><span data-stu-id="9cbba-152">Synced File Count</span></span>
- <span data-ttu-id="9cbba-153">Número de archivos compartidos internamente</span><span class="sxs-lookup"><span data-stu-id="9cbba-153">Shared Internally File Count</span></span>
- <span data-ttu-id="9cbba-154">Número de archivos compartidos externamente</span><span class="sxs-lookup"><span data-stu-id="9cbba-154">Shared Externally File Count</span></span>
- <span data-ttu-id="9cbba-155">Productos asignados</span><span class="sxs-lookup"><span data-stu-id="9cbba-155">Assigned Products</span></span>
- <span data-ttu-id="9cbba-156">Período del informe</span><span class="sxs-lookup"><span data-stu-id="9cbba-156">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="9cbba-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cbba-157">Example</span></span>

#### <a name="request"></a><span data-ttu-id="9cbba-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cbba-158">Request</span></span>

<span data-ttu-id="9cbba-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cbba-159">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getonedriveactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getOneDriveActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="9cbba-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cbba-160">Response</span></span>

<span data-ttu-id="9cbba-161">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cbba-161">The following is an example of the response.</span></span>

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

<span data-ttu-id="9cbba-162">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="9cbba-162">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Is Deleted,Deleted Date,Last Activity Date,Viewed Or Edited File Count,Synced File Count,Shared Internally File Count,Shared Externally File Count,Assigned Products,Report Period
```
