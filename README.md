## Tools

### 
```
source /proj/ndl/home/vks160030/GF65_6325/setup-GF65-cad
```
<br/>
<br/>

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
<br/>
<br/>