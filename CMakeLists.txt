cmake_minimum_required(VERSION 3.16.0 FATAL_ERROR)

set(CMAKE_SYSTEM_VERSION 10.0 CACHE STRING "" FORCE)
project(cpp_concurrency_materclass CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20")


set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

# Global configuration types
set(CMAKE_CONFIGURATION_TYPES
    "Debug"
    "Release"
    CACHE STRING "" FORCE
)

# Global compiler options
# remove default flags provided with CMake for MSVC
set(CMAKE_CXX_FLAGS "")
set(CMAKE_CXX_FLAGS_DEBUG "")
set(CMAKE_CXX_FLAGS_RELEASE "")

# Global linker options
# remove default flags provided with CMake for MSVC
set(CMAKE_EXE_LINKER_FLAGS "")
set(CMAKE_MODULE_LINKER_FLAGS "")
set(CMAKE_SHARED_LINKER_FLAGS "")
set(CMAKE_STATIC_LINKER_FLAGS "")
set(CMAKE_EXE_LINKER_FLAGS_DEBUG "${CMAKE_EXE_LINKER_FLAGS}")
set(CMAKE_MODULE_LINKER_FLAGS_DEBUG "${CMAKE_MODULE_LINKER_FLAGS}")
set(CMAKE_SHARED_LINKER_FLAGS_DEBUG "${CMAKE_SHARED_LINKER_FLAGS}")
set(CMAKE_STATIC_LINKER_FLAGS_DEBUG "${CMAKE_STATIC_LINKER_FLAGS}")
set(CMAKE_EXE_LINKER_FLAGS_RELEASE "${CMAKE_EXE_LINKER_FLAGS}")
set(CMAKE_MODULE_LINKER_FLAGS_RELEASE "${CMAKE_MODULE_LINKER_FLAGS}")
set(CMAKE_SHARED_LINKER_FLAGS_RELEASE "${CMAKE_SHARED_LINKER_FLAGS}")
set(CMAKE_STATIC_LINKER_FLAGS_RELEASE "${CMAKE_STATIC_LINKER_FLAGS}")

include(CMake/Utils.cmake)
include(CMake/GlobalSettingsInclude.cmake OPTIONAL)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)

# Sub-projects
add_subdirectory(common)
# add_subdirectory(barrier)
# add_subdirectory(coroutines)
# add_subdirectory(matrix)
# add_subdirectory(debug_test)
# add_subdirectory(find)
# add_subdirectory(for_each)
# add_subdirectory(HashTableX)
# add_subdirectory(interruptible_thread)
# add_subdirectory(latch)
# add_subdirectory(lock_free_stack)
# add_subdirectory(lockfree_linkedlist)
# add_subdirectory(parallel_stl_intro)
# add_subdirectory(prime_number_generator)
add_subdirectory(s1_how_to_handle_join_in_exception_scenarios)
add_subdirectory(s1_how_to_launch_a_thread)
add_subdirectory(s1_how_to_pass_parameters_to_a_thread)
add_subdirectory(s1_join_and_detach_functions)
add_subdirectory(s1_joinability_of_thread)
add_subdirectory(s1_parallel_accumulate)
add_subdirectory(s1_problamatic_situation_arise_when_passing_parameters_to_a_thread)
add_subdirectory(s1_some_useful_operations_on_threads)
add_subdirectory(s1_transferring_ownership_of_a_thread)
# add_subdirectory(s2_dead_locks)
# add_subdirectory(s2_mutex)
# add_subdirectory(s2_things_to_remember_when_using_mutex)
# add_subdirectory(s2_thread_safe_stack_implementation)
# add_subdirectory(s2_thread_safe_stack_implementation_race_conditions)
# add_subdirectory(s2_unique_locks)
# add_subdirectory(s3_async_task_detail_discussion)
# add_subdirectory(s3_communication_between_threads_using_promises)
# add_subdirectory(s3_details_about_condition_variables)
# add_subdirectory(s3_introduction_to_condition_variables)
# add_subdirectory(s3_introduction_to_futures_and_async_tasks)
# add_subdirectory(s3_introduction_to_package_tasks)
# add_subdirectory(s3_parallel_accumulate_algorithm)
# add_subdirectory(s3_retrieving_exception_using_futures)
# add_subdirectory(s3_shared_futures)
# add_subdirectory(s3_thread_safe_queue_implementation)
# add_subdirectory(s4_thread_safe_queue)
# add_subdirectory(s8_simple_threadpool)
# add_subdirectory(s8_simple_threadpool_waiting)
# add_subdirectory(s8_simple_threadpool_waiting_for_others)
# add_subdirectory(s8_simple_threadpool_with_local_work_queue)
# add_subdirectory(s8_simple_threadpool_with_work_stealing)
# add_subdirectory(scan)
# add_subdirectory(sort)
# add_subdirectory(thread_local_demo)

