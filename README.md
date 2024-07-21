
# <a name="_toc119937694"></a>EvoMass User Guide 使用指引
This user guide is based on EvoMass **0.3.3** and published on **Novermber 21, 2022**.

本指引手册基于EvoMass 0.3.3版本，发布于2022年11月21日
# Contents
[EvoMass User Guide 使用指引	1](#_toc119937694)

[1.	General Overview 总括	3](#_toc119937695)

[1.1.	Installation 安装	3](#_toc119937696)

[1.2.	Start your first run of using EvoMass 开始使用	4](#_toc119937697)

[1.3.	Activation 激活	5](#_toc119937698)

[1.4.	Learn how to use EvoMass 学习使用EvoMass	5](#_toc119937699)

[1.5.	About this user guide 关于该指引	6](#_toc119937700)

[2.	Design Generation Part 1 (Subtractive component) 设计生成1（减法组件）	7](#_toc119937701)

[2.1.	Basic setting 基本设定	7](#_toc119937702)

[2.1.1.	Initial Volume 初始体量	7](#_toc119937703)

[2.1.2.	Subtractor (Voids) 削减体（负空间）	8](#_toc119937704)

[2.1.3.	Boundary Constraint 边界约束	9](#_toc119937705)

[2.1.4.	Generate Cores 生成核心筒	10](#_toc119937706)

[2.1.5.	Target Gross Area 目标建筑面积	10](#_toc119937707)

[2.1.6.	Façade Types 立面类型	11](#_toc119937708)

[2.2.	Advanced setting 高级设定	11](#_toc119937709)

[2.2.1.	Interfering point 干扰点	12](#_toc119937710)

[2.2.2.	Separation Control 分离控制	13](#_toc119937711)

[2.2.3.	Custom Boundary 自定义边界	13](#_toc119937712)

[2.2.4.	External Volume 外部体量	13](#_toc119937713)

[2.2.5.	Remove Small Mass 去除细碎体量	14](#_toc119937714)

[2.2.6.	Fixed Void 固定负空间	14](#_toc119937715)

[2.2.7.	Subtractor Appearing Position 削减体位置控制	14](#_toc119937716)

[2.3.	Transformation Setting 变换设定	15](#_toc119937717)

[2.3.1.	Orientation 朝向	15](#_toc119937718)

[2.3.2.	Shear 切变	16](#_toc119937719)

[2.4.	Generation setting 生成设定	17](#_toc119937720)

[2.4.1.	Scaling 缩放	17](#_toc119937721)

[2.4.2.	Display Boundary 显示边界	18](#_toc119937722)

[2.4.3.	Shuffle Range 随机变化范围	18](#_toc119937723)

[2.4.4.	Save/Load 保存/载入	19](#_toc119937724)

[3.	Design Generation Part 2 (Additive component) 设计生成2 （加法组件）	21](#_toc119937725)

[3.1.	Basic setting 基本设定	21](#_toc119937726)

[3.1.1.	Spatial Boundary 空间边界	21](#_toc119937727)

[3.1.2.	Additive Unit Mass 叠加子体量	23](#_toc119937728)

[3.1.3.	Generate Cores 生成核心筒	24](#_toc119937729)

[3.1.4.	Target Gross Area 目标建筑面积	24](#_toc119937730)

[3.1.5.	Façade Types 立面类型	24](#_toc119937731)

[3.2.	Advance setting 高级设定	24](#_toc119937732)

[3.2.1.	Interfering point 干扰点	25](#_toc119937733)

[3.2.2.	Separation Control 分离控制	26](#_toc119937734)

[3.2.3.	Custom Boundary 自定义边界	26](#_toc119937735)

[3.2.4.	External Volume 外部体量	26](#_toc119937736)

[3.2.5.	Vertical Constraint Check 垂直约束检查	27](#_toc119937737)

[3.2.6.	Fixed Void 固定负空间	27](#_toc119937738)

[3.2.7.	Unit Masses Appearing Position 子体量位置约束	27](#_toc119937739)

[3.3.	Transformation 变换设定	27](#_toc119937740)

[3.4.	Generation setting 生成设定	27](#_toc119937741)

[4.	Design Optimization 设计优化	28](#_toc119937742)

[4.1.	Input/Output 输入/输出	28](#_toc119937743)

[4.1.1.	Connection 连接	28](#_toc119937744)

[4.1.2.	Outputs 输出	29](#_toc119937745)

[4.1.3.	Inputs 输入	30](#_toc119937746)

[4.2.	SSIEA setting SSIEA算法设置	30](#_toc119937747)

[4.3.	Optimization Viewer 优化窗口	33](#_toc119937748)

[4.3.1.	Main Viewer 主窗口	33](#_toc119937749)

[4.3.2.	Improvement Viewer 改进解窗口	34](#_toc119937750)

[4.3.3.	Information Viewer 信息窗口	35](#_toc119937751)

[4.4.	Data Backup 数据备份	36](#_toc119937752)

[4.5.	Restart/Load Optimization 重新开始/载入优化	38](#_toc119937753)



24

1. # <a name="_toc119937695"></a>General Overview 总括
EvoMass is an integrated building massing design generation and optimization tool, primarily aimed at performance-based architectural design. Instead of focusing purely on numerical optimization, the application of EvoMass is aimed to support optimization-based design exploration, where the optimization helps designers to extract design information, understand the design implications related to building performance, and synthesize the information into the ideation and conceptual development process.

EvoMass是一个一体化的建筑体量设计生成及优化工具。该工具主要帮助设计师进行进行性能的建筑设计。与其他设计优化工具有所不同，EvoMass的应用旨在帮助设计师进行基于优化的设计探索，即通过优化帮助设计师提取与性能相关的设计信息和理解设计问题，并最终能够将这些设计信息融入到设计构思和推敲过程之中。

In EvoMass, there are two major parts, including design generation and optimization. For design generation, there are two components that encode the additive and subtractive form generation principles, which can create building massing designs with significant design differentiation and diversity. For design optimization, there is a component implementing a hybrid evolutionary algorithm called SSIEA (steady-state island evolutionary algorithm). SSIEA is aimed to diversify the design population to increase the diversity in the optimization result by using an island-based approach while speeding up the optimization process by using the steady-state replacement strategy. 

EvoMass中的组件包含设计生成和优化两部分。在设计生成部分，其包含两个基于“减法”和“加法”的建筑体量形态生成器，这两个生成器能够生成具有显著差异性和多样性的体量形态。在优化部分，其包含一个基于多岛模型和稳态替换策略的进化式算法（SSIEA算法）。该算法具有较高的搜索效率，同时输出的优化结果也较标准遗传算法有更高的多样性。

The combination of the design generation and optimization component as well as other simulation tools such as Ladybugs and ClimateStudio, allows designers to swiftly define the building form and optimization objective and then conduct the optimization. The optimization result serves as a medium of reflection that aims to help designers identify design patterns and implications related to building performance.

上述两部分算法，和其他建筑性能模拟工具，如Ladybugs和ClimateStudio，的结合可以使设计师快速的对设计生成和优化进行定义，并进行对应的设计优化。设计优化的结果可以帮助设计师发现设计中潜在特征和趋势，并以此作为一种对设计问题进行考察和反思的媒介。

1. ## <a name="_toc119937696"></a>Installation 安装
To install EvoMass, simply drag the gha file to the Grasshopper canvas, or replace the old one in the component folder if you already installed it. Remember to **unblock** the gha if you cannot find EvoMass on the Grasshopper tab as shown below.

安装EvoMass，仅需将相应的gha文件拖入Grasshopper界面，或替换在组件文件夹中原有的gha文件即可。如果在完成上述操作后，在工具栏中未出现EvoMass相关标签，请检查gha文件是否已经检索（右击gha文件-属性第一栏最下部）。

If a **loading error** shows up during you start Rhino, you will need to type in “GrasshopperDeveloperSettings” in the Rhino command line and disable the first option as shown below.

如果安装EvoMass后，出现了下图左中的加载错误，可以在Rhino中键入“GrasshopperDeveloperSettings”，并取消第一个选项（下图右）。

|||
| - | - |

1. ## <a name="_toc119937697"></a>Start your first run of using EvoMass 开始使用
Running EvoMass is easy, there are several examples provided along with the installation zip file. Simply open one of these examples as shown below, and follow the instructions to define the formal feature of the generated building massing design, design context, optimization objectives, and finally, the parameter of SSIEA. **Note that, Ladybugs need to be first installed on your Grasshopper to run these examples.**

为了帮助使用者快速熟悉EvoMass的操作，在下载的压缩包中提供了多个示例文件。使用这些示例文件（下图），只需跟随上面的指引，对生成参数、场地环境和优化参数进行定义后，便可以运行优化过程。注意，运行这些案例需安装Ladybugs。

1. ## <a name="_toc119937698"></a>Activation 激活
When installing EvoMass for the first time, there are 500 trial runs along with the installation. After that, you will need to apply for the activation code to continue using EvoMass. The application of the activation code is free for the moment, and there will be 5000 additional runs added up to your computer. For application, please use these links: [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSf4fYlOATW2Tp3zp6Y9nZynsCx-ZF_2wWzX7xCrRFTzW4x2Jw/viewform) and [腾讯表格](https://docs.qq.com/form/edit/DVGp4VHVGeFpRelN3#/fill), and you will receive an email with the action code soon. The below image shows you how to activate EvoMass on your computer.

第一次安装EvoMass后，将有500次操作次数。随后则需要申请激活码获得更多的操作次数。目前每次激活码申请将获得10000次的操作次数。请使用以下链接申请激活码: [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSf4fYlOATW2Tp3zp6Y9nZynsCx-ZF_2wWzX7xCrRFTzW4x2Jw/viewform) 和 [腾讯表格](https://docs.qq.com/form/edit/DVGp4VHVGeFpRelN3#/fill), 激活码会尽快发至申请中的邮箱。下图为输入激活码的流程。


1. ## <a name="_toc119937699"></a>Learn how to use EvoMass 学习使用EvoMass
Apart from the provided examples, there are several tutorials uploaded to [YouTube](https://youtu.be/DG_VkFP1jB8) and [Bilibili](https://www.bilibili.com/video/BV1w3411C79K?share_source=copy_web). In addition, a couple of research papers also published revolve around the application of EvoMass. You can find the link to these papers on the EvoMass page in Food4Rhino (<https://www.food4rhino.com/en/app/evomass>) as shown below. **It is strongly recommended to read some of these papers, as EvoMass is not a tool simply to produce building forms.**

除了随带的案例，在[YouTube](https://youtu.be/DG_VkFP1jB8) 和 [Bilibili](https://www.bilibili.com/video/BV1w3411C79K?share_source=copy_web) 也提供了影响的教程视频。此外，一些与EvoMass应用相关的研究文章也可以在Food4Rhino找到相关的链接。这些文章也可以帮助使用者更好地理解EvoMass在建筑设计中的应用潜力。

1. ## <a name="_toc119937700"></a>About this user guide 关于该指引
This user guide will take you walk through the major functions of EvoMass. Following this section, the two generative components are first elaborated, followed by the description of the evolutionary algorithm component (SSIEA).

本指引将引导使用者了解EvoMass的主要功能，在本节后，将会对两个生成算法进行介绍，之后再对优化算法进行介绍。


1. # <a name="_toc119937701"></a>Design Generation Part 1 (Subtractive component) 设计生成1（减法组件）
The subtractive component implements the subtractive form generation principle. This component generates building massing by creating several voids in a pre-defined spatial volume. By defining the size and position of the void, you can tailor the general formal feature of the generated building massing volume and make it satisfy your design intent. This section presents the major functions of this component.

减法组件以“减法”原则为核心，通过在一个预定义的体积中去除若干空间实现体量的生成。该组件可以通过对负空间的尺寸和位置进行控制，对生成体量的总体特征进行约束和干预，并以此满足不同的设计条件和意图。
1. ## <a name="_toc119937702"></a>Basic setting 基本设定
The basic setting panel of the subtractive component is shown below. In this panel, you can define the most important parameters that affect the formal features of the generated design, including the initial volume, number of voids, size constraint of voids, etc. Kindly remember to click the “**Set Parameter”** button once you have finished defining the parameters

减法组件的基本设定面包如下图所示。该面板包含了控制生成体量形态整体特征的主要参数，包括初始体量、负空间数量和尺寸等。在输入完成后，需按下“Set Parameter”以完成对设计生成的设定。

1. ### <a name="_toc119937703"></a>Initial Volume 初始体量
The initial volume lets you define the **type** of the generated building massing, such as high-rise towers or middle-rise complex buildings. In this component, the initial volume is horizontally defined by the column-grid numbers and the span size of the column gird and vertically defined by the number of floors and the floor height. In addition, you can define different span sizes in the two directions and the range of the floor numbers for achieving higher design flexibility.

初始体量帮助设计师对生成建筑的类型进行控制，如高层塔楼或多层综合体等。在该塑件中，初始体量有进深、开间和层数，以及柱间距和层高共同控制。同时柱间距提供了两个方向的尺寸调整，以实现更高的形态灵活性。

||||
| :-: | :-: | :-: |
||||
||||
||||

1. ### <a name="_toc119937704"></a>Subtractor (Voids) 削减体（负空间）
Subtractors are used to create the void in the initial volume. The **number** and **size** of the subtractor affect the **complexity** of the generated design. In the subtractive component, there are two types of subtractors: horizontal ones and vertical ones. Regarding horizontal subtractors, they are aimed to create features such as stilts, void decks, and sky gardens. Regarding vertical subtractors, they are aimed to create features such as courtyards and atriums. Therefore, you can set the number to 0 if you don’t want either of the two features appearing in the generated design. In addition, the **size** of the subtractor allows you to define how large the void will be in the generated design.

削减体用于在初始体量中生成负空间。不同的削减体数量和尺寸能够对生成设计的复杂度产生直接影响。减法组件包含水平和垂直两种削减体。前者用于生如架空空间、屋顶平台等水平向空间元素，后者主要生成如中庭、庭院等垂直向空间元素。所以，可以将任一一种的数量设置为0，如果设计师不希望在生成的体量中出现该类空间元素。此外，削减体的尺寸可以帮助设计师对负空间的大小进行干预。

||||
| :-: | :-: | :-: |
||||
||||
||||
||||
||||

1. ### <a name="_toc119937705"></a>Boundary Constraint 边界约束
In the subtractive component, the boundary constraint controls the horizontal position of all **vertical voids**. The purpose of the constraint is to allow users to decide how the vertical voids affect the overall building forms, especially whether or not the initial volume visually remains intact. There are different modes. For the first one, all voids are kept inside the volume, thus the boundary of the initial volume will be preserved. For the second one, all voids are kept on the edge of the boundary, which allows the building to have an L-shaped or U-shaped footprint or a staggering boundary. For the third one, there is no constraint on the voids, and the building can be cut into two or three parts.

在减法组件中，边界约束用于控制所有垂直削减体的水平位置。该约束可以帮助设计师更好地控制生成体量的可变范围，尤其是初始体量是否能被保存。目前提供了三种约束方式，第一种方式使所有的垂直削减体在初始体量中间，即初始体量的边界不会被破坏；第二种使垂直削减体在初始体量边界上，可以生成如L型或U型平面的建筑；第三种不对垂直削减体进行约束，可以生成更为自由的形体，如两个分开的体量。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_ref100776569"></a><a name="_ref100776589"></a><a name="_toc119937706"></a>Generate Cores 生成核心筒
This function is aimed to make the generated design more realistic by inserting cores for structural or circulation purposes. The core will affect the voids close to it. In addition, the core control distance defines the distance between the core boundary to the building's external façade surface or the corner.

该功能用于生成核心筒（交通或结构用途）以使生成的设计具有更高的实际参考价值。当使用该功能时，与核心筒相连的削减体会被影响。同时核心筒将会根据与建筑平面尺寸和外墙的距离自动进行数量和位置计算。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_ref100776596"></a><a name="_toc119937707"></a>Target Gross Area 目标建筑面积
This function allows you to define the rough volume of the building by using the **gross floor area**. When it is activated, it will cost more time to generate the building. In addition, please be aware that the component cannot guarantee the target GFA can be achieved under all circumstances, especially when there is a huge gap between the basic volume and the target GFA.

该功能使设计师可以通过建筑面积对生成体量的体积进行大致的控制。开启该功能会消耗更多的计算时间已完成设计生成。同时需要注意的时，该功能无法保证在所有情况下均输出接近目标建筑面积的设计，尤其是当生成建筑与目标建筑面积间面积差值较大时。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_ref100776572"></a><a name="_ref100776599"></a><a name="_toc119937708"></a>Façade Types 立面类型
When using different simulation tools, the required window geometry can be different. In the subtractive component, there are four types of façade types, including simple strip openings, simple fully glazed walls, window openings, and fully glazed walls. Please choose the appropriate type according to your project. 

不同的性能模拟工具往往需要不同的输入立面类型，因此减法组件提供了四种不同的立面类型，包括连续条形窗、连续落地窗、点窗和玻璃幕墙。请根据性能模拟工具的要求进行选择。

||||
| :-: | :-: | :-: |
||||
||||
||||

1. ## <a name="_toc119937709"></a>Advanced setting 高级设定
In the advanced setting, these parameters allow you to create a more complex building massing design or further navigate the generation process to tailor the formal features. These parameters are not mandatory and can be set as default in most cases.

高级设定包含了对生成更复杂体量形体的参数，以及可以更具体控制生成形体的参数。但这些参数在一般情况下并不需要进行设置。


1. ### <a name="_toc119937710"></a>Interfering point 干扰点
This function allows you to define a point to attract or repel the void to or from it. For example, you can use it to define an entrance area by attracting more voids to this area. When using this function, you need to first draw a point in **Rhino** instead of in Grasshopper and pick it after you click the “Set Point” button. In addition, positive values mean attraction, and negative values mean repulsion.

该功能需要设计师通过干扰点对削减体的位置进行干预。例如可以将削减体吸引至建筑的一侧或一角以生成入口空间。使用该功能需要在Rhino中生成干扰点，并单击“Set Point”键进行拾取。此外，正数值为吸引，负数值为排斥。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_toc119937711"></a>Separation Control 分离控制
This function allows you to define the closeness of the voids. If it is activated, the voids will be more separate from each other in the horizontal and/or vertical directions. 

该功能用于控制削减体间的紧密度。如果开启，削减体在垂直和/或水平方向上会相对分离。

|||
| :-: | :-: |
|||
|||
|||

1. ### <a name="_toc119937712"></a>Custom Boundary 自定义边界
This function allows you to define a more complex building footprint by delineating a closed **polyline** in **Rhino** rather than a curve in Grasshopper. The component will try to maintain the boundary constraint when you use this function.

该功能允许设计师生成具有更为复杂平面形状的建筑体量。目前该功能仅允许输入闭合的多段线。该多段线需要在Rhino中进行绘制，并拾取。此外，该功能会尽量满足在基础设置中的边界约束。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_ref100863042"></a><a name="_toc119937713"></a>External Volume 外部体量
This function allows you to define an external fixed volume and combine it with the generated design. The aim of this function is to enable a part of the building to be varied. For example, the tower (fixed) and the podium (variable).

该功能允许设计师在设计生成中加入一个固定不变的外部体量。该功能可用于仅需要一部分建筑可变的设计条件下，如塔楼不变，裙房可变。

||||
| :-: | :-: | :-: |

1. ### <a name="_toc119937714"></a>Remove Small Mass 去除细碎体量
This function allows you to remove masses that are too small. This function is useful when there is a no-boundary-constraint or a keep-vertical-voids-on-boundary.

该功能将自动去除生成体量中过小的体量。该功能仅在无边界约束或使所有垂直削减体在初始体量边界时有效。

|||
| :-: | :-: |
|||

1. ### <a name="_ref100863536"></a><a name="_toc119937715"></a>Fixed Void 固定负空间
This function allows you to define an invariable void in the initial volume, which can be considered as a courtyard or an L-shaped footprint. 

该功能用于在生成体量中加入一个不可变的负空间，例如一个中庭建筑或L型平面的建筑。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_ref100863612"></a><a name="_toc119937716"></a>Subtractor Appearing Position 削减体位置控制
This function allows you to define the vertical position that all horizontal voids can be generated. The aim of this function is to create a more specific type of building such as a building with stilts and cascading roofs.

该功能用于控制水平削减体在垂直方向的位置。该功能可以进一步精确定义生成设计的特征，如仅存在底层架空或屋顶平台等。

||||
| :-: | :-: | :-: |
||||

1. ## <a name="_ref100926323"></a><a name="_toc108516524"></a><a name="_toc119937717"></a><a name="_ref100926358"></a>Transformation Setting 变换设定
The tab of transformation contains functions that can achieve more complex morphological changes in the generated design.

该部分设置用于实现更复杂的形态变化。

1. ### <a name="_toc108516525"></a><a name="_toc119937718"></a>Orientation 朝向
This function allows you to change the orientation of the building by rotating the building based on its center point. The “Start” and “End” do not directly mean the starting and ending angle, and the rotation range is also affected by the “Step Size”. In this component, the range of rotation is from the starting value \* step size to the ending value \* step size. Therefore, if the starting value is -20 and the ending value is 15, and the step size is 2, these lead to the rotation range from -40 degrees to 30 degrees. In addition, it is not allowed the rotation range smaller than -90 degrees and larger than 90 degrees.

该功能通过旋转体量以改变建筑的朝向。旋转的起始（Start）和结束（End）并非为角度值，而是同时会收到旋转步长的影响。即旋转范围为“起始\*步长“至”结束\*步长“。例如，当起始值为-20，结束值为15，步长为2时，旋转范围为-40至30度。此外，旋转范围仅允许在-90至90度之间。

||||
| :-: | :-: | :-: |
||||

This function is more useful when combined with the custom boundary. When you define a custom boundary, the design can create buildings with a fixed footprint but the void can face different directions.

该功能也可与自定义边界结合使用。当存在自定义边界时，可以通过该功能探索不同朝向的削减体对建筑性能的影响。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_toc108516526"></a><a name="_toc119937719"></a>Shear 切变
This function allows you to easily make shear transformation of the generated building design. Note that the value set here will not be changed during the optimization process.

该功能可以对生成的建筑体量进行切变变换。请注意，所设定的参数，即切变角度，在优化过程不会改变。

||||
| :-: | :-: | :-: |
||||

1. ## <a name="_toc119937720"></a>Generation setting 生成设定
Generation setting allows you to control the generation of the design, such as scaling up the generated building, displaying the boundary, and controlling the range of design variation when shuffling the design.

生成设定帮助设计师对生成的建筑进行控制，例如缩放，显示边界，控制可变范围。

1. ### <a name="_toc119937721"></a>Scaling 缩放
Due to different simulation tools that may use different unit systems, this function allows you to scale up the building geometry.

由于不同的性能模拟软件采用不同的单位，该功能帮助设计师快速对生成的建筑进行缩放。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_toc119937722"></a>Display Boundary 显示边界
This function allows you to display the maximum volume of the generated design. The aim of this function is to help you detect whether the generated design collides with surrounding buildings. This function also works when the custom boundary is defined

该功能用于检查初始体量和自定义边界是否正确，尤其是是否与周边场地建筑存在冲突（如交叠）。

||||
| :-: | :-: | :-: |
||||

1. ### <a name="_toc119937723"></a>Shuffle Range 随机变化范围
This function allows you to control the variability when shuffling the design. This function is aimed to support more detailed and subtle design exploration based on an optimized design, and see whether there is a feasible design similar to the optimized design you select. When the shuffle range is below 100%, the current parameters for the generated design will be restored, and all the variations of the parameters will be conducted based on these restored parameters. If you want to use the parameters of the shuffled design as the basis point for design variation, you can click the “Update Massing” button, and the current parameters will be restored.

该功能用于控制体量随机变化时的可变范围控制。该功能用于针对所选择设计（一般为优化结果中分值较高的设计）进行进一步的细微变化探索。当该值小于100%时，当前设计的参数将被记录，并以此作为中心点进行参数的调整。如果希望以当前设计为中心点，请单击“Update Massing“。

||||
| :-: | :-: | :-: |
||||
||||
||||

1. ### <a name="_toc119937724"></a>Save/Load 保存/载入
This function allows you to save the setting you define as an external file and load it from another \*.gh file or computer. This function makes it easier to restore your setting and re-uses it by others or in other projects.

该功能可以将现有的参数设定（基本设定、高级设定和变换设定）保存为外部文件，并可以被其他gh文件中的相应组件（减法组件）载入。该功能帮助设计师更好地保存不同的生成参数设定，并被其他人或在其他项目总再次使用。


1.
