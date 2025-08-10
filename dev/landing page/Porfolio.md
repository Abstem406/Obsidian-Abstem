# Proyecto de Clonación de Página Web con Astro y ShadcnUI

## 1. Planificación y Análisis
- **~={green}Objetivo=~**: Comprender la estructura y el diseño de la página objetivo.
- **~={cyan}Tareas=~**:
  - Identificar las secciones de la página.
  - Determinar el contenido y estilos de cada sección.
  - Notar cualquier interacción o funcionalidad adicional.

## 2. Configuración del Proyecto
- **~={green}Objetivo=~**: Asegurarse de que el proyecto Astro con Tailwind CSS y React esté configurado correctamente.
- **~={cyan}Tareas=~**:
  - Verificar que el proyecto se ha creado y se ha instalado correctamente.
  - Ejecutar `npm run dev` para asegurarse de que el servidor de desarrollo esté funcionando.

## 3. Diseño de la Estructura
- **~={green}Objetivo=~**: Dividir la página en componentes manejables.
- **~={cyan}Tareas=~**:
  - Crear una lista de componentes necesarios (e.g., Header, Hero, Services, Footer).
  - Crear archivos para cada componente en `src/components`.

## 4. *Creación de Componentes*
- **~={green}Objetivo=~**: Desarrollar los componentes individuales.
- **~={cyan}Tareas=~**:
  - **~={orange}Header=~**:
    - Crear ~={blue}Header.astro=~:
	    - este tiene un navbar donde a la izquierda tiene el nombre del sitio web en mi caso debe ser "bitforges.com" y a la derecha los apartados de la landing page "Inicio", "servicios", "Proyectos", "contacto" y adicionalmente un botón para cambiar entre light mode y dark mode
	    
    
  - **~={orange}Hero Section=~**:
    - Crear ~={blue}Hero.astro=~:
	    - luego seria la hero section, con un componente de pildora que diga "🥇Desarrollo web Profesional" a la parte izquida de la pagina
	    - debajo de la pildora esta el titulo que dice "Soluciones digitales" este tiene que aparecer con un efecto de typing al inicial la pagina 
	    - debajo del titulo tiene que estar una description "Creamos paginas web modernas, sistemas administrativos personalizados y soluciones digitales que impulsen tu negocio hacia el éxito.\n desde landing page hasta sistemas de gestión  completos." 
	    - debajo de la descriptión dos botones
		    - "Comenzar proyecto ➜"
		    - "Ver portafolio"
	
  - ~={orange}**Services Section**=~:
    - Crear ~={blue}Services.astro=~:
	    - tiene que haber un titulo al principio de la sección "Nuestros Servicios" en medio de la pagina
	    - debajo del titulo una breve descripción "Ofrecemos soluciones completas para todas tus necesidades digitales"
	    - ahora debajo de la descripción tiene que haber un 2 filas y 3 columnas conformadas por cards 
	    - las cards deben de ser un componente que tenga un icono un titulo un pequeña descripción y justo debajo de esa pequeña descripción tiene que haber una lista desordenada con los servicios relacionados con la card: 
	      icono para la lista desordenada https://icon-sets.iconify.design/lucide/?icon-filter=check&keyword=lucide+ <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><g fill="none" stroke="#00c71f" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path d="M21.801 10A10 10 0 1 1 17 3.335" /><path d="m9 11l3 3L22 4" /></g></svg>
		    FILA 0 COLUMNA 0:
			- icon\n 
		    - titulo "Landing Pages"
		    - descripción: "Páginas web atractivas y optimizadas para conversión"
		    - lista desordenada: 
			    - Diseño responsive
			    - SEO optimizado
			    - Carga rápida
				
			FILA 0 COLUMNA 1:
			- icon\n 
		    - titulo "Sistemas de Ventas"
		    - descripción: "Plataformas completas para gestionar tus ventas"
		    - lista desordenada: 
				- Control de inventario
				- Reportes detallados
				- Facturación automática
			FILA 0 COLUMNA 2:
			- icon\n 
		    - titulo: "Sistemas Administrativos"
		    - descripción: "Herramientas personalizadas para tu empresa"
		    - lista desordenada: 
				- Gestión de usuarios
				- Dashboard personalizado 
				- Integración con APIs
				
			FILA 1 COLUMNA 0:
			- icon\n 
		    - titulo "Desarrollo a Medida"
		    - descripción: "Soluciones personalizadas para necesidades específicas"
		    - lista desordenada: 
				- Análisis de requerimientos
				- Desarrollo ágil
				- Soporte continuo
				
			FILA 1 COLUMNA 1:
			- icon\n 
		    - titulo "Hosting Web"
		    - descripción: "Alojamiento seguro y confiable para tu sitio web"
		    - lista desordenada: 
				- SSL gratuito
				- Backups automáticos
				- Soporte 24/7
				
			FILA 1 COLUMNA 2:
			- icon\n (este icono tiene que ser que estar dentro de un cuadrado para ponerle un fondo llamativo y que resalte un poco mas )
		    - titulo "Consultoría Personalizada"
		    - descripción: "¿Tienes una idea específica? Hablemos sobre tu proyecto"
		    - un botón que diga "Contactar Ahora"


  - ~={orange}**Projects Section**=~:
    - Crear ~={blue}projects.astro=~:
	    - tiene que haber un titulo al principio de la sección "Proyectos Destacados" en medio de la pagina
	    - debajo del titulo una breve descripción "Algunos de nuestros trabajos más recientes que demuestran nuestra experiencia y calidad"
	    - ahora debajo de la descripción tiene que haber un 2 filas y 4 columnas conformadas por cards 
	    - las cards deben de ser conformadas de la siguiente forma: 
		    FILA 0 COLUMNA 0:
		    - la card en este caso es rectangulo que esta conformado por 2 partes la superior y la inferior que están divididas a la mitad del rectangulo, 
			    - la superior tiene una imagen que muestra una preview del proyecto y que en la parte superior derecha tiene un componente de pildora con el tipo de sistema que es por ejemplo "Web app", "Dashboard", "Landing" "E-commerce"
			    - En la parte inferior un 
				    - titulo "E-commerce Platform"
				    - pequeña descripción: "Plataforma completa de comercio electrónico con..."
				    - y unas cuantas pildoras mas que destaquen con que fue hecho el sistema por ejemplo "React", "Node.js","mongoDB" etc..



  - ~={orange}**Contacts Section**=~:
    - Crear ~={blue}contacts.astro=~:
	    - tiene que haber un titulo al principio de la sección "¿Listo para transformar tu negocio?" en medio de la pagina
	    - debajo del titulo una breve descripción "Contáctanos hoy y descubre cómo podemos ayudarte a crear la solución digital perfecta para tu empresa."
	    - ahora debajo de la descripción tiene que haber un 1 filas y 4 columnas conformadas por cards con las distintas formas de contactar el servicio whatsapp, telegram, Instagram y Email
	    - las cards deben de ser conformadas de la siguiente forma: 
		    FILA 0 COLUMNA 0:
		    - icono de Whatsapp en medio de la carta (Icono de la red socila) 
		    - en este caso el titulo debajo del icono y tambien me medio de la carta debe ser el nombre de la red social en este ejemplo WhatsApp
		- y debajo de las cards de contacto un breve parrafo con el texto "Respuesta garantizada en menos de 24 horas"



  - ~={orange}**Footer**=~:
    - Crear `Footer.astro`.
    - Diseñar y codificar el pie de página.

## 5. Estilo con Tailwind CSS
- **~={green}Objetivo=~**: Aplicar estilos a los componentes usando Tailwind CSS.
- **~={cyan}Tareas=~**:
  - Estilizar cada componente con clases de Tailwind CSS.
  - Asegurarse de que los estilos sean coherentes y se ajusten al diseño deseado.

## 6. Implementación de Funcionalidades
- **~={green}Objetivo=~**: Agregar cualquier funcionalidad necesaria a los componentes.
- ~={orange}**~={cyan}Tareas=~**=~:
  - Implementar enlaces y botones de acción.
  - Si es necesario, integrar React para manejar lógica de estado y eventos.

## 7. Revisión y Optimización
- **~={green}Objetivo=~**: Revisar y optimizar el proyecto.
- **~={orange}~={cyan}Tareas=~=~**:
  - Comprobar que todo esté funcionando correctamente.
  - Optimizar el rendimiento y la accesibilidad si es necesario.

## 8. Despliegue
- **~={orange}~={green}Objetivo=~=~**: Desplegar el sitio web en línea.
- **~={green}~={orange}~={cyan}Tareas=~=~=~**:
  - Configurar el servicio de despliegue (e.g., Vercel, Netlify).
  - Desplegar el proyecto y verificar que esté funcionando en línea.

## Consejos Adicionales
- **~={green}Practicar=~**: La mejor manera de aprender es practicar. No te preocupes si no lo haces perfecto la primera vez.
- **~={green}Documentación=~**: Lee la documentación de Astro y Tailwind CSS para aprender más sobre sus capacidades.
- **~={green}Comunidad=~**: Únete a comunidades en línea, como foros o grupos de Discord, para obtener ayuda y compartir tu progreso.