VULKAN_SDK_PATH = /media/liusheng/Programfiles/Programs/VulkanSDK/1.1.114.0/ubuntu/x86_64
GLFW_SDK_PATH = /media/liusheng/Programfiles/Programs/libs/glfw/glfw-3.3.2
#VULKAN_SDK_PATH = /opt/vulkan/sdk/1.1.114.0/x86_64
CFLAGS = -std=c++17 -I$(VULKAN_SDK_PATH)/include
#LDFLAGS = -L$(VULKAN_SDK_PATH)/lib `pkg-config --static --libs glfw3-static` -lvulkan
LDFLAGS = -L$(VULKAN_SDK_PATH)/lib -lvulkan -L$(GLFW_SDK_PATH)/src -lglfw
Vertex_Buffers:main.cpp
	g++ $(CFLAGS) -o ../Vertex_Buffers main.cpp $(LDFLAGS)

.PHONY:test clean

test:/Vertex_Buffers
	LDF_LIBRARY_PATH=$(VULKAN_SDK_PATH)/lib:$(GLFW_SDK_PATH)/src VK_LAYER_PATH=$(VULKAN_SDK_APTH)/etc/vulkan/explicit_layer.d ./Vertex_Buffers

clean:
	rm -f Vertex_Buffers








