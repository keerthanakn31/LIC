# EXPERIMENT 1
**Transient AC and DC analysis of common source ampliflier**

![Image](https://github.com/user-attachments/assets/259790f8-36fe-4578-bf2a-7c00f236bd80)
<p> The circuit represents the common source ampliflier. To determine the Dc,Ac and Transient analysis of the CS ampliflier circuit.</p> <br>

**COMPONENTS**
<p>
  This circuit consists of TSMC 180nm Transister ,register and voltage source <br> 
  MOSFET LENGTH : 180nm <br>
  MOSFET WIDTH :        <br>
  Threshold voltage : 0.36 <br>
  Resister : 2.72K <br>
  Supply voltage : 1.8V <br>
  Signal generater :    <br>
  DC voltage :     <br>
  Amplitude :      <br>
  Frequency :      <br>  
</p> <br>

**DC Analysis**

![Image](https://github.com/user-attachments/assets/c8701d8c-b1ca-492e-8900-68344b5a2a61)
![Image](https://github.com/user-attachments/assets/043ac623-a42c-4bf2-80a9-9e11be691923)

<p>
From the analysis we got<br> 
Vout =    <br>
Vin =     <br>
Id =      <br>
 If the power dessipation is 100um  across the register ,then 
 currengt  throught the resister is<br>
 Id = 100um/1.8 =55.5um<br>
 The output loadline is given by <br>
 Vout =Vdd-(Id-Rd)<br>
 Rd=(1.8-1.674)/55.5um<br>
   =2.751k ohms<br>
</p> <br>

<p>
  Now replace the resister value by Rd = 2.751891k ohm
  Since the Calculated current doesnot match the simulated value, maintain the MOSFET length 180nm and vary the width untill the required current.  
</p>

<table>
  <tr>
    <td>Length</td>
    <td>Width</td>
    <td>Id</td>
  </tr>
  <tr>
    <td>180nm</td>
    <td>1um</td>
    <td>0.000148351</td>
  </tr>
  <tr>
  <td>180nm</td>
  <td>0.1um</td>
  <td>4.76342e-05	</td>
  </tr><br>
  <tr>
    <td>180nm</td>
    <td>0.19</td>
    <td>5.36419e-05	</td>
  </tr>
  
  <tr>
    <td>180nm</td>
    <td>0.21um</td>
    <td> 5.56616e-05</td>
  </tr>
</table><br>

<p>
   The Dc operating point confirms that NMOS operates in saturation region.<br>
   Vds = Vd-Vs = -0 =  <br>
  Vov + Vgs-Vth =0.9-0.36 =0.54V<br>
  Vds>(Vgs-Vth)<br>
</p>


**AC ANALYSIS**

![Image](https://github.com/user-attachments/assets/cf399197-91c0-491b-95cd-d5d108f54aae)

<P>
  In AC analysis we determine the frequency response by appluing the small signal analysis to the circuit. we do this analysis to check in which frequency the circuit acts as a linear ampliflier.
  For this type of sweep we select 'decade', starting frequency as 0.1Hz and stop frequenct as 1THz.


</P><br>

**TRANSIENT ANALYSIS**

![Image](https://github.com/user-attachments/assets/ae8bf8dd-43b9-4b36-98f7-f1d999f7a36c)

<p>
  In AC Analysis we determine the gain of the circuit. For input we give sinusoidal voltage signal where the DC offset is 0.9v peak voltage Vpeak is 50mv, Frequency is 1kHz and AC amplitude is 1V. set the stop time to 3ms.
</p><br>

<p>
  Gain = Vin/Vout<br>
  AV=  <br>
  This matches the theoritical value which is calculated bt Av = gmRd.<br>
  where gm+ KnVov<br>
  From graph we can observe that there is 180 degree phase shift which is exhibitied by CS ampliflier.
  
</p><br>







