# Descripción

Pipeline para agregar usuarios en linux, crear una clave temporal, genere un archivo pdf con la configuración y permita cambiarla la clave al iniciar sesión.

# IMPORTANTE

- Antes asegurarse de tener permisos en el archivo /etc/sudoers para el usuario jenkins y configurar para que no solicite password como se declara a continuación, de lo contrario agregar la línea al archivo mencionado:

jenkins ALL=(ALL) NOPASSWD: ALL

![image](https://github.com/user-attachments/assets/b305a5e1-fde1-40c5-9f3b-ad86fb49ca6c)


# Instrucciones

- Ir a jenkins 
- Crear nuevo pileline y asignarle un nombre
- Seleccionar pipeline

![image](https://github.com/user-attachments/assets/b7736b70-cb52-4adf-83ee-d4b4526e8f59)

- Una vez dentro de la configuración (Colocar en decripción la misma o la de su preferencia).
- Seleccionar "This project is parameterized"
- Add Parameter string parameter Name = NOMBRE_APELLIDO
- Add Parameter string parameter Name = DEPARTAMENTO

![image](https://github.com/user-attachments/assets/91692031-7480-468f-bb0b-b63c06916dc6)

- Ir a pipeline definition
- Seleccionar en definition "Pipeline script from SCM" 
- Seleccionar en los siguientes campos los valores a continuación 
- SCM = "git"
- Repository URL = https://github.com/D4nHide/linux_Add_User.git

![image](https://github.com/user-attachments/assets/657b26c1-f021-4b97-b671-686b0dfd9415)

- Branch Specifier = */main
- Script Path = jenkinsfile

![image](https://github.com/user-attachments/assets/050f93c8-c9af-4935-aeb7-8d72ae0df167)

- Apply + save
- Luego de salir de la ventana de configuración veremos una imagen como la siguiente:

![image](https://github.com/user-attachments/assets/972e94f2-c725-4e11-a571-916119fdd6ac)

- Donde seleccionaremos "Build with Parameter"
- Rellenamos los campos con la información solicitada y build

![image](https://github.com/user-attachments/assets/76e16201-1cd4-4979-ba30-40b6a8e73dcc)

- Una vez que hayamos buildeado tendremos una respuesta si vamos al console output como esta

![image](https://github.com/user-attachments/assets/989bf202-dea5-4b49-a145-4aa65ba5eb38)

- Directorio creado + pdf

![image](https://github.com/user-attachments/assets/4d27efa3-d9be-4d32-b870-8c6615cb2a47)

![image](https://github.com/user-attachments/assets/5a1d68db-afb3-41d7-a541-f0db8a366f92)

![image](https://github.com/user-attachments/assets/2e196210-c3b7-4f41-b74a-588720d2a7de)





