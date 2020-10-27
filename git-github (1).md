Notas sobre el curso de GIT <br>
Recomendacioon de un curso  - https://miriadax.net/web/gitmooc<br>
=============================
## descripcion

## Comandos
*Tenga en cuenta que estos comandos por lo general se escriben en una sola linea

| Comando * | Que significa | Que hace | ejemplo * | Notas |
| ------- | - | - | - | - |
| git init   |  | Inicializa git | cd "ruta/que/queremos/abrir" git init | Create an empty Git repository or reinitialize an existing one|
| git config |  | ver la configuración actual de git |  |  |
| git config --global user.email "tu@email.com" |  | Configurar tu email |  |  |
| git config --global user.name "Tu Nombre" |  | Configura tu nombre de usuario |  |  |
| git status  |  | Muestra el estado acual de la base de datos |  |  |
| git add _myfile.txt  |  | Agrega el archivo en Staging |  |  |
| git add . |  |  Sube todo los archivos de la carpeta actual |  |  |
| git rm -- cached _myfile.txt |  |  Elimina el archivo de la RAM sin eliminarlo de la carpeta |  |  |
| git commit -m "Primer commit de este archivo" |  | Sube el archivo al repositorio |  |  |
| git log _my file.txt |  | Puede ver todas las modificaciones del archivo asi como ver quien las hizo |  |  |
| git log --stat |  | Puede ver todas las modificaciones detalladas |  |  |
| git diff #old #actual |  | valida los cambios entre dos commits para un mismo archivo|  |  |
| git reset #old --hard |  | Regresa a una version anterior del #old |  |  |




```
  <!-- Este codigo solo se imprime, la sintaxis ruby no es evaluada cuando utilizamos las etiquetas '<%  %>' -->
  <% [1,2,3,4].each do |number| %>
    <p>Número: <%= number %></p>
  <% end %>

  <br>
  <!-- Este codigo se evalua, la sintaxis ruby es evaluada cuando utilizamos las etiquetas '<%=  %>'-->
  <%= [1,2,3,4].each do |number| %>
    <p>Número: <%= number %></p>
  <% end %>
```


## Instalar git
  - sudo apt update && sudo apt upgrade
  - sudo apt install git
  - git --version

## Configuracion git
  - git config --global user.name "vifrac"
  - git config --global user.email "vifrac@gmail.com"
  - git config --global color.ui true
  - git config --global core.editor “atom --wait”
  - git config --global core.editor “‘c:/program files/sublime text 3/sublimetext.exe’ -w”
  - git config --list

  - git config --global core.excludesfile ~/.gitignore_global
  
  - https://www.toptal.com/developers/gitignore

## init git 
   - mkdir git prueba
   - cd 
   - git init
   - verificar archivos
   - touch index.html
   - nano index.html
   - git status
   - git add index.html
   - git status
   - git rm index.html
   - list files 
   - rm index.html
   - nano index.html
   - git add index.html
   - git commit -m 'first commit'
   - modificar html
   - git add .
   - git commit
   - git log 
   - git log index
   - git show index
   - git diff

## integrar cambios github
- crear el repo en github
- clonar el repo con hhtp 
  - git remote add origin hhtps
- git push origin master
- git pull origin master 
- git pull origin master --allow-unrelated--histories
- list files
- git status
- git push origin master

## llaves ssh
  - ssh-keygen -t rsa -b 4096 -C “tu_email@gmail.com”
    - nos pedira una ruta donde gusrdad
    - nos pedira un password - confirmar password
    - nos genera en la ruta por defecto dos archivos
      - llave privada (id_rsa)
      - llave publica (id_rsa.pub)
    - validar creacion de archivos
    - verificamos que el agente ssh este eneble 
      - eval $(ssh-agent -s)
    - agregamos la llave privada a git (pide password)
      - ssh-add ~/.ssh/id_rsa
    - copiamos el contenido de la llave publica a en el apartado de seguridad de git
      - cat ~/.ssh/id_rsa.pub
      - https://github.com/settings/keys
        - new ssh key
        - title (ALGO QUE IDENTIFIQUE EL dominio o server o equipo que se usa)
        - key
    - clonamos un rep con ssh
    - verificamos los remotos
      - git remote -v
    - setear los origenes del repo 
      - git remote set-url origin 


## Lessons

- Lesson 05 - Cómo realizar una petición REST e interpretar sus resultados
- Conceptos extraídos de:
    - https://code.tutsplus.com/es/tutorials/a-beginners-guide-to-http-and-rest--net-16340
