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
 
* Windows Desktop (win11) 
  * scrcpy.exe (tool for android to remote mirror your android screen to windows) and adb.exe (android tool for debugging  
  * OBS Studio (app for recording Windows screen)   

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
  * Phyphox app, phone mounted to the cealing with magnet starts to show invidual spikes below 30hz, especially 1-3 Hz and 30, 40 or 50 Hz
  * From the balcony you might see that Neighbour J goes running, stepping sounds continue but step related vibrations in the ceiling are not in the same scale
  * *Spectroid* (Airborne sound) and *Phyphox* (physical vibrations) show the same frequencies !!! (or not : Check this one) 

* Night time version
  *  Between 3-6 AM , usually at 5 AM neighbour J start walking around. Dragging noises, audible thump sounds. Frequency pics here
 
# Examples 
  # General Examples 
* Spectroid Acceleration measurements via HTTP from android phone
  *  FFT
  *  Accel in Z -axis  (AccZ)
  *  Left side, measurements made from AccZ data, made by powershell script, send to HA via MQTT
<img width="2500" height="1230" alt="image" src="https://github.com/user-attachments/assets/7989e2a5-5992-4434-8efc-8bd66b9c5258" />


* SLM measurements with ESP32 and https://github.com/stas-sl/esphome-sound-level-meter
<img width="790" height="1120" alt="image" src="https://github.com/user-attachments/assets/deed8e85-14e0-45a6-b711-7157f079a1b1" />


* FFT made from AccZ data with Python script 
<img width="995" height="905" alt="image" src="https://github.com/user-attachments/assets/8925f38d-8c8e-48e2-8b9d-9558fbd3a01c" />



* Example of multifrequency ceiling vibrations
<img width="1320" height="1200" alt="a71_10 0 0 61_AccZ_20261106_121128" src="https://github.com/user-attachments/assets/49e672dc-d9f0-4511-96a5-4c0bddd732f0" />

* ~3Hz spike in ceiling vibration and also in sound ( i think this was just a coincidence) ???!??
<img width="1320" height="2280" alt="a71_10 0 0 61_AccZ_20261110_183105" src="https://github.com/user-attachments/assets/2b484ce0-b454-48fa-9965-f429663aa03f" />

* Live Ceiling vibrations and Mic monitoring with FFT 
<img width="1402" height="1147" alt="image" src="https://github.com/user-attachments/assets/87a22a2c-e96b-4138-b0ae-80fec25726ce" />

# No extra vibration examples 

  * Examples of almost no structural vibration
   * "Live" View
  <img width="1501" height="1085" alt="image" src="https://github.com/user-attachments/assets/e844867d-0157-4ee7-92d2-3e46f1c0803f" />
   * 300s summary
  <img width="563" height="968" alt="image" src="https://github.com/user-attachments/assets/3a4779f4-3a47-4d07-9c18-0eecfb087fd0" / >
  
   * Long term RMS 
  <img width="1587" height="727" alt="image" src="https://github.com/user-attachments/assets/9454b5ec-f2dd-49bc-809e-070f4e57a954" />
   * and Range (= AccZ min and max difference) trend .. Seems that this works as a general vibration indicator
  <img width="1717" height="1133" alt="image" src="https://github.com/user-attachments/assets/e1343ee8-4677-4284-8c02-fada0dc47544" />
   * Different RMS
   <img width="702" height="577" alt="image" src="https://github.com/user-attachments/assets/1f376bf2-ac30-47fb-837f-95ec4c209b08" />
   * One range indicator (AccZ min and max that is ) 
   <img width="687" height="527" alt="image" src="https://github.com/user-attachments/assets/9107ac2f-9f8a-4268-a944-9f04c72d0753" />
   * Ok, dominating frequencies also change, more intentionally made structural vibrations => less "random" frequencies
    <img width="707" height="485" alt="image" src="https://github.com/user-attachments/assets/5c20542f-fd49-4f76-88d3-d55bb878e328" />



    <img width="2052" height="847" alt="image" src="https://github.com/user-attachments/assets/9c494527-1b62-42dc-8844-6a03abece5fe" />
