# TP2 Javascript
-149999, 150251, 145809, 150916

---

##Arquitectura
- 2 - Capas y operaciones
- No tiene persistencia
- Stateful
- Orientado a conexión
- Síncrono
![ARQUITECTURA](https://raw.githubusercontent.com/monicavelaje/agenda/master/ARQUITECTURA.PNG)

---

##UML
![UML](https://raw.githubusercontent.com/monicavelaje/agenda/master/UML.PNG)

---
##Clase Estudiante

```javascript
var actual;
var tl=0;
var ESTUDIANTE = (function (n,c,co,p){
    ESTUDIANTE.counter=(++ESTUDIANTE.counter || 1);
    var id=ESTUDIANTE.counter;
    var nombre=n;
    var carrera=c;
    var correo = co;
    var contrasena = p;
    var tiene=null;
    return{
        getID:function(){return id;},
        getNombre:function(){return nombre;},
        setNombre:function(nom){nombre=nom;},
        getCarrera:function(){return carrera;},
        setCarrera:function(carr){ carrera =carr;},
        getTiene:function(){return tiene;},
        setTiene:function(horario){tiene=horario;},
        getCorreo:function(){return correo;},
        setCorreo:function(corr){ correo = corr;},
        getContrasena:function(){return contrasena;},
        setContrasena:function(pass){ contrasena = pass;}
        };
    }
);
```
