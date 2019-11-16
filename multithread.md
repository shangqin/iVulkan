# Vulkan多线程

## Multi-Threading in Vulkan

https://community.arm.com/developer/tools-software/graphics/b/blog/posts/multi-threading-in-vulkan

- 同步

![](https://community.arm.com/cfs-file/__key/communityserver-blogs-components-weblogfiles/00-00-00-20-66/8321.blog_5F00_diagrams.png)

* Semaphores - used to synchronize work across queues or across coarse-grained submissions to a single queue
* Events and barriers - used to synchronize work within a command buffer or a sequence of command buffers submitted to a single queue
* Fences - used to synchronize work between the device and the host

- 多线程

![](https://community.arm.com/cfs-file/__key/communityserver-blogs-components-weblogfiles/00-00-00-20-66/5277.swap2.png)

