Este proyecto tiene como objetivo crear una Web App Single Page en un único fichero html (html/cas/js).
La aplicación trata de la digitalización de un Pasaporte del Vino en el que tenemos una página de inicio (landing Page) con info referente al pasaporte y botones CTA (call to action) para llamar o estimular la acción del visitante a dar de alta su pasaporte del vino. 

El pasaporte permite 4 sellos digitales de diferentes establecimientos para conseguir una recompensa o bonificación.

Se está diseñando esta aplicación como prototipo o demo de lo que se requiere en cuanto a diseño y funcionalidad y para ello se han especificado los siguientes requisitos:

1.- Interface completamente responsive, ya que será desde el móvil cómo se operará tanto por el usuario del pasaporte como por el establecimiento adscrito que sella

2.- La interface presenta de manera general en toda la Single Page un Header, un Footer y el área de contenidos con capacidad de hacer scroll preservando un margen al final para que no quede escondido el contenido debajo del header/footer sticky. 

2.1.- El Header está compuesto por un icono fontawesome referente a vino y pasaporte a modo de logo sencillo plano y un icono de hamburguer o algo más moderno que despliega el menú principal con los distintos items hacia cada página de la aplicación. Cada página de la aplicación se resulve con parámetros en la URL tipo ?page=nombre-pagina

2.1.1.- Las páginas son: inicio, Registrar Pasaporte, Mi pasaporte, Establecimientos, Mi Establecimiento, Escanear QR y Admin.

En en manú principal no presentaremos item de inicio porque lo tenemos en la casita del footer
Descripción de páginas:

Inicio: muestra una landing page con la info del pasaporte y botones para el alta del pasaporte,... 

Registrar Pasaporte: esta página muestra un formulario de registro para dar de alta pasaportes que generan un código QR que leerá el establecimiento para sellarlo. 

Mi pasaporte: permite loguearse para ver el pasaporte, sus datos, el QR generado con la URL:
https://airooc41n.github.io/miapp/?email=[email del pasaporte] con el logo en el centro de la aplicación 

Establecimientos: listado de los establecientos adscritos con sus datos enlazados a sus webs

Mi Establecimiento: formulario de login para que cada establecimiento mire sus datos. También presenta un botón para escanear el QR de un pasaporte que un usuario le presente en su móvil personal. Cuando pulsa el bóton escanear QR aparece una ventana que abre la cámara para escanear el QR, que cuando lo detecte como válido se presente un bótón encima "Sellar" para sellar el pasaporte escaneado. Si el pasaport ya fue sellado por un establecimiento le avisará que ya fue sellado (un establecimiento solo puede sellar un pasaporte. Un pasaporte admite 4 sellos de diferentes establecimientos)

Escanear QR: desparece porque se inplementa en página Mi Establecimiento después de que éste haga login correcto 

Admin: contiene un formulario de login con email=admin@admin.com y passwd=admin para entrar.
La página admin ecoge la información de cada tabla de la db (en arrays de objetos en localStorage), con un CRUD para visualizar y borrar registros y botones para resetear toda la tabla, siempre que se borra algo se alerta al admin para confirmar el borrado.
La página amdin también permitirá dar de alta a los establecimientos porque estarán sujetos a requisitos para darse de alta, y finalmente se hará por parte del administrador. Esto lo incluimos en el menú contextual del footer con icono de tres puntitos con el item Alta Establecimiento. 
En el menú contextual para la página de Admin incluirremos también más opciones como el sistema de import/export db en JSON, que permitirá salvaguardar toda la db almacenada en localStorage hasta el momento. De igual forma cuando importamos un json (backup de la db) no borraremos todo lo que haya sino que se incrementarán debidamente los registros a las tablas correspondientes.

 
2.2.- El Footer: contiene a la izquierda, el icono de la casita que nos lleva a la página de inicio. En el centro la versión de la app en texto y a la derecha el menú contextual de página con el icono de tres puntitos.
Tanto el header como el footer son sticky y el area de contenido de cada página permite scroll  entre ellos (no debe verse ninguna barra de scroll vertical, debe ser natual). El área de contenido se reserva un margen inferior para que nunca se tape el contenido por el footer
 
  