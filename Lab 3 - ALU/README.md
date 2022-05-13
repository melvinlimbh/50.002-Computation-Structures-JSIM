There were many parts to this, we had to code adder, comparator, boolean and 3 shifter units for the ALU

Schematics
(adder was already done in lab 2, so we just need to cascade them to make it signed 32-bits)
s[31:0] is the output, z == 1 (True) when s[31:0] are all 0s, n == 1 when s is negative (i.e MSB of s = 1) 
v is overflow (i.e v == 1 when output is too large to be represented in 32-bits)


![Lab 3](https://user-images.githubusercontent.com/68263531/168217045-53570de6-4854-47ac-9484-75baf15e4c8c.png)


Comparator unit uses a multiplexer (mux) to generate an output based on given selector signals (the ALUFN signals)

![Lab 3-2](https://user-images.githubusercontent.com/68263531/168217536-748838ed-fe4f-4815-af00-59d692834f10.png)


Boolean unit uses a 4-to-1 mux, to choose the operation (ALUFN signals) to be performed 


![Lab 3-3](https://user-images.githubusercontent.com/68263531/168217603-61ea5b9c-7d9f-48e1-a216-5d1715e3d3e6.png)


there are 3 types of shifters
- shift left (SHL) : shift left by x bits, add 0s to fill up to 32-bits, has the same effect as multiplication
- shift right (SHR) : shift right by x bits, add 0s to fill up to 32-bits, has the same effect as division 
- shift-right arithmetic (SRA) : shift right by x bits, add the MSB of original 32-bit input to fill up to 32-bits


![Lab 3-4](https://user-images.githubusercontent.com/68263531/168219023-1161ea24-d21b-4031-b46e-06d18103f212.png)

![Lab 3-5](https://user-images.githubusercontent.com/68263531/168219161-317efd8e-1513-4853-9804-f580d4a067a9.png)

![Lab 3-6](https://user-images.githubusercontent.com/68263531/168219167-9dfe826e-ffff-49b6-85fd-7350a2f46c46.png)


we then combined the units together to implement an ALU

![Lab 3-7](https://user-images.githubusercontent.com/68263531/168219897-021a4cd2-7832-4b10-89b4-a1d52752ddd4.png)

