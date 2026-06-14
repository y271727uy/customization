---
layout: default
title: 魔改模组概述
permalink: /pages/overview/
---

# 魔改模组概述
当前 Minecraft 整合包和模组中魔改模组是常见的内容。而根据使用难度和作用能力我将其分为以下几档：

- Tier 1：基于原版的魔改
- Tier 2：基于模组本体的魔改
- Tier 3：基于第三方模组的魔改
- Tier 4：基于脚本语言的魔改
- Tier 5：基于复杂魔改框架的魔改
- Tier 6：基于极复杂的魔改模组进行魔改
- Tier 7：基于 Forge/Fabric 加载器提供的 Mixin 与 coremod 的魔改

### 基于原版的魔改

原版 Minecraft 提供了一套强大的数据包、资源包与一般用于服务器的配置文件。其中通过前两者的修改可以轻松实现魔改。

### 基于模组本体的魔改
与原版不同，很多模组在除了支持数据包与资源包魔改外，还会提供大量的配置文件。这些配置文件大多都在 minecraft/config 目录下。

### 基于第三方模组的魔改
某些模组作为独立的魔改模组，在其特定领域会有一些参考与使用价值。例如 Bad Mobs 可以通过配置文件进行对生物生成的控制。

### 基于脚本语言的魔改
脚本语言魔改是自定义程度相对更高的方法，代表模组有 KubeJS 与 CraftTweaker，前者使用 JavaScript，后者使用 ZenScript，对于初次接触来说上手门槛略高。此外，大量模组都为 KubeJS 与 CraftTweaker 开放了接口，可以使用封装好的方法进行魔改，同时也存在对其生态进行扩展的附属模组，例如 KubeJS 附属 LootJS、CraftTweaker 附属 ContentTweaker。

### 基于复杂魔改框架的魔改
此类模组有自己的 DSL、封装体系与复杂的点线图，功能强大但学习成本较高，通常需要对脚本魔改有一定基础后再上手。代表模组有 Multiblocked2 与模块化机械社区版（Modular Machinery: Community Edition）。

### 基于极复杂的魔改模组进行魔改
此类型的魔改模组数量相对较少，但功能强大，学习成本较高。此类型模组我个人认为有绷带（Hotai）、创可贴（Bansoukou）、保险库补丁（Vault Patcher）。
其中绷带（Hotai）与创可贴（Bansoukou）会替换字节码 class 文件，需要一定 Java 基础。而保险库补丁（Vault Patcher）用于替换与汉化硬编码语言键，相对复杂。此类型模组均易导致游戏崩溃。

### 基于 Forge/Fabric 加载器提供的 Mixin 与 coremod 的魔改
此类型魔改涉及 Java 语言，需要一定的基础，并需要进行 forge/fabric 模组开发。其中 Mixin 是现代更加推荐和优雅的注入手段，可以通过不同的注解去对类进行不同程度的修改。但是为了确保兼容性需要尽量避免使用 @Overwrite 注解。此外还存在 MixinSquared 这个 Mixin 库，用于"Mixin"进其他模组的 Mixin。   
CoreMod（核心模组）是基于 Forge 体系的一种机制，其核心能力是：在 Minecraft / Java 类被加载之前，直接修改字节码（bytecode），依赖 ASM 做复杂的字节码转换。CoreMod 在 1.12.2/1.7.10 版本较为流行，但随着 Mixin 生态的完善，CoreMod 已逐渐不再在高版本中被使用，并随着版本更新使用门槛正在逐步提升。此外 CoreModAPI 与 DangerAPI 在高版本提供了相对易用且暴力的 coremod 实现库。

[返回首页]({{ '/' | relative_url }})
