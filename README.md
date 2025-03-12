# ExamenCOD - Release v1.0

## Pasos Realizados

1. **Fork y Clonación**:
   - Realicé un fork del repositorio original en GitHub.
   - Cloné el repositorio a mi máquina local.

2. **Trabajo en las Ramas**:
   - `main`: Solo tendrá commits relacionados con releases.
   - `datos`: Contiene la clase de conexión a la base de datos.
   - `interface`: Se encarga de la parte gráfica.

3. **Merge de las Ramas**:
   - Se realizaron los merges de las ramas `datos` e `interface` a `main`.
   - Se decidió excluir un commit en la rama `interface` que contenía código no deseado.

4. **Creación de la Release**:
   - Se creó la etiqueta `v1.0` para marcar la primera release estable.

## Justificación de Decisiones

- **Rama `interface`**: Durante la revisión del código en la rama `interface`, se detectó un commit con código innecesario. Se decidió no incluirlo en la versión final para asegurar que la release solo contuviera el código relevante.

## Comandos Usados

1. **Crear la rama readme**:
   - Creé la rama `readme` y añadí el archivo `README.md` con la información sobre el proyecto.
   - Subí la rama a GitHub.

2. **Pasos para realizar las fusiones y creación de la release v1.0**

### 1. **Preparación**
Me aseguré de que la rama `main` estuviera actualizada antes de comenzar las fusiones. Para esto, ejecuté los siguientes comandos:

- `git checkout main`
- `git pull origin main`

### 2. **Fusionar la rama `datos` en `main`**
Luego de asegurarme que la rama `main` estuviera actualizada, fusioné la rama `datos` en `main` utilizando el siguiente comando:

- `git merge datos --no-ff -m "Merge branch 'datos' into main"`

**Explicación:**
- El parámetro `--no-ff` asegura que se cree un commit de merge, incluso si Git podría hacer un *fast-forward* (fusión directa sin commit). Esto ayuda a mantener un historial claro y con registros de las fusiones.

### 3. **Fusionar la rama `interface` en `main`**
Antes de fusionar la rama `interface`, revisé el último commit de esta rama, ya que contenía código no deseado que no debía incluirse en la versión final. Para evitar incluir ese commit, utilicé un **rebase interactivo**.

**Excluir el último commit de `interface`:**
Primero, cambié a la rama `interface` y luego utilicé el siguiente comando para hacer un rebase interactivo:

- `git checkout interface`


Después de esto, cambié de nuevo a la rama `main` y fusioné la rama `interface` en `main`:

- `git checkout main`
- `git merge interface --no-ff -m "Merge branch 'interface' into main (sin el último commit)"`

### 4. **Etiquetar el último commit**
Después de realizar todas las fusiones, etiqueté el último commit en la rama `main` como `v1.0` para marcar la primera release estable del proyecto. Esto se hizo con el siguiente comando:

- `git tag -a v1.0 -m "Release v1.0"`

Luego, subí la etiqueta a GitHub:

- `git push origin v1.0`

### 5. **Subir los cambios a GitHub**
Finalmente, subí todos los cambios a la rama `main` en GitHub, para que la versión final con las fusiones estuviera disponible en el repositorio remoto:

- `git push origin main`

## Resultado

Después de completar estos pasos, la rama `main` contiene todos los cambios de las ramas `datos` e `interface`, excluyendo el último commit de `interface`. Además, se ha creado la etiqueta `v1.0` para marcar la primera versión estable del proyecto.
