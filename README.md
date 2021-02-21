# multituner-sdr

Original post can be found at https://groups.io/g/NextGenSDRs/topic/hardware_schemes_update/80558935?p=,,,20,0,0,0::recentpostdate%2Fsticky,,,20,2,0,80558935).

Please contact us by E-Mail info#at#coherent-receiver.com or https://coherent-receiver.com if you have interest in any possilble implementations outlined below.

32 bit data bus of FX3 enables to provide following configurations per USB port using parallel ADCs:

    4 tuners x 8 bit or
    2 tuners x 8-16 bit

The hardware example of 2 tuners (R820T2) x 14 bit can be found in this repository (https://github.com/iroks/multituner-sdr), see also https://coherent-receiver.com/products/coherent-receivers/1-supervisory-and-4-coherent-channels (section - single board mutituner receivers). All samples are acquired simultaneously and sent to host interleaved. It is also possible to synchronise multiple USB ports.

It is possible to develop following configurations (all signals are synchronized with a common clock and acquired on host synchronised and interleaved per USB port):

    2 x 30 microphones with I2S output per USB port; multiple USB ports can be synchronised together on host. Technology is tested for a single segment (multiple segment were tested on host without multiple USB ports synchronisation);

or

    30 x 32-bit stereo ADCs with I2S output per USB port; multiple USB ports can be synchronised together on host. Technology is tested for a single segment with sample rates up to 768 kHz per ADC (multiple segement were tested on host without multiple USB ports synchronisation);

    30 x Zero-IF tuner with IQ output and audio ADC with I2S output per USB port; multiple USB ports can be synchronised together on host. Technology is tested for a single segment with sample rates up to 768 kHz per ADC (multiple segement were tested on host without multiple USB ports synchronisation);   
    
    RF broadcast tuners, e.g. SI468x with I2S output; tested successfully, 31+ channels per USB port possible;

    Use multichannel audio ADCs that will increase the number of channels (TDM, not tested, just an idea);

    RF tuners STA709, STA710, TDA7707, TDA7708, Si476x, Si479x or LV25810PEB provide digital I/Q-output via I2S. Typical such chips support about 500 kHz BW signal for further signal processing. 30 such chips can be connected per USB port; multiple USB ports can be synchronised on host. Not tested due to lack of documentations and chips (discussed with both companies behind the tuners; no interest) but should theoretically work;

    30 x RF tuners/frontends per USB and non-audio ADC, not tested, theoretically possible to get 30 x R820T2 (or 15 alternative tuners with IQ output) per USB port; idea for future FX3 generation due to speed requirements or an alternative controller/bus is necessary)
    
Are there any additional features that anyone requests? Please let us know in the comments and many thanks in advance for your feedback!
