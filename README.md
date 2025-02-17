# EXPERIMENT 1
**Transient AC and DC analysis of common source ampliflier**

![Image](https://github.com/user-attachments/assets/259790f8-36fe-4578-bf2a-7c00f236bd80)
<p> The circuit represents the common source ampliflier. To determine the Dc,Ac and Transient analysis of the CS ampliflier circuit.</p> <br>

**COMPONENTS**
<p>
  This circuit consists of TSMC 180nm Transister ,register and voltage source <br> 
  MOSFET LENGTH : 180nm <br>
  MOSFET WIDTH :  0.207nm      <br>
  Threshold voltage : 0.36 <br>
  Resister : 2.72K <br>
  Supply voltage : 1.8V <br>
  Signal generater : 0.9V   <br>
  DC voltage : 1.9V     <br>
  Amplitude :  50mV   <br>
  Frequency :   1k   <br>  
</p> <br>

**DC Analysis**


![Image](https://github.com/user-attachments/assets/5451a73e-98a1-4619-85a9-bf847ceab48a)
![Image](https://github.com/user-attachments/assets/73102711-c45c-461e-905f-f680312c963b)


<p>
From the analysis we got<br> 
Vout =1.68879V    <br>
Vin =950mV <br>
Id = 5.56046e-05     <br>
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
    <td>0.1um</td>
    <td>4.78279e-05</td>
  </tr>
  <tr>
  <td>180nm</td>
  <td>0.2um</td>
  <td> 5.48873e-05	</td>
  </tr><br>
  <tr>
    <td>180nm</td>
    <td>0.205</td>
    <td>5.53984e-05	</td>
  </tr>
  
  <tr>
    <td>180nm</td>
    <td>0.207um</td>
    <td> 5.56046e-05</td>
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
  In Transient  Analysis we determine the gain of the circuit. For input we give sinusoidal voltage signal where the DC offset is 0.9v peak voltage Vpeak is 50mv, Frequency is 1kHz and AC amplitude is 1V. set the stop time to 3ms.
</p><br>

<p>
  Gain = Vin/Vout<br>
  AV= 0.5625 <br>
  This matches the theoritical value which is calculated but Av = gmRd.<br>
  where gm+ KnVov<br>
  From graph we can observe that there is 180 degree phase shift which is exhibitied by CS ampliflier.
  
</p><br>

**INFERENCE**
<p>
  Diode connected MOSFET will always be in the Saturation region.
  From DC analysis we get the dc operation point and confirms whether the mosfet is in saturation region.Transient amalysis shows how the mosfet behave for the time varying Ac signal (sinewave), It shows that ampliflied output with phase shift of 180 degree 
</p><br>

**RESULT**
<p>
  Vout= 1.68879V  <br>
  Id=  5.56046e-05     <br>
  Vin= 950mV   <br>
  Gain= 0.5625   <br>
  
</p>






