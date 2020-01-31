# 描述符

## Descriptor类型

1. Storage Image
    1. VK_DESCRIPTOR_TYPE_STORAGE_IMAGE
    2. 描述的是image资源，通过image view访问
2. Sampler
    1. VK_DESCRIPTOR_TYPE_SAMPLER
    2. 描述的是sampler对象，对sampled image进行采样
3. Sampled Image
    1. VK_DESCRIPTOR_TYPE_SAMPLED_IMAGE
    2. 描述的是image view
4. Combined Image Sampler
    1. VK_DESCRIPTOR_TYPE_COMBINED_IMAGE_SAMPLER
    2. 同时描述sampler对象和sampled image
5. Uniform Texel Buffer
    1. VK_DESCRIPTOR_TYPE_UNIFORM_TEXEL_BUFFER
    2. 描述的是buffer资源，通过buffer view访问
    3. 只可以用来加载
6. Storage Texel Buffer
    1. VK_DESCRIPTOR_TYPE_STORAGE_TEXEL_BUFFER
    2. 描述的是buffer资源，通过buffer view访问
    3. 可以用来加载、**存储**和原子操作
7. Storage Buffer
    1. VK_DESCRIPTOR_TYPE_STORAGE_BUFFER
    2. 描述的是buffer资源，直接通过buffer访问
    3. 可以用来加载、存储和原子操作
8. Uniform Buffer
    1. VK_DESCRIPTOR_TYPE_UNIFORM_BUFFER
    2. 描述的是buffer资源，直接通过buffer访问
    3. 只可以用来加载
9. Dynamic Uniform Buffer
    1. VK_DESCRIPTOR_TYPE_UNIFORM_BUFFER_DYNAMIC
    2. 和uniform buffer相同，除了指定的offset不一样
10. Dynamic Storage Buffer
    1. VK_DESCRIPTOR_TYPE_STORAGE_BUFFER_DYNAMIC
    2. 和storage buffer相同，除了指定的offset不一样
11. Input Attachment
    1. VK_DESCRIPTOR_TYPE_INPUT_ATTACHMENT
    2. 描述的是image资源，通过image view访问
    3. 用在Framebuffer中，用来加载

## Descriptor Set Layout