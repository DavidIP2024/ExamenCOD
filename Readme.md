# 📚 Proyecto DAM – Documentación y Gestión de Versiones

Este repositorio contiene el desarrollo de un proyecto de Desarrollo de Aplicaciones Multiplataforma (DAM). A continuación, se describe el flujo de trabajo utilizado, incluyendo la configuración inicial, la organización en ramas, el desarrollo de funcionalidades y el control de versiones.

---

## 🔧 1. Configuración Inicial

Se partió haciendo un **fork** del repositorio original y se **clonó** localmente. Luego, se crearon ramas específicas para separar cada parte del desarrollo:

### 🔀 Ramas utilizadas

- `main`: Para versiones estables y publicables del proyecto. Contiene solo *merge commits* y etiquetas.
- `datos`: Contiene la lógica de conexión a la base de datos.
- `interface`: Se desarrolla la interfaz gráfica de usuario (GUI).
- `readme`: Documentación y archivos explicativos del proyecto.

### 💻 Comandos utilizados

```bash
# Clonar el repositorio después del fork
git clone https://github.com/tu_usuario/nombre_del_repositorio.git
cd nombre_del_repositorio

# Crear y moverse entre ramas
git checkout main
git branch datos
git branch interface
git branch readme