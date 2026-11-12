LECCION 2:LIMPIEZA Y ESTANDARIZACION

 Excepciones

 Se tuvo que realizar unos cambios para poder que la respuesta saliera sin errores,principalmente en ´LIMPIEZA REUTILIZABLE CON FUNCIONES´.

 en la ultima parte de esta se tubieron que haber pasos adicionales.


 Laboratorio guiado 2: pipeline de limpieza con informe de cambios

 PASO 1:RECARGAR LOS DATOS CRUDOS

 Se tuvo que cambiar el codigo en este parte debido a que en mi proyecto no se identifica la palabra 'RUTA'

 PASO 6: VALIDACION RESULTADOS

 Comparación entre DataFrames originales y limpios

Durante la comparación de los DataFrames orders y orders_limpio, se identificó que ambos tienen las mismas dimensiones (478952 filas y 6 columnas), los mismos nombres de columnas y los mismos tipos de datos.

Sin embargo, al utilizar el método equals(), el resultado fue False.

Al realizar una comprobación adicional, se encontró que los índices de ambos DataFrames son diferentes, aunque sus columnas coinciden.

**Explicación del resultado:**

Esta diferencia se debe a que, durante el proceso de limpieza, Pandas puede conservar los índices originales de las filas que permanecen después de eliminar registros duplicados. Por esta razón, los índices no necesariamente quedan consecutivos ni coinciden con los del otro DataFrame.

**Decisión tomada:**

Se decidió conservar los índices actuales, ya que no representan un error en los datos ni afectan la integridad de los registros. No se consideró necesario utilizar `reset_index()` porque el ejercicio no exige renumerar las filas.

Por lo tanto, el resultado `False` de `equals()` no significa necesariamente que la limpieza sea incorrecta, sino que los DataFrames presentan diferencias en sus índices.






