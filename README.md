# Creación de Archivos y Directorios con touch y mkdir

^[[200~mkdir proyecto_final^[[201~@dayipe120 ➜ /workspaces/practica-terminal (main) $ mkdir proyemkdir proyecto_final
@dayipe120 ➜ /workspaces/practica-terminal (main) $ cd proyecto_final
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ ls
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ mkdir codigo documentacion recursos
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ touch codigo/main.py codigo/config.json
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ touch documentacion/README.md
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ tree proyecto_final
proyecto_final  [error opening dir]

0 directories, 0 files
@dayipe120 ➜ /workspaces/practica-terminal/proyecto_final (main) $ tree
.
├── codigo
│   ├── config.json
│   └── main.py
├── documentacion
│   └── README.md
└── recursos

4 directories, 3 files

# Navegación en el Sistema de Archivos con cd y pwd

/home/dayana$ cd /var/log          → ahora estás en /var/log
/var/log$     cd ..                → subes → ahora estás en /var
/var$         cd -                 → regresas a donde estabas antes → /home/dayana
/home/dayana$ cd ~                 → vas (o regresas) a tu home (lo mismo que cd sin argumentos)
/home/dayana$ pwd                  → te muestra: /home/dayana

# Cambiar al Directorio Raíz

dayipe120 ➜ /workspaces/practica-terminal (main) $ cd /
@dayipe120 ➜ / $ pwd
/
@dayipe120 ➜ / $ ls
bin                etc   lib.usr-is-merged  mnt   run                 sys  vscode
bin.usr-is-merged  go    lib32              opt   sbin                tmp  workspaces
boot               home  lib64              proc  sbin.usr-is-merged  usr
dev                lib   media              root  srv                 var
@dayipe120 ➜ / $ 

# Navegar a un Directorio Específico

@dayipe120 ➜ / $ cd /home
@dayipe120 ➜ /home $ pwd
/home
@dayipe120 ➜ /home $ /home/dayipe120
bash: /home/dayipe120: No such file or directory
@dayipe120 ➜ /home $ echo $HOME
/home/codespace
@dayipe120 ➜ /home $ /home/codespace
bash: /home/codespace: Is a directory

 # Uso de rutas relativas

@dayipe120 ➜ ~ $ cd ~
@dayipe120 ➜ ~ $ pwd
/home/codespace
@dayipe120 ➜ ~ $ cd cd documentacion
bash: cd: too many arguments
@dayipe120 ➜ ~ $ cd documentacion
@dayipe120 ➜ ~/documentacion $ 

# volver al directorio anterior
@dayipe120 ➜ ~ $ cd /tmp
@dayipe120 ➜ /tmp $ cd -
/home/codespace
@dayipe120 ➜ ~ $ cd /tmp
@dayipe120 ➜ /tmp $ cd -
/home/codespace
@dayipe120 ➜ ~ $ cd -



# Ir al Directorio Personal
@dayipe120 ➜ /workspaces/practica-terminal (main) $ cd ~
@dayipe120 ➜ ~ $ pwd
/home/codespace
@dayipe120 ➜ ~ $ touch prueba.txt
@dayipe120 ➜ ~ $ ls
documentacion  java  nvm  prueba.txt
@dayipe120 ➜ ~ $ 

# Subir un Nivel en el Sistema de Archivos
Subir un Nivel en el Sistema de Archivos
@dayipe120 ➜ /home $ cd /home/codespace/documentacion
@dayipe120 ➜ ~/documentacion $ cd ..
@dayipe120 ➜ ~ $ cd ../..

# Combinar Rutas Relativas y Absolutas
@dayipe120 ➜ / $ cd /home
@dayipe120 ➜ /home $ cd codespace/Descargas
@dayipe120 ➜ ~/Descargas $ pwd
/home/codespace/Descargas
@dayipe120 ➜ ~/Descargas $ cd /home
@dayipe120 ➜ /home $ pwd
/home
@dayipe120 ➜ /home $ 

Usa absoluta cuando quieras ir a un lugar específico sin importar dónde estés.

Usa relativa cuando quieras moverte dentro de tu ubicación actual o sus subcarpetas/padres.

  #  Crear y Navegar a un Nuevo Directorio
@dayipe120 ➜ /home $ cd ~/pruebas
@dayipe120 ➜ ~/pruebas $ mkdir nivel1
@dayipe120 ➜ ~/pruebas $ cd nivel1
@dayipe120 ➜ ~/pruebas/nivel1 $ pwd
/home/codespace/pruebas/nivel1
@dayipe120 ➜ ~/pruebas/nivel1 $ 


# Directorios Ocultos
@dayipe120 ➜ ~/pruebas/nivel1 $ cd ~
@dayipe120 ➜ ~ $ ls -a
.              .bash_logout  .conda   .dotnet     .jupyter  .minikube   .php      .rbenv  .vscode-remote  Descargas      nvm
..             .bashrc       .config  .gitconfig  .local    .nvs        .profile  .ruby   .zprofile       documentacion  prueba.txt
.bash_history  .cache        .docker  .hugo       .maven    .oh-my-zsh  .python   .rvmrc  .zshrc          java           pruebas
@dayipe120 ➜ ~ $  cd .config
@dayipe120 ➜ ~/.config $ 
@dayipe120 ➜ ~/.config $ pwd
/home/codespace/.config

Los directorios que empiezan con un punto . son ocultos por convención.

Esto significa que no se muestran con ls normal, solo con ls -a.

La razón principal es evitar saturar tu directorio personal con archivos y configuraciones del sistema.

Suelen contener:

Configuraciones de programas (.config, .gitconfig)

Preferencias de tu terminal o shell (.bashrc, .zshrc)

Llaves y datos de seguridad (.ssh)

# Explora tu directorio actual

@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls
README.md  proyecto_final
@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls -a
.  ..  .git  README.md  proyecto_final
@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls -l
total 12
-rw-rw-rw-  1 codespace root      4831 Mar  2 04:12 README.md
drwxrwxrwx+ 5 codespace codespace 4096 Feb 25 04:06 proyecto_final

Responde: ¿Qué significa el primer carácter d en algunos elementos?

d = directorio (carpeta)

@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls -lah
total 24K
drwxrwxrwx+ 4 codespace root      4.0K Feb 25 04:05 .
drwxr-xrwx+ 5 codespace root      4.0K Feb 25 04:04 ..
drwxrwxrwx+ 8 codespace root      4.0K Mar  2 04:13 .git
-rw-rw-rw-  1 codespace root      5.3K Mar  4 02:17 README.md
drwxrwxrwx+ 5 codespace codespace 4.0K Feb 25 04:06 proyecto_final
@dayipe120 ➜ /workspaces/practica-terminal (main) $ 

 #  Desafío Final
@dayipe120 ➜ /workspaces/practica-terminal (main) $ mkdir mi_practica
@dayipe120 ➜ /workspaces/practica-terminal (main) $ cd mi_practica
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ touch archivo1.txt archivo2.txt
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ mkdir carpeta1 carpeta2
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ ls -lah
total 16K
drwxrwxrwx+ 4 codespace codespace 4.0K Mar  4 02:19 .
drwxrwxrwx+ 5 codespace root      4.0K Mar  4 02:18 ..
-rw-rw-rw-  1 codespace codespace    0 Mar  4 02:18 archivo1.txt
-rw-rw-rw-  1 codespace codespace    0 Mar  4 02:18 archivo2.txt
drwxrwxrwx+ 2 codespace codespace 4.0K Mar  4 02:19 carpeta1
drwxrwxrwx+ 2 codespace codespace 4.0K Mar  4 02:19 carpeta2
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ ls -R
.:
archivo1.txt  archivo2.txt  carpeta1  carpeta2

./carpeta1:

./carpeta2:
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ 



# Copiar un archivo

@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ touch prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ cp prueba.txt copia_prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ ls
archivo1.txt  archivo2.txt  carpeta1  carpeta2  copia_prueba.txt  prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ 

# Copiar un directorio
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ cp -r carpeta1 carpeta2
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ ls carpeta2
carpeta1

# Usar opciones avanzadas

@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ ls carpeta1
archivo1.txt
@dayipe120 ➜ /workspaces/practica-terminal/mi_practica (main) $ cp -fv carpeta1/archivo1.txt carpeta2/
'carpeta1/archivo1.txt' -> 'carpeta2/archivo1.txt'
@dayipe120 ➜ /workspaces/practica-terminal/mi_practi


 # Copiar un archivo

 @dayipe120 ➜ /workspaces/practica-terminal (main) $ touch prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls
README.md  mi_practica  proyecto_final  prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal (main) $ copia_prueba.txt
bash: copia_prueba.txt: command not found
@dayipe120 ➜ /workspaces/practica-terminal (main) $ ls
README.md  mi_practica  proyecto_final  prueba.txt
@dayipe120 ➜ /workspaces/practica-terminal (main) $ 


# touch archivo7.txtCopiar un directorio
@dayipe120 ➜ /workspaces/practica-terminal (main) $ mkdir carpeta3
@dayipe120 ➜ /workspaces/practica-terminal (main) $ cd carpeta3
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ mkdir archivo4.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

 # Forzar la sobrescritura de archivos
dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo7.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ cp archivo7.txt documentos/
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ cp -f archivo7.txt documentos/

# Mostrar mensajes detallados

@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ cp -v archivo7.txt documentos/
'archivo7.txt' -> 'documentos/archivo7.txt'
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Preservar atributos de archivos

'archivo7.txt' -> 'documentos/archivo7.txt'
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo8.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch -d "2022-01-01" archivo8.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ cp -p archivo8.txt copia_archivo8.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ ls -l archivo8.txt copia_archivo8.txt
-rw-rw-rw- 1 codespace codespace 0 Jan  1  2022 archivo8.txt
-rw-rw-rw- 1 codespace codespace 0 Jan  1  2022 copia_archivo8.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Copiar archivos con patrones
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo_a.txt archivo_b.txt archivo_c.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ cp archivo_*.txt documentos/
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ ls documentos/
archivo7.txt  archivo_a.txt  archivo_b.txt  archivo_c.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Renombrar Archivos Simples
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch prueba.txt
mv prueba.txt archivo_renombrado.txt
ls
archivo4.txt  archivo8.txt   archivo_b.txt  archivo_renombrado.txt  documentos
archivo7.txt  archivo_a.txt  archivo_c.txt  copia_archivo8.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

 # Renombrar Directorios
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ mkdir temporal
mv temporal archivos_temporales
ls
archivo4.txt  archivo8.txt   archivo_b.txt  archivo_renombrado.txt  copia_archivo8.txt
archivo7.txt  archivo_a.txt  archivo_c.txt  archivos_temporales     documentos
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 


# Mover Archivos a Otro Directorio

@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ mkdir documentos
touch informe.txt
mv informe.txt documentos/
ls documentos/
mkdir: cannot create directory ‘documentos’: File exists
archivo7.txt  archivo_a.txt  archivo_b.txt  archivo_c.txt  informe.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Mover Múltiples Archivos

@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo1.txt archivo2.txt archivo3.txt
mkdir respaldos
mv *.txt respaldos/
ls respaldos/
archivo1.txt  archivo3.txt  archivo7.txt  archivo_a.txt  archivo_c.txt           copia_archivo8.txt
archivo2.txt  archivo4.txt  archivo8.txt  archivo_b.txt  archivo_renombrado.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Mover y Renombrar al Mismo Tiempo

@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch datos_originales.txt
mkdir backup
mv datos_originales.txt backup/datos_backup.txt
ls backup/
datos_backup.txt
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Evitar Sobrescritura con i

dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo_existente.txt
mkdir documento
touch documento/archivo_existente.txt
mv -i archivo_existente.txt documento/
ls documento/
mv: overwrite 'documento/archivo_existente.txt'? 

# Actualizar Solo Archivos Nuevos con u


echo "Contenido viejo" > archivo_viejo.txt
mkdir respaldo
cp archivo_viejo.txt respaldo/
echo "Contenido nuevo" > archivo_viejo.txt
mv -u archivo_viejo.txt respaldo/
cat respaldo/archivo_viejo.txt
Contenido nuevo

# Mover Archivos a Rutas Absolutas
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch archivo_absoluto.txt
mv archivo_absoluto.txt /tmp/
ls /tmp/
archivo_absoluto.txt  dockerd.log  storage_version.txt         vscode-ipc-4431d0ae-dbb2-4855-9b2e-abca7290edf3.sock
codespaces_logs       sshd.log     vscode-git-cd2785e3aa.sock  vscode-ipc-8645d524-2c56-4972-8a09-da0d0fd09e43.sock
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 

# Mover Archivos con Espacios en el Nombre

@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ touch "mi archivo.txt"
mkdir destino
mv "mi archivo.txt" destino/
ls destino/
'mi archivo.txt'
@dayipe120 ➜ /workspaces/practica-terminal/carpeta3 (main) $ 





