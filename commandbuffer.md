# Command Buffer

[TOC]

## 分类

command buffer中录制的命令，主要分为3类：

1. **执行动作**
   1. **Draw**
      1. vkCmdDraw
      2. vkCmdDrawIndexed
      3. vkCmdDrawIndirect
      4. vkCmdDrawIndexedIndirect
   2. **Clear**
      1. render pass外：
         1. `vkCmdClearColorImage`
         2. `vkCmdClearDepthStencilImage`
      2. render pass内：`vkCmdClearAttachments`
      3. buffer填充：`vkCmdFillBuffer`
      4. buffer更新：`vkCmdUpdateBuffer`
   3. **Copy**
      1. buffer数据copy只需要指定**buffer**即可，image数据copy需要指定**image**和**image layout**
      2. buffer之间copy数据：`vkCmdCopyBuffer`
      3. image之间copy数据：`vkCmdCopyImage`
      4. buffer和image之间copy数据：
         1. `vkCmdCopyBufferToImage`
         2. `vkCmdCopyImageToBuffer`
      5. image拷贝时缩放：`vkCmdBlitImage`
      6. image多重采样解析：`vkCmdBlitImage`
   4. **Dispatch**
      1. vkCmdDispatch
      2. vkCmdDispatchIndirect
      3. vkCmdDispatchBase
   5. 
2. 设置状态
   1. 
3. 执行同步