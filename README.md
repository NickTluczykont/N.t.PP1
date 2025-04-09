# N.t.PP1
N.t.PP1 überarbeitet
## Tasks
  
  ### Task 1: Mapping Symbols to Binary
  Fill out the following table, mapping decimal numbers `0` through `15` to their binary representations:
  
  | Decimal | Binary Representation |
  |---------|------------------------|
  | 0       | 0000                   |
  | 1       | 0001                   |
  | 2       | 0010                   |
  | 3       | 0011                   |
  | 4       | 0100                   |
  | 5       | 0101                   |
  | 6       | 0110                   |
  | 7       | 0111                   |
  | 8       | 1000                   |
  | 9       | 1001                   |
  | 10      | 1010                   |
  | 11      | 1011                   |
  | 12      | 1100                   |
  | 13      | 1101                   |
  | 14      | 1110                   |
  | 15      | 1111                   |
  
  **How many binary digits (bits) are needed?**
  
  Explain how to calculate the number of bits required:
  <details>
  <summary>Your Answer</summary>
  4Bits
  
  ---
  
  ### Task 2: Mapping Binary to Binary
  Digital processors implement **logical functions** using **logic gates** like NAND, AND, OR, etc.
  These functions map binary input sets (voltages) to binary outputs.
  
 Simulate this adder using NAND gates:
 
  | A | B | C | X | Y |
  |---|---|---|---|---|
  | 0 | 0 | 0 | 0 | 0 |
  | 1 | 0 | 0 | 1 | 0 | 
  | 0 | 1 | 0 | 1 | 0 |
  | 1 | 1 | 0 | 0 | 1 | 
  | 0 | 0 | 1 | 1 | 0 |
  | 1 | 0 | 1 | 0 | 1 |
  | 0 | 1 | 1 | 0 | 1 |
  | 1 | 1 | 1 | 1 | 1 |               
  
  
  #### Your Task
  Create a truth table for a **2-bit adder** without carry-in. What are the possible inputs and outputs?
                                                                                                                                                                                                                           
  | A1  | A2  | B1  | B2  | Z   | Y   | X   |
  |-----|-----|-----|-----|-----|-----|-----|
  | 0   | 0   | 0   | 0   | 0   | 0   | 0   |           
  | 1   | 0   | 0   | 0   | 0   | 0   | 1   |           
  | 0   | 1   | 0   | 0   | 0   | 1   | 0   |            
  | 1   | 1   | 0   | 0   | 0   | 1   | 1   |            
  | 0   | 0   | 1   | 0   | 0   | 0   | 1   |            
  | 1   | 0   | 1   | 0   | 0   | 1   | 0   |            
  | 0   | 1   | 1   | 0   | 0   | 1   | 1   |             
  | 1   | 1   | 1   | 0   | 1   | 0   | 1   |            
  | 0   | 0   | 0   | 1   | 0   | 1   | 0   |          
  | 1   | 0   | 0   | 1   | 0   | 1   | 1   |           
  | 0   | 1   | 0   | 1   | 1   | 0   | 0   |           
  | 1   | 1   | 0   | 1   | 1   | 0   | 1   |           
  | 0   | 0   | 1   | 1   | 0   | 1   | 1   |           
  | 1   | 0   | 1   | 1   | 1   | 0   | 0   |           
  | 0   | 1   | 1   | 1   | 1   | 0   | 1   |            
  | 1   | 1   | 1   | 1   | 1   | 1   | 0   |           
 
 
  ### Task 3: Boolean Equations via Karnaugh Maps
  Use the [K-Map method](https://github.com/STEMgraph/4b957490-badf-4264-b9f2-1b5aa370f36e) to derive Boolean equations for each output bit in your 2-bit adder.
  
  1. Fill out Karnaugh Maps
     
            | (A)  | (B)  | (C)  | (D)  |
    X       |  00  |  01  |  10  |  11  |
      ---------------------------------------
    (A) 00  |  000 |  001 |  010 |  011 |
      ---------------------------------------
    (B) 01  |  001 |  010 |  011 |  100 |
      ---------------------------------------
    (C) 10  |  010 |  011 |  100 |  101 |
      ---------------------------------------
    (D) 11  |  011 |  100 |  101 |  110 |
      ---------------------------------------
 
  2. Write down an equation for each cell marked `1`
 
 0=A&A
 
 1=A&B
 
 1=B&A
 
 2=B&B
 
 2=C&A
 
 2=A&C
 
 3=A&D
 
 3=D&A
 
 3=C&B
 
 3=B&C
 
 4=D&B
 
 4=B&D
 
 4=C&C
 
 5=D&C
 
 5=C&D
 
 6=D&D
 
  4. Combine them using OR gates
  
 0=A&A
 
 1=A&B / B&A
 
 2=B&B / C&A / A&C
 
 3=A&D / D&A / C&B / B&C
 
 4=D&B / B&D / C&C
 
 5=D&C / C&D
 
 6=D&D
 
  5. Minimize the equations
  
 0=A&A
 
 1=A&B
 
 2=B&B / C&A 
 
 3=A&D / B&C
 
 4=D&B / C&C
 
 5=D&C
 
 6=D&D
  
 
 
 
  
  ### Task 4: Circuit Implementation
  Using your Boolean equations, build a logic network in [CircuitVerse](https://circuitverse.org) that implements at least one bit of the adder.
  
  A share link to your solution goes here:

  one bit adder
  
  (https://circuitverse.org/users/305867/projects/pp1-n-t)
  
  two bit adder
  
  https://circuitverse.org/users/305867/projects/p1p1n-t
  
  **Remember:** Stop working after 90 minutes and record where you stopped!
