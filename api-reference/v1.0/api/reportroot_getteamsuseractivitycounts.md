# <a name="reportroot-getteamsuseractivitycounts"></a><span data-ttu-id="0be0e-101">reportRoot: getTeamsUserActivityCounts</span><span class="sxs-lookup"><span data-stu-id="0be0e-101">reportRoot: getTeamsUserActivityCounts</span></span>

<span data-ttu-id="0be0e-102">Obtener el número de actividades de Microsoft Teams por tipo de actividad.</span><span class="sxs-lookup"><span data-stu-id="0be0e-102">Get the number of Microsoft Teams activities by activity type.</span></span> <span data-ttu-id="0be0e-103">Los tipos de actividad son mensajes de chat, mensajes privados de chat, llamadas o reuniones de equipo.</span><span class="sxs-lookup"><span data-stu-id="0be0e-103">The activity types are team chat messages, private chat messages, calls, and meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="0be0e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="0be0e-104">Permissions</span></span>

<span data-ttu-id="0be0e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0be0e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="0be0e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0be0e-107">Permission type</span></span>                        | <span data-ttu-id="0be0e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0be0e-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="0be0e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0be0e-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="0be0e-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0be0e-110">Not supported.</span></span>                           |
| <span data-ttu-id="0be0e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0be0e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0be0e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0be0e-112">Not supported.</span></span>                           |
| <span data-ttu-id="0be0e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0be0e-113">Application</span></span>                            | <span data-ttu-id="0be0e-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="0be0e-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="0be0e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0be0e-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="0be0e-116">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0be0e-116">Request parameters</span></span>

<span data-ttu-id="0be0e-117">En la URL de la solicitud, especifique el siguiente parámetro de consulta con un valor válido.</span><span class="sxs-lookup"><span data-stu-id="0be0e-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="0be0e-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0be0e-118">Parameter</span></span> | <span data-ttu-id="0be0e-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="0be0e-119">Type</span></span>   | <span data-ttu-id="0be0e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0be0e-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="0be0e-121">period</span><span class="sxs-lookup"><span data-stu-id="0be0e-121">period</span></span>    | <span data-ttu-id="0be0e-122">cadena</span><span class="sxs-lookup"><span data-stu-id="0be0e-122">string</span></span> | <span data-ttu-id="0be0e-123">Especifica la duración de tiempo durante la que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0be0e-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="0be0e-124">Los valores admitidos para {period_value} son: D7, D30, D90 y D180.</span><span class="sxs-lookup"><span data-stu-id="0be0e-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="0be0e-125">Estos valores tienen el formato D*n*, donde *n* representa el número de días durante el que se agrega el informe.</span><span class="sxs-lookup"><span data-stu-id="0be0e-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="0be0e-126">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0be0e-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="0be0e-127">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0be0e-127">Request headers</span></span>

| <span data-ttu-id="0be0e-128">Nombre</span><span class="sxs-lookup"><span data-stu-id="0be0e-128">Name</span></span>          | <span data-ttu-id="0be0e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="0be0e-129">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="0be0e-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="0be0e-130">Authorization</span></span> | <span data-ttu-id="0be0e-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0be0e-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="0be0e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0be0e-133">Response</span></span>

<span data-ttu-id="0be0e-134">Si se ejecuta correctamente, este método devuelve una respuesta `302 Found` que redirige a una URL de descarga con autenticación previa para el informe.</span><span class="sxs-lookup"><span data-stu-id="0be0e-134">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="0be0e-135">La URL se encuentra en el encabezado `Location` de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0be0e-135">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="0be0e-136">Las URL de descarga con autenticación previa solo son válidas durante un breve período de tiempo (unos minutos) y no necesitan un encabezado `Authorization` para descargarlas.</span><span class="sxs-lookup"><span data-stu-id="0be0e-136">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="0be0e-137">El archivo CSV tiene los siguientes encabezados de columna:</span><span class="sxs-lookup"><span data-stu-id="0be0e-137">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="0be0e-138">Fecha de actualización del informe</span><span class="sxs-lookup"><span data-stu-id="0be0e-138">Report Refresh Date</span></span>
- <span data-ttu-id="0be0e-139">Fecha del informe</span><span class="sxs-lookup"><span data-stu-id="0be0e-139">Report Date</span></span>
- <span data-ttu-id="0be0e-140">Mensajes de chat del equipo</span><span class="sxs-lookup"><span data-stu-id="0be0e-140">Team Chat Messages</span></span>
- <span data-ttu-id="0be0e-141">Mensajes de chat privados</span><span class="sxs-lookup"><span data-stu-id="0be0e-141">Private Chat Messages</span></span>
- <span data-ttu-id="0be0e-142">Llamadas</span><span class="sxs-lookup"><span data-stu-id="0be0e-142">API Calls</span></span>
- <span data-ttu-id="0be0e-143">Reuniones</span><span class="sxs-lookup"><span data-stu-id="0be0e-143">meetings</span></span>
- <span data-ttu-id="0be0e-144">Período del informe</span><span class="sxs-lookup"><span data-stu-id="0be0e-144">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="0be0e-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0be0e-145">Example</span></span>

#### <a name="request"></a><span data-ttu-id="0be0e-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0be0e-146">Request</span></span>

<span data-ttu-id="0be0e-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0be0e-147">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivitycounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="0be0e-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0be0e-148">Response</span></span>

<span data-ttu-id="0be0e-149">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0be0e-149">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```
<span data-ttu-id="0be0e-150">Siga el redireccionamiento 302 y el archivo CSV descargado tendrá el esquema siguiente.</span><span class="sxs-lookup"><span data-stu-id="0be0e-150">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Report Period
```
