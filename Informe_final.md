# INFORME TÉCNICO Y EJECUTIVO

# TPS & MIS QUICKSHOP v3.0

## ISID223 — Introducción a los Sistemas de Información 2026-A

**Profesor:** Iván Carrera — EPN-FIS

**Estudiantes:** Gabriel Quilachamin - Samuel Lucero

**Proyecto:** Diseño e Implementación de una Solución MIS a partir de un TPS

**Fecha:** 28 de Mayo de 2026

**Estado del Proyecto:**  COMPLETADO

---

#  INTRODUCCIÓN

El proyecto **QuickShop TPS & MIS v3.0** consiste en el diseño e implementación de un sistema integrado de procesamiento de transacciones (TPS) y un sistema de información gerencial (MIS) orientado a la administración de un minimarket.

El sistema fue desarrollado en Python utilizando Tkinter para la interfaz gráfica y archivos CSV como mecanismo de persistencia de datos.

El objetivo principal del proyecto fue transformar datos operativos generados por un TPS en información gerencial útil mediante dashboards, KPIs y reportes analíticos que permitan apoyar la toma de decisiones estratégicas.

El proyecto simula un entorno comercial real incluyendo:

* Gestión de ventas
* Administración de inventario
* Gestión de clientes
* Facturación
* Análisis estadístico
* Dashboards gerenciales
* Reportes automáticos

---

#  OBJETIVOS DEL PROYECTO

## Objetivo General

Diseñar, implementar y documentar una solución de Sistema de Información Gerencial (MIS) capaz de transformar datos transaccionales provenientes de un TPS en información estructurada para análisis y toma de decisiones.

---

## Objetivos Específicos

###  Implementar un TPS funcional

* Registro de ventas
* Gestión de inventario
* Control de stock
* Facturación
* Gestión de clientes

###  Diseñar un MIS basado en datos

* Generación de KPIs
* Dashboards visuales
* Reportes ejecutivos
* Análisis estadístico

###  Aplicar procesos ETL

* Extracción de datos
* Transformación
* Limpieza
* Carga y análisis

###  Documentar el sistema

* Informe técnico
* Propuesta ejecutiva
* Manual de uso
* Reportes exportables

---

#  ARQUITECTURA GENERAL DEL SISTEMA

El proyecto está dividido en dos componentes principales:

| Componente                          | Función                                 |
| ----------------------------------- | --------------------------------------- |
| TPS (Transaction Processing System) | Gestión operativa diaria                |
| MIS (Management Information System) | Análisis gerencial y toma de decisiones |

---

# TECNOLOGÍAS UTILIZADAS

| Tecnología       | Función                 |
| ---------------- | ----------------------- |
| Python 3         | Lenguaje principal      |
| Tkinter          | Interfaz gráfica        |
| Pandas           | Procesamiento de datos  |
| NumPy            | Cálculos numéricos      |
| Matplotlib       | Visualización           |
| Seaborn          | Dashboards estadísticos |
| CSV              | Persistencia de datos   |
| Jupyter Notebook | Desarrollo analítico    |

---

# FUNCIONAMIENTO DEL TPS

## Sistema de Punto de Venta

El TPS permite registrar ventas en tiempo real mediante una interfaz gráfica organizada por módulos.

### Funcionalidades principales:

* Búsqueda de productos
* Filtro por categorías
* Carrito de compras
* Métodos de pago
* Generación de transacciones
* Facturación automática
* Actualización de stock

---

##  Gestión de Inventario

El sistema controla automáticamente el inventario después de cada venta.

### Características:

* Stock actualizado en tiempo real
* Productos agotados en rojo
* Stock crítico en amarillo
* Persistencia en CSV
* Validación de disponibilidad

---

## Gestión de Clientes

Nueva implementación incorporada en la versión 3.0.

### Funcionalidades:

* Registro de clientes
* Búsqueda de usuarios
* Asociación cliente-factura
* Base de datos de clientes

### Datos almacenados:

* Cédula
* Nombre
* Correo
* Teléfono
* Fecha de registro

---

## Sistema de Facturación

Cada venta genera automáticamente una transacción con:

* ID único
* Fecha
* Hora
* Cliente
* Cajero
* Subtotal
* IVA
* Total
* Método de pago
* Estado

El IVA se calcula automáticamente al 12%.

---

#  ESTRUCTURA DE DATOS

El sistema utiliza varios archivos CSV organizados modularmente.

| Archivo            | Función               |
| ------------------ | --------------------- |
| productos.csv      | Catálogo de productos |
| inventario.csv     | Stock actualizado     |
| usuarios.csv       | Clientes registrados  |
| transacciones.csv  | Historial de ventas   |
| detalles_venta.csv | Productos vendidos    |

---

#  CATÁLOGO DEL SISTEMA

La nueva versión incorpora:

## Antes:

* 55 productos
* 7 categorías

## Ahora:

* 200+ productos
* 9 categorías

### Categorías:

* Bebidas
* Snacks
* Lácteos
* Panadería
* Abarrotes
* Limpieza
* Personal
* Frutas y verduras
* Carnes y embutidos

---

# GENERACIÓN AUTOMÁTICA DE HISTORIAL

El sistema incorpora simulación automática de actividad comercial.

### Características:

* Generación de 1 año de ventas
* Más de 200 transacciones simuladas
* Clientes aleatorios
* Productos aleatorios
* Métodos de pago variados

Esto permite realizar análisis reales desde la primera ejecución.

---

# IMPLEMENTACIÓN DEL MIS

El MIS fue desarrollado para transformar datos operativos en información gerencial.

---

#  PROCESO ETL IMPLEMENTADO

## EXTRACCIÓN

Se obtienen datos desde:

* transacciones.csv
* detalles_venta.csv
* productos.csv
* usuarios.csv
* inventario.csv

---

## TRANSFORMACIÓN

Procesos aplicados:

* Limpieza de datos
* Conversión de tipos
* Eliminación de duplicados
* Unificación mediante merges
* Creación de variables derivadas
* Segmentación de clientes

---

## CARGA

Resultados generados:

* KPIs
* Dashboards
* Reportes CSV
* Análisis estadísticos

---

# KPIs IMPLEMENTADOS

| KPI                     | Función                  |
| ----------------------- | ------------------------ |
| Ventas Totales          | Evalúa ingresos globales |
| Ticket Promedio         | Analiza consumo promedio |
| Número de Transacciones | Actividad comercial      |
| Clientes Únicos         | Alcance del mercado      |
| Margen de Ganancia      | Rentabilidad             |
| Método de Pago Top      | Preferencia de pago      |
| Crecimiento Mensual     | Tendencias               |
| Ingresos por Categoría  | Distribución comercial   |

---

# DASHBOARDS IMPLEMENTADOS

## Dashboard 1 — KPIs Principales

Incluye:

* Ventas mensuales
* Top productos
* Métodos de pago
* Categorías más rentables

---

## Dashboard 2 — Análisis de Clientes

Incluye:

* Top clientes
* Segmentación
* Frecuencia de compra
* Distribución de ticket promedio

---

## Dashboard 3 — Tendencias Temporales

Incluye:

* Ventas diarias
* Ventas por hora
* Tendencias semanales
* Análisis temporal

---

## Dashboard 4 — Reportes Gerenciales

Incluye:

* Tarjetas KPI
* Ventas últimos 7 días
* Productos TOP
* Categorías TOP

---

# REPORTES GENERADOS

## Reportes rutinarios

* Ventas diarias
* Resumen semanal
* Resumen mensual

## Reportes analíticos

* Top productos
* Top clientes
* Desempeño de cajeros
* Ingresos por categoría

---

#  ARCHIVOS GENERADOS

## Dashboards PNG

* Dashboard_1_KPIs_Principales.png
* Dashboard_2_Analisis_Clientes.png
* Dashboard_3_Tendencias_Temporales.png
* Dashboard_4_Reportes_Programados.png

## Reportes CSV

* KPIs_Resumen.csv
* Top_Productos.csv
* Top_Clientes.csv
* Ingresos_por_Categoria.csv
* Desempeno_Cajeros.csv

---

#  NUEVAS IMPLEMENTACIONES

- **De 55 a 200 productos.**
- **Implementación de gestión de usuarios.**
- **Generación anual de transacciones.**
- **Visualizaciones ejecutivas.**
- **Procesamiento profesional de datos.**
- **Indicadores calculados dinámicamente.**

*Archivos CSV y PNG automáticos.*
---

#  CONCEPTOS DE SISTEMAS DE INFORMACIÓN IMPLEMENTADOS

## TPS (Transaction Processing System)

* Procesamiento operativo
* Ventas en tiempo real
* Facturación
* Gestión de inventario

---

## MIS (Management Information System)

* Dashboards gerenciales
* KPIs
* Reportes ejecutivos
* Análisis estratégico

---

## Reportes Programados

* Reportes diarios
* Semanales
* Mensuales

---

## Reportes de Indicadores Clave

* Visualización ejecutiva
* KPIs estratégicos
* Análisis de rendimiento

---

#  VENTAJAS DEL SISTEMA

## Operativas

* Automatización
* Control de inventario
* Persistencia de datos
* Gestión eficiente

## Estratégicas

* Decisiones basadas en datos
* Análisis comercial
* Identificación de tendencias
* Ventaja competitiva

## Técnicas

* Modular
* Escalable
* Fácil mantenimiento
* Compatible con múltiples plataformas

---

# RESULTADOS OBTENIDOS

| Antes                  | Después                     |
| ---------------------- | --------------------------- |
| Decisiones intuitivas  | Decisiones basadas en datos |
| Sin KPIs               | KPIs visibles               |
| Sin análisis histórico | Tendencias identificadas    |
| Reportes manuales      | Reportes automáticos        |
| Información dispersa   | Dashboards centralizados    |

---

# CONCLUSIONES

QuickShop TPS & MIS v3.0 representa una solución integral que combina procesamiento transaccional y análisis gerencial.

El proyecto evolucionó desde un sistema básico de ventas hacia una plataforma completa capaz de:

* Administrar operaciones comerciales
* Analizar comportamiento de clientes
* Generar reportes estratégicos
* Mostrar indicadores gerenciales
* Facilitar la toma de decisiones

La implementación demuestra la aplicación práctica de conceptos de:

* Sistemas de Información
* ETL
* Dashboards
* KPIs
* TPS
* MIS
* Análisis de datos
* Interfaces gráficas

Todo el sistema fue desarrollado utilizando Python y herramientas de análisis modernas.

---

# REFERENCIAS TECNOLÓGICAS

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from datetime import datetime
```

---

# RESUMEN EJECUTIVO FINAL

El proyecto QuickShop TPS & MIS transforma datos transaccionales en información gerencial mediante dashboards, KPIs y análisis estadísticos.

La solución permite:

* Mejorar la toma de decisiones
* Optimizar recursos
* Analizar ventas
* Identificar tendencias
* Mejorar la rentabilidad

El sistema constituye una implementación completa de un MIS moderno aplicado a un entorno comercial real.

---