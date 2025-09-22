# Traza1-Traza2
Traza 1 + Traza 2 (Java + Lombok)

Este repositorio abarca dos dominios principales, organizados en trazas conceptuales que reflejan una estructura jerárquica y modular:

Traza A: País → Provincia → Localidad → Domicilio → Sucursal → Empresa

Traza B: Artículo → (Insumo | Manufacturado) → Detalle → Categoría → Imagen → UnidadMedida

Ambas trazas convergen mediante la clase puente SucursalArticulo, que permite representar el inventario específico de cada sucursal (stock y, opcionalmente, el precio), evitando acoplamientos rígidos entre los modelos.

Tecnologías y lineamientos implementados:

Java con soporte de Lombok para simplificar código repetitivo (getters, setters, builders, etc.).

Uso de HashSet para manejar relaciones con multiplicidad, preservando unicidad.

Métodos helper que garantizan la consistencia de las asociaciones (por ejemplo, Sucursal.agregarAlInventario(...)).

Métodos toString limpios, excluyendo referencias circulares y colecciones grandes.

Qué hace el main:

Alta de entidades de ambos dominios (traza A y B).

Carga de inventario a través de helpers y objetos SucursalArticulo.

Operaciones de CRUD sobre artículos manufacturados y edición de stock/precio según sucursal.

Organización del código por paquetes:

traza.app/ → Lógica de ejecución principal (demo)

traza.traza1/ → Entidades geográficas y organizacionales: País, Provincia, Localidad, etc.

traza.traza2/ → Modelo de productos: Artículo, Insumo, Manufacturado, etc.

traza.integracion/ → Clase de integración SucursalArticulo (manejo del inventario por sucursal)
