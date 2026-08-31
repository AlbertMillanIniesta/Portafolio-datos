# El lenguaje de la investidura

Análisis lingüístico-computacional de los 15 discursos de investidura de la democracia española actual (1979-2023), con R y `quanteda`.

> **En palabras sencillas**: cogí los discursos con los que cada presidente del Gobierno de España se ha presentado ante el Congreso para pedir la confianza de los diputados y diputadas, desde Adolfo Suárez (1979) hasta Pedro Sánchez (2023), y usé herramientas de análisis de texto para medir cosas difíciles de comparar a simple vista: ¿se ha vuelto más fácil de entender el discurso político? ¿Suena más positivo o más negativo con el tiempo? ¿De qué habla cada presidente que no hablen los demás?

## Hallazgos principales

- El discurso político español se ha vuelto **medible y sostenidamente más fácil de leer** en 44 años — frases más cortas, léxico más accesible.
- El tono ha pasado de una tendencia ascendente hasta 2004 a un **declive sostenido hasta el mínimo histórico de 2023**, confirmado por dos léxicos de sentimiento construidos de forma totalmente independiente (correlación ρ = 0,78; p = 0,001).
- Desde 2015, el discurso de investidura ocupa un **espacio léxico distinto** al de las tres décadas anteriores — coherente con el fin del bipartidismo.
- Aparecen al menos **cuatro maneras distintas** de ocupar el discurso según la etapa: gestión económica nacional, integración institucional europea, ampliación de derechos sociales, y confrontación ideológica directa.

📄 **[Informe completo de resultados y discusión](informe/informe_resultados_discursos_investidura.md)** — pensado para leerse sin necesidad de ejecutar ningún código, con explicaciones accesibles en cada apartado.

🖥️ **[Análisis completo en HTML](analisis_discursos_investidura.html)** — con todos los gráficos, tablas interactivas y el código que los genera. *Aviso: GitHub no lo muestra renderizado al hacer clic directamente (enseña el código fuente en bruto) — descárgalo y ábrelo con tu navegador para verlo como una página web normal. Alternativa sin descargar nada: pega la URL de este archivo en [htmlpreview.github.io](https://htmlpreview.github.io/) y se abre renderizado al instante.*

![Evolución del tono neto del discurso](informe/imagenes/tono_neto.png)

## Qué incluye este repositorio

```
├── analisis_discursos_investidura.Rmd   # Todo el código del análisis
├── analisis_discursos_investidura.html  # Resultado ya ejecutado, con gráficos y tablas interactivas
├── data/discursos/                      # Los 15 discursos originales (.txt)
├── informe/
│   ├── informe_resultados_discursos_investidura.md   # Informe completo
│   ├── Informe_discursos_investidura.docx            # Mismo informe, en Word
│   └── imagenes/                        # Gráficos usados en el informe
```

## Metodología, en resumen

- **Lematización morfosintáctica** con `UDPipe`, filtrando por categoría gramatical.
- **Legibilidad** (índice Fernández-Huerta, adaptación española de Flesch) y **riqueza léxica** (MATTR).
- **Contenido**: frecuencias, *keyness* (chi-cuadrado) por discurso individual, KWIC sobre seis ejes temáticos, diccionario temático propio.
- **Similitud** entre discursos (TF-IDF + coseno) y clustering jerárquico.
- **Modelado de temas** (*Structural Topic Model*), con una prueba de robustez comparando dos configuraciones distintas del modelo.
- **Sentimiento**, con dos léxicos independientes (uno traducido, uno nativo en español) para poder contrastar resultados entre sí.

Cada decisión metodológica está justificada en el propio informe (apartado 2.2), incluidas las limitaciones — con especial atención a documentar honestamente qué no funcionó y por qué (apartado 3.3.1).

## Cómo ejecutarlo

1. Clona este repositorio y abre `analisis_discursos_investidura.Rmd` en RStudio.
2. Instala las dependencias (la primera vez, `UDPipe` descargará automáticamente el modelo de español, y el análisis de sentimiento nativo descargará el léxico ML-Senticon — ambos avisan por consola cuándo lo hacen).
3. `Session > Restart R`, y después `Run All` (o *Knit* para generar el HTML completo).

## Créditos

El análisis de sentimiento con léxico nativo en español usa **ML-Senticon**:

> Cruz, F. L., Troyano, J. A., Pontes, B., & Ortega, F. J. (2014). *ML-SentiCon: Un lexicón multilingüe de polaridades semánticas a nivel de lemas*. Procesamiento del Lenguaje Natural, 53, 113-120.

## Sobre el proceso

Este proyecto se ha desarrollado con la colaboración de Claude (Anthropic) como asistente técnico, para la generación y depuración de código, y como interlocutor en el proceso metodológico. Las decisiones de diseño, la interpretación de los resultados y la verificación final del análisis son mías.

## Licencia

El código de este repositorio se distribuye bajo licencia MIT (ver [`LICENSE`](LICENSE)). Los discursos de investidura son actos oficiales del Congreso de los Diputados, de dominio público.

## Autor

**Albert Millán** — [LinkedIn](https://www.linkedin.com/in/albert-millan-iniesta/) · [Portafolio](https://albertmillan.wordpress.com/)
