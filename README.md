# VVCD & VVCMD

VVCD (Vehicle Voice Commands Dataset) and VVCMD (Vehicle Voice Commands Mixed Dataset) are publicly available datasets for Automatic Speech Recognition (ASR) in the Brazilian Portuguese language.
These datasets were built for testing a Proof of Concept of controlling the vehicle's external lights just by using voice commands.  The project focused on vehicle dashboard control by voice commands for drivers with reduced mobility.



The chosen voice commands are presented below with their english version:
| Brazilian Portuguese  | English | Vehicle Function |
| ------------- | ------------- | ------------- |
|*Seta para direita*     | Right turn signal | Turns on/off the right turn signal      |
|*Seta para esquerda*    | Left turn signal  |  Turns on/off the left turn signal      |
|*Luz baixa*             | Headlights        |  Turns on/off the headlights            |
|*Pisca alerta*          | Hazard warning    |  Turns on/off the hazard warning lights |

# Differences between the two datasets

- VVCD contains 204 audio files and their respective transcriptions, which were automatically validated by Python's SpeechRecognition library using the Google Speech Recognition engine.
- VVCMD contains, in addition to the VVCD audios, 192 synthetic voice audios from Microsoft Azure, totaling 396 audio files with their respective transcriptions.

# Datasets Folder Structure
- Voice ID Folders:
  - luz_baixa: Folder for the headlights voice command.
  - pisca_alerta: Folder for the hazard warning voice command.
  - seta_direita: Folder for the right turn signal voice command.
  - seta_esquerda: Folder for the left turn signal voice command.
  - driver.npy: Numpy array with the driver voice embedding, summarizing the audio features from the driver's voice.
- class_ocurrences.txt: Document containing the distribution of classes for each subset (train, test and dev).
- dev.csv: Document containing the list of audio files of the dev subset, with their filesize and transcript (Ground Truth - automatically validated).
- test.csv: Document containing the list of audio files of the test subset, with their filesize and transcript (Ground Truth - automatically validated).
- train.csv: Document containing the list of audio files of the train subset, with their filesize and transcript (Ground Truth - automatically validated).

Each command folder contains three .wav files of the voice command and a .npy file summarizing the audio features of the voice command.

# Related Publications
## A Simple Method for Voice Command Recognition with a Minimal Dataset

## Design and Development of a Control System for Automotive Vehicles through Voice Commands
(under development)
