# <a name="reportroot-getyammergroupsactivitydetail"></a><span data-ttu-id="8253d-101">reportRoot: getYammerGroupsActivityDetail</span><span class="sxs-lookup"><span data-stu-id="8253d-101">reportRoot: getYammerGroupsActivityDetail</span></span>

<span data-ttu-id="8253d-102">Obtiene información sobre la actividad de grupos de Yammer por grupo.</span><span class="sxs-lookup"><span data-stu-id="8253d-102">Get details about Yammer groups activity by group.</span></span>

> <span data-ttu-id="8253d-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="8253d-103">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="8253d-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8253d-104">Permissions</span></span>

<span data-ttu-id="8253d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8253d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="8253d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8253d-107">Permission type</span></span>                        | <span data-ttu-id="8253d-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8253d-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="8253d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8253d-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="8253d-110">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="8253d-110">Reports.Read.All</span></span>                         |
| <span data-ttu-id="8253d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8253d-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8253d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8253d-112">Not supported.</span></span>                           |
| <span data-ttu-id="8253d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8253d-113">Application</span></span>                            | <span data-ttu-id="8253d-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="8253d-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="8253d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8253d-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityDetail(period='{period_value}')
GET /reports/getYammerGroupsActivityDetail(date={date_value})
```

## <a name="function-parameters"></a><span data-ttu-id="8253d-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="8253d-116">Function parameters</span></span>

<span data-ttu-id="8253d-117">En la URL de la solicitud, especifique uno de los parámetros siguientes con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="8253d-117">In the request URL, provide one of the following parameters with a valid value.</span></span>

| <span data-ttu-id="8253d-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8253d-118">Parameter</span></span> | <span data-ttu-id="8253d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="8253d-119">Type</span></span>   | <span data-ttu-id="8253d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8253d-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="8253d-121">period</span><span class="sxs-lookup"><span data-stu-id="8253d-121">period</span></span>    | <span data-ttu-id="8253d-122">cadena</span><span class="sxs-lookup"><span data-stu-id="8253d-122">string</span></span> | <span data-ttu-id="8253d-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="8253d-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="8253d-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="8253d-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="8253d-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante los que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="8253d-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="8253d-126">date</span><span class="sxs-lookup"><span data-stu-id="8253d-126">date</span></span>      | <span data-ttu-id="8253d-127">Fecha</span><span class="sxs-lookup"><span data-stu-id="8253d-127">Date</span></span>   | <span data-ttu-id="8253d-128">Especifica la fecha en que quiere ver los usuarios que realizaron alguna actividad.</span><span class="sxs-lookup"><span data-stu-id="8253d-128">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="8253d-129">{date_value} necesita tener el formato de AAAA-MM-DD.</span><span class="sxs-lookup"><span data-stu-id="8253d-129">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="8253d-130">Como este informe solo está disponible para los últimos 30 días, {date_value} tiene que ser una fecha de ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="8253d-130">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="8253d-131">**Nota:** Necesita establecer un período o una fecha en la URL.</span><span class="sxs-lookup"><span data-stu-id="8253d-131">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="8253d-132">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8253d-132">Request headers</span></span>

| <span data-ttu-id="8253d-133">Nombre</span><span class="sxs-lookup"><span data-stu-id="8253d-133">Name</span></span>          | <span data-ttu-id="8253d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="8253d-134">Description</span></span>                              |
| :------------ | :--------------------------------------- |
| <span data-ttu-id="8253d-135">Autorización</span><span class="sxs-lookup"><span data-stu-id="8253d-135">Authorization</span></span> | <span data-ttu-id="8253d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8253d-p104">Bearer {token}. Required.</span></span>                |
| <span data-ttu-id="8253d-138">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="8253d-138">If-None-Match</span></span> | <span data-ttu-id="8253d-139">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="8253d-139">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="8253d-140">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8253d-140">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="8253d-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8253d-141">Response</span></span>

<span data-ttu-id="8253d-142">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="8253d-142">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="8253d-143">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8253d-143">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="8253d-144">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="8253d-144">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="8253d-145">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="8253d-145">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="8253d-146">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="8253d-146">Report Refresh Date</span></span>
- <span data-ttu-id="8253d-147">Nombre para mostrar del grupo</span><span class="sxs-lookup"><span data-stu-id="8253d-147">Group Display Name</span></span>
- <span data-ttu-id="8253d-148">Eliminado</span><span class="sxs-lookup"><span data-stu-id="8253d-148">Is Deleted</span></span>
- <span data-ttu-id="8253d-149">Nombre principal de propietario</span><span class="sxs-lookup"><span data-stu-id="8253d-149">Owner Principal Name</span></span>
- <span data-ttu-id="8253d-150">Fecha de la última actividad</span><span class="sxs-lookup"><span data-stu-id="8253d-150">Last Activity Date</span></span>
- <span data-ttu-id="8253d-151">Tipo de grupo</span><span class="sxs-lookup"><span data-stu-id="8253d-151">Group Type</span></span>
- <span data-ttu-id="8253d-152">Office 365 conectado</span><span class="sxs-lookup"><span data-stu-id="8253d-152">Office 365 Connected</span></span>
- <span data-ttu-id="8253d-153">Número de miembros</span><span class="sxs-lookup"><span data-stu-id="8253d-153">Member Count</span></span>
- <span data-ttu-id="8253d-154">Número de publicaciones</span><span class="sxs-lookup"><span data-stu-id="8253d-154">Posted Count</span></span>
- <span data-ttu-id="8253d-155">Número de lecturas</span><span class="sxs-lookup"><span data-stu-id="8253d-155">Read Count</span></span>
- <span data-ttu-id="8253d-156">Número de etiquetados como “Me gusta”</span><span class="sxs-lookup"><span data-stu-id="8253d-156">Liked Count</span></span>
- <span data-ttu-id="8253d-157">Período del informe</span><span class="sxs-lookup"><span data-stu-id="8253d-157">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="8253d-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8253d-158">Example</span></span>

#### <a name="request"></a><span data-ttu-id="8253d-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8253d-159">Request</span></span>

<span data-ttu-id="8253d-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8253d-160">The following is an example of the request.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammergroupsactivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerGroupsActivityDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="8253d-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8253d-161">Response</span></span>

<span data-ttu-id="8253d-162">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8253d-162">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

#### <a name="request"></a><span data-ttu-id="8253d-163">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8253d-163">Request</span></span>
<span data-ttu-id="8253d-164">Si se le llama con un `date`, el ámbito del informe se limita a la actividad en la fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="8253d-164">If called with the `date` parameter, the report is scoped to usage on the given date.</span></span>

<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "reportroot_getyammergroupsactivityuserdetail_date"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerGroupsActivityDetail(date='2018-03-05')
```

#### <a name="response"></a><span data-ttu-id="8253d-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8253d-165">Response</span></span>

<span data-ttu-id="8253d-166">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8253d-166">The following is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.report" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="8253d-167">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="8253d-167">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "ignored"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Group Display Name,Is Deleted,Owner Principal Name,Last Activity Date,Group Type,Office 365 Connected,Member Count,Posted Count,Read Count,Liked Count,Report Period
```
