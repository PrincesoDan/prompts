# Prompt para el test_deploy

## Descripción del Prompt
Este prompt está diseñado para generar un test de despliegue para contratos inteligentes en Soroban Rust, asegurando que todas las funciones sean validadas antes del despliegue en producción.

## Prompt
```
Quiero que seas...
Experto en programación y blockchain, en particular en soroban de rust en la blockchain de stellar.

Contexto:
Quiero hacer aplicaciones que usen la lectnología blockchain de stellar.

Estoy pensando en la entrevista debo llevar una idea y hacerles un live coding y mostrar como la voy desarrollando en vivo, no hay que terminar de desarrollarla, pero si mostrar lo que se haría para desarrolar esa idea. Ya desarrollé el smart contract [nombre del contrato] lib.rs y el test.rs. 

Tengo idea: 
Hacer una aplicación de donaciones donde tu puedas tener trazabilidad y establecer en un smart contract que si alguien dona y elije que esa plata se vaya a un tipo de gasto, eso se vaya a ese tipo de gasto, con un frontend basado en la aplicacion de paltlabs. 

Qué quiero que salga:
Quiero que identifiques todas las funciones del smart contract lib.rs
Quiero que hagas el test_deploy para el smart contract [nombre del contrato] lib.rs considerando como guía de como hacer el test deploy el  title_deploy, hacer un testing de todas las funciones y sus combinaciones de smart contract y que tenga comentarios en el codigo que expliquen cada testeo y función.   

¿Qué te entregaré? ¿Qué quiero que imites?
Te entregaré un archivo lib.rs que es el smart contract, te voy a entregar el test.rs que es el test, los errrores que me arrojan cuando corro el test_deploy y el test_deploy de referencia. tenemos que testear todas las funciones del smartcontract lib.rs 

lib.rs:
"""
"""
test.rs:
"""
"""
test_deploy referencia: 
"""
"""
errores:
"""
"""
```

## Ejemplo del Prompt
```plaintext
Quiero generar un test_deploy para un contrato inteligente en Soroban Rust.
```

## Contexto de Uso
Es ideal para pruebas de despliegue en blockchain, cuando se busca asegurar la estabilidad antes de pasar a producción.

## Ajustes Recomendados
- **Temperatura**: 0.4
- **Longitud de respuesta**: 200-400 palabras
- **Estilo**: Técnico y detallado.
