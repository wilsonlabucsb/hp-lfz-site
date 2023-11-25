# Using the Mass Flow Controller (MFC)

## Setting up communication with the MFC:

1. Plug the black USB-RS232 connector into your computer.
1. Install FlowDDE from the Bronkhorst website (see below) onto your computer. This is needed to run FlowPlot and set the MFC.
2. Install FlowPlot from the Bronkhorst website (see below) onto your computer.

## Using FlowPlot
1. Open FlowDDE and configure communication settings:
    - Go to "Communication” 🡪 "Communication settings” 
    - Select the correct Com port (#6)
1. Start communication with the MFC
    - Go to  "Communication” 🡪 "Open communication”
    - Should display additional text on the FlowDDE screen indicating it is talking to the MFC, final line should say "Server is active and ready for any client”
    - Note that you can check that communication has been established by going to "FLOW-BUS” and clicking on Channel 1 (i.e. the only connected instrument) listed on the left-hand side. The LEDs on top of the MFC should blink red and green.
    - FlowDDE can now be minimized.
1. Open FlowPlot. The "Select Parameter” screen will pop up.
    - Make sure the "Mode” drop-down menu at the bottom left is set to "18. RS232”.
    - The three lines displayed are:
        - Measure – the measured flow rate out of the MFC (in %)
        - Setpoint – the set flow rate of out of the MFC (in %)
        - Valve out – setting of the outlet valve (how "open" it is... not important)
    - If you desire further confirmation you are connected to the MFC, the LEDs can be made to blink from the "Select Parameter” screen by clicking "Identify instrument (wink LEDs)”.
    - Click "OK”

## Links
[MFC data exchange program, FlowDDE](https://www.bronkhorst.com/int/products/accessories-and-software/flowware/flowdde/)

[MFC data plot/parameter setting program, FlowPlot](https://www.bronkhorst.com/int/products/accessories-and-software/flowware/flowplot/#p_lt_ctl07_pageplaceholder_p_lt_ctl01_BRVideoWebPart_divMain)  

## Setting the MFC
1. In the main plotting window (with Value vs Time displayed) of FlowPlot, click the "Start” button on the right – plot lines should appear.
1. The flow rate of the MFC can then be set in a variety of ways:
    - Input box above "Send” button – type value you want and click "Send”. 
    - Press the +5/-5 buttons (in %).
    - Preset value buttons (100, 80, 50, 20 , 0%)
1. The MFC will now attempt to establish flow at the rate indicated by the % setting. The green and red lines should quickly converge to the set value. Flow will continue from the MFC until the upstream and downstream pressures equalize. 

## Determining the MFC flow setting
The value input to the MFC is in %, which is the percent of the full scale of flow the MFC can do. This MFC is calibrated for Ar at 1300 psi (90 bar) with a flow range of .2 – 10 ls/min (standard liters per minute = at 20 °C and 1 atm). 

There are several use-cases for the MFC:

1. You are flowing Ar and the regulator is set to 1300 psi (calibration condition) = MFC can be set by directly converting % to flow rate using the calibrated flow range. So, 10% = 1 ls/min, 50% = 5 ls/min and so on. Anything in the range (0%,.2%] would presumably yield the minimum flow of .2 ls/min.
1. You are flowing Ar, but at a lower pressure than 1300 psi = use conversion factor from Fluidat (see below), then convert to % in the same way. 
1. You are flowing N2, regardless of the outlet pressure from the regulator = use conversion factor from Fluidat (see below), then convert to % in the same way. 

## Using Fluidat

Fluidat is a program provided by Bronkhorst that allows for calculation of gas conversion factors. These factors allow one to provide an equivalent mass flow of a gas different from the one the MFC has been calibrated for. The calibrated gas is directly connected to the % value set in FlowPlot, as described above, but the conversion factor must be applied for a different gas.

1. Go to [https://www.fluidat.com/default.asp](https://www.fluidat.com/default.asp) and use the log-in information provided below
      - Username = e.zoghlin
      - Password = WilsonLab
1. Go to "Conversion Factor” 🡪 "Gas Conversion Factor” at the top of the page, will display the conversion factor calculator.
1. Click on the text in the "Fluid” row for "Fluid from” column and change to the gas you are using (presumably N2). For "Fluid to” change to Ar.
1. Enter the desired flow rate in the box. Be sure to set units to ls/min (standard liters per minute)
1. Enter the outlet pressure of the regular in desired units [psi(g) or bar(g), with "g" = gauge]
1. Make sure temperature reads 20 °C 
1. Change "Instrument model" drop-down menu to "EL-FLOW".
1. Hit calculate, which will provide an equivalent Ar flow. Convert this to % (see "Determining the MFC flow settings” above) and send to the MFC.

