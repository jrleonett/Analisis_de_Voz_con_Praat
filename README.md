# Análisis Forense de Voz con PRAAT

![Licencia](https://img.shields.io/badge/Licencia-GNU%20GPL%20v3-blue)
![GitHub](https://img.shields.io/badge/Python-3.8%2B-green)
![GitHub](https://img.shields.io/badge/Estado-Activo-brightgreen)

Este proyecto permite analizar y comparar dos muestras de audio para determinar si las voces pertenecen a la misma persona. Utiliza técnicas de procesamiento de señales, como la extracción de formantes, MFCC (Mel-Frequency Cepstral Coefficients) y DTW (Dynamic Time Warping), para realizar comparaciones robustas. Además, incluye la detección de emociones y la generación de gráficos detallados para facilitar la interpretación de los resultados. Desarrollada para el **Grupo de Peritos Forenses Digitales de Guatemala** por **José R. Leonett**.

🌐 [www.forensedigital.gt](http://www.forensedigital.gt)

---

# Características Principales.

- **Conversión Automática a WAV**: Convierte archivos de audio en formatos comprimidos (MP3, M4A, etc.) a WAV para un análisis preciso.
- **Detección de Emociones**: Identifica emociones como felicidad, tristeza, enojo o neutralidad basándose en el tono (pitch) y la intensidad.
- **Comparación de Formantes y MFCC**: Utiliza técnicas avanzadas para comparar patrones de voz.
- **Gráficos Detallados**: Incluye oscilogramas, gráficos de pitch, intensidad, formantes y espectrogramas.
- **Información de Archivos**: Muestra detalles de los archivos originales y convertidos para mantener la transparencia y la integridad forense.

---

# Requisitos.

- Python 3.8 o superior.
- Librerías necesarias: `gradio`, `numpy`, `matplotlib`, `praat-parselmouth`, `pydub`, `librosa`, `fastdtw`.

Instala las dependencias con el siguiente comando:

```bash
pip install gradio numpy matplotlib praat-parselmouth pydub librosa fastdtw
```
---

# **Instrucciones de Uso.**
- Clona este repositorio:
```bash
git clone https://github.com/tu-usuario/analisis-voz-forense.git
cd analisis-voz-forense
```
---

# **Ejecuta el programa:**
```bash
python analisis_voz.py
```
- Sube dos archivos de audio en la interfaz de Gradio.
- Revisa los resultados y gráficos generados.

---

# **Ejemplo de Salida.**
```bash
------------------------------------------------
Análisis Forense de Voz con PRAAT
------------------------------------------------
**Archivo Original 1**
Nombre: audio1.mp3, Tamaño: 5.23 MB, Fecha creación: 2023-10-01 12:34:56
Formato: .mp3
------------------------------------------------
**Archivo Convertido 1**
Nombre: audio1_converted.wav, Tamaño: 10.45 MB
------------------------------------------------
Emoción: Feliz
------------------------------------------------
**Archivo Original 2**
Nombre: audio2.wav, Tamaño: 15.67 MB, Fecha creación: 2023-10-02 14:20:30
Formato: .wav
------------------------------------------------
**Archivo Convertido 2**
Nombre: audio2_converted.wav, Tamaño: 15.67 MB
------------------------------------------------
Emoción: Neutral
------------------------------------------------
** Similitud MFCC: 85.32
** Distancia entre formantes: 45.67
------------------------------------------------
**Conclusión**: Las voces son las mismas.
```
---

# **Gráficos Generados.**
- **Oscilograma Comparativo:** Muestra la forma de onda de ambos audios.
- **Pitch (F0):** Compara el tono fundamental de las voces.
- **Intensidad:** Compara la intensidad de las señales.
- **Formantes:** Muestra los formantes (F1, F2, F3) de cada audio.
- **Espectrograma:** Compara el contenido espectral de los audios.

**1. Oscilograma Comparativo**
- *¿Qué es?* Un oscilograma es una representación gráfica de la forma de onda de un sonido. Muestra cómo cambia la amplitud (volumen) del sonido a lo largo del tiempo.
- *¿Para qué sirve?* Este gráfico te permite ver cómo se comparan las formas de onda de los dos audios. Si las formas de onda son muy similares, es una señal de que los audios podrían ser parecidos en términos de contenido sonoro.
- *Ejemplo práctico:* Piensa por un momento que estás viendo dos huellas digitales. Si se ven muy parecidas, es probable que pertenezcan a la misma persona. Aquí, en lugar de huellas, estamos viendo "huellas de sonido".

**2. Pitch (F0)**
- *¿Qué es?* El pitch, o tono fundamental (F0), es la frecuencia principal de un sonido. En el caso de la voz, está relacionado con qué tan grave o aguda suena una persona.
- *¿Para qué sirve?* Este gráfico compara el tono de las voces en los dos audios. Si los tonos son muy similares, es una señal de que las voces podrían ser de la misma persona.
- *Ejemplo práctico:* Piensa en dos personas cantando la misma nota. Si ambas notas suenan igual, es porque tienen un tono similar. Aquí estamos comparando el "tono" de las voces.

**3. Intensidad**
- *¿Qué es?* La intensidad se refiere al volumen del sonido, es decir, qué tan fuerte o suave se escucha.
- *¿Para qué sirve?* Este gráfico compara el volumen de los dos audios a lo largo del tiempo. Si los niveles de intensidad son muy parecidos, es otra señal de que los audios podrían ser similares.
- *Ejemplo práctico:* Imagina que estás comparando dos grabaciones de la misma persona hablando. Si en ambas grabaciones la persona habla con el mismo volumen, es más probable que sea la misma voz.

**4. Formantes (F1, F2, F3)**
- *¿Qué es?* Los formantes son frecuencias específicas que caracterizan el sonido de una voz. Se representan como F1, F2, F3, etc., y están relacionados con la forma en que la boca y la garganta producen los sonidos.
- *¿Para qué sirve?* Este gráfico muestra cómo cambian los formantes en cada audio. Los formantes son como la "firma" única de una voz, y si son muy parecidos en ambos audios, es una señal fuerte de que las voces podrían ser de la misma persona.
- *Ejemplo práctico:* Piensa en los formantes como el "color" de la voz. Si dos voces tienen el mismo "color", es más probable que sean de la misma persona.

**5. Espectrograma**
- *¿Qué es?* Un espectrograma es una representación visual del contenido espectral de un sonido. Muestra cómo las diferentes frecuencias (graves y agudas) cambian a lo largo del tiempo.
- *¿Para qué sirve?* Este gráfico compara el contenido de frecuencias de los dos audios. Si los espectrogramas son muy parecidos, es una señal de que los audios tienen un contenido sonoro similar.
- *Ejemplo práctico:* Imagina que estás viendo dos imágenes de un arcoíris. Si ambos arcoíris tienen los mismos colores en el mismo orden, es porque están hechos de la misma luz. Aquí, estamos comparando los "colores" (frecuencias) de los sonidos.

**¿Por qué son importantes estos gráficos?**
- Estos gráficos son herramientas visuales que nos ayudan a comparar y analizar las características únicas de las voces. En el análisis forense de voz, no solo nos fijamos en lo que escuchamos, sino también en lo que podemos ver. Cada gráfico nos da una pieza del rompecabezas para determinar si dos voces son iguales o diferentes.

**Ejemplo de Uso en un Caso Forense**
- Debes de analizar dos grabaciones de audio: una de un sospechoso y otra de una persona desconocida. Con estos gráficos, puedes:
  - Ver si las formas de onda son similares (Oscilograma).
  - Comparar si el tono de las voces es parecido (Pitch).
  - Analizar si el volumen de las grabaciones es consistente (Intensidad).
  - Revisar si las "firmas" de las voces coinciden (Formantes).
  - Comparar el contenido de frecuencias (Espectrograma).

Si todos estos elementos son muy parecidos, es más probable que las dos grabaciones sean de la misma persona. Si hay diferencias significativas, es posible que sean voces diferentes.

---

# **Cómo citar este trabajo.**
Usa la siguiente entrada BibTeX si utilizas este trabajo en tu investigación:
```bash
@article{joséRLeonett,
  title={Análisis de voces usando Praat},
  author={José R. Leonett},
  year={2024}
}
```
---

# **Licencia.**
- Este proyecto está bajo la licencia GNU General Public License v3.0. Consulta el archivo LICENSE para más detall
---
# **Contribuciones.**
- Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, por favor abre un issue o envía un pull request.
---
# **Agradecimientos.**
- A los desarrolladores de las librerías utilizadas: `gradio`, `numpy`, `matplotlib`, `praat-parselmouth`, `pydub`, `librosa`, `fastdtw`.
