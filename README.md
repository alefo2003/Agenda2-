%%writefile modulo2_hashing/README.md
# Módulo 2: Implementación de Tabla Hash con Diccionarios en Python

## Descripción del Proyecto
Este proyecto implementa una agenda de contactos utilizando la clase `AgendaDeContacto`. El objetivo principal es aplicar el concepto de tablas hash mediante la estructura de datos nativa `dict` de Python para lograr una gestión eficiente de la información.

## Funcionalidades Implementadas
- **Inicialización (`__init__`)**: Crea el diccionario `self.contacto_dict` para almacenar las relaciones clave-valor (Nombre -> Teléfono).
- **Adición de contactos (`add_contacto`)**: Valida si la clave ya existe para evitar sobreescrituras e inserta nuevos registros.
- **Búsqueda eficiente (`buscar_contacto`)**: Utiliza la función `.get()` para acceder a los datos sin riesgo de errores tipo `KeyError`.

## Justificación Teórica: Complejidad Algorítmica $O(1)$ vs $O(n)$

### Búsqueda en una Lista — Complejidad $O(n)$
En una lista tradicional, los elementos se almacenan secuencialmente. Para encontrar un contacto, el algoritmo debe revisar cada elemento uno por uno desde el principio hasta el final. Si la agenda tiene $n$ elementos, en el peor de los casos requerirá $n$ comparaciones.

### Búsqueda en un Diccionario (Tabla Hash) — Complejidad $O(1)$
Un diccionario utiliza una **función hash** que transforma la clave (el nombre del contacto) directamente en una dirección de memoria. 

- **Acceso Directo:** Al buscar `mi_agenda.buscar_contacto("Ana")`, Python calcula la posición de memoria de "Ana" de manera instantánea.
- **Independencia del tamaño:** No importa si la agenda tiene 10 o 1,000,000 de contactos, el tiempo de búsqueda es constante ($O(1)$).
