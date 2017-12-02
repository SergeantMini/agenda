# TP2 Javascript

149999, 150251, 145809, 150916

---
## Objetivos

- Proponer una arquitectura para el diseño de nuestra agenda.
- Crear una agenda web funcional que nos permita administrar las actividades semanales/mensuales de una persona.

---
## Tecnologías utilizadas
- HTML
- CSS
- JavaScript
- Cloud9
---
## Arquitectura
- 2 - Capas y operaciones
- No tiene persistencia
- Stateful
- Orientado a conexión
- Síncrono

![ARQUITECTURA](https://raw.githubusercontent.com/monicavelaje/agenda/master/ARQUITECTURA.PNG)

---

## UML:

![UML](https://raw.githubusercontent.com/monicavelaje/agenda/master/UML.PNG)

---
## Clase ESTUDIANTE

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
---
## Clase HORARIO
```javascript
var HORARIO= (function(){
    var pertenece=null;
    var tiene=[];
    return {
        getPertenece: function(){return pertenece;},
        setPertenece: function(estudiante){pertenece=estudiante;},
        getTiene: function(){return tiene;},
        setTiene: function(act){tiene.push(act);}
    };
})();
```
---
## Clase ACTIVIDAD
```javascript
var ACTIVIDAD=(function(t,d,hi,hf,l,ev){
    var titulo=t;
    var descripcion=d;
    var horaInicial=hi;
    var horaFinal=hf;
    var lugar=l;
    var evaluacion=ev;
    return{
        getLugar:function(){return lugar;},
        setLugar:function(lu){lugar=lu;},
        getEv:function(){return evaluacion;},
        setEv:function(e){return evaluacion=e;},
        getTitulo: function(){return titulo;},
        setTitulo: function(titl){titulo =titl;},
        getDescripcion: function(){return descripcion;},
        setDescripcion: function(ds){descripcion=ds;},
        getHoraInicial:function(){return horaInicial;},
        setHoraInicial:function(hrI){horaInicial=hrI},
        getHoraFinal:function(){return horaFinal;},
        setHoraFinal:function(hrF){horaFinal=hrF;},
    }
});
```
---
## Conclusiones
Utilizamos archivos JavaScript para la funcionalidad de la página.
Anteriormente habíamos creado nuestra página y comprobamos que funcionaba, pero al agregarle los archivos pudimos obtener datos, almacenarlos y recuperarlos, dándole a la página una funcionalidad mayor a la que anteriormente tenía.
