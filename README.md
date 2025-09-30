# taller-accesibilidad
1. Botones sin texto accesible
 Problema: El botón de menú <button> no tiene texto visible ni aria-label.
Solución: Agregar aria-label o texto oculto.
<!--  Antes -->
<button type="button" class="navbar-toggler" id="GA4-abrir">
  <i class="fas fa-bars" id="GA4-abrir-btn"></i>
</button>

<!--  Después -->
<button type="button" class="navbar-toggler" id="GA4-abrir" aria-label="Abrir menú de navegación">
  <i class="fas fa-bars" aria-hidden="true"></i>
</button>

2. Imágenes sin atributo 
 Problema: Las imágenes no tienen alt.
 Solución: Agregar alt descriptivo o role="presentation" si son decorativas.
<!--  Antes -->
<img src="icono-buscador.png" class="GA4-Buscador-movil" id="GA4-Buscador-movil">

<!--  Después -->
<img src="icono-buscador.png" alt="Icono de lupa para búsqueda" class="GA4- Buscador-movil" id="GA4-Buscador-movil"


3. Enlaces sin texto discernible
Problema: Enlace solo con logo sin texto ni aria-label.
Solución: Añadir texto oculto o aria-label.
<!--  Antes -->
<a href="https://www.javeriana.edu.co/hoy-en-la-javeriana/" id="GA4-clic-logo-HEJ">
  <img src="logo.png">
</a>

<!--  Después -->
<a href="https://www.javeriana.edu.co/hoy-en-la-javeriana/" id="GA4-clic-logo-HEJ" aria-label="Hoy en la Javeriana">
  <img src="logo.png" alt="Logo de la Javeriana">
</a>



4. Contraste insuficiente en enlaces
Problema: El color #007bff sobre blanco no cumple WCAG AA.
Solución: Usar un azul más oscuro para asegurar contraste.
/*  Antes */
a.enlace-pestana {
  color: #007bff; /* contraste 3.97:1 */
}

/*  Después */
a.enlace-pestana {
  color: #0056b3; /* contraste > 4.5:1 */
}


5. Meta viewport que impide zoom
Problema: El maximum-scale=1 bloquea el zoom.
Solución: Permitir escalado en dispositivos móviles.
<!--  Antes -->
<meta content="initial-scale=1.0, width=device-width, maximum-scale=1" name="viewport">

<!--  Después -->
<meta content="width=device-width, initial-scale=1.0" name
