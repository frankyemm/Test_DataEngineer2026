# Instrucciones para Subir a GitHub

## Pasos para publicar el repositorio:

### 1. Crear el repositorio en GitHub
1. Ve a https://github.com/new
2. Nombre sugerido: `data-engineer-technical-test-2026`
3. Descripción: "Test técnico para candidatos a Ingeniero de Datos - Sun Valley Investment"
4. Elige **Privado** (para que solo tú y los candidatos invitados lo vean)
5. **NO inicialices** con README, .gitignore o licencia (ya los tenemos)
6. Click en "Create repository"

### 2. Conectar tu repositorio local con GitHub

Después de crear el repositorio en GitHub, ejecuta estos comandos en la terminal:

```powershell
# Agregar el repositorio remoto (reemplaza TU_USUARIO con tu usuario de GitHub)
git remote add origin https://github.com/TU_USUARIO/data-engineer-technical-test-2026.git

# Subir los archivos
git branch -M main
git push -u origin main
```

### 3. Dar acceso a los candidatos

Para cada candidato:

**Opción A: Invitar como colaborador (Recomendado)**
1. Ve a tu repositorio en GitHub
2. Settings → Collaborators → Add people
3. Invita al candidato por su usuario de GitHub o email
4. Ellos podrán clonar el repo y crear su propio fork

**Opción B: Hacer el repositorio público temporalmente**
1. Settings → Danger Zone → Change visibility → Make public
2. Comparte el link con los candidatos
3. Una vez terminen, puedes hacerlo privado de nuevo

**Opción C: Enviar como Release/ZIP**
1. Crea un Release en GitHub
2. Adjunta los archivos como assets
3. Comparte el link de descarga

### 4. Link a compartir con candidatos

Una vez subido, comparte este link:
```
https://github.com/TU_USUARIO/data-engineer-technical-test-2026
```

### 5. Cómo los candidatos deben entregar

Indícales que pueden entregar de dos formas:

**Opción 1: Repositorio propio (Preferida)**
```bash
# El candidato hace fork o crea un nuevo repo
# Desarrolla su solución
# Te comparte el link de su repositorio
```

**Opción 2: Pull Request (Si son colaboradores)**
```bash
# El candidato clona tu repo
git clone https://github.com/TU_USUARIO/data-engineer-technical-test-2026.git
cd data-engineer-technical-test-2026

# Crea una rama con su nombre
git checkout -b solucion-nombre-candidato

# Desarrolla su solución
# Hace commits y push
git push origin solucion-nombre-candidato

# Crea un Pull Request en GitHub
```

---

## Comandos Rápidos de Referencia

### Ver el estado del repositorio
```powershell
git status
```

### Ver commits
```powershell
git log --oneline
```

### Ver remotes configurados
```powershell
git remote -v
```

### Actualizar el test si haces cambios
```powershell
git add .
git commit -m "Actualización del test"
git push
```

---

## Checklist antes de compartir

- [ ] El repositorio está en GitHub
- [ ] README.md está completo y claro
- [ ] TEST_TECNICO_INGENIERO_DATOS.md tiene toda la información necesaria
- [ ] Los 5 PDFs están en la carpeta `data/`
- [ ] Has actualizado la información de contacto en README.md
- [ ] Has establecido la fecha límite en el documento del test
- [ ] Has decidido si el repo será público o privado
- [ ] Has probado que el link funciona

---

## Notas Importantes

- Los archivos PDF suman aproximadamente 20-30 MB, GitHub lo soporta sin problemas
- Si necesitas subir archivos más grandes en el futuro, considera Git LFS
- Mantén el repositorio limpio, no subas carpetas como `output/`, `logs/`, etc. (ya están en .gitignore)
