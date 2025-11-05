# fantastic-waddle
4-BIT BINARY ADDER  WITH  7-SEGMENT DISPLAY USING  VERILOG 

This project focuses on designing a 4-bit binary adder with multiplexed 7-segment displays using Verilog HDL. The system takes two 4-bit binary inputs (A and B), adds them, and produces a 5-bit sum ranging from 0 to 30. The binary result is then converted into decimal digits (tens and units) and displayed on two common-cathode 7-segment displays.

In a Boolean board instead of using separte data lines for both displays,the same 7-segment lines(a-g) are shared through multiplexing. 

 

How it Works: 

 

One set of data lines(a-g) is shared between both displays. 

Each display has its own enable/select signal. 

A 2:1 multiplexer is used here. 

A clock divider generates a slower clock(~1 kHz) from the FPGA clock,which controls the MUX select line.  

 

Switching Process: 

 

When select =0 :Tens digit data is displayed(tens enabled,ones disabled). 

When select =1:Ones digit data is displayed(ones enables,tens disabled0. 

 

Why it Works: 

            The switching happens rapidly,making all displays appear continuously lit due to persistence of vision. 
