# 快捷键

| 按键               | 功能                                                          |
| ---------------- | ----------------------------------------------------------- |
| x                | 删除                                                          |
| shift + a        | 新建物体                                                        |
| shift + MM       | 移动视图                                                        |
| MM               | 旋转试图                                                        |
| rolling + MM     | 缩放 zoom                                                     |
| G/R/S            | 移动/旋转/缩放                                                    |
| ALT + G/R/S      | 复位 移动/旋转/缩放                                                 |
| N                | 打开侧边栏                                                       |
| 小键盘“.”           | 框选选中物体                                                      |
| shift + D        | 复制物体                                                        |
| tab              | 进入编辑模式                                                      |
| E/alt + e        | 挤出命令/挤出菜单                                                   |
| shift + s        | 控制游标                                                        |
| shift + c        | 游标复位                                                        |
| shift + mr       | 移动游标                                                        |
| F                | 填充                                                          |
| z                | 进入shading菜单                                                 |
| alt+z            | 进入透选（toggle x-ray）模式(由于alt + z与nvidia按键冲突，改为ctrl + alt + z) |
| o                | 衰减编辑                                                        |
| ctrl + a         | application                                                 |
| g+g              | 延边移动顶点                                                    |
| ctrl + tab       | 模式选择                                                        |
| ctrl + x         | 删除连线（融并命令）                                                  |
| p                | 分离模型                                                        |
| ctrl + j         | 合并模型                                                        |
| /                | 独立显示                                                        |
| ctrl + v         | 顶点命令组                                                       |
| ctrl + shift + b | 顶点倒角                                                        |
| v                | 断开顶点                                                        |
| j                | 链接两个顶点                                                      |
| m                | 焊接，不在vertex选项中，在mesh选项中 (merge)                             |
| ctrl + e         | 边的命令组，细分、反细分、桥接、环切                                          |
| ctrl + f         | 面的命令组                                                       |
| F9               | 调整物体参数（在下一个操作之前有效）                                          |
| ctrl + i         | 反选                                                          |
| alt + m          | 拆分：mesh->split                                              |
| alt + n          | 法线操作                                                        |
| alt + s          | 编辑模式下，延法线缩放                                                       |
| k                | 使用 knife 工具时，按住 c 实现透切，可以穿过整个对象。 |
|编辑模式 L         | 按下 L 键后，Blender 会自动选择与当前选定元素相连的所有元素|
|编辑模式 shift/alt + h| 隐藏/显示 未选中的顶点或面|

Mesh、Curve 之间的转换：MR -> Convert To -> mesh/Curve

缩放 + 0 可以拉平

# 常用格式&工作流程

常用二维图像格式：

Jpg 有损压缩    不支持透明通道

Png 无损压缩    支持透明通道

Exr 分层通道    可以提取各个通道图层

Blender 做好模型后，渲染的并不是一个视频，而是一张图片，由这一张张图片在后期制作软件里面合成视频。

常用格式：

OBJ：是一种模型文件，不包含动画、材质等信息。

FBX：支持 3D 模型、材质、动画

GLB：支持 3D 模型、材质、动画

ABC：支持烘焙模型、流体、动画、特效等数据，因此可能无法进行修改

基本工作流程：

1、制作模型

2、为模型添加材质

3、添加灯光以及氛围

4、渲染

# 常用网址和插件地址

模型：Bridge    sketchfab 莫顿网 PBRMAX

HDR/贴图：Bridge、PolyHaven、textures.com

图片：花瓣网

音效：爱给网

常用软件下载地址：羽兔网

AE插件下载地址：Look AE

曲线插件：extra curve objects


# 样条曲线
 1. 建模
    
    挤出、倒角

 2. 动画
    
    动画轨迹

 3. 修改与编辑

    手绘

    钢笔 ML 额外加点    ctrl + ML 原有曲线上加点

    挤出 e

    缩放 alt + S

    切变

    随机

 4. 曲线顶点类型

    编辑模式下：
    Control points -> set handle type (快捷键：v)
    shift + n 曲线平滑


#  粒子系统
粒子系统
粒子毛发


# 渲染
Cycles 渲染器，速度慢，效果真实

Eevee 速度快，真实性欠佳