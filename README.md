## Tarea 1
- **Sistema Operativo:** Windows 10 Pro
- **Versión de Git:** `git  2.55.0.windows.5`
- **Editor:** VS Code

## Tarea 2 

Que es SSH? 

SSH es un protocolo de red seguro que permite conectar pcs por internet de manera segura y gracias ello poder traspasar datos o lo que quieras sin preocuparte 


¿Qué diferencia existe entre una clave pública y una clave privada? 

La clave privada es la que mantienes en tu propio pc y sirve para interactuar con la llave publica, que es la que cifra los datos y solo puede abrirse con tu llave privada, es decir que son distintas, pero se necesitan la una a la otra. 


¿Qué clave puede compartirse? 

Solo la pública, porque solo se abre con tu clave privada, que es la que tienes que mantener privada. 


¿Qué clave no debe compartirse nunca? 

Lo acabo de decir en el anterior, la privada. 


¿Qué ventaja presenta SSH frente a introducir continuamente usuario y contraseña? 

Que es más cómodo y seguro, porque autentifica el pc automáticamente y te hace ahorrarte poner todo el rato el usuario y la contraseña con comandos que te la suelen pedir 


¿Qué función cumple el archivo known_hosts? 

Sirve para saber sitios de confianza y evitar que te suplanten la identidad comparando la huella digital de la primera vez que nos conectamos a Github. 


¿Qué podría ocurrir si una clave privada se publica en GitHub? 

Pues si se sube a un repositorio publico cualquiera podria hacerse pasar por mi y modificar mis repositorios 


Conexión SSH con GitHub: comprobada correctamente


## Historial del proyecto

Realizar varios commits pequeños y coherentes en lugar de un único commit masivo presenta múltiples ventajas:

- **Facilidad para detectar errores:** Si un cambio introduce un fallo, es sencillo ver en qué commit exacto se produjo.
- **Reversión precisa:** Permite deshacer o modificar una funcionalidad específica sin perder el trabajo realizado en otras partes del código.
- **Trazabilidad y claridad:** Facilita a otros desarrolladores (o a uno mismo en el futuro) comprender la evolución progresiva del proyecto a través de mensajes descriptivos.

## Conflicto resuelto

- **Causa del conflicto:** Se produjo al intentar fusionar la rama `feature/nuevo-eslogan` en `main` habiendo modificado exactamente la misma línea de código (`<p>` del encabezado en `index.html`) en ambas ramas de forma independiente.
- **Archivo afectado:** `index.html`.
- **Decisión tomada:** Se analizaron ambas propuestas y se redactó una versión consensuada que combina las dos ideas: *"Un espacio para conocer las fases del desarrollo, despliegue y mantenimiento de aplicaciones web."*
- **Comprobación de la resolución:** Se eliminaron los marcadores de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`), se verificó la correcta visualización en el navegador y se completó la fusión mediante `git add` y `git commit`.

## Instrucciones de uso

Para visualizar la página web en tu entorno local:

1. Clona el repositorio o descarga el código fuente.
2. Abre el archivo `index.html` directamente en cualquier navegador web o utiliza una extensión de servidor local como *Live Server* en VS Code.

## Editando desde GitHub

## Diferencia entre Git Fetch y Git Pull

- **¿Qué hizo `git fetch`?:** Descargó los nuevos commits y referencias del repositorio remoto (`origin/main`) a la base de datos local de Git, pero sin modificar ningún archivo de nuestro directorio de trabajo ni alterar nuestra rama `main` local.
- **¿Qué hizo `git pull`?:** Si hubiéramos ejecutado `git pull`, habría realizado automáticamente dos acciones consecutivas en un solo paso: un `git fetch` (descargar datos) seguido de un `git merge` (integrar cambios en la rama local).
- **¿Por qué `git fetch` permite revisar antes de integrar?:** Porque al separar la descarga de la fusión, podemos utilizar comandos como `git diff main..origin/main` o `git log main..origin/main` para inspeccionar con seguridad qué código ha escrito otra persona antes de incorporarlo a nuestro trabajo, evitando posibles conflictos imprevistos.
- **Relación entre `pull`, `fetch` y la integración posterior:** La fórmula fundamental de Git es:  
  `git pull = git fetch + git merge` (o `git rebase`).

  ## Propuesta de cambios