# Para subir un nuevo repositorio
- echo "# example" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin https://github.com/samuelbonet/example.git
- git push -u origin main

# Para actualizar el repositorio
- git remote add origin https://github.com/samuelbonet/example.git
- git branch -M main
- git push -u origin main


# Git & GitHub Cheatsheet 🚀

## **Configuración inicial**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git config --global user.name "Tu Nombre"` | Configura tu nombre de usuario global.               |
| `git config --global user.email "tu@email.com"` | Configura tu correo electrónico global.             |
| `git config --list`                    | Muestra la configuración actual de Git.             |

---

## **Ayuda y estado del repositorio**
| Comando               | Descripción                                          |
|-----------------------|------------------------------------------------------|
| `git help`           | Muestra ayuda general sobre Git.                     |
| `git status`         | Muestra el estado del repositorio (archivos cambiados, no rastreados, etc.). |
| `git log`            | Muestra el historial de commits.                     |
| `git log --oneline`  | Muestra un historial resumido en una sola línea por commit. |

---

## **Iniciar un repositorio**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git init`                             | Crea un repositorio Git en el directorio actual.     |
| `git clone <URL>`                      | Clona un repositorio remoto.                        |

---

## **Ramas (Branches)**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git branch`                           | Lista todas las ramas en el repositorio.            |
| `git branch <nombre-rama>`             | Crea una nueva rama.                                |
| `git checkout <nombre-rama>`           | Cambia a una rama existente.                       |
| `git checkout -b <nombre-rama>`        | Crea y cambia a una nueva rama.                    |
| `git merge <nombre-rama>`              | Fusiona la rama especificada en la actual.          |
| `git branch -d <nombre-rama>`          | Elimina una rama local.                             |

---

## **Rastreo y cambios**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git add <archivo>`                    | Agrega un archivo específico al área de preparación. |
| `git add .`                            | Agrega todos los archivos al área de preparación.    |
| `git commit -m "mensaje"`              | Crea un commit con un mensaje.                      |
| `git commit --amend`                   | Modifica el último commit (incluido el mensaje).     |

---

## **Sincronización con repositorios remotos**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git remote -v`                        | Muestra los remotos configurados.                   |
| `git remote add origin <URL>`          | Conecta un repositorio local con un remoto.         |
| `git pull origin <rama>`               | Descarga y combina cambios del remoto a tu rama actual. |
| `git push origin <rama>`               | Sube tus cambios locales al remoto.                 |
| `git push -u origin <rama>`            | Sube los cambios y configura el seguimiento de la rama. |

---

## **Deshacer cambios**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git restore <archivo>`                | Revierte cambios en el archivo (sin commit).         |
| `git restore --staged <archivo>`       | Saca un archivo del área de preparación.            |
| `git reset <commit>`                   | Deshace cambios a un commit específico (mantiene cambios en los archivos). |
| `git reset --hard <commit>`            | Restablece el repositorio a un commit anterior (se pierden cambios no guardados). |
| `git revert <commit>`                  | Crea un nuevo commit que deshace los cambios de un commit anterior. |

---

## **Etiquetas (Tags)**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git tag`                              | Lista todas las etiquetas.                          |
| `git tag <nombre-etiqueta>`            | Crea una nueva etiqueta.                            |
| `git push origin <nombre-etiqueta>`    | Sube la etiqueta al repositorio remoto.             |

---

## **Inspección y comparación**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git diff`                             | Muestra los cambios no confirmados.                 |
| `git diff <rama1>..<rama2>`            | Compara los cambios entre dos ramas.                |

---

## **Trabajo con Pull Requests (PR)**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `gh pr create`                         | Crea un nuevo Pull Request (requiere GitHub CLI).    |
| `gh pr list`                           | Lista los Pull Requests abiertos (requiere GitHub CLI). |
| `gh pr checkout <id>`                  | Cambia a una rama asociada a un PR.                 |

---

## **Atajos útiles**
| Comando                                | Descripción                                           |
|----------------------------------------|-------------------------------------------------------|
| `git stash`                            | Guarda cambios sin confirmar temporalmente.          |
| `git stash apply`                      | Recupera cambios guardados en stash.                |
| `git alias <alias> '<comando>'`        | Crea un alias para un comando.                      |


---
Template Pull Request

## Describe tus cambios

## Número y enlace del ticket de issue

## Acciones realizadas
- [ ] Ejemplo
- [ ] Ejemplo
- [ ] Ejemplo
- [ ] Ejemplo

---

[![git-flow.png](https://i.postimg.cc/N0XT5dwY/git-flow.png)](https://postimg.cc/LqHhWBX0)


---

### **1. Master**
- **Descripción:** Es la rama principal y estable del proyecto. Contiene el código de producción listo para ser lanzado.
- **Uso:** Solo se actualiza con versiones completamente probadas y liberadas.

---

### **2. Develop**
- **Descripción:** Es la rama de desarrollo principal donde se integra el trabajo de las distintas ramas de *feature*. 
- **Uso:** Sirve como base para las nuevas funcionalidades y se fusiona con `master` al lanzar una nueva versión.

---

### **3. Feature**
- **Descripción:** Ramas temporales creadas para desarrollar funcionalidades específicas o mejoras.
- **Uso:** Se crean a partir de `develop` y, una vez completadas, se fusionan de nuevo en `develop`.

---

### **4. Release**
- **Descripción:** Ramas creadas para preparar una nueva versión de producción.
- **Uso:** Se crean desde `develop` y se utilizan para realizar pruebas finales, correcciones de errores y ajustes antes de fusionarlas en `master` y `develop`.

---

### **5. Hotfix**
- **Descripción:** Ramas temporales creadas para solucionar problemas críticos directamente en `master`.
- **Uso:** Se crean desde `master`, se corrige el problema, y los cambios se fusionan tanto en `master` como en `develop`.

---

