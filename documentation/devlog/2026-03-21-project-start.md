I'v chosen the route I want to take for the hardware path; I chose the ESP32-S3 R8N16 for the following two reasons. First is I have three lying around
and second the device has two pram and ram built in and handles Digital audio with low latency and thus is decent for digital audio interfacing, sadly
it doesn't have built in DAC like the original ESP32.

The guitar audio INPUT -  will be done with the PCM1808 I2S ADC Module.
1/4" Mono & 1/8" Stereo jack OUTPUT - I2S PCM5102 stereo DAC module, which I'll be using to handle digital audio from the ESP32-S3 and output analog audio
Controls will be done with a rotary encoder specifically the KY-040 Rotary Encoder Module 
as for clock cycling and such I'll use the Si5351 25MHz Xtal a clock generator / frequency synthesizer

as for I2S  is a digital audio bus used to send PCM(Pulse Code Modulation)audio between chips. The PCM5102/PCM5102A supports standard I2S and also
left-justified audio formats. TI’s datasheets for the PCM5102 and PCM5102A list the supported
PCM data formats as I2S and left-justified.

Eventually the chain will be this 

# guitar/instrument input → input buffer/preamp/ADC → ESP32-S3 processing → I2S → PCM5102 DAC → output jack
