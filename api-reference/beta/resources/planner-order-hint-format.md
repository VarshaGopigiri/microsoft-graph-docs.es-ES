---
title: Uso de sugerencias de orden en Planner
description: '`)'
ms.openlocfilehash: b7edbcc22a297fc30a98c337daed266b2e599c70
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083266"
---
# <a name="using-order-hints-in-planner"></a><span data-ttu-id="d6c06-103">Uso de sugerencias de orden en Planner</span><span class="sxs-lookup"><span data-stu-id="d6c06-103">Using order hints in Planner</span></span>

> <span data-ttu-id="d6c06-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d6c06-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d6c06-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d6c06-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d6c06-p102">Los objetos de Planner identifican sus criterios de ordenación por sugerencias de ordenación. Los valores de sugerencias de ordenación son cadenas. Los clientes pueden ordenar las cadenas basándose en el valor ordinal de su caracteres para identificar el orden de los elementos. Se comparan los caracteres desde el principio de la cadena hasta que se detecta una diferencia en los valores ordinales de caracteres o termina una cadena, en cuyo caso se colocará la cadena más corta antes que la más larga. Los valores pueden contener cualquier carácter entre ordinales 32 (espacio) y 126 (`~`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-p102">Objects in Planner identify their sort order by order hints. The order hint values are strings. The clients can sort the strings based on ordinal value of characters in them to identify the order of items. The characters are compared from the beginning of the string, until a difference is encountered in the ordinal values of characters, or one string ends, in which case the shorter string would be sorted before the longer. The values can contain any character between ordinals 32 (space) and 126 (`~`)</span></span>

<span data-ttu-id="d6c06-p103">Por ejemplo, un elemento con la sugerencia de ordenación `a` (valor ordinal 97) se colocaría antes que otro con la sugerencia de ordenación `z` (valor ordinal 122). Por ejemplo, un elemento con la sugerencia de ordenación `abc` (valores ordinales 97, 98 y 99) se colocaría antes que otro con la sugerencia de ordenación `abd` (valores ordinales 97, 98, 100). Un elemento con la sugerencia de ordenación `a` se colocaría antes que otro con la sugerencia de ordenación `ab` puesto que todos los caracteres existentes son los mismos, y `a` es más corta.</span><span class="sxs-lookup"><span data-stu-id="d6c06-p103">As an example, an item with order hint `a` (ordinal value 97) would be placed before another item with order hint `z` (ordinal value 122). An item with order hint `abc` (ordinal values 97, 98, 99), would be placed before another item with order hint `abd` (ordinal values 97, 98, 100). An item with order hint `a` would be placed before another item with order hint `ab` since all existing characters are the same, and `a` is shorter.</span></span>

<span data-ttu-id="d6c06-p104">Se calculan los valores de todas las sugerencias de ordenación por el servicio. Para reordenar elementos, el cliente puede especificar la sugerencia de ordenación para el elemento que se ha movido entre dos elementos. Para ello, debe establecer la sugerencia de ordenación en el valor siguiente: `<previous order hint> <next order hint>!`, donde `<previous order hint>` debe sustituirse por la sugerencia de ordenación del elemento que precede a la nueva ubicación deseada y `<next order hint>` debe sustituirse por la sugerencia de ordenación del elemento que viene después de la nueva localización deseada. Hay un carácter de espacio entre estos valores de sugerencia de ordenación, y el valor completo se añade como sufijo con `!`. Si un elemento no está presente, debe utilizarse una cadena vacía en su lugar. Este valor también puede estar compuesto de cálculos previos y puede utilizarse en el cliente para ordenar elementos de forma exacta como el servicio que devuelve sugerencias de ordenación. Una vez que el cliente envía estos valores en una actualización, el servicio calculará un valor pequeño que ordene en la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="d6c06-p104">The values for all order hints are calculated by the service. The client can reorder items by specifying the order hint for the item that got moved between two items with by setting the order hint to the following value: `<previous order hint> <next order hint>!`, where `<previous order hint>` is to be replaced by the order hint of the item that comes before the new desired location, and `<next order hint>` is to be replaced by the order hint of the item that comes after the new desired location. There is a space character between these order hint values, and the entire value is suffixed with `!`. If either item isn't present, empty string should be used instead. This value can also be composed of previous calculations, and can be used in the client to sort items exactly like service returned order hints. Once the client sends these values in an update, the service will calculate a short value that sorts in the desired location.</span></span>

> <span data-ttu-id="d6c06-120">**Nota:** En los ejemplos siguientes, los valores de sugerencia de orden real rodeados en caracteres de comillas simples (`'`) para mayor claridad, sin embargo estos no forman parte de los datos y no se debe enviar al servicio.</span><span class="sxs-lookup"><span data-stu-id="d6c06-120">**Note:** In the following examples, the actual order hint values are surrounded in single quote characters (`'`) for clarity, however these are not part of the data, and must not be sent to the service.</span></span>
 
<span data-ttu-id="d6c06-121">Como ejemplo, considere la siguiente lista de sugerencias de ordenación ya ordenadas:</span><span class="sxs-lookup"><span data-stu-id="d6c06-121">As an example, consider the following list of sorted order hints:</span></span>

1. <span data-ttu-id="d6c06-122">Elemento 1 (sugerencia de ordenación: `'5637'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-122">Item 1 (Order Hint: `'5637'`)</span></span>
2. <span data-ttu-id="d6c06-123">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-123">Item 2 (Order Hint: `'adhg'`)</span></span>

<span data-ttu-id="d6c06-124">Colocar un elemento 3 antes del elemento 1, después, colocar un elemento 4 entre los elementos 1 y 2 y, luego, colocar un elemento 5 después de un elemento 2 crearía las siguientes sugerencias de ordenación en el cliente.</span><span class="sxs-lookup"><span data-stu-id="d6c06-124">Placing an Item 3 before Item 1, then placing item 4 between Item 1 and Item 2, and then placing item 5 after Item 2, would create the following order hints on the client.</span></span> 

1. <span data-ttu-id="d6c06-125">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-125">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="d6c06-126">Elemento 1 (sugerencia de ordenación: `'5637'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-126">Item 1 (Order Hint: `'5637'`)</span></span>
3. <span data-ttu-id="d6c06-127">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-127">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
4. <span data-ttu-id="d6c06-128">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-128">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="d6c06-129">Elemento 5 (sugerencia de ordenación: `'adhg !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-129">Item 5 (Order Hint: `'adhg !'`)</span></span>

<span data-ttu-id="d6c06-130">A continuación, mover un elemento 1 al final de la lista generaría:</span><span class="sxs-lookup"><span data-stu-id="d6c06-130">Then, moving item 1 to the end of the list would generate:</span></span>

1. <span data-ttu-id="d6c06-131">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-131">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="d6c06-132">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-132">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
3. <span data-ttu-id="d6c06-133">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-133">Item 2 (Order Hint: `'adhg'`)</span></span>
4. <span data-ttu-id="d6c06-134">Elemento 5 (sugerencia de ordenación: `'adhg !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-134">Item 5 (Order Hint: `'adhg !'`)</span></span>
5. <span data-ttu-id="d6c06-135">Elemento 1 (sugerencia de ordenación: `'adhg ! !'`) </span><span class="sxs-lookup"><span data-stu-id="d6c06-135">Item 1 (Order Hint: `'adhg ! !'`)</span></span>

<span data-ttu-id="d6c06-136">Finalmente, mover un elemento 5 entre los elementos 3 y 4 generaría:</span><span class="sxs-lookup"><span data-stu-id="d6c06-136">Finally moving Item 5 between Item 3 and Item 4 would generate:</span></span>

1. <span data-ttu-id="d6c06-137">Elemento 3 (sugerencia de ordenación: `' 5637!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-137">Item 3 (Order Hint: `' 5637!'`)</span></span>
2. <span data-ttu-id="d6c06-138">Elemento 5 (sugerencia de ordenación: `' 5637! 5637 adhg!!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-138">Item 5 (Order Hint: `' 5637! 5637 adhg!!'`)</span></span>
3. <span data-ttu-id="d6c06-139">Elemento 4 (sugerencia de ordenación: `'5637 adhg!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-139">Item 4 (Order Hint: `'5637 adhg!'`)</span></span>
4. <span data-ttu-id="d6c06-140">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-140">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="d6c06-141">Elemento 1 (sugerencia de ordenación: `'adhg ! !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-141">Item 1 (Order Hint: `'adhg ! !'`)</span></span>

<span data-ttu-id="d6c06-142">Cuando estos cambios a los valores de sugerencia de orden se envían al servicio de las solicitudes de revisión, el servicio calcularán los valores adecuados que mantener el orden previsto por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d6c06-142">When these changes to order hint values are sent to the service in patch requests, the service will calculate proper values that keep the order intended by the client.</span></span> <span data-ttu-id="d6c06-143">El cliente puede obtener la if inmediato valores el `Prefer: return=representation` encabezado de preferencia se especifica en el `PATCH` las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="d6c06-143">The client can obtain the values immediate if the `Prefer: return=representation` preference header is specified in the `PATCH` requests.</span></span> <span data-ttu-id="d6c06-144">Los valores para el caso anterior pueden tener la apariencia siguiente (los valores reales pueden diferir).</span><span class="sxs-lookup"><span data-stu-id="d6c06-144">The values for the case above may look like the following (the actual values may differ).</span></span> 

1. <span data-ttu-id="d6c06-145">Elemento 3 (sugerencia de ordenación: `'432b'`) </span><span class="sxs-lookup"><span data-stu-id="d6c06-145">Item 3 (Order Hint: `'432b'`)</span></span>
2. <span data-ttu-id="d6c06-146">Elemento 5 (sugerencia de ordenación: `'6F"#'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-146">Item 5 (Order Hint: `'6F"#'`)</span></span>
3. <span data-ttu-id="d6c06-147">Elemento 4 (sugerencia de ordenación: `'7A$6'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-147">Item 4 (Order Hint: `'7A$6'`)</span></span>
4. <span data-ttu-id="d6c06-148">Elemento 2 (sugerencia de ordenación: `'adhg'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-148">Item 2 (Order Hint: `'adhg'`)</span></span>
5. <span data-ttu-id="d6c06-149">Elemento 1 (sugerencia de ordenación: `'de5%'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-149">Item 1 (Order Hint: `'de5%'`)</span></span>

<span data-ttu-id="d6c06-p106">Se pueden especificar las sugerencias de ordenación para crear el primer elemento en la lista como ` !`, puesto que en este caso no existe ni un elemento anterior ni uno posterior. Sin embargo, esto no es necesario dado que el servicio generará automáticamente todos los valores de sugerencia de ordenación de elementos si no se especifican durante la creación del elemento. El ejemplo siguiente muestra que las sugerencias de ordenación se deben utilizar al colocar elementos en una lista previamente vacía. Agregue el primer elemento:</span><span class="sxs-lookup"><span data-stu-id="d6c06-p106">Order Hints can be specified for creating the first item in the list as ` !`, since neither a previous or a next item exists in that case, however this is unnecessary, as the service will auto-generate values for all order hint values on items if they are not specified during creation of the item. Following example illustrates the order hints should be used when placing items in a previously empty list. Add the first item:</span></span>

1. <span data-ttu-id="d6c06-153">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-153">Item 1 (Order Hint: `' !'`)</span></span>

<span data-ttu-id="d6c06-154">Agregue el segundo elemento en la parte superior:</span><span class="sxs-lookup"><span data-stu-id="d6c06-154">Add the second item to top:</span></span>

1. <span data-ttu-id="d6c06-155">Elemento 2 (sugerencia de ordenación: `'  !!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-155">Item 2 (Order Hint: `'  !!'`)</span></span>
2. <span data-ttu-id="d6c06-156">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-156">Item 1 (Order Hint: `' !'`)</span></span>

<span data-ttu-id="d6c06-157">Agregar el tercer elemento en la parte inferior:</span><span class="sxs-lookup"><span data-stu-id="d6c06-157">Add the third item to bottom:</span></span>

1. <span data-ttu-id="d6c06-158">Elemento 2 (sugerencia de ordenación: `'  !!'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-158">Item 2 (Order Hint: `'  !!'`)</span></span>
2. <span data-ttu-id="d6c06-159">Elemento 1 (sugerencia de ordenación: `' !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-159">Item 1 (Order Hint: `' !'`)</span></span>
3. <span data-ttu-id="d6c06-160">Elemento 3 (sugerencia de ordenación: `' ! !'`)</span><span class="sxs-lookup"><span data-stu-id="d6c06-160">Item 3 (Order Hint: `' ! !'`)</span></span>







