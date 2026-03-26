file(GLOB RDMA_SOURCES "*.cpp")

add_library(rdma_transport OBJECT ${RDMA_SOURCES})
target_include_directories(rdma_transport PRIVATE /usr/local/include)
target_link_libraries(rdma_transport PRIVATE JsonCpp::JsonCpp glog::glog pthread fmt pii_runtime)
