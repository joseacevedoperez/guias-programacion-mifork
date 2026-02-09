<!--
Posible prompt:
<prompt>
Tengo un cuestionario con preguntas sobre "Encapsulación". Debes tener en cuenta que los conocimientos previos que tengo (y por tanto tus respuestas deben ser adaptadas), son:
- C/C++ sin orientación a objetos.
- Temas de Java previos: Clases y Objetos.

Cada respuesta debe tener entre 2 - 4 párrafos de longitud (sin contar los trozos de código).

Por favor, escribe en impersonal las respuestas.

</prompt>
----
-->
# TEMA 2. Encapsulación

## 1. En Programación Orientada a Objetos (POO), ¿Qué buscan la **encapsulación** y **la ocultación** de información? Enumera brevemente algunas ventajas de la ocultación de información.

### La _**encapsulación**_ busca agrupar datos y métodos dentro de una misma entidad, normalmente una clase, de forma que podamos manejar objetos como unidades lógicas y coherentes. Esto ayuda a organizar el código y a que cada parte del programa tenga responsabilidades bien definidas. La _**ocultación**_ de información complementa este concepto restringiendo el acceso directo a los atributos internos, lo que evita que otras partes del programa puedan modificarlos de forma incorrecta.

### Gracias a la _ocultación de información_ ganamos seguridad y estabilidad, porque evitamos que un objeto pueda quedar en un estado inválido. Además, facilita el mantenimiento: si en el futuro queremos cambiar cómo funciona algo internamente, lo podemos hacer sin afectar al resto del código, siempre que mantengamos la misma interfaz pública.


## 2. ¿Qué se entiende por la **interfaz pública** de un objeto o clase en POO? Describe brevemente cómo se relaciona con la ocultación de información.

### La _**interfaz pública**_ de una clase es el conjunto de métodos (y a veces constantes) que otras partes del programa pueden utilizar para interactuar con sus objetos. Es básicamente “lo que la clase ofrece al exterior”, y debería ser lo más claro y estable posible para que los usuarios de la clase sepan exactamente cómo usarla.

### La relación con la _**ocultación de información**_ es directa: la interfaz pública es lo que dejamos visible, mientras que los detalles internos se mantienen privados. Así, el usuario de la clase no necesita saber cómo se implementan las cosas por dentro; solo necesita conocer los métodos públicos para interactuar con ella. Esto reduce errores y permite modificar la implementación interna sin romper el código que depende de la clase.


## 3. Brevemente: ¿Por qué hay que ser conscientes y diseñar con cuidado la **interfaz pública** de una clase? ¿Es fácil cambiarla?

### Diseñar bien la _**interfaz**_ pública es importante porque, una vez publicada, otros módulos o desarrolladores empezarán a depender de ella. Si después queremos modificarla, podría ser complicado o incluso imposible sin romper funcionalidades. Por eso se dice que una buena interfaz debe ser estable, sencilla y coherente con el propósito de la clase.

### Además, si la interfaz está mal pensada, la clase puede volverse difícil de usar o demasiado dependiente de cómo está implementada internamente. Esto va en contra de la idea de _**encapsulación**_. En cambio, cuando la interfaz está bien diseñada, trabajar con esa clase resulta más intuitivo y los cambios futuros se pueden hacer con mayor libertad.


## 4. ¿Qué son las **invariantes de clase** y por qué la ocultación de información nos ayuda?

### Las _**invariantes de clase**_ son condiciones que siempre deben cumplirse para que un objeto esté en un estado válido. Por ejemplo, en una clase CuentaBancaria, podríamos exigir que el saldo nunca sea negativo. Estas reglas forman parte de la lógica fundamental de la clase y deben mantenerse antes y después de ejecutar cualquier método.

### La _**ocultación de información**_ ayuda porque evita que código externo modifique directamente los atributos y rompa estas invariantes. Al obligar a que todas las modificaciones se hagan a través de métodos controlados (setters, validaciones, etc.), garantizamos que los objetos nunca entren en estados incoherentes. Es una forma de proteger la integridad del programa.


## 5. Pon un ejemplo de una clase `Punto` en `Java`, con dos coordenadas, `x` e `y`, de tipo `double`, con un método `calcularDistanciaAOrigen`, y que haga uso de la ocultación de información. ¿Cuál es la interfaz pública de la clase `Punto`? ¿Qué significa `public` y `private`?

### Respuesta


## 6. En Java, ¿A quiénes se pueden aplicar los modificadores `public` o `private`?

### En Java, _**public**_ y _**private**_ se pueden aplicar tanto a clases (aunque solo a clases “top-level” en el caso de public) como a atributos, métodos y constructores. Esto permite controlar qué partes del código son visibles desde fuera y cuáles están reservadas para el uso interno de la clase.

### Usarlos correctamente nos ayuda a organizar mejor el código y a evitar dependencias indeseadas entre módulos. También ayuda a los demás programadores a entender qué está pensado para ser usado desde fuera y qué forma parte de la implementación interna.


## 7. En POO, la visibilidad puede ser pública o privada, pero ¿existen más tipos de visibilidad? ¿Qué ocurre en Java? ¿Y en otros lenguajes?

### Sí, además de _**public**_ y _**private**_, existen otros niveles de visibilidad. En Java, por ejemplo, están _**protected**_ y el nivel **“default”** (cuando no se especifica nada). Protected permite el acceso desde la clase, sus subclases y clases del mismo paquete. El nivel por defecto permite el acceso desde cualquier clase del mismo paquete, pero no desde fuera.

### En otros lenguajes también existen variaciones. Por ejemplo, C++ tiene _**public, protected y private**_, pero su funcionamiento está más orientado a jerarquías de herencia que a _paquetes_. Python, en cambio, no tiene visibilidad estricta, pero usa convenciones como el guion bajo _atributo para indicar que algo debería tratarse como privado. Cada lenguaje adapta estos conceptos a su propio modelo de acceso.


## 8. Responde: Los miembros de instancia privados de un objeto están ocultos para (a) otras clases o (b) otras instancias, aunque sean de la misma clase. Pon un ejemplo añadiendo un método `calcularDistanciaAPunto(Punto otro)` y explica la respuesta.

### Respuesta


## 9. ¿Qué son los métodos "getter" y "setter" en los lenguajes orientados a objetos?

### Respuesta


## 10. Cuando nos referimos a que la ocultación de información mejora la "seguridad" del programa, ¿nos referimos a que no pueda ser "hackeado"?

### Respuesta


## 11. ¿Qué diferencia hay entre **miembro de instancia** y **miembro de clase**? ¿Los miembros de clase también se pueden ocultar?

### Respuesta


## 12. Brevemente: ¿Tiene sentido que los constructores sean privados?

### Respuesta


## 13. ¿Cómo se indican los **miembros de clase** en Java? Pon un ejemplo, en la clase `Punto` definida anteriormente, para que incluya miembros de clase que permitan saber cuáles son los valores `x` e `y` máximos que se han establecido en todos los puntos que se hayan creado hasta el momento.

### Respuesta


## 14. Como sería un método factoría dentro de la clase `Punto` para construir un `Punto` a partir de dos coordenadas, pero que las redondee al entero más cercano. Escribe sólo el código del método, no toda la clase ¿Has usado `static`? 

### Respuesta


## 15. Cambia la implementación de `Punto`. En vez de dos `double`, emplea un array interno de dos posiciones, intentando no modificar la interfaz pública de la clase.

### Respuesta


## 16. Si un atributo va a tener un método "getter" y "setter" públicos, ¿no es mejor declararlo público? ¿Cuál es la convención más habitual sobre los atributos, que sean públicos o privados? ¿Tiene esto algo que ver con las "invariantes de clase"?

### Respuesta


## 17. ¿Qué significa que una clase sea **inmutable**? ¿qué es un método modificador? ¿Un método modificador es siempre un "setter"? ¿Tiene ventajas que una clase sea inmutable?

### Respuesta


## 18. ¿Es recomendable incluir métodos "setter" siempre y como convención?

### Respuesta


## 19. ¿La clase `String` en Java es mutable o inmutable? ¿Qué ocurre al concatenar dos cadenas? ¿Qué debemos hacer si vamos a hacer una operación que implique concatenar muchas veces para construir paso a paso una cadena muy larga?

### Respuesta


## 20. En POO ¿Cómo se comparan objetos de una misma clase? ¿Por su contenido o por su identidad? ¿Qué es el método equals en Java? ¿Qué hace por defecto? ¿Cómo se deben comparar dos cadenas en Java? 

### Respuesta


## 21. ¿Qué son las clases "wrapper" en un lenguaje de programación orientado a objetos? ¿Cómo se hace? ¿Es un proceso automático? ¿Qué ventajas tienen? ¿Todos los lenguajes orientados a objetos tienen tipos primitivos y necesitan wrappers? 

### Respuesta


## 22. ¿En POO qué es un **tipo de dato enumerado**? ¿En Java, un tipo de dato enumerado es una clase? ¿Qué ventajas tienen en términos de encapsulación los enumerados en Java?

### Respuesta


## 23. Crea un tipo enumerado en Java que se llame `Mes`, con doce posibles instancias y que además proporcione métodos para obtener cuántos días tiene ese mes, el ordinal de ese mes en el año (1-12), empleando atributos privados y constructores del tipo enumerado. Añade además cuatro métodos para devolver si ese mes tiene algunos días de invierno, primavera, verano u otoño, indicando con un booleano el hemisferio (norte o sur, parámetro `enHemisferioNorte`). Es decir: `esDePrimavera(boolean esHemisferioNorte)`, `esDeVerano(boolean esHemisferioNorte)`, `esDeOtoño(boolean esHemisferioNorte)`, `esDeInvierno(boolean esHemisferioNorte)`

### Respuesta
