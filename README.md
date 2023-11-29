# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
## UP COUNTER :
![Screenshot 2023-11-29 153424](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/496acfc1-057f-4e3c-a979-f47ab243d818)

## DOWN COUNTER :
![Screenshot 2023-11-29 153433](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/fc8bc42d-b512-4940-aece-d5e0b4a9d55e)

### RTL LOGIC UP COUNTER AND DOWN COUNTER:  
## UP COUNTER :
![Screenshot 2023-11-29 153443](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/937cfea5-9b23-478c-acf4-ab90d8ffb2f5)

## DOWN COUNTER :
![Screenshot 2023-11-29 153451](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/d4484d61-7fce-48fc-a2b7-ccf653bad215)

### TIMING DIGRAMS FOR COUNTER:
## UP COUNTER :
![Screenshot 2023-11-29 153459](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/94bb3bd9-6244-41b5-87dd-6d2e9357b3d5)

## DOWN COUNTER :
![Screenshot 2023-11-29 153513](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/474d2f47-276e-4e56-a447-3064d32dbb3e)

### TRUTH TABLE :
## UP COUNTER :
![Screenshot 2023-11-29 153525](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/92124a6e-c8d0-4eda-b37c-9b28dd704be9)

## DOWN COUNTER :
![Screenshot 2023-11-29 153539](https://github.com/bhuvan8903/Exp-7-Synchornous-counters-/assets/151444524/d287c478-0bca-4950-add2-843dd257d9bd)

### RESULTS :
Thus,The 4-bit up and down counter is implemented successfully.
