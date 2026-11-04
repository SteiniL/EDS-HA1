# Digitale Signalverarbeitung – 1. Hausaufgabe

Lösung der 1. Hausaufgabe aus _Introduction to Digital Signal Processing_ (TU Berlin, Wintersemester 2026/27).

**Themen:** Audiosignale, Systemtheorie, Faltung, Diskrete Fourier-Transformation (DFT), Aliasing.

## Inhalt

| Datei                       | Beschreibung                                               |
| --------------------------- | ---------------------------------------------------------- |
| `homework_01_group_A.ipynb` | Notebook mit Code, Plots und Erklärungen zu allen Aufgaben |
| `Homework_1_tasks.pdf`      | Aufgabenblatt                                              |
| `speech.wav`                | Sprachaufnahme (Stereo, 44,1 kHz)                          |
| `impulse_response.wav`      | Impulsantwort (Mono, 44,1 kHz)                             |
| `requirements.txt`          | Benötigte Python-Pakete mit festen Versionen               |

## Aufgaben im Überblick

1. **Audiodateien importieren und darstellen**: Einlesen, Reduktion auf den ersten Kanal, Normierung auf 1, Plot über der Zeit in Sekunden.
2. **Systemeigenschaften**: Formale Prüfung von zwei Systemen auf Linearität, Zeitinvarianz, Rekursivität, Kausalität und Gedächtnislosigkeit.
3. **Faltung**: Kausales Moving-Average-System, eigene Funktion `convolve(a, b)`, Faltung von Sinussignalen (1 kHz und 4 kHz), Kommutativ- und Distributivgesetz.
4. **DFT-Implementierung**: Eigene Funktion `rdft(x, fs)` ohne FFT-Module. Vergleich mit `numpy.fft.rfft` hinsichtlich Genauigkeit und Rechenzeit.
5. **Zeitliches Aliasing**: Ein 15-kHz-Sinus, abgetastet mit 16 kHz und mit 192 kHz.

## Einrichtung

Voraussetzung: Python 3.10 oder neuer.

```bash
# 1. Virtuelle Umgebung im Projektordner anlegen
python3 -m venv .venv

# 2. Aktivieren (macOS/Linux)
source .venv/bin/activate
#    Windows: .venv\Scripts\activate

# 3. Pakete installieren
pip install -r requirements.txt
```

## Ausführen

1. `homework_01_group_A.ipynb` in VS Code oder Jupyter öffnen.
2. Als Kernel die `.venv` aus dem Projektordner auswählen (in VS Code: _Select Kernel_ → _Python Environments_ → `.venv`).
3. Alle Zellen ausführen (_Run All_).

Die Audiodateien müssen im selben Ordner wie das Notebook liegen. Die gemessenen Rechenzeiten in Aufgabe 4 hängen vom Rechner ab.
