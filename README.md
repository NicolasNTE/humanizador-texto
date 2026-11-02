# Humanizador académico

Skill para Codex que revisa informes, tesis, ensayos y trabajos universitarios con una voz natural y consistente. Conserva las citas, los datos, los términos técnicos y el grado de certeza de las afirmaciones.

## Instalación en Codex

Clona este repositorio en tu carpeta personal de skills. El comando funciona tanto en PowerShell como en una terminal compatible con Bash:

```sh
git clone https://github.com/NicolasNTE/humanizador-texto.git "$HOME/.agents/skills/humanizador-academico"
```

Si esa carpeta ya existe, revisa su contenido antes de reemplazarla. Si la skill no aparece en Codex, reinicia la aplicación.

También puedes descargar el repositorio como ZIP y colocar su contenido en una carpeta llamada `humanizador-academico` dentro de tu directorio de skills. El archivo `SKILL.md` debe quedar directamente dentro de esa carpeta.

## Uso

Escribe en un chat de Codex:

```text
$humanizador-academico

Reescribe este texto con un estilo natural, conserva las citas
y mantén el enfoque académico:

[texto]
```

Para trabajar con un archivo:

```text
$humanizador-academico

Revisa el documento adjunto con intensidad equilibrada.
Genera una copia en Word con las citas y los datos originales.
```

La manipulación de Word o PDF requiere las herramientas de documentos disponibles en el entorno; esta skill aporta las instrucciones de edición del texto.

## Voz y preferencias

La voz base es académica universitaria, clara y sobria. Puedes elegir una intensidad **conservadora**, **equilibrada** o **profunda**. La intensidad equilibrada es la predeterminada.

Para adaptar la voz, proporciona una muestra propia e identifícala como referencia de estilo. Si pides guardar tus preferencias, Codex puede crear un archivo `VOZ_ACADEMICA.md` en la carpeta de trabajo. La muestra orienta el estilo y no se usa como fuente de hechos.

El acabado predeterminado mantiene la corrección ortográfica. El modo **borrador natural** admite una redacción menos pulida; las erratas deliberadas requieren una petición expresa y se limitan a una copia de borrador identificada.

## Criterios de revisión

- Conservar las afirmaciones, sus atribuciones, condiciones y limitaciones.
- Mantener las citas textuales, las referencias bibliográficas y las cifras.
- Evitar convertir asociaciones en causas o posibilidades en certezas.
- Ajustar el ritmo, los verbos y las transiciones al contenido.
- Señalar contradicciones materiales sin corregir los datos por conjetura.

La skill no calcula autoría ni garantiza resultados ante detectores. No necesita API ni servicios externos para revisar el texto y no indica enviarlo a humanizadores externos salvo petición del usuario.

## Archivos

- [SKILL.md](SKILL.md): instrucciones principales.
- [Perfil de voz](references/perfil-de-voz.md): voz base, personalización e intensidades.
- [Criterios y ejemplos](references/criterios-y-ejemplos.md): decisiones editoriales y ejemplos originales.
- [Fuentes](references/fuentes.md): skills y herramientas consultadas durante el diseño.
- [Metadatos de Codex](agents/openai.yaml): nombre y ejemplo de invocación.

La versión inicial se comprobó con tres casos sintéticos: resultados estadísticos, citas con una muestra de voz y datos contradictorios. Estas comprobaciones revisaron conservación de contenido; no miden superioridad de estilo ni eficacia ante detectores.
