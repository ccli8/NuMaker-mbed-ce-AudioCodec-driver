# Copyright (c) 2020 ARM Limited. All rights reserved.
# SPDX-License-Identifier: Apache-2.0

add_library(nu-audio-codec STATIC EXCLUDE_FROM_ALL)

target_include_directories(nu-audio-codec
    PUBLIC
        .
)

target_sources(nu-audio-codec
    PRIVATE
        I2S.cpp
        NAU88L25.cpp
        NAU8822L.cpp
)

target_link_libraries(nu-audio-codec PUBLIC mbed-core-flags)
