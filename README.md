# Proyecto 3 Bootcamp UDD - Landing Page
El objetivo del Proyecto 3 es comprender el uso de html, su estructura y la aplicación de hojas de estilo.
Para lograr los objetivos de aprendizaje, se ha creado una página web con HTML y con la hoja de estilos **Tailwind CCS**. La página ofrecerá relojes clásicos o vintage de colección.

## Uso de Tailwind CSS
Tailwind CSS es un marco de trabajo (framework) de CSS que facilita el desarrollo de interfaces de usuario mediante el uso de clases utilitarias predefinidas. En lugar de escribir CSS personalizado para cada componente, puedes aplicar clases directamente en tu HTML para controlar el diseño, el espaciado, la tipografía, los colores, y otros estilos.

## Diseñando el sitio
Antes de comenzar con la programación, diseñamos la página para tener una perspectiva de lo que necesitamos. En este caso, usamos un dibujo (mockup):

![mockup_landing_page_watches](https://github.com/user-attachments/assets/e33adf90-7216-4fa6-ad13-716319769d38)

A continuación, se explicará la estructura de la página **index.html** separada en HEADER, MAIN, PRODUCTOS, FOOTER.

## HEADER
En el HEADER definiremos el título de la página y los links para el retorno al home (Inicio), explicar qué es la empresa o sus fundadores (Acerca de) y para que se comuniquen con los administradores (Contacto).
```html
  <header class="relative">
    <div class="bg-white shadow">
      <div class="container mx-auto py-4 px-6 flex justify-between items-center">
        <div class="text-2xl font-bold">Relojes Vintage</div>
        <nav class="space-x-4">
          <a href="#" class="text-gray-700 hover:text-gray-900">Inicio</a>
          <a href="#" class="text-gray-700 hover:text-gray-900">Acerca de</a>
          <a href="#" class="text-gray-700 hover:text-gray-900">Contacto</a>
        </nav>
      </div>
    </div>
  </header>
```
