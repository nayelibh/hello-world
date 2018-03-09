# hello-world

**primer programa**

*cabecera de programa en bash
~~~
#!/bin/bash -x 
~~~
"menu inicial"
~~~
echo "  MENU    "

echo "a. fecha del dia"
echo "b. IP"
echo "c. Identificador de Usuario"
~~~
"Lectura de primera opcion seleccionada"
~~~
read -p 'de la opcion elegida:  ' num
~~~
"evaluacion de dato"
~~~

case $num in
        a)
           date
        ;;
        b)
           echo "1. Para IP inalambrica "
           echo "2. Para IP cableada"
           echo "Escriba la opcion seleccionada"
           read con

           if [ $con = 1 ];
                then
                ifconfig wlp16s0 | grep inet | awk {print'$1, $2'} | head -n 1
        else
           if [ $con = 2 ];
                then
                ifconfig enp0s25 | grep inet | awk {print'$1, $2'} | head -n 1
        else
                if [$con = *]
                then
                        echo "la opcion seleccionada es incorrecta"
        fi
        fi
        fi

        ;;
        c)
           whoami
        ;;
        *)
           echo "la opcion dada es incorrecta"
        ;;
        esac

echo "FIN" 
~~~
"esto es el fin del programa
