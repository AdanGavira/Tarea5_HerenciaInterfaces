# 🏃⚡ Pikachu vs Charizard: Herencia vs Interfaces en Hilos Java

# 📌 Descripción del Proyecto

Proyecto que demuestra las dos formas principales de crear hilos en Java:

  - Herencia (extends Thread) - Representado por PikachuCorredor

  - Interfaz (implements Runnable) - Representado por CharizardVolador

Este proyecto ilustra conceptos fundamentales de Programación Concurrente y Sistemas Paralelos (PSP) usando una analogía de Pokémon para hacer los conceptos más accesibles y divertidos.

# 🎯 Objetivos de Aprendizaje

  - Comprender la diferencia entre extends Thread e implements Runnable
  
  - Entender las limitaciones de la herencia simple en Java
  
  - Aplicar el concepto de polimorfismo con interfaces
  
  - Implementar programación multihilo básica
  
  - Reconocer cuándo usar cada enfoque en proyectos reales

# 🏗️ Estructura del Proyecto

📂 Paquete: TareaTema5_PSP

Clases Principales:

  - PikachuCorredor.java	Herencia (extends Thread)	Pikachu "ES UN" Thread. Hereda directamente de la clase Thread
  - CharizardVolador.java	Interfaz (implements Runnable)	Charizard "TIENE UNA TAREA". Implementa la interfaz Runnable
  - GimnasioMultihilo.java	Clase principal	Demuestra ambos métodos y compara su funcionamiento
  - Tarea 5 PSP.pdf	Documentación	Preguntas de reflexión y respuestas


# 🔍 Comparación Detallada
# ⚡ PikachuCorredor (extends Thread)

<img width="629" height="264" alt="image" src="https://github.com/user-attachments/assets/fc811a66-018f-4caa-8486-6409fb73ac76" />

<img width="771" height="342" alt="image" src="https://github.com/user-attachments/assets/4f0540ef-8a9a-49f1-8e27-9c4b69fe2a0f" />


# 🔥 CharizardVolador (implements Runnable)

<img width="621" height="270" alt="image" src="https://github.com/user-attachments/assets/01547770-4f93-44e4-9e10-b5fdc8c2b8fe" />

<img width="847" height="335" alt="image" src="https://github.com/user-attachments/assets/eb2cbdc5-c2bf-4da9-9fc1-ffc5307e542b" />


# 📊 Diferencias Clave
Aspecto:	        extends Thread	                                       implements Runnable
Relación:	        "ES UN" Thread	                                       "TIENE UNA" tarea Runnable
Herencia:	        Usa la herencia de clases	                             Usa implementación de interfaz
Flexibilidad:	    Limitada (no puede heredar otra clase)	               Alta (puede heredar otra clase)
Reutilización:	  Menor (está ligado a Thread)	                        Mayor (la tarea es separada del hilo)
Inicialización:	  Directa: objeto.start()	                              Indirecta: new Thread(objeto).start()

# 📝 Ejemplo de Salida Esperada

<img width="701" height="318" alt="image" src="https://github.com/user-attachments/assets/9adb3879-8a14-45ed-b981-4b26f4006002" />

# 🤔 Preguntas para Reflexión

# 1. ¿Cuál es la diferencia en cómo iniciamos PikachuCorredor vs CharizardVolador?

PikachuCorredor: Como hereda de Thread, él mismo tiene el método .start()

CharizardVolador: Solo es una tarea Runnable, necesita que un Thread lo ejecute

# 2. Si PikachuCorredor quisiera heredar también de Pokemon, ¿sería posible? ¿Por qué?

No es posible. Java solo permite herencia simple de clases. Pikachu ya hereda de Thread, por lo que no puede heredar también de Pokemon.

# 3. ¿Y CharizardVolador podría heredar de Pokémon además de implementar Runnable?

¡Sí puede! Charizard podría ser:

<img width="548" height="33" alt="image" src="https://github.com/user-attachments/assets/d53d1a89-df96-40fe-b822-f151b95d5110" />


# 💡 Ventajas y Desventajas

✅ Ventajas de implements Runnable

  - Mayor flexibilidad (puede heredar otra clase)
  - Mejor diseño orientado a objetos
  - Separación de preocupaciones
  - Reutilización de código

⚠️ Desventajas de extends Thread

  - "Gasta" la única herencia disponible
  - Menos flexible para cambios futuros
  - Acoplamiento más fuerte con Thread


# 🎮 Analogía Pokémon
Concepto Técnico	                          Analogía Pokémon
extends Thread	                  Pikachu ES UN corredor (se especializa en correr)
implements Runnable	              Charizard TIENE UNA misión de vuelo (puede hacer otras cosas)
Thread.sleep()	                  Descansar durante la carrera/misión
InterruptedException	            ¡Se tropezó! / ¡Le dio el viento!


# 🛠️ Buenas Prácticas
1. Prefiere implements Runnable sobre extends Thread (más flexible)
2. Nombra tus hilos para debugging más fácil
3. Maneja InterruptedException apropiadamente
4. Considera ExecutorService para proyectos más complejos


# 📚 Conceptos Clave Aprendidos

  - Herencia vs Composición: extends (es-un) vs implements (tiene-un)
  - Herencias Simple: Java solo permite una clase padre
  - Interfaces Múltiples: Se pueden implementar varias interfaces
  - Programación Concurrente: Ejecución paralela de tareas
  - Polimorfismo: Tratar diferentes objetos de manera uniforme

# 👨‍💻 Autor
Adán Gavira - Estudiante 



