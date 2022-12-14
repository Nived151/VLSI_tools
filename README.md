## Tools

### 
```
source /proj/ndl/home/vks160030/GF65_6325/setup-GF65-cad
```
<br/>
<br/>

copy
```
cp -r <source_name> <destination_folder>
```

[Library Compiler](https://personal.utdallas.edu/~Xiangyu.Xu/lc/) ( .lib ---> .db )

```
cd ~/cad/synopsys
```
```
cp /home/cad/startup/EE6325/aux/library.lib .
```
```
. /proj/cad/startup/profile.synopsys_2018
```
```
lc_shell
```
```
read_lib library.lib
write_lib library -format db -output library.db
```

[Design Vision](https://personal.utdallas.edu/~Xiangyu.Xu/dv/)
```
design_vision &
```

[HSPICE](https://personal.utdallas.edu/~Xiangyu.Xu/hspice/)
```
cd ~/cad/spice
```

```
>setupsile.txt
```

```
$example HSPICE setup file

$transistor model
.include "/proj/cad/library/mosis/GF65_LPe/cmos10lpe_CDS_oa_dl064_11_20160415/models/YI-SM00030/Hspice/models/design.inc"
.include "exam.pex.sp"


.option post runlvl=5

xi GND! OUT VDD! A B C exam

vdd VDD! GND! 1.2v
va A GND! pwl(0ns 0v 20ns 0v 20.5ns 1.2v 39.5ns 1.2v 40ns 0v)
vb B GND! pwl(0ns 0v 10ns 0v 10.5ns 1.2v 19.5ns 1.2v 20ns 0v 30ns 0v 30.5ns 1.2v 39.5ns 1.2v 40ns 0v)
vc C GND! pwl(0ns 0v 5ns 0v 5.5ns 1.2v 9.5ns 1.2v 10ns 0v 15ns 0v 15.5ns 1.2v 19.5ns 1.2v 20ns 0v 25ns 0v 25.5ns 1.2v 29.5ns 1.2v 30ns 0v 35ns 0v 35.5ns 1.2v 39.5ns 1.2v 40ns 0v)

cout OUT GND! 100f

$transient analysis
.tr 100ps 40ns
.end

```

```
hspice YOUR_SPICE_FILE.sp
```

```
hspice YOUR_SPICE_FILE.sp > YOUR_SPICE_FILE.out
```

```
wv&
```
<br/>
<br/>