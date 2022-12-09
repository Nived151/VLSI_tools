## Tools

### 
- [Virutoso](https://github.com/Nived151/VLSI_tools#virtuoso-tutorial)
###
 - [PrimeTime](https://github.com/Nived151/VLSI_tools#primetime-tutorial)
### 
- [Innovus]()
### 
- [PrimeLib](https://github.com/Nived151/VLSI_tools#primelib-tutorial)
### 
- [Design Vision]()
### 
- [HSPICE]()

<br/>
<br/>

#  Virtuoso [Tutorial](https://personal.utdallas.edu/~xxx110230/gf65/)
<br/>

```
cd ~/cad/gf65
```

```
. /proj/cad/startup/profile.ee7325
```

```
virtuoso &
```
<br/>
<br/>

#  PrimeTime [Tutorial](personal.utdallas.edu/~xxx110230/gf65/)
<br/>

```
cd ~/cad/primetime
```

```
. /proj/cad/startup/profile.synopsys_2018
```

```
pt_shell -f primetime.script
```
<br/>
<br/>

# Innovus [Tutorial](personal.utdallas.edu/~xxx110230/gf65/)
<br/>

```
cd ~/cad/gf65/innovus
```

```
. /proj/cad/startup/profile.ee7325
```

```
innovus
```
<br/>
<br/>

#  PrimeLib [Tutorial](personal.utdallas.edu/~xxx110230/gf65/)
<br/>

```
cd ~/cad/gf65/primelib_gf65
```

```
. /proj/cad/startup/profile.synopsys_2018
```

```
primelib
```
```
create -legacy INV
```
In Config File - Replace [Configure.tcl](https://github.com/Nived151/VLSI_tools/blob/main/configure.tcl)

In netlist file - Transfer the following files 
-  INV.pex.sp,
- INV.pex.sp.pex
- INV.pex.sp.INV.pxi

In Control File - Replace [INV.inst](https://github.com/Nived151/VLSI_tools/blob/main/INV.inst) / [DFF.inst](https://github.com/Nived151/VLSI_tools/blob/main/DFF.inst)

change  (remember to replace vdd! To VDD, and gnd! to
VSS before copying the files)
- INV.pex.sp filename
- area
- name indefine parameters
- functions/ equations accordingly
```
NAND2: OUT {(!(A&B))}
NOR2: OUT {(!(A+B))}
XOR2: OUT {(((!A)&B)+((!B)&A))}
MUX2:1: OUT {(((!S)&A)+(S&B))}
AOI21: OUT {(!((A&B)+(C)))}
OAI22: OUT {(!((A+B)&(C+D)))}
AOAI211: OUT {(!(((A&B)+C)&(D)))}
```
<br/>
After run these commands in primelib Terminal

```
set_location INV
```
```
configure
```
```
characterize
```
```
model
```
<br/>
<br/>

#  Design Vision [Tutorial](personal.utdallas.edu/~xxx110230/gf65/)
<br/>

```
cd ~/cad/gf65
```

```
. /proj/cad/startup/profile.ee7325
```

```
virtuoso &
```
<br/>
<br/>