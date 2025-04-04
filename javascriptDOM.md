## Seleccionar elemento

```javascript
//por id
const elemento = document.getElementById('id');
//por clase
const elemento = document.getElementsByClassName('clase');
//por etiqueta HTML
const elemento = document.getElementsByTagName('h1');
//por selector CSS
const elemento = document.querySelector('#id');
const elemento = document.querySelector('.clase');
const elemento = document.querySelector('ul li:last-child');
//por selector CSS (todos los elementos)
const elementos = document.querySelectorAll('.clase');
```

## Crear elementos

```javascript
//crear un elemento
const elemento = document.createElement('div');
//crear un nodo de texto
const texto = document.createTextNode('Hola mundo');
```

## Modificar elementos

```javascript
//añadir un nodo de texto a un elemento
elemento.appendChild(texto);
//añadir un elemento a otro elemento
elemento.appendChild(otroElemento);
//insertar un elemento antes de otro
elemento.insertBefore(nuevoElemento, elementoAnterior);
//reemplazar un elemento por otro
elemento.replaceChild(nuevoElemento, elementoAnterior);
//eliminar un elemento hijo
elemento.removeChild(elementoAnterior);
```

## Modificar atributos

```javascript
//obtener un atributo
const atributo = elemento.getAttribute('id');
//establecer un atributo
elemento.setAttribute('id', 'nuevoId');
//eliminar un atributo
elemento.removeAttribute('id');
```

## Modificar estilos

```javascript
//establecer un estilo
elemento.style.backgroundColor = 'red';
//obtener un estilo
const estilo = elemento.style.backgroundColor;
```

## Obtener atributos

```javascript
//obtener el contenido HTML de un elemento
const contenido = elemento.innerHTML;
//establecer el contenido HTML de un elemento
elemento.innerHTML = '<h1>Hola mundo</h1>';
//obtener el contenido de texto de un elemento
const contenido = elemento.textContent;
//establecer el contenido de texto de un elemento
elemento.textContent = 'Hola mundo';
//obtener el valor de un campo de formulario
const input1 = document.getElementById('input1');
const valor = input1.value;
```

## Eventos

```javascript
//añadir un evento
elemento.addEventListener('click', () => {
  console.log('¡Hola mundo!');
});
//eliminar un evento
elemento.removeEventListener('click', () => {
  console.log('¡Hola mundo!');
});
```

## Clases

```javascript
//añadir una clase
elemento.classList.add('clase');
//eliminar una clase
elemento.classList.remove('clase');
//alternar una clase, si la clase existe la elimina, si no existe la añade
elemento.classList.toggle('clase');
//comprobar si un elemento tiene una clase
const tieneClase = elemento.classList.contains('clase');
```