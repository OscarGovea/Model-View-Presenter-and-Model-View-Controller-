# Model View Presenter y Model View Controller
## Model View Controller (MVC)
Recordar que el MVC es un patrón que permite desacoplar la implementación de las vistas de la implementación de la lógica de negocio de nuestro modelo.
### ¿Cómo se aplica actualmente el MVC en Android?
 - Modelos
El encargado de encapsular y mantener la lógica de negocio lo que tiene que hacer nuestra aplicación (Que vamos a mostrar).

 - Vistas
Los encargados de dibujar las vistas de nuestra aplicación ese conjunto de layouts creados en xml. (Cómo lo vamos a mostrar).

 - Controladores
Su función es intercambiar mensajes entre la vista y el modelo, típicamente se usa una subclase de Activity, Fragment y un Service como un controlador. (Formatea el modelo para su visualización y manipula eventos como la entrada del usuario).

## Model View Presenter (MVP)
Modelo–Vista–Presentador (MVP) es una derivación del patrón arquitectónico modelo–vista–controlador (MVC), y es utilizado mayoritariamente para construir interfaces de usuario.

En MVP el presentador asume la funcionalidad del "intermediario". En MVP, toda lógica de presentación es colocada al presentador.

 - View
Una View dentro de MVP no representa una vista del SDK de android (Android class View), es decir no es un TextView, ni un Button, ni un Layout, ni una Custom View, ni mucho menos una Activity o un Fragment.
Una View representa una abstracción de que puedo hacer con la vista, normalmente se asocia a una interface para representar la funcionalidad de una vista. La parte importante está en que una Activity o un Fragmento tienen la responsabilidad únicamente de implementar la interface View y conectar las acciones del usuario con el presenter.

 - Presenter
En este patrón es el encargado de coordinar la implementación de la vista y el modelo, actualiza la vista y actúa sobre los eventos de usuario que se envían por la vista. El presenter también recupera los datos del modelo y los prepara para su visualización.

 - Model
Es el proveedor de los datos que queremos mostrar en la vista, si estuviéramos usando Clean Architecture el modelo sería un interactor que implemente algún caso de uso.
![alt text](https://github.com/OscarGovea/Model-View-Presenter-and-Model-View-Controller-/blob/master/mvp.png)