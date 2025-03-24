rock_find_cmake(Boost COMPONENTS system REQUIRED)

rock_library(aggregator
    SOURCES TimestampEstimator.cpp
            StreamAlignerStatus.cpp
    DEPS_PKGCONFIG base-types base-lib
    DEPS
            Boost::system
    HEADERS TimestampEstimator.hpp
            TimestampEstimatorStatus.hpp
            StreamAligner.hpp
            PullStreamAligner.hpp
            StreamAlignerStatus.hpp
            DetermineSampleTimestamp.hpp)
