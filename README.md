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
## MAIN
En la sección principal o MAIN aplicaremos dos subsecciones, en la zona de arriba aregaremos un texto introductoria del la visión de los productos y en la sección de abajo un formulario de contacto (no está interactuando con un servidor de correos).
Usando las propiedades de CCS de Tailwind aplicaremos un efecto para redondear las puntas de la imagen principal y cambiar el color del texto un gris. De igual forma, utilizaremos las clases para el estilo de los campos de texto del formulario de contacto y el botón de envío.

```html
 <main>
    <div class="container mx-auto py-16 px-6">
      <div class="flex flex-col lg:flex-row items-center">
        <!-- Left Section: Text -->
        <div class="lg:w-1/2 lg:pr-10">
          <h1 class="text-4xl font-bold mb-4">Descubre la Elegancia Atemporal</h1>
          <p class="text-gray-700 mb-8">
            En Relojes Vintage, te ofrecemos una exclusiva colección de relojes atemporales que combinan diseños clásicos con una artesanía inigualable. Cada pieza en nuestra colección ha sido seleccionada cuidadosamente para garantizar la más alta calidad y autenticidad. Explora nuestra colección y encuentra el reloj perfecto que refleje tu estilo y personalidad únicos.
          </p>
          <p class="text-gray-700">
            Ya sea que seas un coleccionista experimentado o simplemente busques una pieza distintiva, nuestra gama de relojes vintage tiene algo para todos. Con diseños que han superado la prueba del tiempo, estos relojes son más que simples relojes; son una pieza de historia.
          </p>
        </div>

        <!-- Right Section: Image -->
        <div class="lg:w-1/2 mt-8 lg:mt-0">
          <img class="mx-auto rounded-lg" src="./assets/img/Breguet-Classique-7137-wristie-azul.jpg" alt="Reloj Vintage">
        </div>
      </div>

      <!-- Comment Box -->
      <div class="mt-16">
        <h2 class="text-3xl font-bold text-center mb-4">Envíanos Tus Comentarios o Consultas</h2>
        <form class="max-w-xl mx-auto bg-white p-8 rounded-lg shadow-lg">
          <div class="mb-4">
            <label for="name" class="block text-gray-700 font-semibold mb-2">Nombre</label>
            <input type="text" id="name" class="w-full px-3 py-2 border rounded" placeholder="Tu Nombre">
          </div>
          <div class="mb-4">
            <label for="email" class="block text-gray-700 font-semibold mb-2">Correo Electrónico</label>
            <input type="email" id="email" class="w-full px-3 py-2 border rounded" placeholder="Tu Correo Electrónico">
          </div>
          <div class="mb-4">
            <label for="message" class="block text-gray-700 font-semibold mb-2">Mensaje</label>
            <textarea id="message" class="w-full px-3 py-2 border rounded" rows="5" placeholder="Tu Mensaje"></textarea>
          </div>
          <button type="submit" class="w-full bg-blue-500 text-white py-2 rounded hover:bg-blue-600">Enviar</button>
        </form>
      </div>
    </div>
```
## PRODUCTS
En la sección de productos, se usaron clases de la hoja de estilo, que permiten generar el efecto de "tarjetas". En cada tarjeta se muestran los productos, descripción y precio.
```html
    <!-- Products -->
    <div class="container mx-auto py-16 px-6">
      <h2 class="text-3xl font-bold text-center mb-8">Nuestra Colección</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Product 1 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/casio_aw.jpg" alt="Reloj 1">
          <h3 class="text-xl font-semibold mb-2">Casio A168</h3>
          <p class="text-gray-700 mb-4">Perfectamente simple.</p>
          <div class="text-gray-900 font-bold">$20 USD</div>
        </div>
        <!-- Product 2 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/casio_calculadora.jpg" alt="Reloj 2">
          <h3 class="text-xl font-semibold mb-2">Casio CA 53 W</h3>
          <p class="text-gray-700 mb-4">El que usaba Marty McFly.</p>
          <div class="text-gray-900 font-bold">$20 USD</div>
        </div>
        <!-- Product 3 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/casio_marlin.jpg" alt="Reloj 3">
          <h3 class="text-xl font-semibold mb-2">Casio MVD 106</h3>
          <p class="text-gray-700 mb-4">El Submariner de Casio.</p>
          <div class="text-gray-900 font-bold">$90 USD</div>
        </div>
        <!-- Product 4 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/mido_ocean_star_gmt.jpg" alt="Reloj 4">
          <h3 class="text-xl font-semibold mb-2">Mido Ocean GMT</h3>
          <p class="text-gray-700 mb-4">Automático con GMT para tener 2 husos horarios.</p>
          <div class="text-gray-900 font-bold">$1000 USD</div>
        </div>
        <!-- Product 5 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/orient_bambino.jpg" alt="Reloj 5">
          <h3 class="text-xl font-semibold mb-2">Orient Bambino</h3>
          <p class="text-gray-700 mb-4">Automático, estilo de los años 60.</p>
          <div class="text-gray-900 font-bold">$200 USD</div>
        </div>
        <!-- Product 6 -->
        <div class="bg-white p-6 rounded-lg shadow-lg">
          <img class="h-48 w-full object-cover mb-4 rounded" src="./assets/img/catalogo/seiko_5.jpg" alt="Reloj 6">
          <h3 class="text-xl font-semibold mb-2">Seiko 5</h3>
          <p class="text-gray-700 mb-4">Automático, clásico entre los clásicos.</p>
          <div class="text-gray-900 font-bold">$300 USD</div>
        </div>
      </div>
    </div>
  </main>
```

## FOOTER
Finalmente en la sección de FOOTER se indican lo derechos de propiedad de la página y los links (simulados) a las redes sociales de Facebook, Twitter (X) e Instagram.

``` html
  <!-- Footer -->
  <footer class="bg-gray-50" aria-labelledby="footerHeading">   
    <div class="bg-gray-800 text-white py-6">
      <div class="container mx-auto px-6">
        <div class="flex justify-between items-center">
          <div>&copy; 2024 Relojes Vintage - Página hecha con fines educativos - Rodrigo Espinoza - Bootcamp UDD</div>
          <div class="space-x-4">
            <a href="https://facebook.com" class="text-white hover:text-gray-400">Facebook</a>
            <a href="https://twitter.com" class="text-white hover:text-gray-400">Twitter</a>
            <a href="https://instagram.com" class="text-white hover:text-gray-400">Instagram</a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</body>
</html>
```
