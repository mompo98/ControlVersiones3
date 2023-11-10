#!/bin/bash
commit_msg_file=$1
commit_msg=$(cat $commit_msg_file)

# Verificar el formato del mensaje de confirmación
if ! [[ $commit_msg =~ ^[A-Z].+\n\n.+$ ]]; then
  echo "ERROR: El mensaje de confirmación no sigue el formato adecuado."
  echo "Debe tener un título seguido de una línea en blanco y una descripción."
  exit 1
fi

if git diff --cached --name-only | xargs grep -P '[\x80-\xFF]' /dev/null; then
  echo "ERROR: Se encontraron caracteres no permitidos en los archivos a confirmar."
  exit 1
fi

ESLINT_PATH="./node_modules/.bin/eslint"

if git diff --cached --name-only | grep '\.html$' | xargs eslint --fix; then
  echo "Se han aplicado correcciones de formato a los archivos HTML."
fi