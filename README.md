# Aku
This started as a project to measure noise from upstairs neighbour walking all the time in his apartment. Noise was so loud that it prevented sleeping. After complaining about the noise things got worse. Later I found out that he/she had systemical plan   to use LF noise .... So this is a story about how to measure and report such things and  
 
Measuring and reporting of sounds 

Sources of noise : devices 
- counting footfall in apartments or collecting evidence
- intentional LF noise harassment 
 - speakers
 - parametric speakers, also called ultrasonic directional speakers. Cannot produce LF noises.

# Types of Measurements  
 * LF Noise : Does'nt really matter where the measurements are made, because the noise can be heard everywhere 
 * Acceleration : Ceiling, Walls, Bed 
 * Overall SPL levels in different places: ESP32 => HA 
 * Ambient sounds : walking, possibly clicking sounds from electric switches 

# Calibration and baselines: 
* Usually these tools cannot be calibrated and we are interested mainly in differences with baseline. Official measurements has to be made with calibrated devices.  


# Tools / Apps / Devices / Sensors
* Audible
* Home Assistant (virtualmachine) and IOT microcontrollers and sensors and used protocols
  * ESPHOME 
  * ESP32 (wifi)
  * MQTT
  * INMP441  / sph0645 / isc-43434 : mems mics
* Android phones and tabs : acceleration and frequency spectrum
  * Spectroid app (Android) 
  * Phyphox app (Android)
  * USB Audio Recorder Pro (Android)

* Measurements

# Modus operandi 
* Example of 2026-10-13 and 
  * Continous LF bass above my bed overnight
  * Neighbour J hears some noise from my apartment below
  * J starts to walk around in his apartment
  * noises of moving of items, walking around
  * you can also hear clicks, possibly electricity switches (mains). These might coincidence near or at the same time with large thumb (made by foot)  
  * Spectroid shows that amplitudes of LF frequencies start to rise, frequency hopping. This happens in inaudible frequency range (<22hz)
  * Continuous spikes with high amplitude, freqs below 100Hz. These sounds are audible.
  * Funny part, frequent small steps. Maybe carrying something heavy .. or the steps are for mimicing child walk or both
  * Phyphox app, phone mounted to the cealing with magnet starts to show invidual spikes below 30hz, especially 9-15 and 30 Hz
  * *Spectroid* (Airborne sound) and *Phyphox* (physical vibrations) show the same frequencies !!!

* Night time version
  *  Between 3-6 AM , usually at 5 AM neighbour J start walking around. Dragging noises, audible thump sounds. Frequency pics here
 
Examples 

* Spectroid Acceleration measurements via HTTP from android phone
  *  FFT
  *  Accel in Z -axis  (AccZ)
<img width="2500" height="1230" alt="image" src="https://github.com/user-attachments/assets/7989e2a5-5992-4434-8efc-8bd66b9c5258" />

* SLM measurements with ESP32 and https://github.com/stas-sl/esphome-sound-level-meter
<img width="790" height="1120" alt="image" src="https://github.com/user-attachments/assets/deed8e85-14e0-45a6-b711-7157f079a1b1" />

* FFT made from AccZ data with Python script 
<img width="995" height="905" alt="image" src="https://github.com/user-attachments/assets/8925f38d-8c8e-48e2-8b9d-9558fbd3a01c" />
