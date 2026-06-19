# Documento de arquitectura del identificador · Amanita v0.3

## Objetivo
Construir un identificador guiado que use IA solo como generador inicial de candidatas. La decisión no la toma la IA: la toma un motor de razonamiento basado en caracteres micológicos, reglas de seguridad y una matriz de confusiones.

## Principio central
La aplicación no debe forzar una identificación. Puede terminar con: identificación insuficiente, requiere más datos, no consumir, o posible identificación con advertencias.

## Flujo del identificador
1. El usuario sube una fotografía.
2. La IA visual propone candidatas.
3. El usuario puede mantener o retirar candidatas.
4. El motor calcula la pregunta más eficiente según las especies restantes.
5. Cada respuesta descarta o pondera especies.
6. El resultado final muestra candidatas compatibles, descartes, motivo de descarte y decisión de seguridad.

## Motor dinámico de preguntas
El sistema no pregunta por preguntar. En cada paso evalúa qué carácter divide mejor las candidatas actuales:
- anillo
- reacción de la carne
- margen
- tipo de volva
- verrugas/restos de velo
- color del sombrero
- olor
- hábitat
- suelo
- fenología

Los caracteres críticos descartan. Los blandos, como hábitat o fenología, ponderan y ayudan, pero no deben eliminar de forma absoluta salvo reglas futuras muy justificadas.

## Reglas de seguridad
- Si queda una Amanita mortal compatible: no consumir y aviso 112 si hubo ingesta.
- Si queda una tóxica compatible: no consumir.
- Si falta la base del pie: identificación insegura.
- Si la seta procede de entorno urbano, carretera, vertedero o zona contaminada: no consumo por bioacumulación aunque sea comestible.
- La IA nunca autoriza consumo.

## Matriz maestra
La matriz maestra almacena los caracteres por especie. Es el núcleo del identificador.

## Matriz de confusiones
La matriz de confusiones vincula especies que compiten realmente en campo. Alimenta:
- juego de confusiones
- fichas
- avisos de seguridad
- preguntas prioritarias del identificador

## Vocabulario pedagógico
Los términos técnicos deben aparecer con explicación: volva sacciforme, circuncisa, napiforme, margen estriado, anillo fugaz, carne inmutable, etc. El identificador debe enseñar micología mientras identifica.

## Estado del paquete
Este paquete constituye el primer entregable oficial del proyecto: Amanita v1.0 estructural.
