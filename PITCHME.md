---?image=assets/images/gitpitch-audience.jpg
@title[UEFI_Driver_Porting Lab]
<br><br><br><br><br>
## <span class="gold"   >UEFI & EDK II Training</span>

#### How to Write a UEFI Driver Lab

<br>
<span style="font-size:0.75em" ><a href='http://www.tianocore.org'>tianocore.org</a></span>
Note:
  PITCHME.md for UEFI / EDK II Training  UEFI Driver Model and Driver Wizard Pres

  Copyright (c) 2018, Intel Corporation. All rights reserved.<BR>

  Redistribution and use in source (original document form) and 'compiled'
  forms (converted to PDF, epub, HTML and other formats) with or without
  modification, are permitted provided that the following conditions are met:

  1) Redistributions of source code (original document form) must retain the
     above copyright notice, this list of conditions and the following
     disclaimer as the first lines of this file unmodified.

  2) Redistributions in compiled form (transformed to other DTDs, converted to
     PDF, epub, HTML and other formats) must reproduce the above copyright
     notice, this list of conditions and the following disclaimer in the
     documentation and/or other materials provided with the distribution.

  THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR
  IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
  MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
  EVENT SHALL TIANOCORE PROJECT  BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
  SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
  PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
  OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
  WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
  OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF
  ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.



---  
@title[Lesson Objective]
<BR>
### <p align="center"<span class="gold"   >Lesson Objective </span></p><br>

<!---  Add bullets using https://fontawesome.com/cheatsheet certificate
-->
<ul style="list-style-type:none">
 <li>@fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Compile a UEFI driver template from UEFI Driver Wizard</span> </li><br>
 <li>@fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Test driver in QEMU using UEFI Shell 2.0</span></li><br>
 <li>@fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Port code into the template driver</span> </li>
</ul>

---?image=assets/images/binary-strings-black2.jpg
@title[UEFI Driver Lab]
<br><br><br><br><br><br><br>
### <span class="gold"  >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;UEFI Driver Porting Lab </span>
<span style="font-size:0.9em" >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</span>


---?image=/assets/images/slides/Slide_LabSec.JPG
@title[Lab 2: Building a UEFI Driver]
<br>
<br>
<p align="Left"><span class="gold" >Lab 2: Building a UEFI Driver</span></p>
<br>
<div class="left1">
<span style="font-size:0.8em" >In this lab, you’ll build a UEFI Driver.<br>You will include the driver in the OVMF project. <br>Build the UEFI Driver from the Driver Wizard </span>
</div>
<div class="right1">
<span style="font-size:0.8em" >&nbsp;  </span>
</div>

---?image=/assets/images/slides/Slide5.JPG
@title[Compile a UEFI Driver?]
<p align="right"><span class="gold" >Compile a UEFI Driver</span></p>

Note:
|Standalone |In a Project	|
|-----------|--------------|
|The build command directly compiles the .INF file |Include the .INF file in the project’s .DSC file	|
|Results:  The driver’s  .EFI file is located in the Build directory|	Results:  The driver’s .EFI file is a part of the project in the Build directory|

---
@title[Lab2: Build the UEFI Driver?]
<p align="right"><span class="gold" >Lab 2: Build the UEFI Driver</span></p>
<ul>
   <li><span style="font-size:0.8em" >Perform <a href="https://gitpitch.com/Laurie0131/Platform_Build_LAB/master#/">Lab Setup</a> from previous Labs  </span></li>
   <li><span style="font-size:0.8em" >Open `~src/edk2/OvmfPkg/OvmfPkgX64.dsc`</span></li>
   <li><span style="font-size:0.8em" >Add the following to the `[Components]` section: </span><br><span style="font-size:0.6em" >Hint: add to the last module in the `[Components]` section   </span></li>
<pre>

   MyWizardDriver/MyWizardDriver.inf{
      <LibraryClasses>    DebugLib|MdePkg/Library/UefiDebugLibConOut/UefiDebugLibConOut.inf
   }

</pre>
   <li><span style="font-size:0.8em" >Save and close the file  </span></li>
</ul>






---  
@title[Summary]
<BR>
### <p align="center"><span class="gold"   >Summary </span></p><br>
<ul style="list-style-type:none">
 <li>@fa[certificate gp-bullet-green]<span style="font-size:0.9em">&nbsp;&nbsp;Generate and compile a driver template </span> </li><br><br>
 <li>@fa[certificate gp-bullet-cyan]<span style="font-size:0.9em">&nbsp;&nbsp;Test driver in QEMU using UEFI Shell 2.0</span></li><br><br>
 <li>@fa[certificate gp-bullet-yellow]<span style="font-size:0.9em">&nbsp;&nbsp;Port code into the template driver</span> </li>
</ul>


 

---?image=assets/images/gitpitch-audience.jpg
@title[Questions]
<br>
![Questions](/assets/images/questions.JPG) 


---?image=assets/images/gitpitch-audience.jpg
@title[Logo Slide]
<br><br><br>
![Logo Slide](/assets/images/TianocoreLogo.png =10x)


---
@title[Acknowledgements]
#### <p align="center"><span class="gold"   >Acknowledgements</span></p>

```c++
/**
Redistribution and use in source (original document form) and 'compiled' forms (converted
to PDF, epub, HTML and other formats) with or without modification, are permitted provided
that the following conditions are met:

Redistributions of source code (original document form) must retain the above copyright 
notice, this list of conditions and the following disclaimer as the first lines of this 
file unmodified.

Redistributions in compiled form (transformed to other DTDs, converted to PDF, epub, HTML
and other formats) must reproduce the above copyright notice, this list of conditions and 
the following disclaimer in the documentation and/or other materials provided with the 
distribution.

THIS DOCUMENTATION IS PROVIDED BY TIANOCORE PROJECT "AS IS" AND ANY EXPRESS OR IMPLIED 
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND 
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL TIANOCORE PROJECT BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, 
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, 
WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS DOCUMENTATION, EVEN IF ADVISED OF THE POSSIBILITY 
OF SUCH DAMAGE.

Copyright (c) 2018, Intel Corporation. All rights reserved.
**/

```
