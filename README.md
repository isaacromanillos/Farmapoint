# Farmapoint

Farmapoint es una aplicación de escritorio desarrollada en C# y WPF (.NET Framework 4.7.2) diseñada para la simulación y gestión de puntos de dispensación farmacéutica y consulta de receta electrónica. 

El sistema permite gestionar la información del paciente, verificar prescripciones pendientes y registrar las dispensaciones correspondientes, contando con soporte para lectura de tarjetas sanitarias inteligentes.

## Características Principales

- Búsqueda y gestión de pacientes: Consulta por CITE, código SNS, tarjeta sanitaria (TSI), tipo de aportación y saldo.
- Módulo de receta electrónica: Consulta de medicamentos prescritos y gestión del repositorio de recetas dispensables.
- Registro de dispensación: Control de sustituciones de medicamentos, causas de sustitución, observaciones y cálculo de precios/aportaciones.
- Lectura de tarjetas inteligentes: Integración con lectores de tarjetas de salud mediante el estándar PCSC (ISO 7816).
- Interfaz gráfica moderna: Diseñada en XAML con navegación por páginas (`Pages`) e integración visual adaptable.

## Tecnologías Utilizadas

- Lenguaje de programación: C#
- Interfaz de usuario: WPF (Windows Presentation Foundation) / XAML
- Plataforma: .NET Framework 4.7.2
- Base de datos: Microsoft Access (`.accdb`) mediante proveedor OLEDB 12.0

## Requisitos de Ejecución

- .NET Framework 4.7.2 instalado.
- Motor de base de datos de Microsoft Access (Microsoft Access Database Engine 2010 o superior / OLEDB 12.0).

## Arquitectura del Proyecto

- `MainWindow.xaml`: Ventana principal que actúa como contenedor de navegación.
- `PageBusquedaPaciente.xaml`: Vista para la localización e identificación del paciente.
- `PageMenuPaciente.xaml`: Panel de control de opciones asignadas al paciente seleccionado.
- `PageMedicamentosDispensables.xaml`: Listado y filtrado de recetas prescritas activas.
- `PageDetallesMedicamentosDispensables.xaml`: Formulario de confirmación y registro de la dispensación.
- `ConexionDb.cs`: Manejo de la conexión local OLEDB a la base de datos Access.
- `CPaciente.cs`, `CRecetaDispensable.cs`, `CRecetaDispensada.cs`: Modelos de datos para el manejo de la lógica de negocio.
