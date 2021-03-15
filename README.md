# multituner-sdr

Original post can be found at https://groups.io/g/NextGenSDRs/topic/hardware_schemes_update/80558935?p=,,,20,0,0,0::recentpostdate%2Fsticky,,,20,2,0,80558935).

Please contact us by E-Mail info#at#coherent-receiver.com or https://coherent-receiver.com if you have interest in any possilble implementations outlined below.

32 bit data bus of FX3 enables to provide following configurations per USB port using parallel ADCs:

    4 tuners x 8 bit or
    2 tuners x 8-16 bit

The hardware example of 2 tuners (R820T2) x 14 bit can be found in this repository (https://github.com/iroks/multituner-sdr), see https://coherent-receiver.com/fx3-multituner (section - single board multituner receivers). This disclosed implementation is based on FX3 development board (EZ-USB FX3 Software Development Kit, costs ~45 EUR) but we also have developed a CYUSB3014BZXC integrated version. 

FX3 supports ADC sampling rates up to 100 MHz (or up to 120 MHz out of spec). Therefore, ~200 MHz spectrum can be observed by 4 * 50 MHz tuners/mixers and can be used for scenarios: 
- bandwidth aggregation for continuous/non-continuous spectrum, 
- synchronized receiving on different frequencies, e.g. for frequency hopping decoding.

All samples are acquired simultaneously and sent to host interleaved. Therefore, this device can also be used for signal decoding improvements, DF, DOA, passive radars or just  beamforming experiments. 

It is also possible to synchronise multiple USB ports.

Are there any additional features that anyone requests? Please let us know in the comments and many thanks in advance for your feedback!  
