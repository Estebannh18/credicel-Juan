# 🍾 Licorera CREDICEL JUAN

![Banner](https://img.shields.io/badge/SQL%20Server-Project-red?style=for-the-badge&logo=microsoftsqlserver)
![Status](https://img.shields.io/badge/Status-Activo-success?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

Proyecto académico desarrollado en **SQL Server**, que representa el modelo de datos lógico y físico de una **licorera**, incluyendo tablas, vistas, procedimientos almacenados y funciones para gestión integral.

---

## 🧠 Objetivo del proyecto
Diseñar y construir una **base de datos relacional completa** para una licorera, permitiendo administrar clientes, productos, ventas, empleados y proveedores, con buenas prácticas de diseño y normalización.

---

## 🗂️ Estructura del proyecto

| Elemento | Descripción |
|-----------|--------------|
| 🧱 **Tablas** | Definen la estructura principal del sistema (clientes, productos, facturas, empleados, proveedores, etc.) |
| 👁️ **Views** | Consultas predefinidas que facilitan reportes y análisis |
| ⚙️ **Stored Procedures** | Automatizan operaciones comunes (registro de ventas, actualización de inventario, etc.) |
| 🧮 **Functions** | Cálculos reutilizables dentro de consultas SQL |

---

## 🧩 Modelo lógico
El sistema está diseñado bajo una estructura **relacional profesional**, con **llaves primarias, foráneas y únicas** claramente definidas para asegurar integridad referencial.

```mermaid
erDiagram
    CLIENTE ||--o{ FACTURA : realiza
    EMPLEADO ||--o{ FACTURA : atiende
    FACTURA ||--|{ DETALLE_FACTURA : contiene
    PRODUCTO ||--o{ DETALLE_FACTURA : se_vende_en
    PROVEEDOR ||--o{ PRODUCTO : suministra
