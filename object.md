# Object

[TOC]

## 分类

1. **dispatchable**
   1. 指针，指向底层实现
   2. 每个实例，生命周期内，**有唯一的handle值**
   3. 可以用于每一个layer之间
2. **non-dispatchable**
   1. 64位的整数类型
   2. 每个实例，生命周期内，不一定有唯一的handle值

## 生命周期

object通过2种方式创建：

1. **vkCreate**创建，vkDestroy销毁
   1. 主要用于低频创建场景
2. **vkAllocate**创建，vkFree销毁
   1. 从资源池中创建，**主要用于高频创建的场景**
   2. 释放后，资源回收，用于新的object创建，提高效率
   3. 包括：

