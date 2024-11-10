<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

Provide an analgo signal in Vin (e.g., some music) and listen to the output of Vout (using an amplifier).
The circuit will probably add some noise, as it is very crude. But it went from the analog domain to digital
and then back.

Future work shoulb be to use that sigma-delta coded signal to do some fun audio processing.

Anyone knowing how to do DSP in the sigma-delta domain?

## How to test
Connect an analog source to your design.

## External hardware

This is a sigma delta AD converter and DA converter.

The input is a the threshold of the DFF input using as comparator, serving as a single bit ADC.

The R and C values can be discussed and experimented.

```


            100k
            ___
   OUT0 o--|___|--+
                  |
            100k  |
            ___   |                                 ____
    Vin o--|___|--o----------o IN0       OUT1 o----|____|---o--------o Vout
                  |                                         |                             
                 ---                                       ---
                 ---  100n                                 ---
                  |                                         |
                  |                                         |
                 ---                                       ---
                  -                                         -
```
