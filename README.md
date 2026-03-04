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



