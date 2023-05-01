Download Link: https://assignmentchef.com/product/solved-embsys100-module-2-iar-ide-and-the-different-debug-views
<br>
The goals for the assignment this week:

<ol>

 <li>To explore the IAR IDE and the different debug views.</li>

 <li>Get a better understanding of machine instructions, addresses, variables and pointers.</li>

</ol>

Setup:

<ol>

 <li>Create a new project in IAR following the steps from the slide deck</li>

 <li>Create a counter local variable and increment the counter several times.</li>

 <li>Run the program in the simulator environment and answer the following questions:</li>

</ol>

Observe and answer:

<ol>

 <li>Inject 0x1FFFFFFF for the “counter” value in the variable window, then step thru the program only once to increment “counter”.

  <ol>

   <li>What is the value of the “counter” from the “Locals” window?</li>

   <li>What is the value of the “counter” in the “Register” window?</li>

   <li>Which flags are set in the APSR register? Explain why?</li>

  </ol></li>

</ol>

<ol start="2">

 <li>If your write all Fs (0XFFFFFFFF) in the Register value for “counter” then step thru the program once to increment “counter”

  <ol>

   <li>What happens to the value of “counter” in the “Locals” window?</li>

   <li>What flags, if any, are set in the APSR?</li>

  </ol></li>

</ol>

<ol start="3">

 <li>Change the “counter” variable type in your code to “unsigned”. Inject the values “<strong>0x1FFFFFFF</strong>” then step thru the program to increment the “counter” once:

  <ol>

   <li>What is the value of “counter” in the “Locals” window after incrementing for each value?</li>

   <li>What flags, if any, are set in the APSR? Explain why?</li>

  </ol></li>

</ol>

<ol start="4">

 <li>Change the “counter” variable type in your code to “unsigned”. Inject the values “<strong>0xFFFFFFFF</strong>” then step thru the program to increment the “counter” once:

  <ol>

   <li>What is the value of “counter” in the “Locals” window after incrementing for each value?</li>

   <li>What flags, if any, are set in the APSR? Explain why?</li>

  </ol></li>

</ol>

<ol start="5">

 <li>Move the “counter’ variable outside of main (at the top of the file):

  <ol>

   <li>What is the scope of the variable “counter”?</li>

   <li>Is it still visible in the “Locals” view?</li>

   <li>In which window view can we track “counter” now?</li>

   <li>What is the address of the “counter” variable in memory?</li>

  </ol></li>

 <li>Change the source code to the following, then run the program still in the simulator:</li>

</ol>

<table width="247">

 <tbody>

  <tr>

   <td width="247"><strong>int counter = 0x0; int main() { </strong><strong>int *p_int = (int *)0x20000000; </strong><strong>++(*p_int); </strong><strong>++(*p_int); ++(*p_int); counter ++; </strong><strong>return 0; </strong><strong>} </strong></td>

  </tr>

 </tbody>

</table>




<ol>

 <li>What is the value of “counter” at the end of the program (halting at the <strong>return 0</strong> statement)</li>

 <li>Explain why the counter value has changed?</li>

 <li>Change the setting of IAR to run the same program on the <strong>evaluation board</strong>:</li>

</ol>

<table width="385">

 <tbody>

  <tr>

   <td width="385"><strong>Setup: </strong>1.       Connect evaluation board to your computer through ST Link cable.2.       Set the IAR to using STLink:3.       Project -&gt; Options -&gt; Debugger -&gt; Device: ST-Link4.       Download setting is flash loader5.       Make sure ST-Link Interface is set to SWD 6. Run the same code described in the simulator. </td>

  </tr>

 </tbody>

</table>




<ol>

 <li>What is the address where “counter” is stored?</li>

 <li>Is the “counter” variable stored in RAM or ROM?</li>

 <li>What is the value of “counter” at the end of the program (halting at the <strong>return 0</strong> statement).</li>

</ol>


