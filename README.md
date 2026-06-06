# 🎬 Agente Recomendador de Películas

Aplicación web desarrollada en HTML, CSS y JavaScript que permite interactuar con un agente conversacional especializado en recomendaciones de películas.

El chat se conecta a una API desplegada en Render y mantiene el contexto de la conversación mediante un `session_id` almacenado en el navegador.

## 🚀 Características

* Chat en tiempo real.
* Recomendaciones personalizadas de películas.
* Memoria persistente mediante `session_id`.
* Almacenamiento local con `localStorage`.
* Opción para iniciar una nueva conversación.
* Diseño responsive para escritorio y dispositivos móviles.
* Despliegue sencillo en Netlify.

## 📂 Estructura del Proyecto

```text
chat-peliculas/
│
├── index.html
└── netlify.toml
```

## 🛠️ Tecnologías Utilizadas

* HTML5
* CSS3
* JavaScript (Vanilla JS)
* API REST
* Netlify
* Render

## 🔌 API Utilizada

### Endpoint principal

```http
POST /consultar
```

Ejemplo de solicitud:

```json
{
  "session_id": "abc-123",
  "mensaje": "Me gustan las películas de ciencia ficción"
}
```

Ejemplo de respuesta:

```json
{
  "session_id": "abc-123",
  "respuesta": "Te recomiendo Interestelar y Blade Runner 2049.",
  "mensajes_en_memoria": 4
}
```

### Reiniciar conversación

```http
DELETE /limpiar/{session_id}
```

Este endpoint elimina el historial almacenado para una sesión determinada.

## 💻 Instalación Local

1. Clonar el repositorio:

```bash
git clone https://github.com/usuario/chat-peliculas.git
```

2. Entrar al proyecto:

```bash
cd chat-peliculas
```

3. Abrir el archivo:

```text
index.html
```

o ejecutar un servidor local.

## 🌐 Despliegue en Netlify

1. Subir el proyecto a GitHub.
2. Crear un nuevo sitio en Netlify.
3. Conectar el repositorio.
4. Configurar:

```text
Build command: (vacío)
Publish directory: .
```

5. Desplegar.

## 📱 Responsive Design

La interfaz se adapta automáticamente a:

* Computadores de escritorio
* Tablets
* Teléfonos móviles

## 📄 Licencia

Este proyecto se distribuye con fines educativos y demostrativos.
