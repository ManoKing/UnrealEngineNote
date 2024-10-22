最顶层是Engine目录以及您所拥有的任何游戏项目。Engine目录包含引擎本身以及所有随附工具。每个游戏文件夹包含与该游戏有关的所有文件。与先前版本的引擎相比，UE4中的引擎和游戏项目有了更明显的区分。

### 根目录
Engine——包含构成引擎的所有源代码、内容等。

Templates——创建新项目时可用的项目模板集合。

GenerateProjectFiles.bat——用于创建在Visual Studio中使用引擎和游戏所需的UE4解决方案和项目文件。请参阅IDE的项目文件以了解详细信息。

UE4Games.uprojectdirs——这是帮助文件，用于帮助引擎发现位于子目录中的项目。

### 通用目录
一些子目录是在引擎和游戏项目目录之间通用的：

Binaries——包含可执行文件或编译期间创建的其他文件。

Build——包含构建引擎或游戏所需的文件，包括创建特定于平台的构建版所需的文件。

Config——配置文件，用于设置用来控制引擎行为的值。游戏项目Config文件中设置的值会覆盖 Engine\Config 目录中设置的值。

Content——保存引擎或游戏的内容，包括资源包和贴图。

DerivedDataCache——包含加载时针对引用内容生成的派生数据文件。引用内容没有相应的缓存文件会导致加载时间显著延长。

Intermediate——包含构建引擎或游戏时生成的临时文件。在游戏目录中，着色器存储在Intermediate目录中。

Saved——包含自动保存、配置（.ini）文件和日志文件。此外，Engine > Saved 目录还包含崩溃日志、硬件信息和Swarm选项与数据。

Source——包含引擎或游戏的所有源文件，包括引擎源代码、工具和游戏类等。

Engine——Engine目录中的源文件组织结构如下：

Developer——编辑器和引擎共同使用的文件。

Editor——仅供编辑器使用的文件。

Programs——引擎或编辑器使用的外部工具。

Runtime——仅供引擎使用的文件。

Game——游戏项目目录中的源文件按模块分组，一个模块一个目录。每个模块包含以下内容：

Classes——包含所有游戏类标头（.h）文件。

Private——包含所有 .cpp 文件，包括游戏类实现文件和模块实现文件。

Public——包含模块标头文件。

### 特定于引擎的目录
部分子目录特定于Engine目录。

Documentation——包含引擎文档，包括源文件和发布的文件。

HTML——发布的HTML文档文件。

Source——源markdown文档文件。

Extras——其他帮助和实用程序文件。

Plugins——包含引擎中使用的插件。

Programs——包含UE4根目录中存储的项目以及其他虚幻程序（如UnrealFrontend和UnrealHeaderTool）的配置文件和日志文件。

Shaders——保存引擎的着色器源文件（.usf）。

##游戏项目目录
目录   说明

Binaries

包含可执行文件或编译期间创建的其他文件。

Config

游戏的默认项目设置。

Content

包含引擎或游戏的内容，包括资源包和贴图。

External dependencies

显示公共引擎标头文件（仅在Visual Studio中可见）。

Intermediate

包含UnrealBuildTool生成的文件，如Visual Studio项目文件。这些文件可以删除并重新构建。

Saved

包含引擎生成的文件，如配置文件和日志。这些文件可以删除并重新构建。

Source

包含游戏模块对象类文件。

### 解决方案目录
目录    说明

Classes

包含游戏对象类定义（.h 文件）。

Config

游戏的默认项目设置。

External dependencies

显示公共引擎标头文件（仅在Visual Studio中可见）。

Private

包含私有游戏对象类实现文件（.cpp 文件）。

Public

包含公共游戏对象类实现文件（.cpp 文件）。