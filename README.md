Retrieval-augmented generation (RAG) and Vector Databases

En este documento se indicaran los pasos para crear una aplicación de tipo RAG (Retrieval Augmented Generation) para la gestion de preguntas y respuestas por medio de un  motor basado en IA. 

Pre requisitos:
Python 3.11
Editor de código, en este tutorial se utilizó VS Code.
Una clave API de OpenAI
Una cuenta de Pinecone

Pasospara preaprar el entorno virtualizado:

1) crear un directorio, el cual se usara se usara para crear un entorno virtual aislado, el cual permitira gestionar las dependencias requeridas por la aplicación, evitando que estas tengan algún tipo de conflicto con las dependencias del SO u otro proyecto.
2) Crear el entorno virtual, para poder crear el entorno virtual, se debe acceder por linea de comandos al directorio creado en el paso anterior y ejecutar el siguiente comando: python3.11 -m venv "nombre del entorno que se desea crear"

![image](https://github.com/user-attachments/assets/97910e01-2217-4fa0-af82-1397aae73d06)

3) Activar el entorno virtual, para activarlo se debe ejecutar el siguiente comando:  "Nombre del entorno"\Scripts\activate

![image](https://github.com/user-attachments/assets/e620d7a1-2fd5-4502-91b3-2de3af9aa4fc)

4) Instalar los componentes requeridos, por medio del siguiente comando: pip install langchain openai, el cual instalara los componentes requeridos para que python pueda procesar las peticiones por medio de openAI.

![image](https://github.com/user-attachments/assets/189788b4-5c21-4eaa-91cf-a593d29386c9)


Una vez creado el entorno virtualizado, se debe crear la aplicaciónRAG ¿que componentes tiene una aplicación RAG?

Una aplicaicón RAG Implica dos componentes principales: indexación y recuperación y generación. El proceso de indexación incluye cargar datos, dividir el texto y almacenarlo en un almacén de vectores. El proceso de recuperación y generación implica recuperar datos relevantes del almacén de vectores y utilizar un modelo de lenguaje para generar una respuesta. El documento también proporciona instrucciones sobre cómo configurar los componentes necesarios, como un modelo de chat, un modelo de incrustación y un almacén de vectores.
Pasos para crear la aplicación RAG

1) Instalar las dependencias requeridas de langchain, por medio del siguiente comando: %pip install --quiet --upgrade langchain-text-splitters langchain-community

![image](https://github.com/user-attachments/assets/fc6cb12d-a884-402e-9a2c-3d343d454432)

2) Importar API KEY, para poder hacer uso del motor de OPENAI se requiere generar una llave, la cual sera importada apra ser usada por la aplicaicón RAG, por emdio del siguiente comando:

![image](https://github.com/user-attachments/assets/02a74103-b93e-4632-be9b-84afc0a071dc)

Donde getpass.getpass() es remplazado por la llave generada en OPEN AI, como se puede ver en el siguiente ejemplo:

![image](https://github.com/user-attachments/assets/3a757caf-196c-4088-82d0-7133eaeb765f)

3) Instalar las dependencias para el langchain-core, por medio del siguiente comando: pip install -qU langchain-core

![image](https://github.com/user-attachments/assets/decb0b55-fea1-4dae-867c-400bfb3456bb)

4) Crear un pipeline apra el proceso de indexación

![image](https://github.com/user-attachments/assets/3a005dfb-1066-4cd8-9b50-975347e3e81c)




