# Sololearn_Javascript
Respuestas a los miniquiz

1
[] Los caracteres que se usan para iniciar una variable son las letras
[] para genear una consola solo debemos poner console.log("¡JS es genial ! ");
[] para poder formar un codigo valido solo debemos poner <script>, nombre "james"; console.log (nombre); al final el </script>.
2
[] El resultado de intentar hacer referencia a un miembro de la matriz que no existe es indefinido
[] ingresando var example = new Array(); creamos una matriz vacia que se pueda llenar en cualquire momento despues.
[]Array tiene la propiedad "length", porque es un objeto.
3
[] En el objeto matematico,¿cual de los siguentes metodos se usa paracalcular la raiz? sqrt
[] ¿cuales de estos nombres son aceptables para la variables de javaScript? _modulo y primer modulo
4
[] para generar "js is cool!" a la consola: console.log ("¡JS es genial!");
[] ¿Que dos palabras clave necesitamos para crear una matriz? nuevo y formacion

Proyecto 1 

Necesitas planificar un viaje por carretera. Viaja a una velocidad promedio de 40 millas por hora .
Dada una distancia en millas como entrada (el código para tomar la entrada ya está presente), envíe a la consola el tiempo que le tomará recorrerlo en minutos . Entrada de muestra: 150 Salida de muestra: 225



function main() {
    var distance = parseInt(readLine(), 10);
    //tu código va aquí
    var i = distance / 40 * 60;
    console.log(i);
}


proyecto 2
El caracol en el pozo


El caracol sube 7 pies cada día y retrocede 2 pies cada noche.
¿Cuántos días tardará el caracol en salir de un pozo con la profundidad dada? Ejemplo de entrada: 31 Ejemplo de resultado: 6 Explicación : Analicemos la distancia que cubre el caracol cada día: Día 1: 7-2 = 5 Día 2: 5 + 7-2 = 10 Día 3:10 + 7-2 = 15 Día 4:15 + 7-2 = 20 Día 5:20 + 7-2 = 25 Día 6:25 + 7 = 32 Entonces, en el Día 6 el caracol alcanzará 32 pies y saldrá del pozo durante el día, sin resbalarse esa noche.

function main() {
    var depth = parseInt(readLine(), 10);
    //your code goes here
    var day = depth / (7-2);
    
    console.log(Math.round(day));
    
}
proyecto 3
Convertidor de moneda


Estás creando una aplicación de conversión de moneda.
Cree una función llamada convertir , que toma dos parámetros: la cantidad a convertir y la tasa, y devuelve la cantidad resultante.
El código para tomar los parámetros como entrada y llamar a la función ya está presente en Playground.
Cree la función para que el código funcione. Entrada de muestra: 100 1.1 Salida de muestra: 110

function main() {
    var amount = parseFloat(readLine(), 10);
    var rate = parseFloat(readLine(), 10);
    console.log(convert(amount, rate));
}
function convert(a,b){
    return a*b;
}
proyecto 4
Gerente de contacto


Estás trabajando en una aplicación Contact Manager.
Ha creado el constructor del objeto de contacto , que tiene dos argumentos, nombre y número.
Debe agregar un método print () al objeto, que generará los datos de contacto en la consola en el siguiente formato: nombre: número
El código dado declara dos objetos y llama a sus métodos print (). Complete el código definiendo el método print () para los objetos.

function contact(name, number) 
{
    this.name = name;
    this.number = number;
    this.print = print;
}

function print()
{
    console.log(this.name + ": " + this.number);
}

var a = new contact("David", 12345);
var b = new contact("Amy", 987654321)
a.print();
b.print();

proyecto 5
Gerente de la tienda


Está trabajando en un programa Store Manager, que almacena los precios en una matriz.
Debe agregar funcionalidad para aumentar los precios en la cantidad dada.
La variable de aumento se toma de la entrada del usuario. Necesita aumentar todos los precios en la matriz dada en esa cantidad y enviar a la consola la matriz resultante.



function main() {
    var increase = parseInt(readLine(), 10);
    var prices = [98.99, 15.2, 20, 1026];
    //your code goes here
    var newPrices = [];
    for( i = 0; i < prices.length; i++){
       newPrices.push(prices[i] + increase);
    }
    console.log(newPrices)
}
poyecto 6
Palabras


Estás creando un cifrador de texto. Debe tomar varias palabras y generar una versión combinada, donde cada palabra está separada por un signo de dólar $.
Por ejemplo, para las palabras " hola ", " cómo ", " estás ", " tú ", la salida debería ser " $ hola $ cómo $ eres $ tú $ ".
El código dado declara una clase llamada Add , con un constructor que toma un parámetro de descanso.
Complete el código agregando un método print () a la clase, que debería generar la salida solicitada.
class Add {
  constructor(...words) {
      this.words = words;
  }
  //your code goes here
  print(){
      var y ="";
      for (x of this.words) {
        if(x == ","){
          x = "";
        }
        else{
          y += "$" + x;
        }
      }

      y = y + "$";
      console.log(y);
  }
}

var x = new Add("hehe", "hoho", "haha", "hihi", "huhu");
var y = new Add("this", "is", "awesome");
var z = new Add("lorem", "ipsum", "dolor", "sit", "amet", ",", "consectetur", "adipiscing", "elit");
x.print();
y.print();
z.print();
