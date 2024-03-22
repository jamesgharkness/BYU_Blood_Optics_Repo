# 400 G Experiments
## Explanation
The 400 G experiments were a series of experiments done on two separate vials of human blood taken at the same time from the same donor. Blood glucose concentration was increased by 400 mg/dL by the addition of a 0.25 mL injection of 3000 mOsmol/L D-glucose solution. This injection happened twice, once approximately thirty-five minutes after the start of the experiment and again approximately seventy minutes after the start of the experiment. The blood was exposed to a beam and optical data was collected.

Light for the experiment came from a mercury arc lamp (Osram HBO 100 W/2). A point source was approximated by an aperture and the light was collimated by lenses. The collimated light was then focused down to a point, chopped at a frequency of 2 kHz for lock-in detection, and passed through a linear variable filter (LVF) to select a 20 nm band of wavelengths. The LVF can be positioned to select the desired band. After the LVF, the beam was recollimated and split approximately 50/50 for the experiment and control branches. Each branch consisted of two integrating spheres with a cuvette placed between them as described by Pickering et al1. Intensity of light reflected by the blood was measured by photodiodes in the spheres before the sample on either branch. Intensity of light transmitted was measured by integrating spheres placed behind the sample on the beam path.  A more detailed explanation of the use of integrating spheres for extracting scattering and absorption coefficients can be found in Prahl2.   

An optical chopper ran at 2 kHz and served as the reference for all four lock-in amplifiers (Stanford Research 830). Lock-in amplifiers measuring reflection data were used in current mode. The amplifiers measuring transmission data were used in voltage mode and a preamplifier was used to amplify the signal 106 V/A. This choice was based on instrumentation availability and operation.

## Interpretation of Data
The data from the experiments were saved as .csv files. Below is an example of how the data shows up and an explanation of each measurement taken. 

| Step | Wave | R1 | T1 | R2 | T2 | Time | Beam | R1/R2 | T1/T2 | R2Ad | T2Ad | Temp1 | Temp2 | Temp3 | Temp4 |
|:----:|:----:|:--:|:--:|:--:|:--:|:----:|:----:|:-----:|:-----:|:----:|:----:|:-----:|:-----:|:-----:|:-----:|
|117192.0|1100|6.8e-12|1.2e-11|4.0e-12|1.2e-11|7.9|-8.0e-07|1.6|1.0|5.0e-06|15.6|23.2|-16.1|17.3|21.8|

Step: Micro-steps on the stepper driver moving the LVF. It was from this data that the center wavelength of the light was calculated

Wave: Center wavelength of the ~20 nm band of light passed through the LVF to the sample

R1: Current across an InGaAs photodiode in the reflection sphere of the glucose branch

T1: Current across an InGaAs photodiode in the transmission sphere of the glucose branch

R2: Current across an InGaAs photodiode in the reflection sphere of the saline branch

T2: Current across an InGaAs photodiode in the transmission sphere of the saline branch

Time: Time from start of experiment in seconds

Beam: Current across Si photodiode sampling main beam. This was to be used to correct data for fluctuations in the beam showing up in the data, but the intensity of the beam proved to be one of the more stable parts of the experiment and this was not used.

R1/R2: Reflection glucose divided by reflection saline

T1/T2: Transmission glucose divided by transmission saline

R2Ad & T2Ad: Vestigial calculation adjusting the R2 and T2 measurements --- Ignore

Temp 1,2,3,4: Temperature calculated by thermistors placed in the blood. Unfortunately, blood is highly corrosive and even our best efforts could not protect the thermistors from degrading. Ignore this. We are sure that the temperature of the blood was between 33 and 37 C. 
