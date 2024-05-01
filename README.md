# mod_log

Story of my PC modding

## system

| part    | piece                                             | link or sth                                                                         |
|---------|---------------------------------------------------|-------------------------------------------------------------------------------------|
| CPU     | Intel Core **i9-14900KF**, 3.2 GHz, 36 MB         | BX8071514900KF                                                                      |
| MB      | MSI PRO Z790-A WIFI DDR4                          | [-> MSI](https://www.msi.com/Motherboard/PRO-Z790-A-WIFI-DDR4)                      |
| GPU     | MSI GeForce RTX 3060 Ventus 2X OC                 | [-> MSI](https://www.msi.com/Graphics-Card/GeForce-RTX-3060-VENTUS-2X-12G/Overview) |
| Mem     | 4x G.Skill Ripjaws V, DDR4, 64 GB, 4400MHz, CL19  | F4-4400C19D-64GVK                                                                   |
| Case    | Fractal Design Define R6                          | FD-CA-DEF-R6-BK                                                                     |
| Cooling | Fractal Design Celsius S36 (top)                  | FD-WCU-CELSIUS-S36-BK, includes 3x                                                  |
| Cooling | + included AIO pomp (Fractal Design)              |                                                                                     |
| Cooling | + included 3x AIO fans (Fractal Design) (fan out) | Fractal Design Dynamic X2 GP-12 PWM                                                 |
| Cooling | 1x 14" fan (rear) (fan out)                       | Fractal Design Dynamic X2 GP-14 PWM                                                 |
| Cooling | 2x 14" fans (front) (fan in)                      | Fractal Design Dynamic X2 GP-14                                                     |
| Cooling | 2x 12" fans (bottom) (fan in)                     | Fractal Design Dynamic X2 GP-12 PWM                                                 |
| SSD     | 3x Samsung 980 PRO 2TB M.2                        | MZ-V8P2T0BW                                                                         |
| System  | Windows 11                                        | 23H2                                                                                |

## BIOS settings

| Setting                    | value          | comment                         |
|----------------------------|----------------|---------------------------------|
| BIOS                       | 7E07v1B        | version 1B                      |
| OverTemperature protection | Enable         | required by XTU                 |
| FLL_OC_MODE                | Mode 1 - Ratio | XTU properly reports core freq. |
| RAM profile                | XMP 1          |                                 |
| RAM freq                   | 3600 MHz       |                                 |

# Goal

The goal of this story is:

* Using system as specified above
* Using benchmarking/stressing tools:
    * CPU: Intel Extreme Tuning Utility
* Avoiding:
    * thermal throttling
    * other disruptions
* Maximizing:
    * CPU: XTU benchmark score
    * GPU performance: no target
    * SSD performance: no target
    * Memory performance: no target
* Obtain components **temperatures as low as possible**
* Obtain whole system as quiet possible

# Measures

* Set all fans: 100%
* Run XTU v.14
* Try
    * to maximize benchmark
* using
    * Stressing in: CPU Stress Test with AVX2
    * Stressing in: Memory Stress Test
* while
    * there is no thermal throttling

## XTU/BIOS profile

|                                   | Working | As optimized by Intel AI |
|-----------------------------------|--------:|-------------------------:|
| _Profile_                         |         |                          |
| 1 Active Performance Core         |  **59** |                       61 |
| 2 Active Performance Cores        |  **59** |                       61 |
| 3 Active Performance Cores        |  **54** |                       59 |
| 4 Active Performance Cores        |  **54** |                       59 |
| 5 Active Performance Cores        |  **54** |                       59 |
| 6 Active Performance Cores        |  **54** |                       59 |
| 7 Active Performance Cores        |  **54** |                       59 |
| 8 Active Performance Cores        |  **54** |                       59 |
| Active Efficient Cores            |  **45** |                       45 |
| Ratio Offset for 1 Active P-Core  |  **-1** |                       -1 |
| Ratio Offset for 2 Active P-Cores |  **-1** |                       -1 |
| Ratio Offset for 3 Active P-Cores |  **-2** |                       -2 |
| Ratio Offset for 4 Active P-Cores |  **-2** |                       -2 |
| Ratio Offset for 5 Active P-Cores |  **-2** |                       -2 |
| Ratio Offset for 6 Active P-Cores |  **-2** |                       -2 |
| Ratio Offset for 7 Active P-Cores |  **-2** |                       -2 |
| Ratio Offset for 8 Active P-Cores |  **-2** |                       -2 |
|                                   |         |                          |
| _Banchmark_                       |         |                          |
| Banchmark (max)                   |   13134 |                    14100 |
| Banchmark (min)                   |   12789 |                    13627 |
| Throttling (while benchmarking)   |      No |                      Yes |
| Max P-Core Freq                   |    5.39 |                     6.09 |
| Max E-Core Freq                   |    4.49 |                     4.49 |
| Max CPU Temp                      |      85 |                          |
|                                   |         |                          |
| _CPU Stress Test with AVX2_       |         |                          |
| Max CPU Temp                      |      85 |                          |
| Max TDP                           |     236 |                          |
|                                   |         |                          |
| _Memory Stress_                   |         |                          |
| Max CPU Temp                      |      93 |                          |
| Max TDP                           |     311 |                          |
                                           
[XTU Profile](resources/Working.xtu)
