cmake_minimum_required(VERSION 3.3)
project(ipd17a-2 CXX)
include(.ipd/cmake/CMakeLists.txt)

add_cxx_test_program(chain_hash_table_test
        test/Chain_hash_table_test.cpp)

add_cxx_test_program(hash_test
        test/hash_test.cpp
        src/Sbox_hash.cpp)

add_cxx_program(collisions
        src/collisions.cpp
        src/hash_trial.cpp
        src/Sbox_hash.cpp
        src/hamlet.cpp)

add_cxx_program(mixers
        src/mixers.cpp
        src/hash_trial.cpp
        src/Sbox_hash.cpp
        src/hamlet.cpp)
