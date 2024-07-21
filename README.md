

This user guide is based on EvoMass __0\.3\.3__ and published on __Novermber 21, 2022__\.

本指引手册基于EvoMass 0\.3\.3版本，发布于2022年11月21日

Contents

[EvoMass User Guide 使用指引	1](#_Toc119937694)

[1\.	General Overview 总括	3](#_Toc119937695)

[1\.1\.	Installation 安装	3](#_Toc119937696)

[1\.2\.	Start your first run of using EvoMass 开始使用	4](#_Toc119937697)

[1\.3\.	Activation 激活	5](#_Toc119937698)

[1\.4\.	Learn how to use EvoMass 学习使用EvoMass	5](#_Toc119937699)

[1\.5\.	About this user guide 关于该指引	6](#_Toc119937700)

[2\.	Design Generation Part 1 \(Subtractive component\) 设计生成1（减法组件）	7](#_Toc119937701)

[2\.1\.	Basic setting 基本设定	7](#_Toc119937702)

[2\.1\.1\.	Initial Volume 初始体量	7](#_Toc119937703)

[2\.1\.2\.	Subtractor \(Voids\) 削减体（负空间）	8](#_Toc119937704)

[2\.1\.3\.	Boundary Constraint 边界约束	9](#_Toc119937705)

[2\.1\.4\.	Generate Cores 生成核心筒	10](#_Toc119937706)

[2\.1\.5\.	Target Gross Area 目标建筑面积	10](#_Toc119937707)

[2\.1\.6\.	Façade Types 立面类型	11](#_Toc119937708)

[2\.2\.	Advanced setting 高级设定	11](#_Toc119937709)

[2\.2\.1\.	Interfering point 干扰点	12](#_Toc119937710)

[2\.2\.2\.	Separation Control 分离控制	13](#_Toc119937711)

[2\.2\.3\.	Custom Boundary 自定义边界	13](#_Toc119937712)

[2\.2\.4\.	External Volume 外部体量	13](#_Toc119937713)

[2\.2\.5\.	Remove Small Mass 去除细碎体量	14](#_Toc119937714)

[2\.2\.6\.	Fixed Void 固定负空间	14](#_Toc119937715)

[2\.2\.7\.	Subtractor Appearing Position 削减体位置控制	14](#_Toc119937716)

[2\.3\.	Transformation Setting 变换设定	15](#_Toc119937717)

[2\.3\.1\.	Orientation 朝向	15](#_Toc119937718)

[2\.3\.2\.	Shear 切变	16](#_Toc119937719)

[2\.4\.	Generation setting 生成设定	17](#_Toc119937720)

[2\.4\.1\.	Scaling 缩放	17](#_Toc119937721)

[2\.4\.2\.	Display Boundary 显示边界	18](#_Toc119937722)

[2\.4\.3\.	Shuffle Range 随机变化范围	18](#_Toc119937723)

[2\.4\.4\.	Save/Load 保存/载入	19](#_Toc119937724)

[3\.	Design Generation Part 2 \(Additive component\) 设计生成2 （加法组件）	21](#_Toc119937725)

[3\.1\.	Basic setting 基本设定	21](#_Toc119937726)

[3\.1\.1\.	Spatial Boundary 空间边界	21](#_Toc119937727)

[3\.1\.2\.	Additive Unit Mass 叠加子体量	23](#_Toc119937728)

[3\.1\.3\.	Generate Cores 生成核心筒	24](#_Toc119937729)

[3\.1\.4\.	Target Gross Area 目标建筑面积	24](#_Toc119937730)

[3\.1\.5\.	Façade Types 立面类型	24](#_Toc119937731)

[3\.2\.	Advance setting 高级设定	24](#_Toc119937732)

[3\.2\.1\.	Interfering point 干扰点	25](#_Toc119937733)

[3\.2\.2\.	Separation Control 分离控制	26](#_Toc119937734)

[3\.2\.3\.	Custom Boundary 自定义边界	26](#_Toc119937735)

[3\.2\.4\.	External Volume 外部体量	26](#_Toc119937736)

[3\.2\.5\.	Vertical Constraint Check 垂直约束检查	27](#_Toc119937737)

[3\.2\.6\.	Fixed Void 固定负空间	27](#_Toc119937738)

[3\.2\.7\.	Unit Masses Appearing Position 子体量位置约束	27](#_Toc119937739)

[3\.3\.	Transformation 变换设定	27](#_Toc119937740)

[3\.4\.	Generation setting 生成设定	27](#_Toc119937741)

[4\.	Design Optimization 设计优化	28](#_Toc119937742)

[4\.1\.	Input/Output 输入/输出	28](#_Toc119937743)

[4\.1\.1\.	Connection 连接	28](#_Toc119937744)

[4\.1\.2\.	Outputs 输出	29](#_Toc119937745)

[4\.1\.3\.	Inputs 输入	30](#_Toc119937746)

[4\.2\.	SSIEA setting SSIEA算法设置	30](#_Toc119937747)

[4\.3\.	Optimization Viewer 优化窗口	33](#_Toc119937748)

[4\.3\.1\.	Main Viewer 主窗口	33](#_Toc119937749)

[4\.3\.2\.	Improvement Viewer 改进解窗口	34](#_Toc119937750)

[4\.3\.3\.	Information Viewer 信息窗口	35](#_Toc119937751)

[4\.4\.	Data Backup 数据备份	36](#_Toc119937752)

[4\.5\.	Restart/Load Optimization 重新开始/载入优化	38](#_Toc119937753)

# <a id="_Toc119937695"></a>General Overview 总括

EvoMass is an integrated building massing design generation and optimization tool, primarily aimed at performance\-based architectural design\. Instead of focusing purely on numerical optimization, the application of EvoMass is aimed to support optimization\-based design exploration, where the optimization helps designers to extract design information, understand the design implications related to building performance, and synthesize the information into the ideation and conceptual development process\.

EvoMass是一个一体化的建筑体量设计生成及优化工具。该工具主要帮助设计师进行进行性能的建筑设计。与其他设计优化工具有所不同，EvoMass的应用旨在帮助设计师进行基于优化的设计探索，即通过优化帮助设计师提取与性能相关的设计信息和理解设计问题，并最终能够将这些设计信息融入到设计构思和推敲过程之中。

In EvoMass, there are two major parts, including design generation and optimization\. For design generation, there are two components that encode the additive and subtractive form generation principles, which can create building massing designs with significant design differentiation and diversity\. For design optimization, there is a component implementing a hybrid evolutionary algorithm called SSIEA \(steady\-state island evolutionary algorithm\)\. SSIEA is aimed to diversify the design population to increase the diversity in the optimization result by using an island\-based approach while speeding up the optimization process by using the steady\-state replacement strategy\. 

EvoMass中的组件包含设计生成和优化两部分。在设计生成部分，其包含两个基于“减法”和“加法”的建筑体量形态生成器，这两个生成器能够生成具有显著差异性和多样性的体量形态。在优化部分，其包含一个基于多岛模型和稳态替换策略的进化式算法（SSIEA算法）。该算法具有较高的搜索效率，同时输出的优化结果也较标准遗传算法有更高的多样性。

The combination of the design generation and optimization component as well as other simulation tools such as Ladybugs and ClimateStudio, allows designers to swiftly define the building form and optimization objective and then conduct the optimization\. The optimization result serves as a medium of reflection that aims to help designers identify design patterns and implications related to building performance\.

上述两部分算法，和其他建筑性能模拟工具，如Ladybugs和ClimateStudio，的结合可以使设计师快速的对设计生成和优化进行定义，并进行对应的设计优化。设计优化的结果可以帮助设计师发现设计中潜在特征和趋势，并以此作为一种对设计问题进行考察和反思的媒介。

## <a id="_Toc119937696"></a>Installation 安装

To install EvoMass, simply drag the gha file to the Grasshopper canvas, or replace the old one in the component folder if you already installed it\. Remember to __unblock__ the gha if you cannot find EvoMass on the Grasshopper tab as shown below\.

安装EvoMass，仅需将相应的gha文件拖入Grasshopper界面，或替换在组件文件夹中原有的gha文件即可。如果在完成上述操作后，在工具栏中未出现EvoMass相关标签，请检查gha文件是否已经检索（右击gha文件\-属性第一栏最下部）。
