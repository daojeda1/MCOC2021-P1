# MCOC2021-P1
Optimización estructural de un puente reticular

En el siguiente informe se explicara el proceso realizado para diseñar un puente de reticulado en secciones ICHA de acero;

Incialmente se usó el codigo del profesor, sobre el cual comenzamos a crear nodos tanto para las uniones de las barras como para graficar en una interfaz 3D los puntos de las superficie sobre la cual estaria emplazado nuestro puente, a continuación, se puede visualizar una de las primerar aproximaciones del reticulado, en la cual, no teniamos más que los nodos y algunas barras que posteriormente irian tomando forma:

![image](https://user-images.githubusercontent.com/53507891/135769759-0b22ea6b-7b2a-49af-aa5d-32b10c2748c9.png)

Luego de crear todos los nodos, procedimos a crear el resto de las barras, el diseño se baso en piramides con diagonales en las bases, a medida que el puente iba tomando forma se veia similiar a esto:

![image](https://user-images.githubusercontent.com/53507891/135769823-fe9f760b-f674-486e-9bb9-3dba7dcf5fa6.png)

Sin embargo, este puente aún era inviable, de todas formas faltaba una columna que fuera capaz de tomar esfuerzos que el puente sin esta no era capaz de tomar, es por esto que se agrego una columna en la parte central de la quebrada, en el punto correspondiente al nodo 18.

Tambien es posible notar que los distintos tipos de secciones poseen colores distintos y además en las ocpiones graficas se tuvo que tomar la decision de eliminar la vista de nro de nodos y de barras, asi como se achicó el grosor de las barras (solo el grosor en el grafico, la sección corresponde a la misma)

![image](https://user-images.githubusercontent.com/53507891/135769927-87407730-cc79-41b6-8cbc-66bccf72a911.png)

Lamentablemente, con este último diseño del puente, el cual esperariamos que fuera el final, posee una matriz de rigidez singular, por lo tanto el problema de rigidez directa no tiene solución

Los pasos a seguir para lograr solucionar nuestro problema de matriz singular correspondieron en primer lugar a chequear que no tengamos algun nodo o barra que quedara libre y pueda generar un mecanismo, por otro lado tambien aplicamos cambios en los apoyos, iterando en dejar algunos fijos, otros simples y finalmente todos fijos, para lo cual, tampo tuvimos una respuesta satisfactoria. Finalmente comenzamos a hacer cambios en las secciones ICHA utilizadas, sin importar el peso en primer lugar, sino que preocupados de que el puente fuera viable, lamentablemente el peso se disparó para el ultimo diseño creado, y a pesar de ello, la matriz aún es singular. A continuación podemos ver el peso total del puente en una captura de pantalla

![image](https://user-images.githubusercontent.com/53507891/135770081-23a66e5f-f61b-4921-b30e-b44b5494e016.png)
