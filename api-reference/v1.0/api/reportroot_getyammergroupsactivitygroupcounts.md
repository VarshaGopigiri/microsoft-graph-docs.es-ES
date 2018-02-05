# <a name="reportroot-getyammergroupsactivitygroupcounts"></a><span data-ttu-id="378f0-101">reportRoot: getYammerGroupsActivityGroupCounts</span><span class="sxs-lookup"><span data-stu-id="378f0-101">reportRoot: getYammerGroupsActivityGroupCounts</span></span>

<span data-ttu-id="378f0-102">Obtiene el número total de grupos que existen y en cuántos se incluyeron actividades de conversaciones de grupo.</span><span class="sxs-lookup"><span data-stu-id="378f0-102">Get the total number of groups that existed and how many included group conversation activity.</span></span>

> <span data-ttu-id="378f0-103">**Nota:** Para obtener información sobre los diferentes nombres de informes y vistas de informes, vea [Informes de Office 365: Actividad de grupos de Yammer](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span><span class="sxs-lookup"><span data-stu-id="378f0-103">**Note:** For details about different report views and names, see [Office 365 Reports - Yammer groups activity](https://support.office.com/client/Yammer-groups-activity-report-94dd92ec-ea73-43c6-b51f-2a11fd78aa31).</span></span>

## <a name="permissions"></a><span data-ttu-id="378f0-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="378f0-104">Permissions</span></span>

<span data-ttu-id="378f0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="378f0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="378f0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="378f0-107">Permission type</span></span>                        | <span data-ttu-id="378f0-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="378f0-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="378f0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="378f0-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="378f0-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="378f0-110">Not supported.</span></span>                           |
| <span data-ttu-id="378f0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="378f0-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="378f0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="378f0-112">Not supported.</span></span>                           |
| <span data-ttu-id="378f0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="378f0-113">Application</span></span>                            | <span data-ttu-id="378f0-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="378f0-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="378f0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="378f0-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getYammerGroupsActivityGroupCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="378f0-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="378f0-116">Request parameters</span></span>

<span data-ttu-id="378f0-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="378f0-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="378f0-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="378f0-118">Parameter</span></span> | <span data-ttu-id="378f0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="378f0-119">Type</span></span>   | <span data-ttu-id="378f0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="378f0-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="378f0-121">period</span><span class="sxs-lookup"><span data-stu-id="378f0-121">period</span></span>    | <span data-ttu-id="378f0-122">cadena</span><span class="sxs-lookup"><span data-stu-id="378f0-122">string</span></span> | <span data-ttu-id="378f0-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="378f0-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="378f0-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="378f0-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="378f0-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="378f0-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="378f0-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="378f0-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="378f0-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="378f0-127">Request headers</span></span>

| <span data-ttu-id="378f0-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="378f0-128">Name</span></span>          | <span data-ttu-id="378f0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="378f0-129">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="378f0-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="378f0-130">Authorization</span></span> | <span data-ttu-id="378f0-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="378f0-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="378f0-133">If-None-Match</span><span class="sxs-lookup"><span data-stu-id="378f0-133">If-None-Match</span></span> | <span data-ttu-id="378f0-134">Si se incluye el encabezado de la solicitud y la eTag proporcionada coincide con la etiqueta actual del archivo, se devuelve un código de respuesta `304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="378f0-134">If this request header is included and the eTag provided matches the current tag on the file, a `304 Not Modified` response code is returned.</span></span> <span data-ttu-id="378f0-135">Opcional.</span><span class="sxs-lookup"><span data-stu-id="378f0-135">Optional.</span></span> |

## <a name="response"></a><span data-ttu-id="378f0-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="378f0-136">Response</span></span>

<span data-ttu-id="378f0-137">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="378f0-137">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="378f0-138">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="378f0-138">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="378f0-139">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="378f0-139">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="378f0-140">El archivo CSV tiene los siguientes encabezados de columna.</span><span class="sxs-lookup"><span data-stu-id="378f0-140">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="378f0-141">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="378f0-141">Report Refresh Date</span></span>
- <span data-ttu-id="378f0-142">Total</span><span class="sxs-lookup"><span data-stu-id="378f0-142">Total</span></span>
- <span data-ttu-id="378f0-143">Activo</span><span class="sxs-lookup"><span data-stu-id="378f0-143">Active</span></span>
- <span data-ttu-id="378f0-144">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="378f0-144">Report Date</span></span>
- <span data-ttu-id="378f0-145">Período del informe</span><span class="sxs-lookup"><span data-stu-id="378f0-145">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="378f0-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="378f0-146">Example</span></span>

#### <a name="request"></a><span data-ttu-id="378f0-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="378f0-147">Request</span></span>

<span data-ttu-id="378f0-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="378f0-148">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getyammergroupsactivitygroupcounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getYammerGroupsActivityGroupCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="378f0-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="378f0-149">Response</span></span>

<span data-ttu-id="378f0-150">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="378f0-150">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="378f0-151">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="378f0-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Total,Active,Report Date,Report Period
```
