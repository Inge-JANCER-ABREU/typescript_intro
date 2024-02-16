# typescript_intro

# que es typescript
##### TypeScript es un superconjunto de JavaScript que añade tipado estático opcional y funciones avanzadas a JavaScript. Ha sido desarrollado por Microsoft y se publicó por primera vez en octubre de 2012


#### Static type-checking
TypeScript proporciona un sistema de tipado estático que permite detectar errores en tiempo de compilación, mejorando la robustez y mantenibilidad del código.

```typescript
function greet(name: string) {
    return "Hello, " + name + "!";
}

// Error: Argument of type 'number' is not assignable to parameter of type 'string'.
// greet(42); 
```
# Non-exception Failures

En lugar de depender de excepciones, TypeScript utiliza un enfoque de manejo de errores no excepcional, lo que significa que los errores de tipo se tratan como fallos normales durante la compilación.

```typescript
let x: number = 10;
// Error: Type 'string' is not assignable to type 'number'.
// x = "hello";
```
# Types for Tooling
Los tipos en TypeScript no solo ayudan en la detección de errores, sino que también mejoran la experiencia de desarrollo al proporcionar información útil para las herramientas, como autocompletado y sugerencias.

```typescript
interface Person {
    name: string;
    age: number;
}

const person: Person = {
    name: "John",
    age: 30,
};

// TypeScript proporciona autocompletado y verificación de tipos
console.log(person.);
```

# tsc, the TypeScript compiler
tsc es el compilador de TypeScript que convierte el código TypeScript en JavaScript, permitiendo la ejecución del código en entornos que admiten JavaScript.

Ejecutar tsc en la terminal:
```typescript
tsc mi_archivo.ts
```
# Emitting with Errors
Incluso cuando hay errores en el código TypeScript, el compilador puede generar un archivo de salida JavaScript, lo que facilita la identificación y corrección progresiva de problemas.
```typescript
let y: number = 10;
// Error: Cannot find name 'z'.
// console.log(z);
```
# Explicit Types
TypeScript fomenta la declaración explícita de tipos, lo que mejora la legibilidad y comprensión del código al proporcionar información clara sobre la forma y estructura de los datos.
```typescript
let z: number;
z = 42;
// Error: Type 'string' is not assignable to type 'number'.
// z = "hello";
```
# Erased Types
TypeScript elimina los tipos en tiempo de compilación, lo que significa que, aunque se utilice un sistema de tipos estático, este no tiene impacto en el rendimiento del código ejecutado.
En términos generales, una vez que el compilador de TypeScript termina de verificar su código, borra los tipos para producir el código "compilado" resultante. Esto significa que una vez compilado el código, el código JS simple resultante no tiene información de tipo.

# Downleveling:

El downleveling en TypeScript se refiere al proceso de generar código JavaScript compatible con versiones anteriores del estándar ECMAScript. TypeScript permite compilar a versiones específicas de ECMAScript para garantizar la compatibilidad con navegadores y entornos que pueden no admitir las últimas características de JavaScript.
```typescript
{
  "compilerOptions": {
    "target": "es5",
    "downlevelIteration": true,
    // Otros parámetros de configuración
  }
}
```


# Strictness
La opción strict en TypeScript es un conjunto de configuraciones que habilitan un conjunto más estricto de reglas y comprobaciones durante la compilación. Incluye configuraciones como strictNullChecks, strictFunctionTypes, strictPropertyInitialization y otras, mejorando la robustez y calidad del código.
```typescript
{
  "compilerOptions": {
    "strict": true,
    // Otros parámetros de configuración
  }
}
```

# noImplicitAny
La opción noImplicitAny en TypeScript se utiliza para evitar la inferencia implícita del tipo any cuando el compilador no puede determinar un tipo específico. Al habilitar esta opción, se requiere que todas las variables tengan un tipo explícito asignado para evitar posibles errores de tipo.
```typescript
{
  "compilerOptions": {
    "noImplicitAny": true,
    // Otros parámetros de configuración
  }
}

```


# strictNullChecks
La opción strictNullChecks en TypeScript ayuda a prevenir errores relacionados con valores null o undefined. Cuando está habilitada, el compilador verifica de manera más rigurosa las asignaciones de tipos, lo que ayuda a evitar errores comunes asociados con referencias nulas o indefinidas.
```typescript
{
  "compilerOptions": {
    "strictNullChecks": true,
    // Otros parámetros de configuración
  }
}

```


