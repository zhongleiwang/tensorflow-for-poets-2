package(default_visibility = ["//visibility:public"])

licenses(["notice"])  # Apache 2.0

android_binary(
    name = "tflite",
    srcs = glob(["java/**/*.java"]),
    assets = [
        "//app/src/main/assets:graph.lite",
        "//app/src/main/assets:labels.txt",
    ],
    assets_dir = "",
    custom_package = "com.example.android.tflitecamerademo",
    manifest = "AndroidManifest.xml",
    nocompress_extensions = [
        ".lite",
    ],
    resource_files = glob(["res/**"]),
    # In some platforms we don't have an Android SDK/NDK and this target
    # can't be built. We need to prevent the build system from trying to
    # use the target in that case.
    tags = ["manual"],
    deps = [
        "@androidsdk//com.android.support:support-v13-25.2.0",
        "@androidsdk//com.android.support:support-v4-25.2.0",
        "@tensorflow_lite//aar",        
    ],
)

exports_files(["jcenter.xml"])
