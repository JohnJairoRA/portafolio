# Portafolio-Curso4
Este proyecto es un portafolio creado como parte del curso de Oracle sobre HTML y CSS. El portafolio incluye varias secciones y funcionalidades, incluyendo un carrusel de imágenes para mostrar certificaciones.

# Funcionalidades
1. Carrusel de Imágenes
El carrusel de imágenes permite mostrar múltiples imágenes de certificaciones de manera secuencial. Cada imagen se muestra durante 5 segundos antes de cambiar a la siguiente. El carrusel se repite indefinidamente.

# HTML
El carrusel está definido en el archivo certificaciones.html:

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Certificaciones</title>
    <link rel="stylesheet" href="styles/style.css">
</head>
<body>
    <nav class="header__menu">
        <a class="header__menu__link" href="index.html">Home</a>
        <a class="header__menu__link" href="about.html">Sobre mí</a>
        <a class="header__menu__link" href="certificaciones.html">Certificaciones</a>
    </nav>
    <div class="carousel">
        <div class="carousel-inner">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-24-04.png" alt="Certificación 1">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-25-05.png" alt="Certificación 2">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-25-28.png" alt="Certificación 3">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-25-56.png" alt="Certificación 4">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-26-17.png" alt="Certificación 5">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-26-46.png" alt="Certificación 6">
            <img src="assets/certificaciones/Captura desde 2025-03-19 00-27-05.png" alt="Certificación 7">
            <!-- Agrega más imágenes según sea necesario -->
        </div>
    </div>
</body>
</html>

# CSS
El estilo del carrusel está definido en el archivo styles/style.css:
.carousel {
    width: 100%;
    height: 100vh; /* Ajusta la altura para que ocupe toda la pantalla */
    overflow: hidden;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

.carousel-inner {
    display: flex;
    width: 100%;
    animation: slide 35s infinite;
}

.carousel-inner img {
    width: 100%;
    height: 100vh; /* Ajusta la altura para que ocupe toda la pantalla */
    object-fit: cover; /* Asegura que la imagen cubra todo el área sin distorsión */
    flex: 1;
}

@keyframes slide {
    0% { transform: translateX(0%); }
    14.28% { transform: translateX(0%); }
    28.56% { transform: translateX(-100%); }
    42.84% { transform: translateX(-200%); }
    57.12% { transform: translateX(-300%); }
    71.40% { transform: translateX(-400%); }
    85.68% { transform: translateX(-500%); }
    100% { transform: translateX(-600%); }
}
2. Menú de Navegación
El menú de navegación permite a los usuarios navegar entre las diferentes secciones del portafolio.

# HTML
El menú de navegación está definido en el archivo certificaciones.html:
<nav class="header__menu">
    <a class="header__menu__link" href="index.html">Home</a>
    <a class="header__menu__link" href="about.html">Sobre mí</a>
    <a class="header__menu__link" href="certificaciones.html">Certificaciones</a>
</nav>

# CSS
El estilo del menú de navegación está definido en el archivo styles/style.css:

.header__menu {
    display: flex;
    gap: 80px;
}

.header__menu__link {
    font-family: var(--fuente-montserrat);
    font-size: 1.5rem;
    font-weight: 600;
    color: var(--color-terciario);
    text-decoration: none;
    transition: color 0.3s, text-shadow 0.3s;
}

.header__menu__link:hover {
    color: var(--color-hover);
    text-shadow: 0 0 8px var(--color-terciario);
}

#Instalación
Clona el repositorio en tu máquina local.
Abre el archivo index.html en tu navegador para ver el portafolio.
Contribución
Si deseas contribuir a este proyecto, por favor sigue los siguientes pasos:

Haz un fork del repositorio.
Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).
Realiza tus cambios y haz commit (git commit -am 'Agrega nueva funcionalidad').
Haz push a la rama (git push origin feature/nueva-funcionalidad).
Abre un Pull Request.
