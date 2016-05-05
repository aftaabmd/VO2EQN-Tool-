# VO2EQN-Tool-
Tool converts verilog synthesized file (.VO extension) to .eqn file
The tool was designed for functional verification purposes.
Then this ,eqn file is put in to petboss (which only works in 64 bit linux)
which substitues all the intermediate equations in to the final output signature to generate the input signature.
Problems encountered:
1)expanding the equations wasn't easy so used a symbolic library called sympy
2) first half was done in c++, other half in python and a .sh file was created to call both programs.

Commands to use petboss:
Usage:

./petBoss.exe -l < *.eqn 
(it prints the extracted input signature when all the equations are rewritted.)

eqn format:
    Each equation represents one gate in the verilog file.
    The output signature must be written in the bottom of the file.
    (You have to write a passer to translate verilog into eqn.)
    
    
    
    
    The commands to use our tool are in the attached report file.
    
    The verilog code taken from here and also has other omportant stuff
    
    https://bitbucket.org/ycunxi/arithverification_by_funcextraction/overview
    
    
    Watch out for the copyright issues everything done here is academic level. Petboss tool is under the project of professor maceij ceiselski.
    
