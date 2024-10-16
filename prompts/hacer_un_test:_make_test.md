# Hacer un test: Make Test

## Descripción del Prompt
Crea pruebas para contratos inteligentes en Soroban SDK Rust, asegurando que cubren todas las funciones clave y se evitan alucinaciones comunes.

## Prompt
```
Quiero hacer una prueba para un smart contract en Soroban SDK Rust. La prueba debe considerar el test.rs que te daré de referencia, el lib.rs que es smartcointract a testear y los siguientes puntos para evitar alucinaciones comunes:
"""
    Consistencia en invocaciones y argumentos: Utilizar Vec<Val> construidos con un array, para pasar los argumentos a todas las funciones del smart contract cuando se ocupe mockauth en lugar de pasarlos directamente. Los argumentos deben ser convertidos utilizando .into_val(&env) antes de crear el Vec<Val>. Te dejo un ejemplo de guía:
    """ // Crear un Vec<Val> a partir de un array
      let args: Vec<Val> = Vec::from_array(&env, [
        user.into_val(&env), 
        new_title.clone().into_val(&env)
    ]);

    // Autenticar al usuario y modificar el título
    let result = client
        .mock_auths(&[MockAuth {
            address: &user,
            invoke: &MockAuthInvoke {
                contract: &contract_id,
                fn_name: "modify_title",
                args: args.into_val(&env), // Usar el vector como argumento
                sub_invokes: &[],
            },
        }])
        .modify_title(&user, &new_title);

"""

    Autenticación adecuada: Para invocar las funciones del contrato, siempre utilizar client.mock_auths() y definir correctamente MockAuth con el contrato, función (fn_name), y argumentos. Además, asegúrate de que los sub-invokes se definan como sub_invokes: &[].

    Eliminar el uso de .unwrap() .expect() para funciones que devuelven (): Evita desempaquetar (unwrap()) el resultado de funciones que devuelven (). Utiliza una cadena lógica adecuada para verificar el comportamiento de las funciones.

    Uso correcto de Address::generate(&env): Para crear direcciones virtuales (admin, donantes, etc.), utiliza Address::generate(&env) en lugar de métodos obsoletos o incorrectos.

    Actualización de funciones obsoletas: Utilizar String::from_str(&env, "example") en lugar de String::from_slice(), para alinearse con las prácticas actuales de soroban-sdk. No ocupar .as_str(), no existe.

    Mantener consistencia en el uso de referencias y conversiones: Asegúrate de pasar referencias adecuadas cuando sea necesario, y convierte los valores de manera consistente usando .into_val(&env).
"""

Crea pruebas para las todas funciones del smart contract libr.rs y asegúrate de incluir comentarios explicativos.

lib.rs:
"""
"""
test.rs:
"""
"""
```

## Ejemplo del Prompt
```plaintext
Quiero hacer una prueba para un smart contract en Soroban SDK Rust. Asegúrate de utilizar mock_auths y evitar unwrap().
```

## Contexto de Uso
Útil para desarrolladores que necesitan validar contratos inteligentes en Rust con un enfoque en evitar errores comunes.

## Ajustes Recomendados
- **Temperatura**: 0.3
- **Longitud de respuesta**: 150-300 palabras
- **Estilo**: Técnico y enfocado en la validación de contratos.
