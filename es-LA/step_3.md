## Agrega un personaje

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
El jugador en tu mundo será un Gato o un Mapache. 
</div>
<div>
![La vista de escena con personaje.](imagenes/caracter-anadido.png){:width="300px"}
</div>
</div>

--- task ---

Haga clic en la carpeta **Modelos** en la ventana Proyecto. Un modelo describe cómo se ve un objeto 3D y se puede crear usando herramientas de modelado 3D como Blender. Hemos incluido algunos modelos que puedes utilizar.

Elija el modelo `Gato` o `Mapache` y arrástrelo desde la ventana Proyecto a la vista Escena:

![Animación de 'Mapache' siendo arrastrado desde la ventana del Proyecto a la vista de Escena.](images/drag-character.gif)

**Sugerencia:** Si accidentalmente agregó los modelos 'BaseGato' o 'BaseMapache', o si desea cambiar su personaje en este punto, puede eliminar el modelo de la escena. Haga clic derecho en el modelo Objeto de juego en la ventana de Jerarquía y seleccione 'Eliminar'.

![La ventana Jerarquía con el menú del botón derecho del ratón para el modelo y 'Eliminar' resaltado.](images/delete-model.png)

--- /task ---

Tu personaje aparecerá en la vista de escena con una pose T.

<p style="border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;">
La <span style="color: #0faeb0">**pose T**</span> es la posición predeterminada para un personaje de juego antes que este haya sido animado.
</p>

--- task ---

Haz clic en tu personaje en la vista de escena y presiona la tecla <kbd>F</kbd>.

**Sugerencia:** Si estas perdido en la vista de Escena, puedes hacer clic en su personaje (u otro Objeto de juego) en la ventana de Jerarquía y luego hacer clic en <kbd>Shift</kbd>+<kbd>F</kbd> para enfocar tu personaje en la vista de Escena.

--- /task ---

Hmm, tu personaje lleva varios accesorios.

--- task ---

Haz clic en tu personaje en la ventana de Jerarquía. Esto abrirá la configuración de Objeto de juego en la ventana de Inspeccion.

Haz clic en la flecha al lado de tu personaje en la ventana de Jerarquía para ver los 'objetos hijos'. Haga clic en **Malla de engranajes de construcción** y desmarque la casilla junto a su nombre en la ventana de Inspeccion. Esto ocultará el casco y el chaleco de alta visibilidad:

![Inspector con la propiedad 'Malla de engranajes de construcción' resaltada y sin marcar.](images/uncheck-hat-active.png)

![La vista de escena con 'Malla de engranajes de construcción' eliminada del Mapache.](images/no-hat-scene.png)

Oculta los otros accesorios para tu personaje de la misma manera, o simplemente mantén uno activo.

**Sugerencia:** Los Objetos de juego que no están activos aparecen atenuados en la ventana Jerarquía:

![Ventana de jerarquía con 'Malla de engranajes de construcción' en gris.](images/greyed-out-mesh.png)

--- /task ---

--- task ---

El jugador verá el juego a través de la 'Cámara principal', que se muestra como un ícono de cámara de video en la Escena. Seleccione la cámara en la ventana Jerarquía para ver la vista de cámara incrustada:

![Cámara seleccionada en la vista de escena.](images/camera-in-scene.png)

--- /task ---

La vista del juego muestra cómo se verá tu proyecto para un jugador.

--- task ---

Haz clic en la pestaña Vista del juego. Tu personaje estará en cualquier posición a la que lo hayas arrastrado en la vista de escena (es posible que no puedas verlo).

--- /task ---

Si tienes suficiente espacio en pantalla, entonces es realmente útil ver la vista de escena y la vista de juego al mismo tiempo.

--- task ---

Arrastre la pestaña Vista de juego hacia la derecha para que aparezca junto a la vista Escena:

![Arrastrar la pestaña Vista de juego para colocar la vista de juego a la derecha de la vista de escena.](images/side-by-side-views.gif)

--- /task ---

Unity usa coordenadas x, y y z para colocar lso Objetos de Juego en el espacio 3D:

[[[unity-3D-coordinates]]]

--- task ---

Selecciona tu personaje (en la ventana Jerarquía o en la vista Escena) y luego cambia su configuración de 'Transformar' para que la 'Posición' sea (0, 0, 0) — el centro del mundo:

![Transformar para el personaje seleccionado con la posición establecida en 0, 0, 0.](images/transform-centre.png)

Tu personaje se moverá al centro en la vista de escena y en la vista de juego:

![La vista Escena con el personaje en 0, 0, 0 en medio del plano.](images/transform-centre-scene-view.png)

--- /task ---

--- task ---

Cambia el nombre de tu personaje a 'Jugador' en la ventana de Inspeccion. Esto hará que sea más fácil de encontrar si agrega más Objetos de juego.

![El nombre del jugador se muestra en la ventana de Inspeccion.](images/player-name.png)

--- /task ---


--- save ---
