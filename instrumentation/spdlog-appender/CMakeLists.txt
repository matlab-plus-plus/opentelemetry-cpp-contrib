cmake_minimum_required(VERSION 3.23)

project(spdlog-appender VERSION 0.0.1)

include(FetchContent)

FetchContent_Declare(
	googletest
	GIT_REPOSITORY https://github.com/google/googletest
	GIT_TAG main
)

FetchContent_Declare(
	spdlog
	GIT_REPOSITORY https://github.com/gabime/spdlog
	GIT_TAG v1.x
)

FetchContent_MakeAvailable(spdlog googletest)

# Looking for system install of otel or parent project which already
# included it.
find_package(opentelemetry-cpp)