## Our Goggles in Action
![Goggles in Action](/Screen Shot 2019-05-01 at 12.03.16 AM.png)

## Original Baseline Goals
● Construct comfortable goggles with dynamic light emission and rechargeable battery.

● Programmatically filter lux and wavelength of a matrix of colored LEDs based on medical
protocols.

● Measure brain pulse activity for medical analysis of device.

## Updated Goals
● Measure EOG activity and use feedback to determine stage of sleep on patient

● Measure Heart Rate and use feedback to determine stage of sleep on patient 

● Emit light that follows the trajectory based on data from Doctor 

● Create a Dashboard for the administrator of the test to follow the progress of the patient


### Motivation
Circadian Rhythm Sleep Disorders (CRSD) is a condition that is characterized by various psychological and physiological effects, such as fatigue, irritability, poor concentration, and work errors. It affects health, working and living. Besides Jet lag, CRSDs affects shift workers, and cause “social jet lag” in the irregular sleeping population. Current treatments to CRSDs are medicine like Melatonin and light therapy by using blue lights such as Re-timer, Sunbox, Lumos and Verilux. None of those light therapies are FDA approved and the general outcomes of those methods are poor.

### How We Did It
We used a MBED to control colored LED lighting dynamically through multiple threads. We adjusted both the lux and wavelength of the light throughout a night to adhere to the stakeholders protocols. We had different stages of sleep cycle and in each stage we showed different lighting. The three stages were awake, non-REM sleep, and REM sleep. To progress from one stage to another, the patient has to have a low enough heart rate and a fast enough eye movement rate. We have three electrodes that measure the patients heart rate and three that measure the patients eye movement. We continuously take readings and if the patient meets the thresholds for the next stage, then the lights will change to help the patient transition into that stage. If the patient does not meet the threshold values, then they restart the current stage they are in.


### Week1

Before working with the LED Matrix board, we first wanted to get the project working with RGB LEDs from the lab. We were able to output the the LEDs with PWM out pins on the MBED. See the images below to look at our basic working circuit.

__Images from Week 1__

![Image1](/IMG_6808 copy.jpg) ![Image2](/IMG_6809 copy.jpg)


### Week 2
We had the new LED Matrix board which we replaced the invidivual RBG LEDs with. The Board required a 16 pin connector and 8 Output pins to work. With the MBED it was impossible to get it working properly. We were able to get the board to flash in different colors but we could not get it to switch to other colors without reseting the MBED. Additionally, this board was way too bright for something that would be put to your eyes. We decided to switch to an LED strip for the baseline demo. 



### Week 3: Baseline Demo

For the baseline demo we replaced the board with an LED Strip. We attached the LED strip into our Goggles and wired it to an output pin from the MBED board. We were able to use a graphics library for the RGB LED except the strip that we had was RGBW instead of the basline RGB library. So we had to update the library to allow it to send more information and then we could control the LEDs. We got the change in color working and programmed it to change color and brightness along the trajectory given to us by the doctor. 

Besides the LEDs, we also got the Heartrate and EOG signals working for our system. We used the breakout board seen in the image below to get a crisp signal. For the heartrate, we were able to get a clean reading by just counting the amount of peaks in an interval and then stretching that out over 1 min to get a beats per minute number. For the eye movement, it was a little more difficult as the signal showed up as an oscillation from 1.6 V rather than a sharp spike like the heart rate. So for this signal we had to perform signal progressing in the code to get a number for eye movements per minute. We looked for deviations from the steady state value and if one occured, we would wait before checking again to make sure we did not count a blink twice. With this system working, we were able to demo our closed loop signal for baseline demo day.

We had the basic components working for baseline demo day but had to change a few things. We needed to determine how to disipate the light so that the user is not staring at the led strip but rather just a haze of colored light. We also needed a dashboard for the administrator of the test to watch as the patient underwent the test. Finally, we had to cleanup our breadboard to make it all look better. 


__Images from Week 3__

#### My heartbeat on the scope:
![Image3](/IMG_6831 copy.jpg)

#### Pictures of our beautiful faces with the electrodes on them:
![Image4](/IMG_6842 copy.jpg)

![Image5](/IMG_6845 copy.jpg)

#### Our breadboard for Baseline demo (Clunky and No Dashboard):
![Image4](/IMG_6865 copy.jpg)



### Week 4: Reach Demo
For our reach demo, we read several medical papers to determine new thresholds for stage progression.  Essentially, we wanted to ensure that a patient progresses from wakefulness to NREM sleep to REM sleep.  We found ranges of heart rate and blink rate and used averages of different data sets to determine new threshold values betweeen stages.  In general, as the patient gets into deeper sleep the heart rate decreases while the blink rate decreases.  

From these new threshold values, we also added display information on our breadboard such that a different LED shows a patients current sleep stage.

Research into sleep data; adjust staging and display REM, NREM, and wake information.  

insert more here about improvements from baseline to reach etc. 

__Images from Week 4__

#### Our Final Breadboard with Dashboard:
![Image3](/IMG_6869.jpeg)



### Schematic
![Schematic](/Screen Shot 2019-05-12 at 4.59.39 PM.png)

### Software Technologies

### Experiments
MQTT

