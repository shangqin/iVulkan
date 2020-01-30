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
         1. **transfer命令**，pipeline类型是**transfer**，buffer usage必须包括`VK_BUFFER_USAGE_TRANSFER_DST_BIT`
         2. render pass外
         3. 使用uint32_t的数据填充到buffer中
      4. buffer更新：`vkCmdUpdateBuffer`
         1. **transfer命令**，pipeline类型是**transfer**，buffer usage必须包括`VK_BUFFER_USAGE_TRANSFER_DST_BIT`
         2. render pass外
         3. 使用
         4. dataSize大小需要小于等于`65536`字节，由于首先**拷贝用户数据到command buffer内存**中，然后**再拷贝数据到dstBuffer中**，会有额外的内存开销，所以不适合大块数据更新。如果需要大块数据更新，
            1. 方法1：分多次调用`vkCmdUpdateBuffer`，**不建议**
            2. 方法2：使用`vkCmdCopyBuffer`命令完成buffer拷贝更新
   3. **Copy*
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