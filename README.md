CIFRADO CÉSAR
=============

Cifrando
--------
___________________________________________________________________________________________________________________________________________
**Creamos una función** cipher (question)

Pedimos al usuario ingresar un texto y lo

convertimos a mayúsculas todas las  letras

``question = prompt("Ingrese un texto").toUpperCase();  ``



 creamos una nueva variable con un array vacio

 ``newPhrase= [ ]; ``

**Iniciamos un ciclo que pida solo inigresar texto**

     var verification = parseInt(question);
        while(verification >=0 || verification <=0 || question === ' '){
          question= prompt("Ingrese un texto").toUpperCase();
             verification = parseInt(question);}


  **Mediante split hacemos la separación de cada letra independientemente**

 `` question = question.split('');``

  **Iniciamos el ciclo que recorrera todo el texto**

  ``for(var i =0; i<question.length;i++){ ``

  **Pedimos la posición en el codigo ASCCI**

    var position = question[i].charCodeAt();

   **Aplicamos la formula para que nos de la posicion de la legtra deseada**


     var letter = ((position-65+33)%26+65);

   **Aplicamos el método para que nos retorne la letra en el cifrado**


     var encryptedLetter = String.fromCharCode(letter)};
           newPhrase.push(encryptedLetter); //agregamos al nuevo array


**Pedimos que nos retorne las letras unidas**

  ``return newPhrase.join('')};``

**Lo vemos en consola**
 `` console.log(cipher()); ``




 Descifrando
-------------
________________________________________________________________________________________________________________


 **Creamos una función** decipher (phrase)

Pedimos al usuario ingresar un texto y lo

convertimos a mayúsculas todas las  letras

``phrase = prompt("Ingrese un texto").toUpperCase();  ``



 creamos una nueva variable con un array vacio

 ``newA= [ ]; ``

**Iniciamos un ciclo que pida solo inigresar texto**

     var verification = parseInt(phrase);
        while(verification >=0 || verification <=0 || phrase === ' '){
          phrase= prompt("Ingrese un texto").toUpperCase();
             verification = parseInt(phrase);}


  **Mediante split hacemos la separación de cada letra independientemente**

 `` phrase = phrase.split('');``

  **Iniciamos el ciclo que recorrera todo el texto**

  ``for(var i =0; i<phrase.length;i++){ ``

  **Pedimos la posición en el codigo ASCCI**

    var place = phrase[i].charCodeAt();

   **Aplicamos la formula para que nos de la posicion de la legtra deseada**


     var words = ((place-65+33)%26+65);

   **Aplicamos el método para que nos retorne la letra en el cifrado**


     var encrypt = String.fromCharCode(words)};
           newA.push(encrypt); //agregamos al nuevo array


**Pedimos que nos retorne las letras unidas**

  ``return newA.join('')};``

**Lo vemos en consola**
 `` console.log(decipher()); ``

 $ git push origin master



Diagrama de flujo
-----------------

![Con titulo](CIFRADO_CESAR/d.jpg "Diagrama")
