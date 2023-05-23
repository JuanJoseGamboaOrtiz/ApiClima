## Consumiendo la API de OpenWeatherMap con JavaScript (usando Fetch)

Este repositorio contiene un ejemplo de cómo consumir la API de OpenWeatherMap utilizando JavaScript y la función `fetch()` para obtener datos meteorológicos de diferentes ciudades. OpenWeatherMap proporciona información detallada sobre el clima actual y pronósticos futuros.

### Uso de la API de OpenWeatherMap

Para comenzar a utilizar la API de OpenWeatherMap, sigue estos pasos:

1. Regístrate en [OpenWeatherMap](https://home.openweathermap.org/users/sign_up) si aún no tienes una cuenta.
2. Inicia sesión en tu cuenta de OpenWeatherMap.
3. Obtén tu clave de API en la sección "API Keys" dentro de tu perfil.

### Configuración

Antes de comenzar, asegúrate de tener un archivo HTML básico y un archivo JavaScript en tu proyecto. A continuación, agrega el siguiente código en tu archivo JavaScript:

```javascript
// Reemplaza 'YOUR_API_KEY' con tu clave de API obtenida de OpenWeatherMap
const apiKey = 'YOUR_API_KEY';

// Función para obtener los datos meteorológicos de una ciudad
function getWeather(city) {
  const apiUrl = `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}`;

  fetch(apiUrl)
    .then(response => response.json())
    .then(data => {
      // Manipula los datos recibidos como desees
      console.log(data);
    })
    .catch(error => {
      // Manejo de errores en caso de falla en la solicitud
      console.error('Error:', error);
    });
}

// Ejemplo de uso
const city = 'London'; // Nombre de la ciudad para la cual deseas obtener el pronóstico del tiempo
getWeather(city);
```

### Uso

Una vez que hayas configurado tu clave de API y tengas el código JavaScript en tu archivo, simplemente abre tu archivo HTML en un navegador web. El código JavaScript llamará a la función getWeather() con el nombre de la ciudad que desees obtener el pronóstico del tiempo.

Los datos meteorológicos se mostrarán en la consola del navegador, pero puedes manipularlos y mostrarlos en la página HTML según tus necesidades.

### Personalización
Puedes personalizar el código JavaScript según tus necesidades. Por ejemplo, puedes utilizar otros endpoints de la API de OpenWeatherMap, agregar parámetros adicionales en la URL, manejar la respuesta de manera diferente, etc.

Ten en cuenta que OpenWeatherMap tiene documentación detallada sobre los diferentes endpoints y parámetros disponibles en su sitio web.