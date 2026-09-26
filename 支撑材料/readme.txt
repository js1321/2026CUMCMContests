一、内容概述
本支撑包包含问题一至问题四的完整求解Python程序、代表性仿真输出结果、论文公式LaTeX源码以及AI工具使用说明。
程序使用Python内置HiGHS求解器，不需要额外安装商业求解器，无需GPU。

二、运行环境
- 操作系统：Windows 10/11 64位
- Python版本：3.12.14
- 依赖库：
    numpy==2.3.5
    scipy==1.18.1
    openpyxl
安装依赖执行命令：
pip install numpy==2.3.5 scipy==1.18.1 openpyxl

三、目录结构
readme.txt                 # 本说明文档
源程序代码1，2，3，4题.ipynb        # 问题求解程序
附件/                      # 赛题输入附件1‑4.xlsx
C题微网调控_公式源码.tex         # 论文全部数学公式LaTeX源码
AI工具使用详情.pdf         # AI工具使用情况说明

四、运行方法
解压后在命令行进入本包根目录，执行：

# 问题一
python run_q1_reproduce.py --data-dir 附件 --output-dir q1_output

# 问题二
python run_q2_reproduce.py --data-dir 附件 --output-dir q2_output

# 问题三
python run_q3_reproduce.py --data-dir 附件 --output-dir q3_output

# 问题四
python reproduce_q4.py --data-dir 附件 --output-dir recomputed_results

说明：
1. --data‑dir 指定存放赛题Excel附件的文件夹；输出文件夹会自动创建。
2. 程序仅读取输入文件，不会修改原始附件。
3. 问题二、三、四为365天逐日滚动计算，运行耗时取决于电脑性能。
4. Mac/Linux环境请把命令中的 python 替换为 python3。

五、输出说明
运行后结果生成在对应 --output‑dir 文件夹内，包含json核验文件、csv时段结果。
output_sample目录仅存放部分代表性结果样例；完整结果运行上面的代码即可生成。

六、精度与模型说明
1. 计算全程使用双精度，中间过程不做舍入；论文展示数值保留两位小数。
2. 本模型属于线性规划，存在多重最优解：在总费用一致的情况下，逐时段充放电计划可能不同。
3. 每个程序自带独立数值核验，输出的*_checks.json记录残差，残差小于1e‑6代表求解可行。

七、其他
1. 包内所有文件均已匿名，不含学校、队员个人信息。
2. 全部输入数据均来自赛题提供的附件。
3. 详细计算口径，参见论文附录。

