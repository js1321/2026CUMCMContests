2026-CUMCM-Contest README.md
2026 全国大学生数学建模竞赛 · C题
面向分时电价的微网储能优化调度模型研究

Team Members：沈嘉朔、孙阮奕洋、唐骁扬

Competition：2026 China Undergraduate Mathematical Contest in Modeling

Project Overview / 项目简介
This project focuses on the optimal scheduling of microgrid energy storage under time-of-use electricity prices. Based on actual power load, photovoltaic output and time-sharing tariff data, we established a linear programming optimization model aiming at minimizing the daily operating cost of the microgrid.
Considering energy storage SOC constraints, charge-discharge efficiency, power limit and power balance constraints, we completed quantitative calculation, multi-scenario analysis and sensitivity analysis for all four sub-problems of Question C.
本项目围绕分时电价下微网储能优化调度问题展开建模研究。以微电网单日运行总成本最小为优化目标，结合光伏出力、用电负荷、分时电价等真实约束条件，建立线性规划优化模型，完成C题全部四小问的求解、场景对比与参数敏感性分析，输出最优储能充放电调度策略。

Model & Methodology / 模型与方法
- Model Type：Linear Programming (LP) 线性规划优化模型
- Core Objective：Minimize daily microgrid operation cost (purchase cost + energy storage loss cost)
- Solving Tool：Python / PuLP Solver / Pandas / NumPy
- Main Constraints：
  
  - Energy storage SOC upper and lower limit constraints
  - Charge and discharge power limit constraints
  - Charge-discharge efficiency loss constraints
  - Microgrid power supply-demand balance constraints

File Structure / 仓库文件结构

2026-CUMCM-Contest/
├── README.md                                   # 项目说明文档

├── C题.pdf                                      # 竞赛原题

├── 面向分时电价的微网储能优化调度模型研究.pdf    # 最终完整版建模论文

└── 支撑材料/
    
    └── 附件/
        
        ├── 源程序代码1，2，3，4题.ipynb        # 全套四问求解代码
        
        ├── C题微网调控_公式源码.tex            # 论文公式LaTeX源码
        
        ├── AI工具使用详情.pdf                  # AI辅助工具使用说明
        
        ├── readme.txt                          # 原始说明文档
        
        └── result1~result4-3.xlsx              # 各问完整输出结果表

Running Environment & Usage / 运行说明

Environment Requirements

pip install pandas numpy pulp openpyxl matplotlib

How to Run

1. Open 支撑材料/附件/源程序代码1，2，3，4题.ipynb
2. Run the code cell by cell in order
3. The program will automatically calculate and export Excel result files

Research Content & Results / 研究内容
- Problem 1：Establish the basic optimal scheduling model, solve the minimum daily operation cost and charge-discharge strategy.
- Problem 2：Analyze scheduling differences under different time-of-use electricity price scenarios.
- Problem 3：Carry out sensitivity analysis of energy storage capacity parameters.
- Problem 4：Expand multi-scene optimization and comprehensive evaluation of microgrid dispatch.

Team Information / 团队信息

Team Member：沈嘉朔、孙阮奕洋、唐骁扬

Completion Time：2026 National College Students Mathematical Modeling Competition
