# 以Construct2制作'Ghost Shooter'演示游戏

![游戏演示](C:\Users\14347\Desktop\新建文件夹\liuxt-homework\游戏演示1.gif)


## 1.安装*Construct2*

点击[此处](https://www.scirra.com/construct2/releases/r262)获取最新版本的Construct 2的副本。

## 2.入门

启动Construct 2.单击File按钮，然后选择New。

![1](https://www.scirra.com/images/articles/filenew.png)

您将看到“模板或示例”对话框。这会显示您可以随意调查的示例和模板列表。现在，只需单击框底部的“打开”即可创建
一个空白的空项目。

![2](https://www.scirra.com/images/articles/newprojdialog65.png)

## 3.插入对象

### 插入背景

我们想要的第一件事是重复的背景图块。该平铺背景对象可以为我们做到这一点。首先，这是你的背景纹理 - 右键单击​​它并将其保存到你的计算机某处：

![Background](https://www.scirra.com/images/articles/bg.png)

现在，双击布局中的空格以插入新对象。出现*Insert New Object*对话框后，双击*Tiled Background*将其插入。
此后将出现一个十字准线，指示放置对象的位置。单击布局中间附近的某个位置。在纹理编辑器会立即打开，你输入的纹理瓷砖。让我们导入您之前保存的图块图像。单击文件夹图标以从磁盘加载纹理，找到将文件下载到的位置，然后选择它。
单击右上角的X关闭纹理编辑器。如果系统提示您，请务必保存！现在，您应该在布局中看到平铺的背景对象。让我们调整它以覆盖整个布局。确保选中它，然后左侧的属性栏应显示对象的所有设置，包括其大小和位置。将其位置设置为0,0（布局的左上角），并将其大小设置为1280,1024（布局的大小）。

![3](https://www.scirra.com/images/articles/tiledproperties.png)

### 添加图层

管理图层，请单击*Layers*选项卡，该选项卡通常位于*Projects*栏旁边。

单击铅笔图标并将第0层重命名为Background，因为它是我们的背景图层。现在单击绿色的“添加”图标为我们的其他对象添加新图层。我们称之为一个Main。最后，如果单击“ 背景”旁边的小挂锁图标，它将被锁定。这意味着您将无法选择任何内容。这对我们的平铺背景非常方便，这很容易被意外选择，不需要再次触摸。但是，如果您需要进行更改，只需再次单击挂锁即可解锁。现在，**确保在图层栏中选择了“Main”图层**。

### 添加输入对象

双击以插入另一个新对象。这次，选择Mouse对象，因为我们需要鼠标输入。对Keyboard对象再次执行相同操作。现在我们项目中的所有布局都可以接受鼠标和键盘输入。

### 添加游戏对象


![Player](https://www.scirra.com/images/articles/player.png)

![Monster](https://www.scirra.com/images/articles/monster.png)

![Bullet](https://www.scirra.com/images/articles/Bullet.png)

![Explosion](https://www.scirra.com/images/articles/explode.png)

双击以插入新对象，双击 “Sprite”对象。当鼠标变为十字准线时，单击布局中的某个位置。工具提示应为“Main”。（请记住这是活动布局。）弹出纹理编辑器。单击打开图标，然后加载四个纹理中的一个。关闭纹理编辑器，保存更改。

将子弹和爆炸精灵移动到布局边缘的某个位置 - 我们不希望在游戏开始时看到它们。

这些对象将被称为Sprite，Sprite2，Sprite3和Sprite4。根据需要将它们重命名为Player，Monster，Bullet和Explosion。您可以通过选择对象，然后更改属性栏中的Name属性来执行此操作。

## 添加行为


### 如何添加行为


让我们为Player添加*8 Direction*行为。单击播放器以选择它。在属性栏中，请注意“ 行为”类别。单击“ 添加/编辑”。播放器的“行为”对话框将打开。

![4](https://www.scirra.com/images/articles/openbehaviors.png)

单击行为对话框中的绿色“添加行为”图标。双击8方向移动以添加它。再次执行相同操作，这次添加*Scroll To*行为，使屏幕跟随播放器，以及绑定到布局行为，以使它们保持在布局中。

### 添加其他行为


我们可以通过相同的方法向其他对象添加行为 - 选择它，单击添加/编辑以打开行为对话框，并添加一些行为。让我们添加其他行为：

- 将*Bullet*和*Destroy outside layout*添加到Bullet对象

- 将*Bullet*添加到Monster对象

- 将*Fade*添加到Explosion对象

- 选择Monster对象。请注意，自从我们添加了一个行为后，属性栏中出现了一些额外的属性：

![5](https://www.scirra.com/images/articles/bulletproperties.png)

将速度从400更改为80（这是以每秒行进的像素数为单位）。
同样，将Bullet对象的速度更改为600，将Explosion对象的淡入淡出行为的淡出时间更改为0.5（即半秒）。

## 添加更多怪物


按住控件，单击并拖动Monster对象。你会注意到它产生了另一个对象。使用control + drag，创建7或8个新怪物。不要放置太靠近玩家，否则他们可能会立即死亡！

## 添加事件


事件由条件，行动和子事件（本次未用到）组成。

### 添加条件


- 单击顶部的“ 事件表1”选项卡以切换到“ 事件”表编辑器。事件列表称为事件表，您可以为游戏的不同部分或组织设置不同的事件表。

- 双击事件表中的空格。不同的对象具有不同的条件和动作，这取决于它们可以做什么。

- 双击 System对象。

- 双击的*Every tick*的条件，将其插入。对话框将关闭并创建事件，不执行任何操作。

![6](https://www.scirra.com/images/articles/everytickempty.png)


### 添加行动


- 现在我们要添加一个动作让玩家看鼠标。单击事件右侧的“ 添加操作”链接。（确保您获得添加操作链接，**而不是其下方的添加事件链接**）

- 与添加条件一样，我们有相同的对象列表可供选择，但这次是添加行动。双击Player对象。

- 双击*Set angle towards position*。

- 输入Mouse.X为X，和Mouse.Y为y以将角度设置为鼠标位置。

### 进行同样的操作添加其他游戏行为：

- 条件：Mouse -> On click -> Left clicked 
行为: Player -> Spawn another object -> Bullet  将图层保存为第一层，图像点保存为0.

- 条件：Bullet -> On collision with another object -> Monster.
行为：Monster -> Destroy
    Bullet -> Spawn another object -> Explosion, layer 1
    （为去除Explosion的黑色边框，单击右下角的对象栏中的Explosion对象，或单击项目栏（带有图层栏的选项卡）。其属性显示在左侧的属性栏中。在底部，将其Blend mode属性设置为Additive。）
    Bullet -> Destroy

- 条件: System -> On start of Layout
行为: Monster -> Set angle -> random(360)

- 条件: Monster -> Is outside layout
行为：Monster -> Set angle toward position -> For X, Player.X - for Y, Player.Y.


## 添加实例变量

假设我们想要在它死前五次射击怪物，而不是像现在这样瞬间死亡。我们怎么做？如果我们只存储一个“健康”计数器，那么一旦我们击中一个怪物五次，所有的怪物都会死亡。相反，我们需要每个怪物记住自己的健康。我们可以用实例变量做到这一点。

- 单击项目栏或对象栏中的怪物，这将在属性栏中显示怪物的属性。点击添加/编辑通过编辑变量。

- 在弹出的对话框中，键入health作为名称，将Type保留为Number，对于Initial value，输入5。这启动了5个生命中的每个怪物。当它们被击中时，我们将从健康状态中减去1，然后当健康状态为零时，我们将摧毁该物体。

- 完成后，单击“确定”。


## 改变事件

- 切换回事件表，找到事件： Bullet - on collision with Monster。请注意，我们有一个*destroy monster*动作。让我们用“从健康中减去1”来代替它。右键单击*destroy monster*操作，然后单击“ replace”。

![7](https://www.scirra.com/images/articles/replaceaction.png)

- 选择Monster - > Subtract from（在Instance variables category中）- > Instance变量“health”，并为Value输入1。单击完成。

- 现在，当我们射击怪物时，它们会失去1点生命值，子弹会爆炸，但是当它们的生命值达到零时，我们还没有杀死怪物。添加另一个事件：
条件: Monster -> Compare instance variable -> Health, Less or equal, 0
行为: Monster -> Spawn another object -> Explosion, layer 1
      Monster -> Destroy


## 设置得分

- 右键单击事件表底部的空间，然后选择“ 添加全局变量”。

- 输入Score作为名称，它将使其成为从0开始的数字。现在，全局变量在事件表中显示为一行。它位于此事件表中，但可以从任何布局中的任何事件表访问它。

![8](https://www.scirra.com/images/articles/globalscorevar.png)

- 在“Monster：health less or equal 0”事件中（当怪物死亡时），单击Add action，然后选择System - > Add to- > Score，value 1

![9](https://www.scirra.com/images/articles/scoreeevent.png)

## 设置抬头显示器

- 双击空格以插入另一个对象。这次选择Text对象。将其放在布局的左上角。很难看出它是否是黑色的，所以在属性栏中，使其变为粗体，斜体，黄色，并选择稍大的字体大小。将其大小调整到足以容纳合理数量的文本。

![10](https://www.scirra.com/images/articles/textinlayout.png)

- 切换回事件表。让我们用播放器的分数更新文本。在我们之前添加的Every tick事件中，添加操作Text - > Set text。

- 使用＆运算符，我们可以将数字转换为文本并将其连接到另一个文本字符串。因此，对于文本，请输入：
**"Score: " & Score**

## 完成接触

- 添加事件使Monster数量定时自动增加：
Condition: System -> Every X seconds -> 3
Action: System -> Create object -> Monster, layer 1, 1400 (for X), random(1024) (for Y)

- 添加事件杀死Player：
Condition: Monster -> On collision with another object -> Player
Action: Player -> Destroy 

**游戏制作完成！**














