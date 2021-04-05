# AddressBook

Programa en Java para poder crear contactos telefonicos, eliminar contactactos, buscar contactos, realizar una lista de los contactos que tenemos almacenados.

Se implementarán tres métodos para modificar la información de los contactos.

a. list: mostrar los contactos de la agenda.

b. create: crear un nuevo contacto.

c. delete: borrar un contacto.

Metodos

switch (opcion) {
case 1:

                       
nombre = teclado.pedirString("Introduce el nombre").toLowerCase().trim();
telefono = teclado.pedirInt("Introduce el telefono");
                        
                        
if(!agenda.containsKey(nombre)){
agenda.put(nombre.toLowerCase().trim(), telefono);
System.out.println("Se ha añadido el contacto");
}else{
System.out.println("Ya existe el contacto");
}
                        
break;
case 2:
                        
                       
if(agenda.entrySet().isEmpty()){
System.out.println("No hay contactos");
}else{
                            
for(Map.Entry<String, Integer> entry: agenda.entrySet()){
System.out.println("Nombre: "+entry.getKey()+" Telefono:"+entry.getValue());
}
}
                        
break;
case 3:

                        
nombre = teclado.pedirString("Introduce el nombre").toLowerCase().trim();
                        
                    
if(agenda.containsKey(nombre)){
System.out.println("El telefono es "+agenda.get(nombre));
}else{
System.out.println("El contacto no existe");
}
                        
break;
case 4:
                        
                        
nombre = teclado.pedirString("Introduce el nombre").toLowerCase().trim();
                        
                     
if(agenda.containsKey(nombre)){
System.out.println("El contacto existe");
}else{
System.out.println("El contacto no existe");
}
break;
case 5:

                       
nombre = teclado.pedirString("Introduce el nombre").toLowerCase().trim();
                        
                         
if(agenda.containsKey(nombre)){
agenda.remove(nombre);
System.out.println("El contacto se ha borrado");
}else{
System.out.println("El contacto no existe");
}
                        
break;
case 6:

salir = true;
break;
default:
System.out.println("Solo números entre 1 y 6");
}

Ejemplo
-----Actividad 4 AddressBook-----

1. Create contacto
2. List contactos
3. Buscar contacto
4. Existe contacto
5. Delete contacto
6. Salir
Escribe una de las opciones
1
Introduce el nombre
Dionei
Introduce el telefono
83838485
Se ha añadido el contacto
1. Create contacto
2. List contactos
3. Buscar contacto
4. Existe contacto
5. Delete contacto
6. Salir
Escribe una de las opciones

Programa finalizado correctamente

-----Dionei Lucio-----

Licencia

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
