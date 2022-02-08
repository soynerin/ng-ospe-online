
# Arquitectura Angular!

> **Cuando quieras construir algo que perdure, procura que los cimientos sean sólidos**

## Estructura de la aplicación
Se seguirá con una estructura orientada a módulos.
```
app/
|- core/
	|- core.module.ts
	|- services/
		|- auth.service.ts
	|- core-routing.module.ts
	|- core.module.ts
	|- index.ts
|- section1/
	|- components/
		|- component1/
			|- ...
			|- component1.component.ts
		|- component2/
			|- ...	
		|- shared/
			|- ...
	|- models/
		|- ...
	|- services/
		|- ...
	|- section1-routing.module.ts
	|- section1.module.ts
	|- index.ts
|- section2/
	|- ...
|- section3/
	|- ...
|- shared/
	|- components/
		|- component1/
			|- ...
			|- component1.component.ts
		|- component2/
			|- ...
		|- models/
		|- pipes/
			|- pipe1.pipe.ts
   |- index.ts
   |- shared.module.ts
|- app-component.sass
|- app-component.spec.ts
|- app-component.ts
|- app.module.ts

assets/
environments/
```
Existen tres módulos principales en la estructura:
- **AppModule**: es el módulo principal de la aplicación, responsable de su arranque y de la combinación con otros módulos
- **CoreModule**: incluye las funcionalidades básicas de la aplicación, que se utilizarán en toda la aplicación a nivel global. No debe ser importado por los módulos de funcionalidades de la aplicación
- **SharedModule**: normalmente un conjunto de componentes o servicios que se reutilizarán en otros módulos de la aplicación, pero que *no son aplicados globalmente en la aplicación*. Puede ser importado por los módulos de funcionalidades.
