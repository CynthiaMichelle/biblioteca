# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

# Aplicación React de Gestión de Libros

## Descripción
Esta aplicación React es un sistema estructurado para la creación y visualización de libros. Los usuarios pueden añadir libros proporcionando detalles como el título, autor, imagen de portada, una breve introducción y una reseña. Los libros creados se visualizan en la página principal, proporcionando una interfaz interactiva y fácil de usar.

## Componentes Principales

- **Book**: Muestra un libro individual con su portada, título y un enlace para más detalles. Interactúa con otros componentes para presentar una vista cohesiva.
- **View**: Despliega detalles completos de un libro seleccionado, incluyendo autor, introducción y reseña.
- **Create**: Permite a los usuarios crear un nuevo libro, capturando todos los detalles necesarios a través de un formulario interactivo.
- **Index**: La página principal que muestra todos los libros disponibles, actualizándose dinámicamente con cada nuevo libro agregado.
- **Layout**: Define el diseño general, incluyendo la barra de navegación (NavBar) y el espacio para el contenido principal.
- **NavBar**: Una barra de navegación intuitiva con enlaces a las páginas de inicio y creación de libros, mejorando la navegabilidad.

## Hooks

- `useState`: Gestiona el estado local de los formularios (Create) y los detalles del libro (View), asegurando una experiencia de usuario interactiva.
- `useEffect`: Utilizado en View para cargar los detalles del libro cuando la página se carga, asegurando que los datos estén actualizados.
- `useContext`: Permite compartir el estado de los libros entre componentes (Book, Index, View) sin pasar props manualmente, simplificando el flujo de datos.

## Gestión de Datos (`store.js`)

- **AppContext**: Un contexto de React que proporciona funciones para crear, obtener y actualizar libros. Facilita la administración del estado global de los libros y mejora la escalabilidad de la aplicación.

## Navegación y Rutas

- Se utiliza `react-router-dom` para manejar la navegación entre diferentes páginas y componentes, con rutas bien definidas que mejoran la experiencia del usuario y facilitan la mantenibilidad del código.

## Flujo de Usuario
- Creación de un Libro: El usuario navega a la página de creación, llena el formulario y envía los detalles. El libro se agrega al estado global y se muestra en la página principal, con retroalimentación adecuada al usuario.

- Visualización de Libros: La página principal muestra todos los libros creados con una interfaz actualizable que refleja inmediatamente las nuevas adiciones.

- Navegación: La barra de navegación permite una transición fluida y clara entre la creación de libros y la vista principal, destacando por su diseño intuitivo y accesibilidad.
