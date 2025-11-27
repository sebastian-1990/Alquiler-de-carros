# 🚗 Sistema de Alquiler de Carros

Una aplicación de escritorio desarrollada en **Java** con interfaz gráfica moderna usando **Swing**. Este sistema permite gestionar de manera eficiente el alquiler de vehículos, clientes y transacciones.

---

## 📋 Tabla de Contenidos

- [Características](#características)
- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Uso](#uso)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Funcionalidades Principales](#funcionalidades-principales)
- [Datos Guardados](#datos-guardados)

---

## ✨ Características

✅ **Gestión de Carros**: Agregar, modificar, consultar y eliminar vehículos  
✅ **Gestión de Clientes**: Registro y consulta de clientes  
✅ **Gestión de Alquileres**: Crear, modificar y consultar alquileres  
✅ **Interfaz Moderna**: Diseño profesional con colores personalizados  
✅ **Persistencia de Datos**: Guardado automático en archivos  
✅ **Fecha y Hora en Tiempo Real**: Reloj actualizado constantemente  
✅ **Enlace a Redes Sociales**: Botón de Facebook para seguimiento  
✅ **Iconos y Visuals**: Interfaz intuitiva con iconografía

---

## 💻 Requisitos

- **Java**: JDK 17 o superior
- **Sistema Operativo**: Windows, macOS o Linux
- **RAM**: Mínimo 256 MB
- **Espacio en Disco**: 50 MB

---



## 📖 Uso

### Ventana Principal
Cuando inicias la aplicación, verás una ventana con **6 pestañas** principales:

1. **Ingreso de Carros** 🚗
2. **Consulta de Carros** 🔍
3. **Ingreso de Clientes** 👤
4. **Consulta de Clientes** 👥
5. **Ingreso de Alquiler** 📋
6. **Consulta de Alquiler** 📊

### Panel Inferior
- **Fecha y Hora**: Se actualiza en tiempo real
- **Botón Facebook**: Haz clic para seguirnos en redes sociales

---

## 🏗️ Funcionalidades Principales

### 🚗 Gestión de Carros

#### Ingreso de Carros
- **Placa**: Identificador único del vehículo (obligatorio)
- **Marca**: Marca del carro (ej: Toyota, Honda)
- **Modelo**: Modelo del vehículo
- **Color**: Color del carro
- **Año**: Año de fabricación
- **Precio Día**: Tarifa diaria de alquiler
- **Disponible para Alquilar**: Checkbox para indicar disponibilidad

**Acciones:**
- ✏️ **Guardar Carro**: Registra un nuevo carro o actualiza uno existente
- 🧹 **Limpiar**: Limpia los campos del formulario

#### Consulta de Carros
- Visualiza todos los carros registrados en una tabla
- Busca carros por placa
- Ordena por cualquier columna
- Elimina carros (selecciona y presiona eliminar)

---

### 👤 Gestión de Clientes

#### Ingreso de Clientes
- **Cédula**: Identificación única (obligatorio)
- **Nombre**: Nombre completo del cliente
- **Teléfono**: Número de contacto
- **Email**: Correo electrónico
- **Dirección**: Domicilio del cliente

**Acciones:**
- ✏️ **Guardar Cliente**: Registra o actualiza un cliente
- 🧹 **Limpiar**: Limpia los campos

#### Consulta de Clientes
- Visualiza todos los clientes registrados
- Busca por cédula
- Ordena por columnas
- Elimina clientes si es necesario

---

### 📋 Gestión de Alquileres

#### Ingreso de Alquiler
- **Placa del Carro**: Selecciona de los carros disponibles
- **Cédula del Cliente**: Selecciona el cliente
- **Fecha de Inicio**: Cuándo comienza el alquiler
- **Fecha de Fin**: Cuándo finaliza el alquiler
- **Valor Total**: Se calcula automáticamente según los días

**Acciones:**
- ✏️ **Guardar Alquiler**: Registra un nuevo alquiler
- 🧹 **Limpiar**: Limpia el formulario

#### Consulta de Alquiler
- Visualiza todos los alquileres realizados
- Busca por cédula del cliente o placa del carro
- Ordena y filtra información
- Elimina registros de alquileres

---

## 📁 Estructura del Proyecto

```
carrosalquiler/
├── src/
│   ├── Main.java                          # Punto de entrada de la aplicación
│   ├── datos/
│   │   ├── ArchivoCarro.java             # Manejo de archivo de carros
│   │   ├── ArchivoCliente.java           # Manejo de archivo de clientes
│   │   └── ArchivoAlquiler.java          # Manejo de archivo de alquileres
│   ├── logica/
│   │   ├── Carro.java                    # Modelo de datos: Carro
│   │   ├── CarroController.java          # Controlador: Carros
│   │   ├── Cliente.java                  # Modelo de datos: Cliente
│   │   ├── ClienteController.java        # Controlador: Clientes
│   │   ├── Alquiler.java                 # Modelo de datos: Alquiler
│   │   └── AlquilerController.java       # Controlador: Alquileres
│   ├── presentacion/
│   │   ├── MenuPrincipal.java            # Ventana principal
│   │   ├── CarroForm.java                # Formulario de carros
│   │   ├── ClienteForm.java              # Formulario de clientes
│   │   ├── AlquilerForm.java             # Formulario de alquileres
│   │   ├── ConsultaCarroForm.java        # Consulta de carros
│   │   ├── ConsultaClienteForm.java      # Consulta de clientes
│   │   ├── ConsultaAlquilerForm.java     # Consulta de alquileres
│   │   ├── JDateChooser.java             # Componente selector de fechas
│   │   └── util/
│   └── util/
│       └── DateUtil.java                 # Utilidades de fechas
├── resources/
│   ├── carros.txt                        # Archivo de datos: Carros
│   ├── clientes.txt                      # Archivo de datos: Clientes
│   ├── alquileres.txt                    # Archivo de datos: Alquileres
│   └── recursos/
│       ├── icono.png                     # Icono principal
│       ├── car.png                       # Icono de carros
│       ├── 1.png                         # Icono de clientes
│       ├── 2.png                         # Icono de consulta clientes
│       ├── 3.png                         # Icono de alquileres
│       └── 4.png                         # Icono de consulta alquileres
├── bin/                                   # Archivos compilados
├── build/                                 # Archivos de construcción
├── nbproject/                             # Configuración del proyecto (NetBeans)
├── build.xml                              # Script de compilación (Ant)
└── README.md                              # Este archivo
```

---

## 💾 Datos Guardados

Los datos se guardan automáticamente en archivos serializados ubicados en la carpeta `resources/`:

### Archivos de Datos
- **carros.txt**: Lista de todos los carros registrados
- **clientes.txt**: Lista de todos los clientes
- **alquileres.txt**: Historial de alquileres

### Persistencia
- Los datos se cargan automáticamente al iniciar la aplicación
- Los cambios se guardan inmediatamente al hacer operaciones (agregar, modificar, eliminar)
- Si los archivos no existen, se crean automáticamente

---

## 🎨 Esquema de Colores

La aplicación utiliza un esquema de colores profesional:

- 🔵 **Principal**: Azul (#3498DB) - Botones principales, encabezados
- 🔷 **Secundario**: Azul más oscuro (#2980B9) - Variaciones
- 🟠 **Advertencia**: Naranja (#E67E22) - Botones de limpieza/cancelación
- ⚪ **Fondo**: Gris claro (#F5F5F5) - Fondo general

---

## 🐛 Solución de Problemas

### La aplicación no inicia
- Verifica que tengas Java 17 o superior instalado
- Ejecuta `java -version` en terminal para verificar

### Los datos no se guardan
- Asegúrate de que la carpeta `resources/` existe
- Verifica permisos de lectura/escritura en la carpeta del proyecto

### Iconos no se cargan
- Coloca los archivos PNG en la carpeta `resources/recursos/`
- Verifica los nombres de los archivos

---

## 📞 Soporte

Para reportar problemas o sugerencias, síguenos en **Facebook** usando el botón en la esquina inferior derecha de la aplicación.

---

## 📄 Licencia

Este proyecto es de uso libre. Puedes modificarlo y distribuirlo libremente.

---

## 👨‍💻 Autor: SEBASTIAN

Desarrollado con ❤️ en Java Swing

**Versión**: 1.0  
**Última Actualización**: Noviembre 2025

---

## 🚀 Próximas Mejoras

- [ ] Exportar datos a PDF
- [ ] Backup automático de datos
- [ ] Reportes de alquileres
- [ ] Integración con bases de datos SQL
- [ ] Aplicación móvil
- [ ] Panel de estadísticas

---

**¡Gracias por usar nuestro Sistema de Alquiler de Carros! 🚗**
