COPTS = ["-std=c++11",
         "-D_DEFAULT_SOURCE",
         "-DHAVE_CONFIG_H"]

cc_library(
  name = "snappy",
  copts = COPTS,
  srcs = ["snappy.cc"],
  hdrs = ["config.h", "snappy-stubs-public.h", "snappy-sinksource.h", "snappy.h"],
  deps = [
    ":snappy-internal"
  ]
)

cc_library(
  name = "snappy-c",
  copts = COPTS,
  srcs = ["snappy-c.cc"],
  hdrs = ["snappy-c.h"],
  deps = [
  ]
)

cc_library(
  name = "snappy-internal",
  copts = COPTS,
  hdrs = ["snappy-internal.h"],
  deps = [
    ":snappy-stubs-internal"
  ]
)

cc_library(
  name = "snappy-sinksource",
  copts = COPTS,
  srcs = ["snappy-sinksource.cc"],
  hdrs = ["snappy-sinksource.h"],
  deps = [
  ]
)

cc_library(
  name = "snappy-stubs-internal",
  copts = COPTS,
  srcs = ["snappy-stubs-internal.cc"],
  hdrs = ["snappy-stubs-internal.h", "snappy-stubs-public.h", "config.h"],
  deps = [
  ]
)

cc_library(
  name = "snappy-stubs-public",
  copts = COPTS,
  hdrs = ["snappy-stubs-public.h"],
  deps = [
  ]
)

cc_library(
  name = "snappy-test",
  copts = COPTS,
  srcs = ["snappy-test.cc"],
  hdrs = ["snappy-test.h", "config.h"],
  deps = [
    ":snappy-stubs-internal",
  ]
)

cc_test(
  name = "snappy_unittest",
  copts = COPTS,
  srcs = ["snappy_unittest.cc"],
  deps = [
    "@gtest//:main",
    ":snappy-internal",
    ":snappy-test",
  ]
)
