add_library(core_library SHARED
  
  utils/blob.cpp 
  utils/deserializer.cpp 
  utils/id_context.cpp 
  utils/id_placeholder.cpp 
  utils/identifiable.cpp 
  utils/object_data.cpp 
  utils/property.cpp 
  utils/property_container.cpp 
  utils/property_eigen.cpp 
  utils/property_container_manager.cpp 
  utils/property_identifiable.cpp 
  utils/serializable.cpp 
  utils/serialization_context.cpp 
  utils/serializer.cpp 
    
  messages/base_sensor_message.cpp 
  messages/odometry_message.cpp 
  messages/pose_message.cpp
)



# add_library(core_library SHARED
  
#   data_structures/matrix.hpp data_structures/matrix.h 

#   utils/blob.cpp utils/blob.h
#   utils/deserializer.cpp utils/deserializer.h
#   utils/id_context.cpp utils/id_context.h
#   utils/id_placeholder.cpp utils/id_placeholder.h
#   utils/identifiable.cpp utils/identifiable.h
#   utils/object_data.cpp utils/object_data.h
#   utils/property.cpp utils/property.h
#   utils/property_container.cpp utils/property_container.h
#   utils/property_eigen.cpp utils/property_eigen.h
#   utils/property_container_manager.cpp utils/property_container_manager.h
#   utils/property_identifiable.cpp utils/property_identifiable.h
#   utils/serializable.cpp utils/serializable.h
#   utils/serialization_context.cpp utils/serialization_context.h
#   utils/serializer.cpp utils/serializer.h
    

#   messages/base_sensor_message.cpp messages/base_sensor_message.h
#   messages/odometry_message.cpp messages/odometry_message.h
#   messages/pose_message.h messages/pose_message.cpp
# )