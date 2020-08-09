****************************************************************************************************
      This code is provided here for educational purpose(s) only.  For questions/suggestions
 please email Haroon Waris (haroonwaris@nuaa.edu.cn) or Dr. Weiqiang Liu (liuweiqiang@nuaa.edu.cn)
****************************************************************************************************

This directory contains the Verilog sources of our paper,” Hybrid Partial Product-based High-Performance Approximate Recursive Multipliers”, which is currently under review. 


1.  NxFA.v is the NOR-based approximate full adder.
2.  NxHA1.v is the more-approximated half adder.
3.  NxHA2.v is the less-approximated half adder.
4.  Exact_FA.v is the accurate full adder.
5.  Exact_HA.v is the accurate half adder.

6.  Accurate.v is the exact 4x4 multiplier.
    Dependencies: Exact_FA.v, Exact_HA.v
	 
7.  LxA.v is the less-significant approximated 4x4 multiplier block.
    Dependencies: NxFA.v, NxHA2.v

8.  MxA.v is the more-significant approximated 4x4 multiplier block.
    Dependencies: NxFA.v, NxHA1.v

9.  Ax8_1.v is the approximate 8x8 multiplier.
    Dependencies: MxA.v, NxFA.v, NxHA1.v, Accurate_FA.v, Accurate_HA.v

10. Ax8_2.v is the approximate 8x8 multiplier.
    Dependencies: LxA.v, MxA.v, NxFA.v, NxHA1.v, NxHA2.v, Accurate_FA.v, Accurate_HA.v

11. Ax8_3.v is the approximate 8x8 multiplier.
    Dependencies: LxA.v, MxA.v, NxFA.v, NxHA1.v, NxHA2.v, Accurate_FA.v, Accurate_HA.v


