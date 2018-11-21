# <a name="registrykeystate-resource-type"></a><span data-ttu-id="6a905-101">Tipo de recurso registryKeyState</span><span class="sxs-lookup"><span data-stu-id="6a905-101">registryKeyState resource type</span></span>

<span data-ttu-id="6a905-102">Contiene información acerca de los cambios clave del registro relacionados con la alerta y el proceso que ha cambiado las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="6a905-102">Contains information about registry key changes related to the alert, and the process that changed the registry keys.</span></span>

## <a name="properties"></a><span data-ttu-id="6a905-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a905-103">Properties</span></span>

| <span data-ttu-id="6a905-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a905-104">Property</span></span>     | <span data-ttu-id="6a905-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a905-105">Type</span></span>        | <span data-ttu-id="6a905-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a905-106">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="6a905-107">colmena</span><span class="sxs-lookup"><span data-stu-id="6a905-107">Hive</span></span>|<span data-ttu-id="6a905-108">registryHive</span><span class="sxs-lookup"><span data-stu-id="6a905-108">registryHive</span></span>|<span data-ttu-id="6a905-109">Una [colmena del registro de Windows](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives):</span><span class="sxs-lookup"><span data-stu-id="6a905-109">A [Windows registry hive](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-hives) :</span></span> <ul><li><span data-ttu-id="6a905-110">HKEY_CURRENT_CONFIG</span><span class="sxs-lookup"><span data-stu-id="6a905-110">HKEY_CURRENT_CONFIG</span></span></li> <li><span data-ttu-id="6a905-111">HKEY_CURRENT_USER</span><span class="sxs-lookup"><span data-stu-id="6a905-111">HKEY_CURRENT_USER</span></span></li> <li><span data-ttu-id="6a905-112">HKEY_LOCAL_MACHINE\SAM</span><span class="sxs-lookup"><span data-stu-id="6a905-112">HKEY_LOCAL_MACHINE\SAM</span></span></li> <li><span data-ttu-id="6a905-113">HKEY_LOCAL_MACHINE\Security</span><span class="sxs-lookup"><span data-stu-id="6a905-113">HKEY_LOCAL_MACHINE\Security</span></span></li> <li><span data-ttu-id="6a905-114">HKEY_LOCAL_MACHINE\Software</span><span class="sxs-lookup"><span data-stu-id="6a905-114">HKEY_LOCAL_MACHINE\Software</span></span></li> <li><span data-ttu-id="6a905-115">HKEY_LOCAL_MACHINE\System</span><span class="sxs-lookup"><span data-stu-id="6a905-115">HKEY_LOCAL_MACHINE\System</span></span></li> <li><span data-ttu-id="6a905-116">HKEY_USERS\\.Default.</span><span class="sxs-lookup"><span data-stu-id="6a905-116">HKEY_USERS\\.Default.</span></span></li></ul> <span data-ttu-id="6a905-117">Los valores posibles son: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem`, `usersDefault`.</span><span class="sxs-lookup"><span data-stu-id="6a905-117">Possible values are: `unknown`, `currentConfig`, `currentUser`, `localMachineSam`, `localMachineSamSoftware`, `localMachineSystem`, `usersDefault`.</span></span>|
|<span data-ttu-id="6a905-118">Key</span><span class="sxs-lookup"><span data-stu-id="6a905-118">key</span></span>|<span data-ttu-id="6a905-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-119">String</span></span>|<span data-ttu-id="6a905-120">Clave de registro actual (es decir, modificada) (excluye la COLMENA).</span><span class="sxs-lookup"><span data-stu-id="6a905-120">Current (i.e. changed) registry key (excludes HIVE).</span></span>|
|<span data-ttu-id="6a905-121">oldKey</span><span class="sxs-lookup"><span data-stu-id="6a905-121">oldKey</span></span>|<span data-ttu-id="6a905-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-122">String</span></span>|<span data-ttu-id="6a905-123">Clave de registro anterior (es decir, antes de que haya sido cambiada) (excluye la COLMENA).</span><span class="sxs-lookup"><span data-stu-id="6a905-123">Previous (i.e. before changed) registry key (excludes HIVE).</span></span>|
|<span data-ttu-id="6a905-124">oldValueData</span><span class="sxs-lookup"><span data-stu-id="6a905-124">oldValueData</span></span>|<span data-ttu-id="6a905-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-125">String</span></span>|<span data-ttu-id="6a905-126">Datos de valor (contenidos) de la clave de registro anterior (es decir, antes de que haya sido cambiada).</span><span class="sxs-lookup"><span data-stu-id="6a905-126">Previous (i.e. before changed) registry key value data (contents).</span></span>|
|<span data-ttu-id="6a905-127">oldValueName</span><span class="sxs-lookup"><span data-stu-id="6a905-127">oldValueName</span></span>|<span data-ttu-id="6a905-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-128">String</span></span>|<span data-ttu-id="6a905-129">Nombre de valor de la clave de registro anterior (es decir, antes de que haya sido cambiada)</span><span class="sxs-lookup"><span data-stu-id="6a905-129">Previous (i.e. before changed) registry key value name.</span></span>|
|<span data-ttu-id="6a905-130">operación</span><span class="sxs-lookup"><span data-stu-id="6a905-130">operation</span></span>|<span data-ttu-id="6a905-131">registryOperation</span><span class="sxs-lookup"><span data-stu-id="6a905-131">registryOperation</span></span>|<span data-ttu-id="6a905-132">Operación que ha cambiado el nombre y/ valor de la clave de registro.</span><span class="sxs-lookup"><span data-stu-id="6a905-132">Operation that changed the registry key name and/or value.</span></span> <span data-ttu-id="6a905-133">Los valores posibles son: `unknown`, `create`, `modify` y `delete`.</span><span class="sxs-lookup"><span data-stu-id="6a905-133">Possible values are: `unknown`, `create`, `modify`, `delete`.</span></span>|
|<span data-ttu-id="6a905-134">processId</span><span class="sxs-lookup"><span data-stu-id="6a905-134">processId</span></span>|<span data-ttu-id="6a905-135">Int32</span><span class="sxs-lookup"><span data-stu-id="6a905-135">Int32</span></span>|<span data-ttu-id="6a905-136">Identificador del proceso (PID) del proceso que modifica la clave de registro (los detalles del proceso aparecerán en la colección 'procesos' de alerta).</span><span class="sxs-lookup"><span data-stu-id="6a905-136">Process ID (PID) of the process that modified the registry key (process details will appear in the alert 'processes' collection).</span></span>|
|<span data-ttu-id="6a905-137">valueData</span><span class="sxs-lookup"><span data-stu-id="6a905-137">valueData</span></span>|<span data-ttu-id="6a905-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-138">String</span></span>|<span data-ttu-id="6a905-139">Datos de valor (contenidos) de la clave de registro actual (es decir, cambiados).</span><span class="sxs-lookup"><span data-stu-id="6a905-139">Current (i.e. changed) registry key value data (contents).</span></span>|
|<span data-ttu-id="6a905-140">valueName</span><span class="sxs-lookup"><span data-stu-id="6a905-140">valueName</span></span>|<span data-ttu-id="6a905-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="6a905-141">String</span></span>|<span data-ttu-id="6a905-142">Nombre de valor de la clave de registro actual (es decir, cambiado)</span><span class="sxs-lookup"><span data-stu-id="6a905-142">Current (i.e. changed) registry key value name</span></span>|
|<span data-ttu-id="6a905-143">valueType</span><span class="sxs-lookup"><span data-stu-id="6a905-143">valueType</span></span>|<span data-ttu-id="6a905-144">registryValueType</span><span class="sxs-lookup"><span data-stu-id="6a905-144">registryValueType</span></span>|[<span data-ttu-id="6a905-145">Tipo del valor de la clave de registro</span><span class="sxs-lookup"><span data-stu-id="6a905-145">Registry key value type</span></span>](https://docs.microsoft.com/en-us/windows/desktop/sysinfo/registry-value-types) <ul><li><span data-ttu-id="6a905-146">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="6a905-146">REG_BINARY</span></span></li> <li><span data-ttu-id="6a905-147">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="6a905-147">REG_DWORD</span></span></li> <li><span data-ttu-id="6a905-148">REG_DWORD_LITTLE_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6a905-148">REG_DWORD_LITTLE_ENDIAN</span></span></li> <li><span data-ttu-id="6a905-149">REG_DWORD_BIG_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6a905-149">REG_DWORD_BIG_ENDIAN</span></span></li><li><span data-ttu-id="6a905-150">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="6a905-150">REG_EXPAND_SZ</span></span></li> <li><span data-ttu-id="6a905-151">REG_LINK</span><span class="sxs-lookup"><span data-stu-id="6a905-151">REG_LINK</span></span></li> <li><span data-ttu-id="6a905-152">REG_MULTI_SZ</span><span class="sxs-lookup"><span data-stu-id="6a905-152">REG_MULTI_SZ</span></span></li> <li><span data-ttu-id="6a905-153">REG_NONE</span><span class="sxs-lookup"><span data-stu-id="6a905-153">REG_NONE</span></span></li> <li><span data-ttu-id="6a905-154">REG_QWORD</span><span class="sxs-lookup"><span data-stu-id="6a905-154">REG_QWORD</span></span></li> <li><span data-ttu-id="6a905-155">REG_QWORD_LITTLE_ENDIAN</span><span class="sxs-lookup"><span data-stu-id="6a905-155">REG_QWORD_LITTLE_ENDIAN</span></span></li> <li><span data-ttu-id="6a905-156">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="6a905-156">REG_SZ</span></span></li></ul> <span data-ttu-id="6a905-157">Los valores posibles son: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian` y `sz`.</span><span class="sxs-lookup"><span data-stu-id="6a905-157">Possible values are: `unknown`, `binary`, `dword`, `dwordLittleEndian`, `dwordBigEndian`, `expandSz`, `link`, `multiSz`, `none`, `qword`, `qwordlittleEndian`, `sz`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6a905-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a905-158">JSON representation</span></span>

<span data-ttu-id="6a905-159">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6a905-159">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.registryKeyState"
}-->

```json
{
  "hive": "@odata.type: microsoft.graph.registryHive",
  "key": "String",
  "oldKey": "String",
  "oldValueData": "String",
  "oldValueName": "String",
  "operation": "@odata.type: microsoft.graph.registryOperation",
  "processId": 1024,
  "valueData": "String",
  "valueName": "String",
  "valueType": "@odata.type: microsoft.graph.registryValueType"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "registryKeyState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->