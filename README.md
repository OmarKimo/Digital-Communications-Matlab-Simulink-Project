# ELC325 Project

## _Common Reproducing Steps_

1. Open **_Matlab_** (with any way you choose)
2. Open **_Simulink_** by typing **simulink** in the **command window** or by clicking on **_Simulink_** Button in **Home** Tab.
3. Create **Blank Model** in **New** Tab.
4. Add the necessary blocks by typing the name of it on the blank window.
    - **Random Integer Generator**.
    - **Modulator** & **Demodulator** for chosen scheme.
    - **AWGN Channel**.
    - Two **constellation diagrams** for plotting the symbols at the transmitter and receiver.
    - **Error rate calculation**.
    - **Display** for BER.
    - **To Workspace** block for generating the BER-vs-SNR figures. 
5. Connect the blocks in the way shown in [Blocks](/Blocks) folder.
6. Set the **Simulation stop time** (in a text box in the above buttons) to 100.
7. In the **Random Integer Generator** : Set **Source of initial seed** to **Parameter** and Set **Initial seed** to _37_.
8. In the **AWGN Channel**: Set **Eb/No (dB)** to _10_.
9. In **Error rate calculation** : Set **Output data** to **Port**, tap **Stop Simulation**, and set **Maximum number of symbols** to _1e4_.
10. In **To Workspace** : Set **Limit data points to last** to _2_, set **Save format** to **Array**, and **Save 2-D signals as 2-D array**.
11. Save the model (by clicking on the **Save** button or by using the shortcut **_Ctrl+S_**) with any name and location you choose.
12. Click on **Run** Button to produce the scatter plots.
13. In the **AWGN Channel** : Set **Eb/No (dB)** to _Eb/No_ to be able to produce **BER** figure.
14. **_Don't forget to Save_**.
15. Type **bertool** in the **command window** then click **_Enter_**.
16. In **Theoritical** tab : choose the specific **Modulation Type** you are using with **Modulation Order** you are using, then click **Plot**.
17. In **Monte Carlo** tab : Set the **Eb/No range** to _-10:1:10_.
18. Choose the model you are using and previously saved in **Simulation MATLAB File or Simulink model** tab.
19. Set **BER variable name** to the name of **To Workspace** block in your model (default: _simout_, mine: _ber_).
20. Set **Number of bits** to _1e4_.
21. Click **Run** to produce the **BER** figure.

## **BPSK**

- ###  Description

    BPSK is the simplest (Binary) form of phase shift keying (PSK).<br>It uses two phases which are separated by 180° and so can also be termed 2-PSK.<br>

- ###  Additional Reproducing Steps
- ###  Scatter Plots
    **Before Noise** figure is the plot of symbols at transmitter, and **After Noise** figure is the plot of symbols at receiver:
    ![BPSK_ScatterPlots](/Scatter&#32;Plots/BPSK_Scatter.png)
- ###  BER Performance figure
    The **theoretical-exact0** curve is the Theoretical (Exact), and **simulation0** curve is for the simulation of the model:
    ![BPSK_BER](BER&#32;Figures/BPSK_BER.png)

## **QPSK**

- ###  Description

    Quadrature phase-shift keying (QPSK) is one of PSK forms.<br>
    QPSK uses four points on the constellation diagram, equispaced around a circle.<br>
    With four phases, QPSK can encode two bits per symbol to minimize the bit error rate (BER) — sometimes misperceived as twice the BER of BPSK.<br>

- ###  Additional Reproducing Steps
- ###  Scatter Plots
    **Before Noise** figure is the plot of symbols at transmitter, and **After Noise** figure is the plot of symbols at receiver:
    ![QPSK_ScatterPlots](/Scatter&#32;Plots/QPSK_Scatter.png)
- ###  BER Performance figure
    The **theoretical-exact0** curve is the Theoretical (Exact), and **simulation0** curve is for the simulation of the model:
    ![QPSK_BER](BER&#32;Figures/QPSK_BER.png)

## **FSK**

- ###  Description

    Frequency-shift keying (FSK) is a frequency modulation scheme in which digital information is transmitted through discrete frequency changes of a carrier signal.<br>
    The simplest FSK is binary FSK (BFSK) which I have used.<br>
    BFSK uses a pair of discrete frequencies to transmit binary (0s and 1s) information.<br>
    With this scheme, the "1" is called the mark frequency and the "0" is called the space frequency.<br>

- ###  Additional Reproducing Steps
- ###  Scatter Plots
    **Before Noise** figure is the plot of symbols at transmitter, and **After Noise** figure is the plot of symbols at receiver:
    ![FSK_ScatterPlots](/Scatter&#32;Plots/FSK_Scatter.png)
- ###  BER Performance figure
    The **theoretical-exact0** curve is the Theoretical (Exact), and **simulation0** curve is for the simulation of the model:
    ![FSK_BER](BER&#32;Figures/FSK_BER.png)

## **QAM 16**

- ###  Description

    Quadrature amplitude modulation (QAM) is the name of a family of digital modulation methods and a related family of analog modulation methods widely used in modern telecommunications to transmit information.<br>
    It conveys two analog message signals, or two digital bit streams, by changing (modulating) the amplitudes of two carrier waves, using the amplitude-shift keying (ASK) digital modulation scheme or amplitude modulation (AM) analog modulation scheme.<br>
    The two carrier waves of the same frequency are out of phase with each other by 90°, a condition known as orthogonality and as quadrature.<br>
    Since in digital telecommunications the data is usually binary, the number of points in the grid is usually a power of 2 (2, 4, 8, …).<br>
    Since QAM is usually square, some of these are rare — the most common forms are 16-QAM, 64-QAM and 256-QAM.<br>
    So this (QAM-16) is one of the most common forms of QAM.<br>

- ###  Additional Reproducing Steps
- ###  Scatter Plots
    **Before Noise** figure is the plot of symbols at transmitter, and **After Noise** figure is the plot of symbols at receiver:
    ![QAM16_ScatterPlots](/Scatter&#32;Plots/QAM16_Scatter.png)
- ###  BER Performance figure
    The **theoretical-exact0** curve is the Theoretical (Exact), and **simulation0** curve is for the simulation of the model:
    ![QAM16_BER](BER&#32;Figures/QAM16_BER.png)

## **QAM 64**

- ###  Description
        QAM-64 is one of the most common forms of QAM.
- ###  Additional Reproducing Steps
- ###  Scatter Plots
    **Before Noise** figure is the plot of symbols at transmitter, and **After Noise** figure is the plot of symbols at receiver:
    ![QAM64_ScatterPlots](/Scatter&#32;Plots/QAM64_Scatter.png)
- ###  BER Performance figure
    The **theoretical-exact0** curve is the Theoretical (Exact), and **simulation0** curve is for the simulation of the model:
    ![QAM64_BER](BER&#32;Figures/QAM64_BER.png)