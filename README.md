
# 💻 Reto Integrador: Sistema de Auditoría para Tienda de Hardware

**Contexto:** Gestión administrativa y ventas de componentes de computadora.

Una tienda local de tecnología necesita digitalizar el corte de caja de sus vendedores. Actualmente, los empleados cometen errores al sumar las facturas al final del día y al calcular los impuestos de componentes individuales.

### 📝 Descripción del Problema

Desarrolla una herramienta de consola que automatice la auditoría de ventas diarias y cuente con una calculadora de impuestos integrada.

**Requerimientos del Sistema (Reglas de Negocio):**

1. **Panel Principal🎛️:** El programa debe arrancar mostrando un menú de opciones (1. Auditar Facturas, 2. Calculadora de Impuestos, 3. Cerrar Turno). Este panel debe garantizar que se muestre al menos una vez al abrir el programa y debe mantenerse activo, reapareciendo después de cada operación, hasta que el empleado seleccione la opción de "Cerrar Turno".
   
2. **Módulo de Auditoría (Opción 1)🔍💰:** El sistema debe preguntar cuántas facturas se emitieron durante el día. Con base en ese número exacto, el programa solicitará de manera secuencial y estructurada el total cobrado en cada una de esas facturas, sumándolas en tiempo real para emitir el corte de caja total al terminar el conteo.
   
3. **Módulo de Impuestos (Opción 2)📈:** El sistema solicitará el precio bruto de un componente.
 
4. **Restricción de Arquitectura (Cálculo de Impuestos)🚧🏗️:** Por políticas de calidad de software, la operación matemática para calcular el IVA (16%) está estrictamente prohibida dentro del bloque principal del menú. Debes construir un **módulo o subrutina independiente** que reciba el precio bruto ingresado, calcule el precio neto (precio + IVA) y le devuelva ese resultado final al sistema principal para que este lo muestre en pantalla.

### 📤 Salida Esperada

* **Ejemplo de Ejecución:**

```text
=== SISTEMA DE AUDITORÍA TECH ===
1. Auditar Facturas del Día
2. Calculadora de Impuestos (IVA)
3. Cerrar Turno
Seleccione una operación: 1

¿Cuántas facturas se emitieron hoy?: 3
Monto de la factura 1: 1500.50
Monto de la factura 2: 800.00
Monto de la factura 3: 3200.00

>> Corte de caja completado. Ingreso total del día: $5500.50

=== SISTEMA DE AUDITORÍA TECH ===
1. Auditar Facturas del Día
2. Calculadora de Impuestos (IVA)
3. Cerrar Turno
Seleccione una operación: 2

Ingrese el precio bruto del componente: 1000.00
>> Precio neto procesado con 16% de IVA: $1160.00

=== SISTEMA DE AUDITORÍA TECH ===
1. Auditar Facturas del Día
...
Seleccione una operación: 3

>> Turno cerrado exitosamente. Sistema apagado.
