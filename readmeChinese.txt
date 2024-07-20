输入文件：inputMieDISORT.txt
输出文件：方向反射率文件 brfMieDISORT.txt，球面反照率文件 albedoMieDISORT.txt
运行程序：windows平台，双击runMieDISORT.bat 调用 MieDISORT.exe即可。

inputMieDISORT.txt 文件为Fortran namelist格式

1. radius，雪粒径，单位为微米，取值范围是10~3000。如果设置为0，则输出所有粒径（1000微米以下间隔为10微米，以上的间隔是100微米）的结果。
2. wavelength，波长，单位为微米，取值范围是0.3~2.5。如果设置为0，则输出所有波长的结果。
3. shapeTyp, 雪粒形状，1 for sphere, 2 for spheroid，3 for hexagonal plate, 4 for koch snowflake，查找表来自SNICAR。
4. irrDir，直射光比例，取值范围0~1，黑天空条件取1.0，白天空取0.0。默认为0。
5. sza, 入射天顶角度，0~90，默认为0.
6. PHI0, 入射方位角度，0~360，默认为0。
对于观测角度的条件，有2种方式可以选择，一种是等间隔批量处理，一种是自定义一组角度。

等间隔角度设置：
7. NUMU, 观测天顶角个数，默认为1. 比如，1度分辨率可以设置NUMU为91。
8. NPHI, 观测方位角个数，默认为1. 比如，1度分辨率可以设置为181。
此时第9第10个参数无效。
或者自定义一组角度：
7. NUMU, 观测天顶角个数，但要设置为负数。
8. NPHI, 观测方位角个数，但要设置为负数。
9. iUMU, 观测天顶角，abs(NUMU)个数据，但必须是降序排列。
10. iPHI, 观测方位角，abs(NPHI)个数据。

11. optD，雪层光学厚度，对于半无限可以设置一个大值（默认30000）。

12. ALBEDO,积雪下地表反照率，默认为0。
13. NSTR，流数，默认32。

