# Sistema de Detección y Gestión de Parqueaderos con Inteligencia Artificial

## **Descripción del Proyecto**
Este proyecto implementa una plataforma inteligente para gestionar la disponibilidad de parqueaderos en un campus universitario. Utiliza un sistema basado en **cámaras y modelos de visión por computadora (YOLO)** para detectar los espacios ocupados y libres en tiempo real. El objetivo es optimizar el uso de los parqueaderos y reducir las filas y los tiempos de espera de los usuarios.

## **Características Principales**
- **Detección de espacios libres y ocupados**: Uso de cámaras estratégicamente ubicadas para monitorear el estado de los espacios.
- **Plataforma en tiempo real**: Actualización constante de la disponibilidad de parqueaderos en una app web o móvil.
- **Predicciones basadas en datos**: Análisis de patrones históricos para anticipar horarios de mayor demanda.
- **Adaptabilidad al clima y condiciones**: El modelo está entrenado para operar bajo diferentes condiciones de iluminación y clima.
- **Interfaz de usuario**: Mapa interactivo que muestra la ubicación de los espacios disponibles.

## **Tecnologías Utilizadas**
### **Hardware:**
- Cámaras IP resistentes al clima (certificación IP66 o superior).
- Dispositivos Edge como **Raspberry Pi** o **NVIDIA Jetson Nano** (opcional).

### **Software:**
- **Visión por Computadora**: Modelo YOLO (You Only Look Once) para detección de objetos.
- **Procesamiento de Imágenes**: OpenCV.
- **Backend**: Python con Flask/Django.
- **Frontend**: HTML, CSS y JavaScript (Bootstrap).
- **Base de Datos**: SQLite o PostgreSQL.
- **Infraestructura en la Nube**: AWS o Google Cloud (opcional).

## **Requisitos del Proyecto**
### **Hardware:**
- Cámaras de alta resolución con soporte para HDR.
- Conexión estable a internet para transmitir las imágenes al servidor.

### **Software:**
- Python 3.8 o superior.
- Librerías necesarias (instalables mediante `requirements.txt`):
  ```bash
  pip install -r requirements.txt
  ```
  **Librerías clave:**
  - ultralytics (YOLOv8)
  - OpenCV
  - Flask o Django
  - SQLAlchemy

## **Instalación y Configuración**
1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/tu_usuario/sistema-parqueadero-ia.git
   cd sistema-parqueadero-ia
   ```
2. **Instala las dependencias:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Configura las variables de entorno:**
   Crea un archivo `.env` con los siguientes datos:
   ```env
   FLASK_ENV=development
   DATABASE_URL=sqlite:///parqueadero.db
   SECRET_KEY=tu_clave_secreta
   ```
4. **Entrena el modelo (opcional):**
   Si deseas entrenar el modelo para condiciones específicas de tu parqueadero:
   ```bash
   python train_model.py --data ruta_a_tus_datos --epochs 50
   ```
5. **Ejecuta el servidor:**
   ```bash
   flask run
   ```

## **Uso del Sistema**
1. Accede a la plataforma a través del navegador en `http://localhost:5000`.
2. Visualiza el mapa del parqueadero y consulta los espacios disponibles en tiempo real.
3. Usa la app para recibir notificaciones y planificar tu llegada al campus.

## **Estructura del Proyecto**
```
.
├── app/
│   ├── static/                # Archivos estáticos (CSS, JS, imágenes)
│   ├── templates/             # Plantillas HTML
│   ├── models.py              # Modelos de la base de datos
│   ├── routes.py              # Rutas principales del backend
│   └── utils.py               # Utilidades para procesamiento
├── train_model.py             # Script para entrenar el modelo YOLO
├── requirements.txt           # Dependencias del proyecto
├── README.md                  # Documentación del proyecto
└── .env.example               # Ejemplo de configuración de entorno
```

## **Futuras Mejoras**
- Implementar soporte para detección nocturna con cámaras infrarrojas.
- Optimizar el algoritmo para reducir el consumo de recursos en dispositivos Edge.
- Desarrollar una versión de la app móvil para iOS y Android.

## **Contribuciones**
Las contribuciones son bienvenidas. Si deseas colaborar:
1. Haz un fork del repositorio.
2. Crea una rama nueva para tus cambios:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Envía un pull request describiendo tus cambios.

## **Contacto**
Si tienes preguntas o sugerencias, por favor contáctanos a:
- **Email:** sdominguer@eafit.edu.co


