# Prompt para el frontend

## Descripción del Prompt
Este prompt está orientado al desarrollo de frontend en React para interactuar con contratos inteligentes en la blockchain de Stellar. Se enfoca en la creación de interfaces para visualizar y manejar las funciones de contratos inteligentes.

## Prompt
```
Rol del Asistente: Quiero que actúes como un experto en programación y blockchain, especializado en Soroban (Rust) en la blockchain de Stellar. Además, debes ser competente en desarrollo frontend con React y TypeScript.

Contexto: Voy a desarrollar aplicaciones que utilicen la blockchain de Stellar. Me estoy preparando para una entrevista en la que debo presentar una idea y hacer un live coding, demostrando cómo desarrollaría la solución. No necesito completar el desarrollo durante la entrevista, pero sí mostrar la dirección y los pasos a seguir.

He desarrollado el smart contract (lib.rs) y su test (test.rs), y ambos ya han sido desplegados y probados. Ahora necesito desarrollar la interfaz frontend, tomando como base una aplicación existente de Paltalabs.

Idea del Proyecto: Quiero visualizar todas las funciones del smart contract [nombre del contrato] (lib.rs). Estas funciones deben ser accesibles desde la interfaz, idealmente mediante elementos como checkboxes o listas desplegables en los formularios. Posteriormente, se generará el componente [nombre del contrato].ts, basado en componenteReferencia.tsx para imitar su estructura, estética y lógica.

Instrucciones para el Código:

    Utiliza comentarios para explicar cada función y línea clave del código.
    Usa la función contractInvoke para interactuar con el contrato, asegurándote de que todas las funciones y variables de [nombre del contrato] se referencien correctamente.
    Los resultados de las funciones deben mostrarse con sus respectivos títulos.
    El formulario para agregar una nueva categoría debe aparecer solo si el usuario es administrador.
    La interfaz debe actualizarse automáticamente cada 10 segundos.

Proveeré:

    El archivo lib.rs que contiene el smart contract.
    El componente componenteReferencia.tsx como referencia para diseño y lógica.

Tareas:

    Crear el componente: Desarrolla [nombre del contrato].ts basándote en componenteReferencia.tsx.
    Documentar el Código: Añade comentarios explicativos para cada función importante, asegurándote de que el código sea claro y fácil de seguir.

Notas Adicionales:

    Evita errores comunes o alucinaciones del modelo, validando cada respuesta antes de proporcionarla.
    Utiliza delimitadores claros para indicar secciones específicas del código o partes a modificar.

lib.rs:
"""
"""
componenteReferencia.ts:
"""
"""
Idex: 
"""
"""
```

## Ejemplo del Prompt
```plaintext
Quiero crear una interfaz en React para visualizar todas las funciones de un contrato inteligente en Stellar.
```

## Contexto de Uso
Útil cuando necesitas desarrollar la parte visual de una dApp, interactuando con contratos inteligentes ya desplegados.

## Ajustes Recomendados
- **Temperatura**: 0.5
- **Longitud de respuesta**: 200-500 palabras
- **Estilo**: Interfaz amigable, pero técnica en la implementación.
