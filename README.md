#**Mapa de puntos de consumo – Demo**

Aplicación interactiva desarrollada en **Streamlit** para visualizar puntos de consumo de drogas y servicios relacionados en la ciudad de Barcelona.
Esta es una **versión demo** que utiliza **datos completamente ficticios**, creada con fines educativos y de divulgación técnica.


##**📊 Objetivo de la app**
Esta herramienta busca simular una aplicación para el análisis territorial de restos de consumo de drogas y recursos de atención en el espacio urbano.
Permite explorar visualmente los datos por barrio, tipo de resto o servicio, y su distribución temporal.
Puede ser útil como modelo para iniciativas de reducción de daños, salud comunitaria o investigación social aplicada.

##**📷 Vista previa**

![Capturas de la app](images)


##**🚀 Funcionalidades principales**

Visualización interactiva en mapa de:
- Restos de consumo (jeringuillas, utensilios, etc.)
- Servicios de atención (centros, dispositivos móviles, etc.)
- Filtro dinámico por tipo de punto (consumos / servicios / ambos).
- Cambio de estilo del mapa base.
- Filtro por rango de fechas reales (mes y año).
- Acceso protegido por contraseña configurable.

##**🧪 Demo pública**

🔗 [Abrir app en Streamlit Cloud](https://mapapuntosdeconsumodemo.streamlit.app/)
🔐 Contraseña de acceso: holademo


##**📁 Estructura del repositorio**

mapa_puntos_consumo_demo/
├── .gitignore               # Archivos y carpetas ignorados por Git
├── LICENSE                  # Licencia del proyecto
├── README.md                # Documentación principal del proyecto
├── app_home.py              # App principal con menú y navegación
├── app_mapa_interactivo.py  # Visualización del mapa interactivo
├── app_stadistics.py        # Visualización de estadísticas (si aplica)
├── requirements.txt         # Dependencias del entorno
├── utils.py                 # Funciones auxiliares
├── inputs/                  # Datos ficticios utilizados por la app.⚠️ Si son datos sensibles, no incluir en proyecto real. Incluir en .gitignore
│   ├── mapa_consumos_demo.csv
│   └── recursos_drogas.csv
├── images/                 # Capturas de la app
│   └── captura_demo.png
└── .streamlit/
   └── secrets.toml         # ⚠️ No incluir en proyecto real. Incluir en .gitignore
   

##**🔐 ¿Qué es secrets.toml y cómo se configura?**

La app utiliza un archivo llamado **secrets.toml** para cargar datos y proteger el acceso con contraseña.
En proyectos reales, este archivo **no debe subirse** al repositorio porque suele contener información sensible.
Sin embargo, en esta demo educativa, incluimos un archivo de ejemplo (secrets.toml) y datos ficticios
en la carpeta inputs/ para que puedas ejecutar la app sin configuración adicional.

└── **🧩 ¿Cómo acceder a los secretos desde el código?**
    Si tu archivo **secrets.toml** tiene este contenido:
    
    ```toml
    access_password = "demo123"
    data_1_url = "inputs/datos_consumo.csv"
    data_2_url = "inputs/datos_servicios.csv" ```

 └── ``` python
    import streamlit as st
    # Acceder a los valores del archivo secrets.toml
    password_correcta = st.secrets["access_password"]
    ruta_datos_consumo = st.secrets["data_1_url"]
    ruta_datos_servicios = st.secrets["data_2_url"] ```


##🛠️ **Cómo ejecutar la app en local**

1. Clona el repositorio:
   ``` python
   git clone https://github.com/MikiLeon/mapa_puntos_consumo_demo.git```
2. Instala las dependencias:
   ``` python
   pip install -r requirements.txt ```
3. Ejecuta la app:
   ``` python
   streamlit run app.py```
   

##📌 **Notas**

- Este proyecto es una adaptación ficticia para mostrar el funcionamiento de
  una herramienta orientada al análisis territorial del consumo de drogas y los servicios de apoyo.
- No contiene información real.
- Inspirado en iniciativas reales de reducción de daños y salud comunitaria.

  ##👤 **Autoría**
  
  Miguel Ángel García León
  📧 miiguelleon@gmail.com
  🔗 [LinkedIn](www.linkedin.com/in/miguel-ángel-garcía-león)
  🔗 [GitHub](https://github.com/MikiLeon)
   









    
