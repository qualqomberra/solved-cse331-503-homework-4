Download Link: https://assignmentchef.com/product/solved-cse331-503-homework-4
<br>
<span class="kksr-muted">Rate this product</span>

In this project, you will use Altera Quartus II with Verilog. You will implement a different version of 32-bit MIPS processor. The block that you will design will get no inputs from outside. You will have two memories: Data Memory and Instruction Memory. The instructions must be loaded to the instruction memory and the data must be put in data memory. You will support lw, sw, j, jal, jr, beq, bne, addn, subn, xorn, andn, orn, ori and lui instructions.

But the R-type instructions will execute different than the conventional MIPS we have seen. This is why they have ‘n’ at the end (representing new). The new instructions have the same opcode and function fields as the conventional R-type instructions. For instance the opcode and function field of orn is same as or.

But the execution is different. For instance:

<pre>                        addn $rd, $rs, $rt                        RTL Representation</pre>

<pre>                        $rs &lt;= $rs + $rt                        if($rs + $rt == 0)                        $rd &lt;= 1                        else if($rs + $rt &lt; 0)                        $rd &lt;= 2</pre>

else$rd &lt;= 3

In order to implement that, you must be able to write two different register addresses in one cycle Design your register accordingly.

You will write test bench and simulate your design for verification. You will write the register and memory contents before and after the execution of instructions using writememh in your test bench verilog code. You will initialize memory contents using readmemh.

The data memory size will be 256KB whereas the instruction memory size will be 16KB. Remember that addressing for a 256KB memory only requires 18 bits instead of 32 bits in regular MIPS. Update your design accordingly.

(Bonus) There is no BONUS and we do not want you to implement any other instruction than specified above. Otherwise you get 0 due to cheating.