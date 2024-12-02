java c
Department of Electrical Engineering 
Simulation of   Buck Converters Using PSIM
1 Objectives The   purpose of   the experiment   is to   understand a circuit simulation package –   PSIM    (Power   Simulation),   and   use   the   programmes   to   study   and   analyse   power   electronic   circuits.   PSIM   has   the characteristics of   high    simulation speed, high accuracy and friendly user interface, which   provides   a powerful   simulation   environment   for power   electronic   circuit   analysis,   control   system   design   and   so   on.   The   following   sections   will   show   you how to   construct   a   Buck   converter   and   a   Full-Bridge   inverter   and how to   use PSIM   to   study   its performance.
2 Apparatus/Software 
(1) IBM PC   or   compatible   computer
(2) Microsoft Windows   7   or newer versions
(3) PSIM
3 Procedures 
The workstation   is   an PC   or   compatible   computer with   Windows   7   or newer versions   installed.
3.1      Install PSIM 
(1)    Download    PSIM    Demo    Version   at https://powersimtech.com/products/psim/psim-pricing- and-licensing/download-demo/ ;
(2)   Select   “Skip.   I will register later”   during the   installation.
3.2.    Creating Project 
To begin   with,   open this   software   and   set   a new project.   The procedures   are   as   follows,
-         Click “File >> New      Project”

Then,   create   a name   and   choose the project   location.         Click   “OK”   .

A blank project will be   created   successful.

3.3.    Creating Schematic Diagram 
Schematic   diagram   can   be   constructed   in   the   main   window   of the   programme.       The   procedure   for   constructing   a   schematic   diagram   for   simulation   in PSIM   are   in the   followings:
-          Search    components   in   “Library   Browser”(a)   or   “Elements”   menu   (b)   or   The   bottom   menu bar      (c).

(a)                                                                                                                                                                                                                              (b)

(c)
-          Select the   component   and pull   it   to   the   main   window   for   placing   it   in   the   diagram.
-          Make   connection   between   components by   clicking   a junction   of a   component,   pull   the   line   to   the   junction   of   another   component.

-          Set parameters   or values   of   the   components by   double   clicking.

-          Set the   Current Flag to    1, the   current   of   this   component   can be viewed   in the   SIMVIEW.

-          Place   Simulation Control   component to   set the   simulation time   step   length, total   time   and   so   on.

NOTE:
The    PSIM    demo    version    limits    the    maximum    number    of   data    points    to    6000,    so    if   possible,      please   set   the   simulation time   step   length   as   small   as   possible   to   display   a   longer   simulation   time.

-          To   delete   a   component   or   a   line,   select   it   and press   “Delete” key   on the   keyboard
3.4.    Simulation 
Operation   of   the   circuit   in   the   created   schematic   diagram   can be   predicted   with   simulation   using
PSIM.   The procedures are   shown   as   follows,
-          Sketch   circuit   diagrams   as below,

-          For   carrier wave   setting, you   can   set   its values   according to   the   picture   below.

-          Save the work before running the   simulation.
-         Click “Run PSIM Simulation (F8).

-      The progress bar below the page   shows the   simulation   progress.

-          After the   simulation is   completed,   click   “Run   SIMVIEW” to view the   waveform.

-          Select the variable(s)   you   are   interested   in   to   view   its(their)   waveform(s).


4. Buck Converter Buck   converter   is   a popular   DC/DC   converter   for which   the   output   voltage   can be   stepped   down.   One   of   the   most   useful   applications   is   the   switched   mode   power   supply   that   has   the   advantages      of   high   efficiency   and   small   size.The   major   components   of   a   Buck   converter   include   a   semiconductor   switch   (e.g.   IGBT),   a   free-   wheeling   diode,   an   inductor   and   an   output   filtering   capacitor.      The   control   circuits   include   a   DC   voltage    source,    a    triangular-wave    voltage    source,    a    voltage   comparator   and   an   on-off   switch   controller  代 写Simulation of Buck Converters Using PSIMPython
代做程序编程语言 to   interface   between   the   control   circuit   and   the   power   circuit.   All   these   components   can be   found in ELements.
4.1.   Buck Converter in CCM 
4.1.1.    Open-loop Control of   Buck Converter in CCM 
Construct    a    circuit   diagram       of    the    buck    converter    with   open-loop      control      as       shown    below.   Specifications   of   the   circuit   are:
.             Input voltage is    100V.
.             Switching   frequency is   5kHz.
.             Output voltage is   50V.

Getting    inductors,    capacitors    and    resistors   from    Elements,    the   keyword   for   searching   of   the   components   are L,   C,   andR, respectively.    Resistance of   load is   5Ω. L1 is    1mH.   C1 is   100uF.Performing   the   transient   analysis,   the   recommended   time   step   and   simulation   time   that   are    10µs   and    10ms,   respectively.       It    is   noted   that   entering   units   of parameters   is   not   necessary.       Observe   the      waveforms      and      check      if    the      end      time      of    the      simulation      is      appropriated      for      obtaining   simulation   results.      If   not,   enter   a new   total time   and repeat the   simulation.
Expected Results:

4.1.2.    Closed-loop Control of   Buck Converter in   CCM 
Construct   the   closed   loop   control   Buck   converter   as   shown   below   with   PSIM.   The   specification of   the   closed-loop   control   Buck   converter   is   the   same   as   the   open-loop   control   converter   except   that   the   modulation   signal   is   replaced   by   a   feedback   control   circuit,   not   a   constant   DC   voltage   source. 

Closed   loop   control   of   a buck   converterThe   reference   output   voltage   is   50V.   Voltage   sensor   and   current   sensor   are   adopted   to   get   the   values   of   current   and   voltage   to   facilitate   the   closed-loop   control.   The   lable   (IL,    Vout)    can   be   found   at:

H(s)   is   s-domain   Transfer   Function.

K   is proportional   blcok.

You   can   try   to   modify   the   parameters   of   the   PI   and   P   controllers   to   improve   the   performance and   control   the   output   voltage.   Change   the   end   time   of   the   simulation to   an   appropriate value   for   transient   analysis to   obtain   a   steady   state   output   voltage.   Observe the   simulated   output voltage. 
Expected Results:

It   can   be   seen   that   the   transient   response   of Buck   converter   with   closed-loop   control   is   faster   than   that   with   open-loop   control.
4.2.   Buck Converter in DCM 
When    the    load   is    very   low,   the   inductance   current   will   be   discontinuous,   that   is,   the   Buck   converter runs   in DCM.
4.2.1. Open-loop Control of   Buck Converter in DCM 
The   specification   of   the   Buck   converter   in   DCM   is the   same   as   that   in   CCM   except   that   the   load   resistor   is   changed to 40Ω   .

In   DCM,   the   relationship   between   output   voltage   Vo   and   input   voltage   Vin   does   not   satisfy   the   formula:   Vo   =   D    *   Vin,   and   the   output   voltage   is   affected   by   the   load.   Therefore,   when the   duty   cycle   is   set   to   0.5   under   open-loop   control,   the   output   voltage   is   not   50V.   The   results   are   as   follws. 

4.2.2. Closed-loop Control of   Buck Converter in DCM 
The   closed-loop   control   can make   the   output   voltage   constant regardless   of   the   load   change.
The   specification   of   the   closed-loop Buck   converter in   DCM   is the   same   as the   closed-loop control   converter in   CCM   except   that the   load resistor   is   changed to   40Ω   and   K   of   proportional   block   is   changed to   0.01. 

Expected results:

5. The Report 
The    report       should      include      simulation    results       of    output    voltage,       inductor      current,    MOSFET   current   of   each   case.    Answering the   following   questions:
i)          Identify the   critical   condition   for the   CCM   and   DCM.
ii)       Is the   steady-state voltage the   same   with   the   calculated   results?   If it   is   not,   why?
Bonus:   Suggest what   improvements   can be   done to   achieve   a better   steady-state waveforms.
The   waveforms   and   circuit   can   be   obtained   by   using   PrtScn   or   Snipping   Tool   to   capture   and   paste to any Paint tools.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
