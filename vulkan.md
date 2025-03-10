# 渲染管线

![](./Assets/img/vulkan/vulkan_simplified_pipeline.svg)

1. 输入装配器（input assembler）

从我们指定的 buffers 中获取原始的顶点数据，也可以使用顶点缓冲来重复某一些元素，而不是必须复制顶点数据本身。

2. 顶点着色器（vertex shader）

顶点着色器逐个的处理每个顶点，并执行旋转，平移等变换。通常会应用变换将顶点位置从模型空间转换为屏幕空间。它还会将每个顶点的数据传递到管道中。

3. 曲面细分（tessellation shaders）

允许我们依据某些规则去细分我么的一个几何体，以增加网格（mesh）质量。

4. 几何着色器（geometry shaders）

几何着色器在每个图元（primitive）（三角形、线段、点）上运行，可以丢弃图元或者输出比输入更多的图元。这与细分着色器类似，但灵活性更高。然而，在如今的应用程序中，他的使用并不多。

5. 光栅化（rasterization）

将每个图元（primitive）离散化成片段（fragment）。这些片段是它们在帧缓冲区中填充的像素元素。任何超出屏幕的片段都会被丢弃，顶点着色器输出的属性会在片段之间进行插值，如图所示。通常，位于其他图元片段后面的片段也会在此处被丢弃，这是由于深度测试的原因。

6. 片段着色器（fragment shader）

片段着色器会对每个存活的片段进行调用，并确定这些片段写入哪个帧缓冲区，以及使用什么颜色和深度值。它可以利用来自顶点着色器的插值数据来完成这一操作，这些数据可以包括纹理坐标和用于光照的法线等信息。

7. 颜色混合（color blending）

混合映射到帧缓冲中相同像素的不同片段。片段之间可以简单的复写、相加或透视混合。

绿色阶段称为固定功能阶段。这些阶段允许您使用参数调整其操作，但它们的工作方式是预定义的。

橙色阶段是可编程阶段。我们可以上传我们的代码到显卡上，以实现我们想要的操作。例如，我们可以使用片段着色器实现从纹理和光线追踪等任何功能。这些程序同时在多个gpu核心上运行。例如顶点和片段。

# Device