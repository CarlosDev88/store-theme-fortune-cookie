## 📦 Dependencias

Este `store-theme` utiliza las siguientes dependencias principales:

- [`vtex.store`](https://developers.vtex.com/docs/apps/vtex.store)  
- [`vtex.store-header`](https://developers.vtex.com/docs/apps/vtex.store-header)  
- [`vtex.store-footer`](https://developers.vtex.com/docs/apps/vtex.store-footer)  
- [`vtex.flex-layout`](https://developers.vtex.com/docs/apps/vtex.flex-layout)  
- [`valtech.fortune-cooky-app`](https://developers.vtex.com/) (aplicación personalizada que muestra mensajes de la fortuna)  

---

## 🚀 Instalación y Ejecución

1. **Clonar el repositorio:**

   git clone git@github.com:valtech/store-theme.git
   cd store-theme


2. **Instalar dependencias:**


   yarn install


3. **Iniciar workspace en VTEX IO:**

   vtex use {workspace}
   vtex link


4. **Publicar (opcional):**


   vtex publish


---

## 🌐 Landing de Fortune Cookie

Se creó una **landing** en el `store-theme` que consume el bloque expuesto por `fortune-cooky-app`.

### 📍 Path

```
https://{workspace}--{vendor}.myvtex.com/fortune-cookie
```



### 📄 Configuración (`store-theme` JSON)

```json

{
  "store.custom#fortune-cookie": {
    "blocks": [
      "rich-text#fc-title",
      "cookie-fortune-message#fc-message"
    ]
  },
  "rich-text#fc-title": {
    "props": {
      "text": "# Bienvenido a Fortune Cookie 🎉",
      "alignment": "CENTER",
      "textPosition": "CENTER",
      "blockClass": "fc-header"
    }
  },
  "cookie-fortune-message#fc-message": {
    "props": {
      "title": "Tu mensaje de la fortuna",
      "buttonText": "Sacar otra"
    }
  }
}
```


### Resultado esperado:

1. El usuario accede a `/fortune-cookie`.
2. Se muestra un título con **Rich Text**.
3. El componente `cookie-fortune-message` despliega un mensaje de la fortuna desde la app.
4. El botón `"Sacar otra"` permite obtener un nuevo mensaje.

---

## 🛠️ Otros paths configurados

Este `store-theme` también incluye páginas básicas:

* `/about-us` → Página de información
* `/faq` → Preguntas frecuentes
* `/contact-us` → Formulario de contacto
* `/fortune-cookie` → **Landing personalizada (Fortune Cookie)**

---

## 📄 Scripts útiles

* `yarn install` → Instala dependencias
* `vtex link` → Linkea el proyecto al workspace actual
* `vtex publish` → Publica la versión del tema

---



