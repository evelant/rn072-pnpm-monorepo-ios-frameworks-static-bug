React-native 0.72 fails to compile for iOS when using `use_frameworks! :linkage => :static`

```

The following build commands failed:
	CompileC /Users/imagio/Library/Developer/Xcode/DerivedData/testproj-aijjqxpffhriwvdbnbtslrapnlmx/Build/Intermediates.noindex/Pods.build/Debug-iphonesimulator/React-utils.build/Objects-normal/arm64/RunLoopObserver.o /Users/imagio/dev/test/node_modules/.pnpm/react-native@0.72.1_@babel+core@7.20.2_@babel+preset-env@7.20.2_react@18.2.0/node_modules/react-native/ReactCommon/react/utils/RunLoopObserver.cpp normal arm64 c++ com.apple.compilers.llvm.clang.1_0.compiler (in target 'React-utils' from project 'Pods')
(1 failure)

```

To reproduce:
`pnpm install`
`cd apps/testproj/ios`
`USE_FRAMEWORKS=static pod install`
`cd ..`
`pnpm react-native run-ios`
