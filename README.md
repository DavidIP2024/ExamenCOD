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

```bash
git checkout -b readme  # Crear la rama readme
git add README.md       # Agregar el archivo README.md
git commit -m "Agregado README con pasos y justificación de decisiones"
git push origin readme  # Subir la rama readme