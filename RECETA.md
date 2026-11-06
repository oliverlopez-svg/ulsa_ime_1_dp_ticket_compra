# Receta: Ticket de compra

<!-- Escribe aquí tus recetas en pseudocódigo, ANTES de programar.
     Primero la receta del programa principal (main) y después una receta corta para cada módulo que vas a escribir tú.
     El primer paso de main es solo un ejemplo del formato; el resto es tuyo.
     Si las corriges después de probarlas a mano, deja aquí la versión final. -->

## Receta del programa principal (`main`)

<!-- Debe leerse casi igual que tu árbol de análisis descendente (sección 6 del README). -->

```text
## Receta del programa principal (`main`)

```text
1. Mostrar mensaje de bienvenida al sistema de ventas.
2. Pedir el nombre del producto y leerlo (utilizando utilerias.h).
3. Pedir el precio unitario y validar mediante un ciclo que sea mayor a 0.
4. Pedir la cantidad de piezas y validar mediante un ciclo que sea mayor a 0.
5. Pedir el porcentaje de descuento y validar mediante un ciclo que esté entre 0 y 100.
6. Calcular el subtotal llamando a la función calcularSubtotal(precio, cantidad).
7. Calcular el monto del descuento llamando a la función calcularPorcentaje(subtotal, descuentoPorc).
8. Obtener la base imponible restando el descuento al subtotal.
9. Calcular el IVA llamando a la función calcularPorcentaje(baseImponible, tasaIVA).
10. Calcular el total final sumando la base imponible y el IVA.
11. Llamar al procedimiento imprimirTicket con todos los valores calculados y los datos del producto.


```

## Recetas de los módulos

<!-- Para cada módulo: qué recibe, qué hace y qué devuelve. -->

### `calcularIVA`


  recibe: El monto sobre el cual se calculará el impuesto (base) y la tasa de IVA (ej. 16.0).
  Qué hace: Multiplica la base por la tasa dividida entre 100.
  Qué devuelve: El valor numérico del IVA.
  RETORNAR base * (tasa / 100.0)
FIN MODULO




### `imprimirTicket`

```text

MODULO imprimirTicket(nombreProd, precio, cantidad, descPorc, subtotal, montoDesc, iva, total)
  recibe: Todos los datos del producto, importes calculados y constantes de formato.
  Qué hace: Imprime la cabecera, los detalles del producto alineados con setw, los subtotales, totales y la firma del cajero.
  Qué devuelve: No devuelve nada (es un procedimiento).
  IMPRIMIR encabezado del ticket
  IMPRIMIR detalles del producto, cantidad y precio unitario
  IMPRIMIR línea divisoria
  IMPRIMIR subtotal, descuento aplicado, e IVA
  IMPRIMIR línea divisoria final
  IMPRIMIR total a pagar y la constante del cajero
FIN MODULO

FIN MODULO
```

### `calcularPorcentaje` (Fase 4)

```text
MODULO calcularPorcentaje(cantidadBase, porcentaje)
recibe: Una cantidad numérica base y el porcentaje que se desea aplicar.
hace: Aplica la regla de proporción matemática (base * porcentaje / 100).
devuelve: El resultado de la operación en formato decimal.
  RETORNAR cantidadBase * (porcentaje / 100.0)
FIN MODULO


FIN MODULO
```

### Otros módulos que agregues (por ejemplo, para tu reto)

```text

```
