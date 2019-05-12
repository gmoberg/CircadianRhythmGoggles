## Our Goggles in Action
![Goggles in Action](/Screen Shot 2019-05-01 at 12.03.16 AM.png)

### Motivation
Circadian Rhythm Sleep Disorders (CRSD) is a condition that is characterized by various psychological and physiological effects, such as fatigue, irritability, poor concentration, and work errors. It affects health, working and living. Besides Jet lag, CRSDs affects shift workers, and cause “social jet lag” in the irregular sleeping population. Current treatments to CRSDs are medicine like Melatonin and light therapy by using blue lights such as Re-timer, Sunbox, Lumos and Verilux. None of those light therapies are FDA approved and the general outcomes of those methods are poor.

### How We Did It
We used a MBED to control colored LED lighting dynamically through multiple threads. We adjusted both the lux and wavelength of the light throughout a night to adhere to the stakeholders protocols. We had different stages of sleep cycle and in each stage we showed different lighting. The three stages were awake, non-REM sleep, and REM sleep. To progress from one stage to another, the patient has to have a low enough heart rate and a fast enough eye movement rate. We have three electrodes that measure the patients heart rate and three that measure the patients eye movement. We continuously take readings and if the patient meets the thresholds for the next stage, then the lights will change to help the patient transition into that stage. If the patient does not meet the threshold values, then they restart the current stage they are in.


### Week1 
We manipulated LEDs with PWM and MBED.

Before working with the LED Matrix board, we first wanted to get the project working with RGB LEDs from the lab. We were able to output the the LEDs with PWM out pins on the MBED.

__Images from Week 1__

![Image1](/IMG_6808 copy.jpg) ![Image2](/IMG_6809 copy.jpg)


### Week 2
We had the new board.



### Week 3: Baseline Demo
EOG, ECG, RGBW LED strip with brightness and color control.


__Images from Week 3__

#### My heartbeat on the scope:
![Image3](/IMG_6831 copy.jpg)

#### Pictures of our beautiful faces with the electrodes on them:
![Image4](/IMG_6842 copy.jpg)

![Image5](/IMG_6845 copy.jpg)

#### Our breadboard for Baseline demo (Clunky and No Dashboard):
![Image4](/IMG_6865 copy.jpg)

### Week 4: Reach Demo
Research into sleep data; adjust staging and display REM, NREM, and wake information.

__Images from Week 3__

#### Our Final Breadboard with Dashboard:
![Image3](/IMG_6869.jpeg)


### Schematic

### Software Technologies

### Experiments
MQTT

