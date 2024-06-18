# Test strategy

## Errores identificados y soluciones

1. **Generación de números aleatorios**:
   - **Error**: El número aleatorio estaba entre 0 y 10. `let randomNumber = Math.random() * 10;`
   - **Solución**: Cambiar la fórmula para que el número esté entre 1 y 100. `let randomNumber = Math.floor(Math.random() * 100) + 1;`
2. **Eventos de botón**:
   - **Error**: Los eventos estaban escritos incorrectamente. `guessSubmit.addeventListener('click', checkGuess);`
   - **Solución**: Usar `addEventListener` en lugar de `addeventListener`. `guessSubmit.addEventListener('click', checkGuess);`
3. **Selección de elementos**:
   - **Error**: `lowOrHi` no se seleccionaba correctamente. `const lowOrHi = document.querySelector('lowOrHi');`
   - **Solución**: Corregir la selección con la clase `.lowOrHi`. `const lowOrHi = document.querySelector('.lowOrHi');`
4. **Lógica de comparación**:
   - **Error**: Mensajes y colores incorrectos.
   - **Solución**: Ajustar los mensajes y colores según los requisitos.
5. **Validación de entrada**:
   - **Error**: No se validaba si la entrada era unn número entero.
   - **Solución**: Añadir validación para asegurar que `userGuess` sea un número entero entre 1 y 100

## Pasos de prueba

1. Abrir el archivo `index.html` en el navegador.
2. Ingresar números fuera del rango (e.g., 0, 101) y no enteros (e.g., "a", 1.5) para verificar que se muestren las alertas.
3. Ingresar números válidos para verificar que el juego funcione según los requisitos.
4. Probar adivinar el número dentro de 10 intentos y verificar los mensajes.
5. Probar no adivinar el número en 10 intentos y verificar los mensajes.
