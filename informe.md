# Informe de Errores y Soluciones en Docker sobre Windows

## 1. Error: **Docker Desktop - WSL distro terminated abruptly**
### **Descripción**
Este error ocurre cuando la distribución de WSL utilizada por Docker se cierra inesperadamente, generalmente debido a que un proceso externo detuvo WSL.
![-](image.png)

### **Mensaje de error**
```
running wsl-bootstrap: exit status 1
```

### **Posible solución**
1. **Reiniciar Docker Desktop** → Clic en "Restart" en la ventana de error.
2. **Reiniciar WSL manualmente** ejecutando en PowerShell:
   ```powershell
   wsl --shutdown
   ```
3. **Verificar el estado de WSL** ejecutando:
   ```powershell
   wsl -l -v
   ```
4. **Actualizar WSL** con:
   ```powershell
   wsl --update
   ```
5. **Reinstalar Docker Desktop** si el problema persiste.

---
