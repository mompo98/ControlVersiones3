# Git Hooks

Esta carpeta contiene scripts de Git Hooks que automatizan ciertas tareas y verificaciones antes de realizar confirmaciones en nuestro repositorio. A continuación, se detallan los hooks disponibles y su funcionalidad.

## Pre-commit

El hook "pre-commit" se encarga de verificar el formato del mensaje de confirmación. Asegura que cada confirmación tenga un formato consistente y significativo. Si el formato es incorrecto, se rechaza la confirmación.

## Post-checkout

El hook "post-checkout" se activa después de que se realiza una operación de checkout. En nuestro caso, se utiliza para automatizar la reinstalación de las dependencias del proyecto al realizar un clonado o checkout del repositorio.

## Pre-receive

El hook "pre-receive" se ejecuta en el servidor Git antes de aceptar una confirmación. Puede usarse para aplicar políticas de calidad de código, rechazar confirmaciones con problemas de estilo o realizar otras verificaciones a nivel de servidor.

## Pre-commit-msg

El hook "pre-commit-msg" verifica el mensaje del commit para asegurarse de que siga un formato específico. Esto ayuda a mantener un registro de confirmaciones legibles y coherentes.

## Pre-push

El hook "pre-push" se ejecuta antes de que los cambios se envíen al repositorio remoto. Puede usarse para realizar pruebas automáticas antes de la actualización del repositorio remoto.

## Pre-rebase

El hook "pre-rebase" se activa antes de un rebase y permite realizar verificaciones personalizadas antes de aplicar cambios de otras ramas.

Cada uno de estos hooks contribuye a mejorar la calidad y la consistencia de nuestro repositorio y procesos de desarrollo.
