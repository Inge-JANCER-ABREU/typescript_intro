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
