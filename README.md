# C++ Ejercicio Clase Reloj

<img alt="points bar" align="right" height="36" src="../../blob/status/.github/activity-icons/points-bar.svg" />


```c++
//
//  main.cpp
//  AppReloj
//
//  Created by Ma. Guadalupe Roque Díaz de León on 08/11/22.
//

#include <iostream>
#include "Reloj.hpp"

int menu(){
    int opcion;
    /*
    cout << "Menú de opciones" <<
    "\n1. setHora(int)" <<
    "\n2. setMinutos(int)" <<
    "\n3. incremetar Minutos" <<
    "\n4. Salir" <<
    "\nTeclea la opcion:";
    // leer la opcion
     */
    cin >> opcion;
    
    return opcion;
}

int main() {
    // Declaración del objeto de la clase Reloj
    Reloj evento;
    int opcion, hr, min;
    
    // 1º Inicializar la vccc - la función menu( ) retorna la opcion elegida por el usuario
    opcion = menu( );
    
    while (opcion != 4){ // 2º Incluir la condición la vccc
        
        if (opcion == 1){
            // leer hora
            //cout << "Ingresa la nueva hora:";
            cin >> hr;
            evento.setHora(hr);
        }
        else if (opcion == 2){
            // leer minutos
            //cout << "Ingresa los nuevos minutos:";
            cin >> min;
            evento.setMinutos(min);
        }
        else if (opcion == 3){
            evento.incrementaMinutos();
        }
       
        else
            cout << "Opcion incorrecta\n";
        
        cout << evento.str( ) << endl;
        opcion = menu(); // 3º Actualizar la vccc dentro del ciclo
    }
    
    return 0;
}

```

```c++
/* Casos de Prueba
// caso 1 - opcion 1
Datos de entrada:
1
10
2
30
3
3
1
80
1
0
2
59
3
3
4
Datos de salida:
10:00
10:30
10:31
10:32
10:32
00:32
00:59
01:00
01:01
```

2. Push your changes back to your assignment GitHub repo. Remember to try to make your commits atomic and your commit messages descriptive.

3. Wait a minute for the tests to run. Refresh the repo page to see if you have completed the exercise successfully.
You should score 100 marks if the test passes.
